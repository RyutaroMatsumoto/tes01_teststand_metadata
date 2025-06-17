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
| period | 5 | 
| run | 1-5 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-05-16 | 
| Operators | Yuki Mitsuya, Ryutaro Matsumoto | 
| Goal of measurement | Readout of TES Signal with hybrid setup, without switching noise and lower noise level. With 2amps in the Fridge |
| | |

## Experimental setup description
Used 100mK for TES. HBT amp **CMTLF1S**  and **AE-ADL5535** were set in 3K chamber and touched tight to the Cu for thermal release.<br>
Long Ni-Ti cabling deployed between TES and HBT amps, also tightly fixed on the 3K stage with Cu boards.<br>
Wave length of the light source was `1547nm` and `855nm`. With Variable Optical Attenuator, ranging from 0dB to -45dB, number of photons was controlled.  <br>
For better PNR, `855`nm introduced and TES Ib was set lower.
## TES detector
Not connected
| | |
|:----------------| :----------------|
| Type | Ir TES | 
| Name | NA | 
| Bias Current(Ib) | ``µA | 
| FLL Resistance(Rf) | `100`kΩ |
| ~~~(GBW) | `0.55`GHz |
| | |
## SQUID
| | |
|:----------------| :----------------|
| Name | F39 A or B | 
| Ib | `10.364`µA | 
| Vb | `169.4`µV | 
| Phib | `16.36`µA | 
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
detail data is in: ./../hardware/scope/p05

## Runs
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture). Swept OAT value.
|          |                 |        |            |              |                       |
| :------- | :-------------- |:----   | :--------- | :---------   |:----------------------   |
| **runs** | **waveforms**   |**WL**  | **OAT**    | **HBT_Amps** |**short description**     |
|`r001`    |`10000`          |`855`nm |`--dB`     | ON          | signal  10 photons level                  |
|`r002`    |`3000`           |`855`nm |`--dB`     | ON          | noise   10 photons level               |
|`r003`    |`10000`          |`855`nm |`--dB`     | ON          |signal  5 photons level                 |
|`r004`    |`3000`           |`855`nm |`--dB`     | ON          | noise   5 photons level                |
|`r005`    |`10000`           |`855`nm |`--dB`     | ON          | SQUID Saturation level                   |



## Remarks and comments
Reported progress on LTD upto this exp.
