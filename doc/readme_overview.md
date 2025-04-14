## <img src="./../logo/utokyo_logo.png" alt="logo" width="50"/> Teststand overview 
This is an overview of the  TES `tes01` measurements. <br>
`tes01` measurement is with a novel readout system, `SQUID(PNR) + HBT(Timing)`.<br>
For more details on the individuals runs, see the readme files in this directory. 

The follow the following naming scheme: `readme_<period>_<runs>.md`.  

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../logo/lbnl_logo_dark.png");
  }
}
</style>

## Overview table: period 1 `p01`: CMTLF1S + Oscilloscope /Noise measurement
All runs in this period are taken with the **CMTLF1S** at room temperature for noise measurent.<br>
Used Oscilloscope as Spectrum Analyzer was not reliable.<br>
No special cover or termination introduced.<br>

|                   |                 |            |            |                                   |
| :---------------- | :-------------- | :--------- | :--------- | :----------------------------------------------------------------------------------------------------------- |
| **runs**          | **# waveforms** | **Amp connection** | **Termination** | **short description**                                                                                        |
| `r004`            | 500           | yes | no  | Noise measurement for high frequency                        |
| `r005`            | 500           | yes | no  | Noise measurement for low frequency                         |
| `r006`            | 100           | no  | -- | Scope noise for low frequency                               |
| `r007`            | 100           | no  | -- | Scope only noise High frequency    |
|                   |                 |            |            |                       |



## Overview table: period 2 `p02`: Pulser + CMTLF1S + AE-ADL +Oscilloscope/Gain measurement
All runs in this period are taken with the **FastEdge** pulser(Rise-time of 32ps) and **CMTLF1S + AE-ADL** SiGe HBT amplifiers.<br> 
All measuments are done under room temperature.<br> 
|          |                 |              |                       |     |
| :------- | :-------------- | :----------- | :-------------------- | :---|
| **runs** | **# waveforms** | **Attenuator** | **CMTLF1S** | **AE-ADL**|
| `r001`   | 1,000           | no             | `3.0`V      | `0`V      |
| `r002`   | 1,000           | no             | `3.0`V      | `5.0`V    |
| `r003`   | 1,000           | no             | `3.0`V      | NC        |
| `r004`   | 1,000           | yes            | `3.0`V      | NC        |
| `r005`   | 1,000           | yes            | `3.0`V      | `5.0`V    |


## Overview table: period 3 `p03`: TES(w/ SQUID) + CMTLF1S + AE-ADL/Actual read out test 
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture).
|          |                 |            |            |                         |
| :------- | :-------------- | :--------- | :--------- | :---------------------- |
| **runs** | **# waveforms** | **buffer** | **cables** | **short description**   |

