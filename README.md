# ssb_calculate
online calculate: https://dustinchen26.github.io/ssb_calculator_advance/

## Usage
```
Author: Dustin_Chen Email: Dustin_Chen@compal.com or chuhpsdustin@gmail.com
earfcn to freq convert : https://5g-tools.com/5g-nr-arfcn-calculator/

[Usage] Input carrier(band/ freq_low/ freq_high/ carrierBw(RB)), then it will calculate the valid (gscn /absFreqPointA /absArfcnPointA /absFreqSsb /absArfcnSsb /dlEarfcn /nDlCenterFreq /Kssb /offsetToPointA )
n41 => freq range [2496000, 2690000]
n48 => freq range [3550000, 3700000]
n78 => freq range [3300000, 3800000]
n79 => freq range [4400000, 5000000]

For n79, CORESET0 use 38.213 Table 13-6 Index 4.
For others, if BW>=48, CORESET0 use Table 13-4 Index 10. // Try to have 48 RB size for CS-0 to avoid allocation failure for SIB1 during SSB(20RBs) overlap
For others, if BW<48, use Table Index 0. // if 48 RB is not available, get the best fit CS0

(Note) bandwidth RB: SCS30 100M=273RB, 90M=245RB, 80M=217RB, 70M=189RB, 60M=162RB, 50M=133RB, 45M=119RB, 40M=106RB, 35M=92RB, 30M=78RB, 25M=65RB, 20M=51RB, 15M=38RB, 10M=24RB, 5M=11RB
```

## Example
```
Please input the following parameters:
band: 48
carrierBw(RB): 106
freq_low: 3624990
freq_high: 3624990
offsetToCarrier: 102
coreset0RB: 24
coreset0offset: 2

Calculate:
gscn=7923, absFreqPointA=3569190, absArfcnPointA=637946, absFreqSsb=3610560, absArfcnSsb=640704, dlEarfcn=641666, nDlCenterFreq=3624990, Kssb=22, offsetToPointA=208
gscn=7924, absFreqPointA=3569190, absArfcnPointA=637946, absFreqSsb=3612000, absArfcnSsb=640800, dlEarfcn=641666, nDlCenterFreq=3624990, Kssb=22, offsetToPointA=216
gscn=7925, absFreqPointA=3569190, absArfcnPointA=637946, absFreqSsb=3613440, absArfcnSsb=640896, dlEarfcn=641666, nDlCenterFreq=3624990, Kssb=22, offsetToPointA=224
...etc
```
