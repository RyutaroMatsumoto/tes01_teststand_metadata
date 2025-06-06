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
| period | 4 | 
| run | 1-6 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-05-12 | 
| Operators | Yuki Mitsuya, Ryutaro Matsumoto | 
| Goal of measurement | Readout of TES Signal with hybrid setup, without switching noise and lower noise level |
| | |

## Experimental setup description
Used 100mK for TES. HBT amp **CMTLF1S** was set in 3K chamber and touched tight to the Cu for thermal release.<br>
Long Ni-Ti cabling deployed between TES and HBT amps, also tightly fixed on the 3K stage with Cu boards.<br>
Wave length of the light source was `1547nm` and `855nm`. With Variable Optical Attenuator, ranging from 0dB to -45dB, number of photons was controlled.  <br>
For better PNR, `855`nm introduced and TES Ib was set lower.
## TES detector
Not connected
| | |
|:----------------| :----------------|
| Type | Ir TES | 
| Name | NA | 
| Bias Current(Ib) | `33`µA | 
| FLL Resistance(Rf) | `23.1`Ω |
| ~~~(GBW) | `1.04`GHz |
| | |
## SQUID
| | |
|:----------------| :----------------|
| Name | F39 A or B | 
| Ib | `10.364`µA | 
| Vb | `169.4`µV | 
| Phib | `15.57`µA | 
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
detail data is in: ./../hardware/scope/p02

## Runs
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture).
|          |                 |        |            |              |             |        |            |                          |
| :------- | :-------------- |:----   | :--------- | :---------   |:---------   |:-----  |:---------  |:----------------------   |
| **runs** | **waveforms**   |**WL**  | **OAT**    | **HBT_Amps** |**I_b(TES)** |**Rf**  |**GBW**     |**short description**     |
|`r001`    |`10000`          |`855`nm |`-50dB`     | OFF          |`33µA`       |`100`kΩ | `1.04GHz`  | SQUID only Measurement for PNR calibration(light ON = signal)     from exp1 signal                    |
|`r002`    |`3000`           |`855`nm |`-50dB`     | OFF          |`33µA`       |`100`kΩ | `1.04GHz`  | SQUID only Measurement for PNR calibration(light OFF = noise)      from exp1 noise                   |
|`r003`    |`10000`          |`855`nm |`-50dB`     | OFF          |`33µA`       |`23.1`kΩ| `1.04GHz`  | SQUID only Measurement for PNR calibration(light ON = signal)     from exp1 signal                    |
|`r004`    |`3000`           |`855`nm |`-50dB`     | OFF          |`33µA`       |`23.1`kΩ| `1.04GHz`  | SQUID only Measurement for PNR calibration(light OFF = noise)      from exp1 noise                   |
|`r005`    |`4000`           |`855`nm |`-50dB`     | ON          |`33µA`       |`23.1`kΩ| `1.04GHz`  | Just measured                  |
|`r006`    |`120`          |--------|------------| ON           |   ||   | Room temp HBT signal readout confirmation. Pulser: 20MHz, Vin = 1.0mVpp sin wave      |

NC = Not Connected.
## Remarks and comments
During noise measurement, we observed some dark counts(unstable superconducting state) with lower Ib(TES). To address this, we set Rf@FLL lower than usual:(=23.1Ω)
Tried several connection paterns making sure connectings were correct, but still not be able to catch the signal. Connections were confirmed later w/ room temp experiments.<br>
We assumed without 2nd amplifier, we couldn't get enough S/N ratio. (2nd amp has 15-18dB 20MHz - 1GHz) <br>

Good point is that we succeeded to eliminate switching noise by either of solutions: <br>
1. adding noise-cut trans pulser DC source <br>
2. re-wired SMA-TES on board cable which potencially had been touching GND and Signal lines.

