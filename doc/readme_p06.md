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
| period | 6 | 
| run | 1-10 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-06-14 | 
| Operators | Yuki Mitsuya, Ryutaro Matsumoto | 
| Goal of measurement | Readout of TES Signal with hybrid setup. W/ 1 amp in the Fridge. w/ large data |
| | |

## Experimental setup description
Used 100mK for TES. HBT amp **CMTLF1S**  was set in 3K chamber and touched tight to the Cu for thermal release.<br>
Long Ni-Ti cabling deployed between TES and HBT amps, also tightly fixed on the 3K stage with Cu boards.<br>
Wave length of the light source was `1547nm`. With Variable Optical Attenuator, ranging from 0dB to -45dB, number of photons was controlled.  <br>
For better PNR, TES Ib was set low.
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
| Vb | `181.03`µV | 
| Phib | `17.27`µA | 
| | |
## Electronics
| |||||
|:----------------| :----------------| :----| :----| :----|
|Name| Vd(V) |Id(A)| datasheet Gain(Roomtemp) | Band Width| 
|CMTLF1S|`3.0`| `0.01`| `20` dB(@1GHz) |`1MHz-10GHz` |
|Room temp amp | `15.0` | `0.128` |`40`dB|`1kHz-2GHz` |
||||||


## DAQ
Oscilloscope LECROYHDO6104B.
detail data is in: ./../hardware/scope/p06

## Runs
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture). Swept OAT value.
|          |                 |        |            |              |                       |
| :------- | :-------------- |:----   | :--------- | :---------   |:----------------------   |
| **runs** | **waveforms**   |**WL**  | **OAT**    | **HBT_Amps** |**short description**     |
|`r001`    |`10,000`          |`1547`nm |`45dB`     | OFF          | signal  1 photon level, w/o semiconductor, PNR                  |
|`r002`    |`3000`           |`1547`nm |`45dB`     | OFF          | noise   1 photon level, w/o semiconductor, PNR              |
|`r003`    |`10,000`          |`1547`nm |`45dB`     | ON          |signal  1 photons level, w/ semiconductor, PNR                 |
|`r004`    |`3000`           |`1547`nm |`45dB`     | ON          | noise   1 photons level, w/ semiconductor, PNR                |
|`r005`    |`400,000`           |`1547`nm |`45dB`     | ON          | signal  1 photons level, Timing      |
|`r006`    |`3000`           |`1547`nm |`45dB`     | ON          | noise universal, Timing      |
|`r007`    |`10,000`          |`1547`nm |`40dB`     | ON          |signal  3 photons level, w/ semiconductor, PNR                 |
|`r008`    |`3000`           |`1547`nm |`40dB`     | ON          | noise   3 photons level, w/ semiconductor, PNR                |
|`r009`    |`400,000`           |`1547`nm |`40dB`     | ON          | signal  3 photons level, Timing      |
|`r010`    |`3000`           |`1547`nm |`0dB`     | ON          | timing signal, reference      |



## Remarks and comments
Reported progress on LTD upto this exp.