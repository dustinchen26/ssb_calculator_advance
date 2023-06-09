# ssb_calculate
online calculate: https://dustinchen26.github.io/ssb_calculate/

## Usage
```
Author: Dustin_Chen Email: Dustin_Chen@compal.com or chuhpsdustin@gmail.com
[Usage] Input (band /freq_low /freq_high /carrierBw(RB)), then it will calculate the valid (gscn /absFreqPointA /absArfcnPointA /absFreqSsb /absArfcnSsb /dlEarfcn /nDlCenterFreq /Kssb /offsetToPointA )
// support BW
n41 => freq range [2496000, 2690000]
n48 => freq range [3550000, 3700000]
n78 => freq range [3300000, 3800000]
n79 => freq range [4400000, 5000000]
For BW>=48, choose Spec 38.213 Table 13-4 CORESET index=10
For BW<48, choose Spec 38.213 Table 13-4 CORESET index=0
(Note) bandwidth RB: SCS30 100M=273RB, 90M=245RB, 80M=217RB, 70M=189RB, 60M=162RB, 50M=133RB, 45M=119RB, 40M=106RB, 35M=92RB, 30M=78RB, 25M=65RB, 20M=51RB, 15M=38RB, 10M=24RB, 5M=11RB
Please input the following parameters: ex:(band,freq_low,freq_high,carrierBw(RB))=(41, 2565749, 2565751, 273)
```
## Example
```
Please input 3 parameters: 
ex: 
band = 41
freq_low = 2565749
freq_high = 2565751
carrierBw(RB) = 273

Calculate:
gscn=6312, absFreqPointA=2516610, absArfcnPointA=503322, absFreqSsb=2524950, absArfcnSsb=504990, dlEarfcn=513150, nDlCenterFreq=2565750, Kssb=4, offsetToPointA=26
gscn=6315, absFreqPointA=2516610, absArfcnPointA=503322, absFreqSsb=2526150, absArfcnSsb=505230, dlEarfcn=513150, nDlCenterFreq=2565750, Kssb=12, offsetToPointA=32
gscn=6318, absFreqPointA=2516610, absArfcnPointA=503322, absFreqSsb=2527350, absArfcnSsb=505470, dlEarfcn=513150, nDlCenterFreq=2565750, Kssb=20, offsetToPointA=38
... etc
```
