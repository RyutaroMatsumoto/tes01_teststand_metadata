## <img src="./../logo/utokyo_logo.png" alt="logo" width="30"/> Teststand data 

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../logo/utokyo_logo.png");
  }
}
</style>

## General measurement information
| | |
|:----------------| :----------------|
| Setup name | `tes01`|
| period | 3 | 
| run | 1-14 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-04-11 | 
| Operators | Yuki Mitsuya, Ryutaro Matsumoto | 
| Goal of measurement | Readout of TES Signal with SQUID and HBT amps |
| | |

## Experimental setup description
Used 100mK for TES. HBT amps were set in 3K chamber and touched tight to the Cu for thermal release.<br>
Long Ni-Ti cabling deployed between TES and HBT amps, also tightly fixed on the 3K stage with Cu boards.<br>
Wave length of the light source was `1547nm`. With Variable Optical Attenuator, ranging from 0dB to -45dB, number of photons was controlled.  

## TES detector
Not connected
| | |
|:----------------| :----------------|
| Type | Ir TES | 
| Name | NA | 
| Bias Current(Ib) | `45`µA | 
| | |
## SQUID
| | |
|:----------------| :----------------|
| Name | F39 A or B | 
| Ib | `10.364`µA | 
| Vb | `169.4`µV | 
| Phib | `15.93`µA | 
| | |
## Electronics
| |||||
|:----------------| :----------------| :----| :----| :----|
|Name| Vd(V) |Id(A)| datasheet Gain(Roomtemp) | Band Width| 
|CMTLF1S|`3.0`| `0.01`| `20` dB(@1GHz) |`1MHz-10GHz` |
|AE-ADL | `5.0` |`0.079`| `15~18`dB |`20MHz-1GHz`  |
|Room temp amp | `15.0` | `0.128` |`40`dB|`1kHz-2GHz` |
||||||

## DAQ
Oscilloscope LECROYHDO6104B.
detail data is in: ./../hardware/scope/p03

## Runs
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture).
|          |                 |            |              |           |            |                          |
| :------- | :-------------- | :--------- | :---------   |:--------- | :--------- |:----------------------   |
| **runs** | **waveforms** | **OAT**    | **HBT_Amps** |**I_bias** |**GBW**     |**short description**     |
|`r001`    |`10000`          |`-45dB`     | OFF          |`45µA`     | `7.2GHz`   | SQUID only Measurement for PNR calibration(light ON = signal)     from exp1 signal                    |
|`r002`    |`3000`           |`-45dB`     | OFF          |`45µA`     | `7.2GHz`   | SQUID only Measurement for PNR calibration(light OFF = noise)      from exp1 noise                   |
|`r003`    |`10000`          |`-45dB`     | ON           |`45µA`     | `7.2GHz`   |  Read out from both lines. 2 photons input      from exp2 signal                   |
|`r004`    |`3000`           |`-45dB`     | ON           |`45µA`     | `7.2GHz`   | Noise Measurement(light OFF = noise) with Amps ON      from exp2 noise                   |
|`r005`    |`5000`           |`0dB`       | ON           |`45µA`     | `1.0GHz` ? | Read out from both lines. Maximum strength light source     from exp3                    |
|`r006`    |`700`           |`-40dB`     | ON           |`45µA`     | `1.0GHz` ? | Read out from both lines. In serch of minimum strength light source detected via HBT    from exp4                    |
|`r007`    |`0`           |`-35dB`     | ON           |`45µA`     | `1.0GHz` ? | Read out from both lines. With the light strength at which TES signal from SQUID saturated.      from exp5                    |
|`r008`    |`3000`           |`-0dB`      | ON           |`125µA`     | `1.0GHz` ? | Read out from both lines. With the Maximum light strength.      from exp6-1                    |
|`r009`    |`3000`           |`-35dB`     | ON           |`125µA`     | `1.0GHz` ? | Read out from both lines. With the minimum light strength HBT signal visible.      from exp6-2                    |
|`r010`    |`0`              |`0dB`       | ON           |`285µA`     | `1.0GHz` ? | Read out from both lines. With the Maximum light strength. Signals apprently getting smaller     from exp7               |
|`r011`    |`5000`           |`0dB`       | ON           |`35µA`     | `1.0GHz` ? | Read out from both lines. With the maximum light.     from exp8-1                    |
|`r012`    |`5000`           |`-40dB`      | ON           |`35µA`     | `1.0GHz` ? | Read out from both lines. With the minimum light strength HBT signal visible.     from exp8-2                   |
|`r013`    |`10000`          |`-40dB`     | OFF          |`35µA`     | `1.0GHz`   | SQUID only Measurement for PNR calibration(light ON = signal)     from exp8 squid signal                    |
|`r014`    |`3000`           |`-40dB`     | OFF          |`35µA`     | `1.0GHz`   | SQUID only Measurement for PNR calibration(light OFF = noise)      from exp8 squid noise                   |
NC = Not Connected.
## Remarks and comments
r012 rise time constant of HBT signal(averaged) is around 15ns, which is clearly slower than initial bias point(r006, etc)<br>
comparing r003 and r004, there seems no difference in HBT output, suggesting that readout is something different?
Turned out later, single photon V shift would be 10mV, where we had assumed it to be around 20mV.

