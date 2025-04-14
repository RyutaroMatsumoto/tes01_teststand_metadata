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
| period | 1 | 
| run | 4-7 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-04-03 | 
| Operators | Katsuhiro Dobashi, Ryutaro Matsumoto | 
| Goal of measurement | Characterization of CMTLF1S: Noise |
| | |

## Experimental setup description
Under room temperature. Used Oscilloscope as Spectrum Analyzer was not reliable.<br>
No special cover or termination introduced.<br>

## TES detector
Not Connected.
| | |
|:----------------| :----------------|
| Type | TES | 
| Name | NA | 
| Operation Current | NA | 
| | |

## Electronics
| ||
|:----------------| :----------------|
|Name| Vd(V) |
|CMTLF1S|`3.0`|
|||


## DAQ
Oscilloscope LECROYHDO6104B.
detail data is in: ./../hardware/scope/p01

## Runs
|                   |                 |            |            |                                   |
| :---------------- | :-------------- | :--------- | :--------- | :----------------------------------------------------------------------------------------------------------- |
| **runs**          | **# waveforms** | **Amp connection** | **Termination** | **short description**                                                                                        |
| `r004`            | 500           | yes | no  | Noise measurement for high frequency                        |
| `r005`            | 500           | yes | no  | Noise measurement for low frequency                         |
| `r006`            | 100           | no  | yes | Scope noise for low frequency                               |
| `r007`            | 100           | no  | yes | Scope only noise High frequency    |
|                   |                 |            |            |                       |

## Remarks and comments
Spectrum Analyzer was not reliable.<br>
Termination and isolation could be improved. Also, DC was directly provided from **NAMEOFDCSUPPLIER** Using Enelope(1.2V*3+ LDO) or, super capasitor+LDO will be lower noise DC supplier.

