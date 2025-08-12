# Compton Scattering 
### Objective: 
- The objective of the Compton scattering experiment is to use a scintillation detector and radioactive sources to determine various attributes of high-energy EM radiation and EM radiation in general. The experiment will include verifying the inverse-square law and calculating the attenuation coefficient of copper sheets from observational data collected from the scintillation detector, using the MAESTRO-7 software package. Additionally, the rest mass of an electron will be determined by observing the shifts in photo-peaks as the angle between source and detector are changed, with a metallic rod at the fulcrum of the angle. Lastly using the same data collected during the electron mass proportion, the classical radius of an electron will be calculated using the Klein-Nishina differential scattering cross section.
## Equipment: 
- Sources of radiation, including 
	- Barium-133
	- Cesium-137
- Photo-detecting Scintillation tube
- Desktop PC with MAESTRO-7 software
- Housing for 10 mci Cs-137 source
- Copper square sheets
- Aluminum scattering rod 
- Unknown metallic scattering rod 
- Ruler
- Caliper
- Rubber gloves
- USB Flash Drive

## Background Calibration: 
There exists background EM radiation all around us, and we removed this interference from our scans by way of a background scan acquired before the other scans. After we calibrated the MAESTRO-7 software and verified all the settings were in the right positions, these background scans were saved and later removed from our scans. 
### Procedure: 
- We started maestro, and verified the following settings: 
	- Detector set to 0001 DESKTOP-VMO...
	- High voltage -> on, 900 v
	- Amplifier -> Gain 0.6, Shaping time 0.75
	- ADC -> Conversion Gain 1024, low-level disc 7, high level disk 1023
	- Preset -> real time 120s, live time 120s
- Next, we removed the previous calibration by selecting the Calculate-> Destroy Calibration option 
- Next, we closed all the housings and pointed the detector away from the Cs-137 source.
- We took 3 background scans in different locations.
- To save the data, we saved the resulting energy spectra file as SPE files. 

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from scipy.optimize import curve_fit, leastsq
from scipy.odr import Model, RealData, ODR
import matrepr as matp
from scipy.integrate import quad

# Read and trim spe files
def read_spe(filename):
    data = pd.read_csv(filename)
    data = np.array(data[12:1035])
    return data.astype(int)
# Slicing out individual photopeaks and removing background noise
def slicer(a,b, array):
    bins = np.ravel(np.arange(0,1023))
    array = np.ravel(array[a:b])
    array = np.subtract(array, backgroundavg[a:b])
    bins = bins[a:b]
    return(bins, array)

# Create Background Average
background1 = read_spe('DataPart2/Background/BackgroundScan1.Spe')
background2 = read_spe('DataPart2/Background/BackgroundScan2.Spe')
background3 = read_spe('DataPart2/Background/BackgroundScan3.Spe')
backgroundtotal = np.array([background1, background2, background3])
global backgroundavg
backgroundavg = np.mean(backgroundtotal, axis=0)
backgroundstd = np.std(backgroundtotal, axis=0)
backgroundavg = [int(x) for x in backgroundavg]


## Energy Calibration: 
Each channel # in MAESTRO-7 corresponds to a specific energy level, but we wouldn't know what each channel corresponds to if we didn't calibrate it. By using some sources we knew the photopeaks of, we could associate the specific channel to a quantitative energy level in keV

### Procedure: 
- We ensured the scattering rod is not in the setup
- Next, we opened the CS-137 housing and aligned the scintillator with the source. 
- To collect the data, we followed the same procedure as before, saving it as an SPE file again. 
- Next, we used the barium samples to collect more energy spectra reading. This allowed us to have a wider spread of photopeaks and a more accurate energy-to-bin conversion
### Data

#plotting calibration tests
barium_calibration = np.ravel(read_spe("DataPart2/Background/Barium Calibration.Spe"))
cesium_calibration = np.ravel(read_spe("DataPart2/Background/Cesium Calibration.Spe"))
fig = plt.figure()
gs = fig.add_gridspec(2, hspace=0.25)
axs = gs.subplots(sharex=True, sharey=True)
fig.suptitle('Counts Vs Energy')
fig.legend()
axs[0].axis([0, 400, 0, 30000])
axs[1].axis([0, 400, 0, 30000])
axs[0].bar(slicer(0,1023,cesium_calibration)[0],slicer(0,1023,cesium_calibration)[1], label="Cesium Calibraton", color = "r")
axs[1].bar(slicer(0,1023,barium_calibration)[0],slicer(0,1023,barium_calibration)[1], label="Barium Calibration", color = "g")
fig.legend()

Figure 1: Cesium and barium calibration scans

### Analysis

![image.png](attachment:image.png)

> Figure 2

Figure above shows known photopeaks of cesium-137. The large, high-energy photopeak corrosponds with the 662 keV peak, and we expect somewhere between 250 and 300 to represent the 662 keV peak. 

![image-2.png](attachment:image-2.png)

> Figure 3

Figure Above shows known barium photopeaks. The number and size of the peaks corrospond with our measured results, with a large 31 keV peak, and a smaller 356 keV peak. 



#Slicing out barium 31kev peak and fitting a guassian
#Define the Gaussian function 
def gaus(params,x):
    return params[0] * np.exp( - ( x - params[1] )**2/( 2 * params[2]**2) )
def gaussFit(fileName,start,end,params):
    bins, data = slicer(start,end, read_spe(fileName))
    model = Model(gaus)
    data = RealData(bins, data)
    odr = ODR(data, model, beta0 = params)
    odr_result = odr.run()
    params_fit = odr_result.beta
    covar_fit = odr_result.sd_beta
    chisquared = odr_result.res_var
    V_fit = gaus(params_fit, bins)
    return V_fit,params_fit,covar_fit,chisquared

bins, counts = slicer(10,20,barium_calibration)
params = 16000,15,-1
v_fit,params_fit,covar_fit,chisquared = gaussFit("DataPart2/Background/Barium Calibration.Spe",10,20,params)
plt.bar(bins,counts)
plt.plot(bins, v_fit, color = "red", label="Fitted Gaussian")
plt.legend()
plt.ylabel("Counts")
plt.xlabel("Energy")
plt.title("Barium 31keV Photopeak")
plt.gcf().text(0.95,0.5,"The 31 kev photopeak corrosponds to: ")
plt.gcf().text(0.95,0.45,"bin # " + str(round(params_fit[1],3)) +  "$\\pm$" + str(round(covar_fit[1],3)))
plt.gcf().text(0.95,0.30, "$\\chi^2/NDF$ = " + str(chisquared))

plt.show()
peak31 = params_fit[1], covar_fit[1]
#Plotting and finding the center of the barium 356 keV peak
bins, counts = slicer(137,163,barium_calibration)
params = 1700,150,-0.3
v_fit,params_fit,covar_fit,chisquared = gaussFit("DataPart2/Background/Barium Calibration.Spe",137,163,params)
plt.bar(bins,counts)
plt.plot(bins, v_fit, color = "red", label="Fitted Gaussian")
plt.legend()
plt.ylabel("Counts")
plt.xlabel("Energy")
plt.title("Barium 356keV Photopeak")
plt.gcf().text(0.95,0.5,"The 356 kev photopeak corrosponds to: ")
plt.gcf().text(0.95,0.45,"bin # " + str(round(params_fit[1],3)) +  "$\\pm$" + str(round(covar_fit[1],3)))
plt.gcf().text(0.95,0.30, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()
peak356 = params_fit[1], covar_fit[1]

bins, counts = slicer(250,290,cesium_calibration)
params = 26000,270,-1
v_fit,params_fit,covar_fit,chisquared = gaussFit("DataPart2/Background/Cesium Calibration.Spe",250,290,params)
plt.bar(bins,counts)
plt.plot(bins, v_fit, color = "red", label="Fitted Gaussian")
plt.legend()
plt.ylabel("Counts")
plt.xlabel("Energy")
plt.title("Cesium 662keV Photopeak")
plt.gcf().text(0.95,0.5,"The 662 kev photopeak corrosponds to: ")
plt.gcf().text(0.95,0.45,"bin # " + str(round(params_fit[1],3)) +  "$\\pm$" + str(round(covar_fit[1],3)))
plt.gcf().text(0.95,0.30, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()
peak662 = params_fit[1], covar_fit[1]


These three graphs above, figures 4,5 and 6 respectively, are the 3 primary photopeaks in the bariumn and cesium calibration samples, with a gaussian curve fit over them for analysis and plotting out the middle of the photopeak. 

Now there is 3 data points relating the bins on the x axis and real-world energy levels. We can make a function to output the real world energy of any bin, with uncertainty, next. 
#Array with column peaks and array with uncertainties for each peak
peakArray = peak31[0], peak356[0], peak662[0]
peakUncertArray = peak31[1], peak356[1], peak662[1]
energyArray = 31,356,662
#Define the linear function
def linear(params, x):
    return params[0] + params[1] * x
params = 2,2
model = Model(linear)
data = RealData(peakArray, energyArray, sx = peakUncertArray)
odr = ODR(data, model, beta0 = params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
print(covar_fit)
poptEnergy, pcovEnergy = curve_fit(linear,peakArray, energyArray, sigma=peakUncertArray)
#Defining the translation function:
#Returns a translated energy value:
def binToEnergy(bin):
    return 2.44649493 * bin, 7.5325808+ 0.0416798 * bin
print("For example, the bin 280 corrosponds to: ", binToEnergy(280)[0], "keV $\\pm$", binToEnergy(280)[1])
### Section Conclusion: 
We derived a method to convert a given bin number to an energy level in keV. The photopeaks derived from the scans appear to quantitatively and qualitatively line up with the given photopeaks from literature. All 3 reduced chi-squared values were in satisfactory limits, although the BA 356 keV and 31 keV scans appeared to be slightly overconstrained, potentially due to the limtations of the resolution of the scintillator.
## Section 1: Inverse Square relation
EM Radiation obeys an inverse square law, where a doubling of distance approximately halves the intensity of EM radiation. This can be measured with varied distance between the detector and the source. 

### Procedure:
- We pointed the detector away from the Cs-137 housing to limit interference
- Acquired and placed the barium sources in the holder, and measured the distance from the holder to the scintillator. 
- We ran 3 scans at each distance, and varied the distance 4 times, from 3-12 cm. 

### Data
# Importing Data
ba3avg = np.ravel(np.mean([read_spe('DataPart2/Section I/Ba3_1.Spe'), read_spe('DataPart2/Section I/Ba3_2.Spe'), read_spe('DataPart2/Section I/Ba3_3.Spe')], axis=0))
ba6avg = np.ravel(np.mean([read_spe('DataPart2/Section I/Ba6_1.Spe'), read_spe('DataPart2/Section I/Ba6_2.Spe'), read_spe('DataPart2/Section I/Ba6_3.Spe')], axis=0))
ba9avg = np.ravel(np.mean([read_spe('DataPart2/Section I/Ba9_1.Spe'), read_spe('DataPart2/Section I/Ba9_2.Spe'), read_spe('DataPart2/Section I/Ba9_3.Spe')], axis=0))
ba12avg = np.ravel(np.mean([read_spe('DataPart2/Section I/Ba12_1.Spe'), read_spe('DataPart2/Section I/Ba12_2.Spe')], axis=0))
# Removing background interference
ba3avg = np.subtract(ba3avg, backgroundavg)
ba6avg = np.subtract(ba6avg, backgroundavg)
ba9avg = np.subtract(ba9avg, backgroundavg)

#Histograms
bins = np.ravel(np.arange(0,1023))
fig = plt.figure()
gs = fig.add_gridspec(4, hspace=0)
axs = gs.subplots(sharex=True, sharey=True)
fig.suptitle('Counts Vs Energy')
fig.legend()
axs[0].axis([0, 200, 0, 25000])
axs[1].axis([0, 200, 0, 25000])
axs[2].axis([0, 200, 0, 25000])
axs[3].axis([0, 200, 0, 25000])
axs[0].bar(bins,ba3avg, label="3 cm", color = "r")
axs[1].bar(bins,ba6avg, label="6 cm", color = "g")
axs[2].bar(bins,ba9avg, label="9 cm", color = "b")
axs[3].bar(bins,ba12avg, label="12 cm", color = "black")
fig.legend()

# Hide x labels and tick labels for all but bottom plot.
for ax in axs:
    ax.label_outer()
fig.show()




Figure 7: This graph shows the detected photopeaks for ranges 3,6,9 and 12 centimeters. Notice how the intensity and size of the photopeaks rapidly diminishes with distance. 

### Analysis

# Define the inverse square function
def invsq(params,x):
    a,b = params
    return  b * 1/(np.power(x,a))

# Determine total counts of decays for each distance and stddevs 
start = 140
stop = 170
ba3sum = sum(ba3avg[start:stop])
ba6sum = sum(ba6avg[start:stop])
ba9sum = sum(ba9avg[start:stop])
ba12sum = sum(ba12avg[start:stop])

xs = [0.03,0.06,0.09,0.12]
ys = [ba3sum, ba6sum, ba9sum, ba12sum]
xerr = [0.001,0.001,0.001,0.001]
yerr = [1000,1000,800,800]
print(yerr)
model = Model(invsq)
data = RealData(xs, ys, sx=xerr, sy=yerr)
odr = ODR(data, model, beta0=[2,500])
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
V_fit = invsq(params_fit, xs)
chisquared = odr_result.res_var

#Create array with counts and distance in latex
distCounts = xs, ys
distCountStr = matp.to_latex(distCounts)

plt.figure(figsize=(10, 6))
plt.plot(xs, ys, label='Data')
plt.plot(xs, V_fit, 'r-', label='Fitted Curve')
plt.errorbar(xs,ys,xerr = xerr, yerr = yerr, fmt="o", color="r")
plt.xlabel('Distance (m)')
plt.ylabel('Total Counts')
plt.title('Inverse Square Curve Fitting for 356kev barium peak counts')
plt.legend()
plt.grid(True)
plt.gcf().text(0.95,0.8,"Exponent Value:" + str(np.round(params_fit[0],3)) + "+/-" +  str(np.round(covar_fit[0],3)))
plt.gcf().text(0.95,0.7,"Scaling Factor:" + str(params_fit[1]))
plt.gcf().text(0.95,0.6, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()
expValue = params_fit[0]
Figure 8: This plot represents the  total counts within the barium 356keV photopeak as a function of distance from the detector, as well as the exponent value and reduced chi-squared value. 

Table of various distances and total counts of detected decays at 662 keV photopeak

$\left[\begin{array}{cccc}
    distance (m): & 0.03 & 0.06 & 0.09 & 0.12 \\
    Counts: & 3.879 \times 10^{4} & 1.785 \times 10^{4} & 9945 & 6838
\end{array}\right]
$
#modified gaussFit for removing background radiation for 20deg
def gaussFit(fileName,start,end,params,angle):
    bins, data = slicer(start,end, read_spe(fileName))
    data = data - backgroundavg[start:end]
    model = Model(gaus)
    data = RealData(bins, data)
    odr = ODR(data, model, beta0 = params)
    odr_result = odr.run()
    params_fit = odr_result.beta
    covar_fit = odr_result.sd_beta
    chisquared = odr_result.res_var
    V_fit = gaus(params_fit, bins)
    return V_fit,params_fit,covar_fit,chisquared

def gaussFitFileLimited(file,start,end,params):
    bins, data = slicer(start,end, file)
    data = data - backgroundavg[start:end]
    model = Model(gaus)
    data = RealData(bins, data)
    odr = ODR(data, model, beta0 = params)
    odr_result = odr.run()
    params_fit = odr_result.beta
    covar_fit = odr_result.sd_beta
    return params_fit, covar_fit


params = 1700,150,-0.3
ba3Amp = gaussFitFileLimited(ba3avg, start, stop, params)[0][0]
params = 1500,150,-0.3
ba6Amp = gaussFitFileLimited(ba6avg, start, stop, params)[0][0]
params = 1700,150,-0.3
ba9Amp = gaussFitFileLimited(ba9avg, start, stop, params)[0][0]
params = 1700,150,-0.3
ba12Amp = gaussFitFileLimited(ba12avg, start, stop, params)[0][0]

xs = [0.03,0.06,0.09,0.12]
ys = [ba3Amp, ba6Amp, ba9Amp, ba12Amp]
xerr = [0.001,0.001,0.001,0.001]
yerr = [100,100,100,100]
model = Model(invsq)
data = RealData(xs, ys, sx=xerr, sy=yerr)
odr = ODR(data, model, beta0=[2,500])
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
V_fit = invsq(params_fit, xs)
chisquared = odr_result.res_var

#Create array with counts and distance in latex
distCounts = xs, ys
distCountStr = matp.to_latex(distCounts)

plt.figure(figsize=(10, 6))
plt.plot(xs, ys, label='Data')
plt.plot(xs, V_fit, 'r-', label='Fitted Curve')
plt.errorbar(xs,ys,xerr = xerr, yerr = yerr, fmt="o", color="r")
plt.xlabel('Distance (m)')
plt.ylabel('Total Counts')
plt.title('Inverse Square Curve Fitting for 356kev barium peak amplitudes')
plt.legend()
plt.grid(True)
plt.gcf().text(0.95,0.8,"Exponent Value:" + str(np.round(params_fit[0],3)) + "+/-" +  str(np.round(covar_fit[0],3)))
plt.gcf().text(0.95,0.7,"Scaling Factor:" + str(params_fit[1]))
plt.gcf().text(0.95,0.6, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()
expValue = params_fit[0]
Figure 9: Similar to the previous figure, but instead of total counts contained with the peak we are plotting the amplitude of the gaussian fit to the peak.
### Conclusions:
The data aquired fit the model well, however, it did not yield the expected a=2 value from literature. The chi-squared values were within expected parameters, slightly overconstrained but that could also be due to a lack of data points. The general structure of the inverse square does fit the data well, but the actual exponential parameter appears to be slightly incorrect. A very small proportion of this could be due to air molecules abosrbing a proportion of the energy, but this is likely a minimal source of interference. 
## Section 2: Attenuation
Attenuation of EM radiation through a material is a function of the composition of the target material, as well as thickness. This is modeled by the following relation: 
$$
T = e^{-\mu x}
$$
Where $T$ is the transmission coefficient, a value between 0 and 1 that signifies the proportion of EM radiation that is able to penetrate. This transmission coefficient is only good for a certain energy level, in this case we will be using the 662 keV  photo-peak to determine the transmission coefficient of copper sheets. 

### Procedure:
- We started by collecting a scan with no copper sheets present. This scan served as the baseline energy scan, or an attenuation constant of 1. 
- Next, we measured the copper sheets, being sure to collect various measurements from different parts of the sheet. After we averaged the measurements and collected proper uncertainty data, we could collect data with the copper sheets attenuating the gamma rays from the source.
- We collected 2 scans, one with 1 copper sheet and one with 2. 

### Data: 
# Import data 
sheet_1 = read_spe("DataPart2/Section II/1 sheet.Spe")
sheet_2 = read_spe("DataPart2/Section II/2 sheet.Spe")
plt.plot(slicer(0,350,cesium_calibration)[0], slicer(0,350,cesium_calibration)[1], color = "red", label= "0 Sheets")
plt.plot(slicer(0,350,sheet_1)[0], slicer(0,350,sheet_1)[1], color = "green", label="1 Sheet")
plt.plot(slicer(0,350,sheet_2)[0], slicer(0,350,sheet_2)[1], color = "blue", label = "2 Sheets")
plt.title("0,1 and 2 sheets of copper")
plt.xlabel("Energy")
plt.ylabel("Counts")
plt.legend()
plt.show()

Figure 10: Overlaid plot showing collected photocounts at various energy levels for 0, 1 and 2 sheets of copper.
def transmissionFunct(x,u):
    return np.exp(-u * x)

#Removing background noise and slciing out 662 keV peak
total0Sheet = np.sum(slicer(225,310,cesium_calibration)[1])
total1Sheet = np.sum(slicer(225,310,sheet_1)[1])
total2Sheet = np.sum(slicer(225,310,sheet_2)[1])
totals = total0Sheet, total1Sheet, total2Sheet
totals = np.ravel(totals)
transcoeffs = totals/total0Sheet

#Thickness of each sheet. They happened to be the same.
sheetThickness = 0.00169 #in meters
sheets = 0, sheetThickness, 2*sheetThickness
sheets = np.ravel(sheets)

model = Model(transmissionFunct)
data = RealData(sheets, transcoeffs, sx=[0.0001,0.0001,0.0001],)
odr = ODR(data, model, beta0=[55])
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = transmissionFunct(sheets, params_fit[0])


plt.plot(sheets, V_fit, color="red", label="Fitted Curve")
plt.scatter(sheets, transcoeffs, color = "blue", label= "Data")
plt.ylabel("Transmission Coefficents (Detected/Total)")
plt.xlabel("Thickness of copper")
plt.errorbar(sheets,transcoeffs,xerr=[0.0001,0.0001,0.0001], fmt="none")
plt.title("Thickness Vs Transmission Coefficent for Copper Sheet for 662 keV photopeak")
plt.gcf().text(0.95,0.55, "Attenuation Coefficent for Copper: ")
plt.gcf().text(0.95,0.50, str(round(params_fit[0],3)) + "$\\pm$" + str(round(covar_fit[0],2)))
plt.gcf().text(0.95,0.45, "$\\chi^2/NDF$ = " + str(chisquared))
plt.legend()
plt.plot()

Figure 11: This graph shows the fit between the measured thickness of copper and the calculated transmission coefficent for the 662 keV photopeak. 

The transmission coefficent was calculated by summing across the entire photopeak for the 3 different cases, and then dividing the 1 sheet and 2 sheet cases by the 0 sheet case to determine the proportion of photons stopped by the sheet. This was plotted against the thickness of copper, and the transmission model was fit to it. 
### Conclusion: 
The data collected fit thje experimental model almost perfectly. This, along with only having 3 real data points, led to an astronomically small chi-squared value, on the order of 10E-8. However, the literature value of copper sheet was 100x less then the produced value, but that is due to the literature values being in units of cm, while I used meters in this analysis. Accounting for this, the values obatained here corrospond to the literature well. 
## Section 3: Compton Scattering: 
The effect known as Compton scattering results when high-energy photons are scattered by electrons within a material. Some of the energy of the photon is transferred to the electron, and the scattered waves emerge with a longer wavelength, and thus lower energy, then the incident waves. This effect could be seen by varying the angle between the detector and the source, with some material at the fulcrum of the angle. The energy shift in the detected photopeaks as a function of angle will be used to determine the rest mass of an electron via conservation of momentum. 

### Procedure: 
-  We decided to use 4 angles, 0 degrees, 20 degrees, 40 degrees and 60 degrees for this experiment. 
- At each angle we ran a scan with the aluminum rod, the mystery rod, and no rod at all, making sure to close the cesium source between scans. 
- This gave us 12 scans to work with for the fitting and analysis. 
### Data:


### Below are the graphs for Aluminum Compton scattering at various angles
def plotterTool(filename):
    bins, data = slicer(0, 350, read_spe(filename))
    fig = plt.bar(bins, data)
    plt.xlabel("Energy (keV)")
    plt.ylabel("Counts")
    plt.xticks(bins[0:350:50], np.round(binToEnergy(bins[0:350:50])[0],2))
    return plt

def plotAndFit(filename, start, end ,params, angle):
    fit,params,covar,chi = gaussFit(filename,start,end,params,angle)
    bins, data = slicer(start,end, read_spe(filename))
    plt.bar(bins,data,label="Data", color = "blue")
    plt.plot(bins, fit, label = "Fit", color = "red")
    plt.gcf().text(0.95,0.5,"Amplitude: " + str(params[0]))
    plt.gcf().text(0.95,0.4,"x_0: " + str(params[1]))
    plt.gcf().text(0.95,0.3,"sigma: " + str(params[2]))
    plt.gcf().text(0.95,0.2, "$\\chi^2/NDF$ = " + str(chi))
    plt.title("ODR for 662keV at " + angle + " degrees")
    plt.show()
    plt.close()
    return params, covar

# Plots for Aluminum
fig, axs = plt.subplots(2, 2)
axs[0, 0].bar(slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/0 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/0 degrees.Spe"))[1], color = "black")
axs[0, 0].set_title('0 degree scattering')
axs[0, 1].bar(slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/20 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/20 degrees.Spe"))[1], color = "blue")
axs[0, 1].set_title('20 degree scattering')
axs[1, 0].bar(slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/40 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/40 degrees.Spe"))[1], color = "green")
axs[1, 0].set_title('40 degree scattering')
axs[1, 1].bar(slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/60 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Aluminum/60 degrees.Spe"))[1], color = "red")
axs[1, 1].set_title('60 degree scattering')

for ax in axs.flat:
    ax.set(xlabel='Energy Levels', ylabel='Counts')
fig.suptitle('Aluminum Scattering at Various Angles with background radiation removed')
fig.tight_layout()   

plt.show()
Figure 12: Shifting of photopeaks being scattered by an aluminum rod at 4 different angles. Negative counts in the final 2 scans are a byproduct of removing background radiation, and had no effect on the final photopeak data.

params =22000,277,-10
peaksAl = np.zeros(4)
peaksAlUnc = np.zeros(4)
params1, covar = plotAndFit("DataPart2/Section III/Aluminum/0 degrees.Spe", 260,300,params,"0")
peaksAl[0] = params1[1]
paramsAl0 = params1
peaksAlUnc[0] = covar[1]
params =750,272,-12
params1, covar = plotAndFit("DataPart2/Section III/Aluminum/20 degrees.Spe", 260,290,params, "20")
peaksAl[1] = params1[1]
paramsAl20 = params1
peaksAlUnc[1] = covar[1]
params =80,215,-10
params1, covar = plotAndFit("DataPart2/Section III/Aluminum/40 degrees.Spe", 185,240,params, "40")
peaksAl[2] = params1[1]
paramsAl40 = params1
peaksAlUnc[2] = covar[1]
params =120,160,-12
params1, covar = plotAndFit("DataPart2/Section III/Aluminum/60 degrees.Spe", 155,190,params, "60")
peaksAl[3] = params1[1]
paramsAl60 = params1
peaksAlUnc[3] = covar[1]
peaksAlUnc = np.ravel(peaksAlUnc)
Figure 13,14,15 and 16 above: These 4 figures represent the shifting photopeaks from the aluminum rod scattering with a gaussian curve fit.
#Electron mass curve fit 
#Params [0] is E, or calibration energy
#Params [1] is the mass of an electron
#x is theta (scattering angle)
def compton(params,x):
    E = params[0]
    m = params[1]
    c = 3 * 10 ** 8 
    return E/(1+(E/(m * c**2))*(1-np.cos(np.radians(x))))

xs = [0,20,40,60]
xerr = [1,1,1,1]
uncert = np.add(binToEnergy(peaksAlUnc)[1], binToEnergy(peaksAl)[1])
uncert = (uncert *1000) * (1.6022 * 10**-19)
model = Model(compton)
energyJoules = (binToEnergy(peaksAl)[0]*1000) * (1.6022 * 10**-19)
data = RealData(xs, energyJoules, sx=xerr, sy=uncert,)
params = 9 * 10**-20,9 * 10**-31
odr = ODR(data, model, beta0=params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = compton(params_fit, xs)
#Plotting Photopeak to Scattering Angles

plt.plot(xs, V_fit, color = "red", label = "Fitted Curve")
plt.scatter(xs, energyJoules, label = "data")
plt.title("Aluminum Angle vs Photopeak Location")
plt.errorbar(xs, energyJoules,xerr=xerr, yerr= uncert,  fmt="none")
plt.xlabel("Angle")
plt.ylabel("Photopeak Location (Joules)")
Emass0 = params_fit[1] 
massuncert = covar_fit[1] 
plt.gcf().text(0.95,0.5,"E: " + str(params_fit[0]))
plt.gcf().text(0.95,0.4,"Mass of Electron: " + str(np.round(Emass0,33)) + "$\\pm$" + str(np.round(massuncert,32)) + " Kg")
plt.gcf().text(0.95,0.3, "$\\chi^2/NDF$ = " + str(chisquared))
plt.legend()
plt.show()

Figure 17: This figure plots the energy of the photopeak in joules as a function of angle. Using the formula:
$$
E' = \frac{E}{1+(E/mc^{2})(1-\cos\theta)}
$$
Where E' is the shifted photopeak, E is the original photopeak, theta is the angle of scattering, c is the speed of light, and m is the mass of an electron, we can fit a parameter to the electron mass, experimentally determining the electrons mass.
### Below are the plots of photopeaks at various angles with fitted curves for the unknown material
# Plots for Unknown
fig, axs = plt.subplots(2, 2)
axs[0, 0].bar(slicer(0, 350, read_spe("DataPart2/Section III/Unknown/0 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Unknown/0 degrees.Spe"))[1], color = "black")
axs[0, 0].set_title('0 degree scattering')
axs[0, 1].bar(slicer(0, 350, read_spe("DataPart2/Section III/Unknown/20 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Unknown/20 degrees.Spe"))[1], color = "blue")
axs[0, 1].set_title('20 degree scattering')
axs[1, 0].bar(slicer(0, 350, read_spe("DataPart2/Section III/Unknown/40 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Unknown/40 degrees.Spe"))[1], color = "green")
axs[1, 0].set_title('40 degree scattering')
axs[1, 1].bar(slicer(0, 350, read_spe("DataPart2/Section III/Unknown/60 degrees.Spe"))[0],slicer(0, 350, read_spe("DataPart2/Section III/Unknown/60 degrees.Spe"))[1], color = "red")
axs[1, 1].set_title('60 degree scattering')

for ax in axs.flat:
    ax.set(xlabel='Energy Levels', ylabel='Counts')
fig.suptitle('Unknown Scattering at Various Angles')
fig.tight_layout()   

plt.show()

Figure 18: Like figure 12, this series of plots displays the same shifting of photopeaks but with the unknown material instead of the previous aluminum sample.

params =22000,277,-10
peaksUn = np.zeros(4)
peaksUnUnc = np.zeros(4)
params1, covar = plotAndFit("DataPart2/Section III/Unknown/0 degrees.Spe", 260,300,params,"0")
paramsUn0=params1 
peaksUn[0] = params1[1]
peaksUnUnc[0] = covar[1]
params =750,272,-12
params1, covar = plotAndFit("DataPart2/Section III/Unknown/20 degrees.Spe", 255,290,params, "20")
paramsUn20=params1 
peaksUn[1] = params1[1]
peaksUnUnc[1] = covar[1]
params =80,215,-20
params1, covar = plotAndFit("DataPart2/Section III/Unknown/40 degrees.Spe", 185,240,params, "40")
paramsUn40=params1 
peaksUn[2] = params1[1]
peaksUnUnc[2] = covar[1]
params =80,170,-10
params1, covar = plotAndFit("DataPart2/Section III/Unknown/60 degrees.Spe", 155,190,params, "60")
paramsUn60=params1 
peaksUn[3] = params1[1]
peaksUnUnc[3] = covar[1]

Figures 19,20,21 and 22: 
The 4 figures above are the photopeaks seen in figure 18 with all extraenous data removed and a gaussian function fit over the curve to determine the center of the photopeak. 

uncert = np.add(binToEnergy(peaksUnUnc)[1], binToEnergy(peaksUn)[1]) 
uncert = (uncert *1000) * (1.6022 * 10**-19)
model = Model(compton)
energyJoules = (binToEnergy(peaksUn)[0]*1000) * (1.6022 * 10**-19)
data = RealData(xs, energyJoules, sx=xerr, sy=uncert,)
params = 9 * 10**-20,9 * 10**-31
odr = ODR(data, model, beta0=params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = compton(params_fit, xs)
#Plotting Photopeak to Scattering Angles

plt.plot(xs, V_fit, color = "red", label = "Fitted Curve")
plt.scatter(xs, energyJoules, label = "data")
plt.title("Unknown Material Angle vs Photopeak Location")
plt.errorbar(xs, energyJoules,xerr=xerr, yerr= uncert,  fmt="none")
plt.xlabel("Angle")
plt.ylabel("Photopeak Location (Joules)")
Emass = np.round(params_fit[1] ,32)
massuncert = np.round(covar_fit[1],32)
plt.gcf().text(0.95,0.5,"E: " + str(params_fit[0]))
plt.gcf().text(0.95,0.4,"Mass of Electron: " + str(Emass) + "$\\pm$" + str(massuncert) + " Kg")
plt.gcf().text(0.95,0.3, "$\\chi^2/NDF$ = " + str(chisquared))
plt.legend()
plt.show()

Figure 23: This curve fit is a direct analogue to the figure 17 curve fit, but using the data from the unknown material trials instead. 
### Conclusion: 

Both curve fits yielded values for electron mass within uncertainty of the given literature values for electron mass. The data appeared to fit the model much better for the higher-count trials at a more direct angle, this could be due to the higher counts "drowning out" any unwanted interference. Despite this, our data fit the model somewhat well, with reduced chi squared values starting in the sub-1 range for the higher-count trials and reaching around 10-15 for the noisier trials. The final curve fits for both trials yielded a satisfactory result, with the curve fit falling within the expected uncertainty of the data, combined with the agreement with literature values it demonstrates that this data fits the given model with a relatively high degree of accuracy.
## Section 4
Using the data retrieved from the Compton scattering portion of the lab, we can also calculate the classical radius of an electron, as well as the makeup of the unknown material. The classical radius of an electron can be calculated by using the Klein-Nishina differential cross section. 

### Procedure: 
- We collected the mass, length and diameter of the aluminum and unknown rods. 
- We also measured the distance from the center of the rod to the front of the detector.
- The rest of the data we needed was acquired in the previous sections of the lab. 

### Data 
Length from detector to rod center: 
18.6 $\pm$ 0.1 cm

|          | Mystery Rod         | Aluminum Rod       |
|----------|---------------------|--------------------|
| Diameter | 1.90 $\pm$ 0.001 cm | 2.00 $\pm$ 0.05 cm |
| Length   | 19.6 $\pm$ 0.1 cm   | 18.8 $\pm$ 0.1 cm  |
| Mass     | 479.7 $\pm$ 0.1 g   | 146.5 $\pm$ 0.1 g  |


## Analysis Calculations

## Finding a relation for $\frac{d\sigma}{d\Omega}$
If we take equation 6 and 7 together, we get the following relation: 

$$
\frac{d\sigma}{d\Omega} = \frac{r^{2}}{2} \left[ \frac{1 + \cos ^{2}\theta}{[1 + \alpha(1-\cos\theta)]^{2}} \right] \left[ 1 + \frac{\alpha^{2} (1+\cos\theta)^{2}}{(1+\cos ^{2}\theta)[1+\alpha(1+\cos\theta)]} \right] = \frac{\Sigma'_{\gamma}}{n_{\theta} I \Delta\Omega t \epsilon} \tag{1}
$$
With the following parameters:
$\alpha$ is defined as:

$$
\alpha=\frac{E_{\gamma}}{mc^{2}} = \frac{1.0601602\times 10^{-13 }\text{ joules}}{9.109 \times 10 ^{-31} \text{ kg} \cdot ( 3\times 10^{8} \text{ m/s})^{2}} = 1.2931
$$

$$
\Sigma'_{\gamma} = \sum_{\text{photopeak}} \text{ counts}
$$

$$
n_{\theta} = \rho VN_{A} \sum_{i} w_{i} \frac{z_{i}}{M_{i}}
$$

### Calculating $n_{\theta}$
For aluminum: 

$$
\rho \text{ (density)} = 2.7   \ g/cm^{3}
$$

$$
V \text{ (Scattering Volume)} = \pi r^{2}  \cdot h
$$

$$
V = 6.2831\begin{aligned} \Delta V &= \sqrt{\left( \frac{\partial V}{\partial d} \Delta d \right)^2 + \left( \frac{\partial V}{\partial h} \Delta h \right)^2} \\ &= \sqrt{\left( \left( h / 2 * pi * d \right) \cdot \Delta d \right)^2 + \left( \left( pi * (d / 2) ^ 2 \right) \cdot \Delta h \right)^2} \\ &= 0.4443\\ &= 4.4443 \times 10^{-1} \\ &= 4 \times 10^{-1} \end{aligned}
$$

$$
V = \left( 6.3 \pm 0.4 \right) \times 10^{0} \text{ cm}^{3}
$$
$N_{a}$ is Avogadro’s number
$$
N_{A} = 6.023 \times 10^{23}
$$
Sum of weight fractions should be about 1 for a pure sample of aluminum
$$
\sum_{i} w_{i} \approx 1
$$
$z_{i}$ is the atomic number, aluminum is 13
$$
z_{i} = 13
$$
$M_{i}$ is the molar mass of the material
$$
M_{i}=26.9815
$$
With this we can calculate $n_{\theta}$
$$
N_\theta = 3.594 \times 10^{27}\begin{aligned} \Delta N_\theta &= \sqrt{\left( \frac{\partial N_\theta}{\partial V} \Delta V \right)^2} \\ &= \sqrt{\left( \left( 5.704e+26 \right) \cdot \Delta V \right)^2} \\ &= 2.287e+26 \\ &= 2.287 \times 10^{26} \\ &= 2 \times 10^{26} \end{aligned}
$$
$$
N_\theta = \left( 3.6 \pm 0.2 \right) \times 10^{27}
$$
With $N_{\theta}$, we need $I$, $\Delta\Omega$ and $\epsilon$
### Calculating $\Delta\Omega$
This one is simpler. The formula is given by 
$$
\Delta \Omega = \frac{\pi(D/2)^{2}}{R_{2}^{2}}
$$
Where $D$ is the diameter of the scintillator: 
$$
D = 5.08 \text{ cm}
$$
and $R_{2}$ is the distance from the center of the scattering rod to the front of the detector
$$
R_{2} = 18.6 \pm 0.1 \text{ cm}
$$
Calculating for $\Delta\Omega$
$$
\Delta\Omega = 0.0586
$$
$$
\begin{aligned} \Delta \Delta\Omega &= \sqrt{\left( \frac{\partial \Delta\Omega}{\partial R_2} \Delta R_2 \right)^2} \\ &= \sqrt{\left( \left( pi * -16129 / 1250 / R_2 ^ 3 \right) \cdot \Delta R_2 \right)^2} \\ &= 0.0006299535 \\ &= 6.299535 \times 10^{-4} \\ &= 6 \times 10^{-4} \end{aligned}
$$
$$
\Delta\Omega = \left( 5.86 \pm 0.06 \right) \times 10^{-2}
$$
## Other Parts:
- $t$ in the time of the scan, 120 seconds
- $\epsilon$ is given by the following relation: 
$$
\epsilon = -0.50E + 0.58
$$
	- Where $E$ is 661.7 keV
$$
\epsilon = -0.5(661.7) + 0.58= −330.27
$$

### Intensity: 
- There are two approaches to finding the intensity at the rod. One computational, and one analytical. We will follow the analytical approach first. 
$$
I = \frac{A_{0}f}{4\pi R_{1}^{2}}
$$With the following variables: 
$$
A_0\text{ (Activity of the source)} = 10 mCi = 370000000 \text{ decays/sec}
$$
$$
f \text{ (Fraction of gamma ray emissions )} = .851
$$
$$
R_{1} \text{ (Distance from source to center of rod)}= 31cm 
$$
Plugging all this in, we get 
$$
I = 2.6 \times 10^4
$$
### Coefficient for $\Sigma_{\gamma}'$
We can combine these numbers to determine the coefficient in front of $\Sigma_{\gamma}'$
$$
\beta = 4.6 \times 10^{-36}\begin{aligned} \Delta \beta &= \sqrt{\left( \frac{\partial \beta}{\partial n_{0}} \Delta n \right)^2 + \left( \frac{\partial \beta}{\partial \Delta\Omega} \Delta \Delta\Omega \right)^2} \\ &= [\left( \left( -(\Delta\Omega * 1.03e+9 / (1.03e+9 * n_{0} * \Delta\Omega) ^ 2) \right) \cdot \Delta n_{0} \right)^2 + \\ &   \left( \left( -(n_{0} * 1.03e+9 / (1.03e+9 * n_{0} * \Delta\Omega) ^ 2) \right) \cdot \Delta \Delta\Omega \right)^2] ^{1/2} \\ &= 3e-10 \\ &= 3 \times 10^{-10} \\ & \end{aligned}
$$
$$
\beta = \left( 4.6 \pm 0.3 \right) \times 10^{-36} 
$$
This is our coefficient value. We can use this to rewrite equation 1 as follows: 
$$
\frac{r^{2} \cdot 4.6\times 10^{36}}{2} \left[ \frac{1 + \cos ^{2}\theta}{[1 + \alpha(1-\cos\theta)]^{2}} \right] \left[ 1 + \frac{\alpha^{2} (1+\cos\theta)^{2}}{(1+\cos ^{2}\theta)[1+\alpha(1+\cos\theta)]} \right] = \Sigma'_{\gamma}
$$
Which gives us a direct relation between scattering angle, and $\Sigma'_{\gamma}$

def kleinNishina(params, x):
    alpha = 1.2931
    coeff = (params[0]**2 * 4.6 * 10 ** 34)/2
    cos_theta = np.cos(x)
    term1 = (1 + cos_theta**2) / (1 + alpha * (1 - cos_theta))**2
    term2 = 1 + (alpha**2 * (1 + cos_theta)**2) / ((1 + cos_theta**2) * (1 + alpha * (1 + cos_theta)))
    result = coeff * term1 * term2
    return(result)
def gausFlip(x, params):
    return params[0] * np.exp( - ( x - params[1] )**2/( 2 * params[2]**2) )
def gaussIntegrate(start, stop, args):
    return quad(gausFlip, start, stop , args=(args))

uncert = np.add(binToEnergy(peaksAlUnc)[1], binToEnergy(peaksAl)[1]) * 1000 
sum0, intUncert0 = gaussIntegrate(260,300,paramsAl0)
sum20, intUncert20 = gaussIntegrate(260,290,paramsAl20)
sum40,intUncert40 = gaussIntegrate(200,230,paramsAl40)
sum60, intUncert60 = gaussIntegrate(155,190,paramsAl60)
intUncerts = intUncert0, intUncert20, intUncert40, intUncert60
uncert = uncert + intUncerts
peakSum = sum0,sum20,sum40,sum60
peakSum = np.ravel(peakSum)
model = Model(kleinNishina)
data = RealData(xs, peakSum, sx=xerr, sy=uncert)
params = 3.24232058e-15,
odr = ODR(data, model, beta0=params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = kleinNishina(params_fit, xs)
electronRadius = params_fit[0]

plt.scatter(xs, peakSum, label = "Fitted Data" )
plt.errorbar(xs,peakSum, xerr= xerr, yerr = uncert)
plt.title("Counts at primary peak as a function of angle")
plt.xlabel("Theta")
plt.ylabel("Counts")
plt.plot(xs, V_fit, color = "orange", label = "Fitted Curve")
plt.gcf().text(0.95,0.5,"Electron Radius: " + str(np.round(params_fit[0],17)) + " $\\pm$ " + str(np.round(covar_fit[0],19)))
plt.gcf().text(0.95,0.4, "$\\chi^2/NDF$ = " + str(chisquared))
plt.legend()
plt.show()
Figure 24: The relation between the total counts across the photopeak as a function of angle is displayed above.
def kleinNishinaTheoretical(theta):
    alpha = 1.2931 
    coeff = (electronRadius**2)/2
    cos_theta = np.cos(theta)
    term1 = (1 + cos_theta**2) / (1 + alpha * (1 - cos_theta))**2
    term2 = 1 + (alpha**2 * (1 + cos_theta)**2) / ((1 + cos_theta**2) * (1 + alpha * (1 + cos_theta)))
    return coeff * term1 * term2  

V_fit_theoretical = kleinNishinaTheoretical(xs)
plt.plot(xs, V_fit_theoretical)
plt.title("Fit of $\\frac{d\\sigma}{d\\Omega}$ against $\\theta$")
plt.ylabel("$\\frac{d\\sigma}{d\\Omega}$")
plt.xlabel("$\\theta$")
plt.show()

Figure 25: This figure plots $\frac{d\sigma}{d\Omega}$ as a function of scattering angle


### Approach 2, Computational intensity
The distance from the detector to the source is the combination of the distance from the rod to the detector and the source to the detector. 
$$
18.6 \pm 0.1 \text{ cm} + 31 \text{ cm} = 49.6 \pm 0.1 \text{ cm}
$$
We can make a ratio between the photon flux at the detector and the photon flux at the rod using the inverse square relation we derived earlier.

$$
Q
$$
$$
T_{rod} = \frac{1}{0.31^{1.252\pm 0.063}}
$$
$$
T_\text{detector} = \frac{1}{0.496^{1.252+0.063}} 
$$
$$
\gamma  = 361671 \text{ counts}  \cdot T_\text{detector} = I \cdot T_\text{rod}
$$
$$
361671 = I \cdot \frac{T_{rod}}{T_\text{detector}}
$$
$$
T_{detector} = 0.007538014\begin{aligned} \Delta T_{detector} &= \sqrt{\left( \frac{\partial T_{detector}}{\partial a} \Delta a \right)^2 + \left( \frac{\partial T_{detector}}{\partial r} \Delta r \right)^2} \\ &= \sqrt{\left( \left( -(log(r) / r ^ a) \right) \cdot \Delta a \right)^2 + \left( \left( -(a / r ^ (a + 1)) \right) \cdot \Delta r \right)^2} \\ &= 0.0018540829 \\ &= 1.8540829 \times 10^{-3} \\ &= 2 \times 10^{-3} \end{aligned}
$$
$$
T_{detector} = \left( 8 \pm 2 \right) \times 10^{-3}
$$
$$
T_{detector} = 0.0135773546\begin{aligned} \Delta T_{detector} &= \sqrt{\left( \frac{\partial T_{detector}}{\partial a} \Delta a \right)^2} \\ &= \sqrt{\left( \left( -(3.4339872044851463 / 31 ^ a) \right) \cdot \Delta a \right)^2} \\ &= 0.0029373411 \\ &= 2.9373411 \times 10^{-3} \\ &= 3 \times 10^{-3} \end{aligned}
$$
$$
T_{detector} = \left( 1.4 \pm 0.3 \right) \times 10^{-2}
$$
$$
T_{ratio} = 1.75 \begin{aligned} \Delta T_{ratio} &= \sqrt{\left( \frac{\partial T_{ratio}}{\partial T} \Delta T \right)^2 + \left( \frac{\partial T_{ratio}}{\partial t} \Delta t \right)^2} \\ &= \sqrt{\left( \left( -(t / T ^ 2) \right) \cdot \Delta T \right)^2 + \left( \left( 1 / T \right) \cdot \Delta t \right)^2} \\ &= 0.5762215286 \\ &= 5.762215286 \times 10^{-1} \\ &= 6 \times 10^{-1} \end{aligned}
$$
$$
T_{ratio} = \left( 1.8 \pm 0.6 \right)
$$
$$
I = 200928.3333333333\begin{aligned} \Delta I &= \sqrt{\left( \frac{\partial I}{\partial R} \Delta R \right)^2} \\ &= \sqrt{\left( \left( -(3.61671e+5 / R ^ 2) \right) \cdot \Delta R \right)^2} \\ &= 66976.1111111111 \\ &= 6.6976111111 \times 10^{4} \\ &= 7 \times 10^{4} \end{aligned}
$$
$$
I = \left( 2 \pm 0.7 \right) \times 10^{5}
$$
It is worth noting that this calculated photon flux is an order of magnitude higher then the previously calculated value.
Using this value, and the previously calculated values we can find the coefficient in front of $\Sigma_{\gamma}'$ using the following relation: 
$$
\frac{d\sigma}{d\Omega} = \frac{\Sigma_{\gamma}'}{n_{\theta }I \Delta\Omega t\epsilon}
$$
Our coefficient is:
$$
\beta = 1.6721702207999995 \times 10^{36} \begin{aligned} \Delta \beta &= \sqrt{\left( \frac{\partial \beta}{\partial I} \Delta I \right)^2 + \left( \frac{\partial \beta}{\partial n} \Delta n \right)^2 + \left( \frac{\partial \beta}{\partial DO} \Delta DO \right)^2} \\ &= \sqrt{\left( \left( DO * 1.98162e+5 / 5 * n \right) \cdot \Delta I \right)^2 + \left( \left( DO * 1.98162e+5 / 5 * I \right) \cdot \Delta n \right)^2 + \left( \left( n * 1.98162e+5 / 5 * I \right) \cdot \Delta DO \right)^2} \\ &= 5.92833881279609e+35 \\ &= 5.9283388128 \times 10^{35} \\ &= 6 \times 10^{35} \end{aligned}
$$
$$
\beta = \left( 1.7 \pm 0.6 \right) \times 10^{36}
$$
def kleinNishina2(params, x):
    alpha = 1.2931
    coeff = (params[0]**2 * 1.7 * 10 ** 34)/2
    cos_theta = np.cos(x)
    term1 = (1 + cos_theta**2) / (1 + alpha * (1 - cos_theta))**2
    term2 = 1 + (alpha**2 * (1 + cos_theta)**2) / ((1 + cos_theta**2) * (1 + alpha * (1 + cos_theta)))
    result = coeff * term1 * term2
    return(result)
def gausFlip(x, params):
    return params[0] * np.exp( - ( x - params[1] )**2/( 2 * params[2]**2) )

def gaussIntegrate(start, stop, args):
    return quad(gausFlip, start, stop , args=(args))

model = Model(kleinNishina2)
data = RealData(xs, peakSum, sx=xerr, sy=uncert)
params = 3.24232058e-15,
odr = ODR(data, model, beta0=params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = kleinNishina2(params_fit, xs)
electronRadius2 = params_fit[0]


plt.scatter(xs, peakSum )
plt.errorbar(xs,peakSum, xerr= xerr, yerr = uncert)
plt.title("Counts at primary peak as a function of angle")
plt.xlabel("Theta")
plt.ylabel("Counts")
plt.plot(xs, V_fit, color = "orange", label = "Fitted Curve")
plt.gcf().text(0.95,0.5,"Electron Radius: " + str(np.round(params_fit[0],17)) + " $\\pm$ " + str(np.round(covar_fit[0],19)))
plt.gcf().text(0.95,0.4, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()
Figure 26: This figure is analogous to figure 24, but using the second, computational approach of determining intensity. 

## Finding unknown material: 

All values in the coefficient for $\Sigma_{\gamma}'$ should stay the same except for the $n_{\theta}$ value. We also have the value for electron radius now, so we can rewrite the previous equation 2 in a form that solves for $n_{\theta}$
$$
\frac{1}{2 }r^{2}n_{\theta} I \Delta\Omega t \epsilon\left[ \frac{1 + \cos ^{2}\theta}{[1 + \alpha(1-\cos\theta)]^{2}} \right] \left[ 1 + \frac{\alpha^{2} (1+\cos\theta)^{2}}{(1+\cos ^{2}\theta)[1+\alpha(1+\cos\theta)]} \right] = \Sigma'_{\gamma} 
$$

We can solve for all the constants in the front: 
$$
\frac{1}{2} r^{2}_{\text{elecron}}  \times I \times \Delta\Omega \times t\times \epsilon
$$
None of these should have changed from before, and using the value of electron radius we can calculate the following: 

$$
\beta = -2.076 \times 10^{-22}\begin{aligned} \Delta \beta &= \sqrt{\left( \frac{\partial \beta}{\partial DO} \Delta DO \right)^2 + \left( \frac{\partial \beta}{\partial R} \Delta R \right)^2} \\ &= \sqrt{\left( \left( -(5.152212e+8 * R) \right) \cdot \Delta DO \right)^2 + \left( \left( -(5.152212e+8 * DO) \right) \cdot \Delta R \right)^2} \\ &= 1.6e-23 \\ &= 1.6 \times 10^{-23} \\ &= 2 \times 10^{-23} \end{aligned}
$$
$$
\beta = \left( -2.076 \pm 2 \right) \times 10^{-22}
$$
Using this to rewrite the above equation: 
$$
 \beta rn_{\theta}\left[ \frac{1 + \cos ^{2}\theta}{[1 + \alpha(1-\cos\theta)]^{2}} \right] \left[ 1 + \frac{\alpha^{2} (1+\cos\theta)^{2}}{(1+\cos ^{2}\theta)[1+\alpha(1+\cos\theta)]} \right] = \Sigma'_{\gamma} 
$$
Now we fit the curve for unknown material data to this, and solve for $n_{\theta}$
def kleinNishinaMod(params, x):
    alpha = 1.2931
    coeff = params[0] * 2.076129e-22
    cos_theta = np.cos(x)
    term1 = (1 + cos_theta**2) / (1 + alpha * (1 - cos_theta))**2
    term2 = 1 + (alpha**2 * (1 + cos_theta)**2) / ((1 + cos_theta**2) * (1 + alpha * (1 + cos_theta)))
    result = coeff * term1 * term2
    return result

uncert = np.add(binToEnergy(peaksAlUnc)[1], binToEnergy(peaksAl)[1]) * 1000 
sum0, intUncert0 = gaussIntegrate(260,300,paramsUn0)
sum20, intUncert20 = gaussIntegrate(260,290,paramsUn20)
sum40,intUncert40 = gaussIntegrate(200,230,paramsUn40)
sum60, intUncert60 = gaussIntegrate(155,190,paramsUn60)
intUncerts = intUncert0, intUncert20, intUncert40, intUncert60
uncert = uncert + intUncerts
peakSum = sum0,sum20,sum40,sum60
peakSum = np.ravel(peakSum)
model = Model(kleinNishinaMod)
data = RealData(xs, peakSum, sx=xerr, sy=uncert)
params = 3.24232058e-15,
odr = ODR(data, model, beta0=params)
odr_result = odr.run()
params_fit = odr_result.beta
covar_fit = odr_result.sd_beta
chisquared = odr_result.res_var
V_fit = kleinNishinaMod(params_fit, xs)
n_t = params_fit[0]
plt.scatter(xs, peakSum )
plt.errorbar(xs,peakSum, xerr= xerr, yerr = uncert)
plt.title("Counts at Primary electron peak as a function of angle in unknown material")
plt.xlabel("Theta")
plt.ylabel("Counts")
plt.plot(xs, V_fit, color = "orange", label = "Fitted Curve")
plt.gcf().text(0.95,0.5,"$N_{\\theta}$: " + str("{:e}".format(params_fit[0],1)) + " $\\pm$ " + str("{:e}".format(covar_fit[0],1)))
plt.gcf().text(0.95,0.4, "$\\chi^2/NDF$ = " + str(chisquared))
plt.show()


### Finding material
Now we have the value of $n_{\theta}$ for the unknown material, we can proceed to find the specific terms that will determine what the unknown rod is made of. 
$$
n_{\theta} = \rho VN_{A} \sum_{i} w_{i} \frac{z_{i}}{M_{i}}
$$
We know the value of $V$, and $N_{a}$ is a constant. We can remove those:

$$
\frac{4.48276\times 10^{26}}{N_{A}V} = 118 \pm 9 
$$

This is equal to the following:

$$
D = 118.158287338 \begin{aligned} \Delta D &= \sqrt{\left( \frac{\partial D}{\partial n} \Delta n \right)^2 + \left( \frac{\partial D}{\partial v} \Delta v \right)^2} \\ &= \sqrt{\left( \left( v * 6.022e+23 / (6.022e+23 * v) ^ 2 \right) \cdot \Delta n \right)^2 + \left( \left( -(n * 6.022e+23 / (6.022e+23 * v) ^ 2) \right) \cdot \Delta v \right)^2} \\ &= 8.9692344681 \\ &= 8.9692344681 \times 10^{0} \\ &= 9 \times 10^{0} \end{aligned}
$$

$$
D = 118 \pm 9
$$
$$
118 \pm 9 = \rho\sum_{i} w_{i} \frac{z_{i}}{M_{i}}
$$

We took measurements of the weight of the mystery rod, and we have the dimensions, so we can calculate the density: 

$$
\frac{\text{mass}}{\pi h r^{2}} = \text{ density}
$$
$$
D = 8.1101295469\begin{aligned} \Delta D &= \sqrt{\left( \frac{\partial D}{\partial m} \Delta m \right)^2 + \left( \frac{\partial D}{\partial d} \Delta d \right)^2 + \left( \frac{\partial D}{\partial h} \Delta h \right)^2} \\ &= \sqrt{\left( \left( h * pi / (pi * h * (d / 2) ^ 2) ^ 2 * (d / 2) ^ 2 \right) \cdot \Delta m \right)^2 + \left( \left( m * -1 / 2 / (pi * h * (d / 2) ^ 2) ^ 2 * pi * h * d \right) \cdot \Delta d \right)^2 + \left( \left( -(m / (pi * h * (d / 2) ^ 2) ^ 2 * (d / 2) ^ 2 * pi) \right) \cdot \Delta h \right)^2} \\ &= 0.4077981634 \\ &= 4.077981634 \times 10^{-1} \\ &= 4 \times 10^{-1} \end{aligned}
$$
$$
D = 8.1 \pm 0.4 \text{ g/cm}^{3}
$$
This leads me to suspect the mystery material is bronze. We can factor out this density to yield the following: 
$$
\frac{118\pm9}{8.1 \pm 0.4 \text{ g/cm}^{3}} = \sum_{i} w_{i} \frac{z_{i}}{M_{i}}
$$
$$
w = 14.5679012346\begin{aligned} \Delta w &= \sqrt{\left( \frac{\partial w}{\partial n} \Delta n \right)^2 + \left( \frac{\partial w}{\partial d} \Delta d \right)^2} \\ &= \sqrt{\left( \left( 1 / d \right) \cdot \Delta n \right)^2 + \left( \left( -(n / d ^ 2) \right) \cdot \Delta d \right)^2} \\ &= 1.3236721277 \\ &= 1.3236721277 \times 10^{0} \\ &= 1 \times 10^{0} \end{aligned}
$$
$$
 15\pm 1  = \sum_{i} w_{i} \frac{z_{i}}{M_{i}}
$$
Assuming that the material is primarily made of 2 elements, copper and tin. We can find $\frac{z_{i}}{m_{i}}$ for both of these 
$$
\begin{cases}
\text{ copper } \frac{z}{m} = 0.4563623202 \\
\text{ tin} \frac{z}{m} = 0.42119450762
\end{cases}
$$
### Conclusions: 
The anaylsis of the compton scattering data with the Klien-Nishina differential scattering model yielded literature-matching results for the classical interaction radius of an electron. Our data fit the model well with a chi-squared of ~0.75, and the fit was within the experimental uncertainty for 3 out of the 4 data points. It is likely if we had taken more trials at the 20 degree point we would have obtained a better fit. The second approach seemed less accurate, with similar chi-squared values but values for electron radius that were outside of uncertainty from the given literature values for the classical electron interaction radius of 2.817E-15.

Unfortunately, it appears that there exists no real combination of the materials under our current model that would sum to 15. This indicates a mistake in either data collection or analysis. However, this being said, I believe that the material is bronze, due to its hue and weight. The quantitative data for the material is inconclusive. 
