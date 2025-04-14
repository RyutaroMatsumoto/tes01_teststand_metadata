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
| period | 2 | 
| run | 1-5 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-04-07,8 | 
| Operators | Ryutaro Matsumoto | 
| Goal of measurement | Characterization of CMTLF1S + AE-ADL: Gain |
| | |

## Experimental setup description
Under room temperature. Used Oscilloscope to see the pulser waveform and output waveform.
Attenuator was introduces from r`004` right next to the pulser.

## TES detector
Not connected
| | |
|:----------------| :----------------|
| Type | TES | 
| Name | NA | 
| Operation Current | NA | 
| | |
## Pulser
| | |
|:----------------| :----------------|
| Type | Pulser | 
| Name | FastEdge | 
| Rise time | `32` ps | 
| Fall time | ---- |
| Freqency | `1` kHz|
| Amplitude(raw) | ~`350` mV|
| Amplitude (w/ Attenuator) | ~`4`mV|
|||
Attenuator was hand-made π-type attenuator
## Electronics
| ||||
|:----------------| :----------------| :----| :----|
|Name| Vd(V) |Id(A)| datasheet Gain(Roomtemp, ~1GHz) |
|CMTLF1S|`3.0`| `0.01`| `20` dB | 
|AE-ADL | `5.0` |`0.079`| --- |
|||||

## DAQ
Oscilloscope LECROYHDO6104B.
detail data is in: ./../hardware/scope/p02

## Runs
|          |                 |              |                       |     |
| :------- | :-------------- | :----------- | :-------------------- | :---|
| **runs** | **# waveforms** | **Attenuator** | **CMTLF1S** | **AE-ADL**|
| `r001`   | 1,000           | no             | `3.0`V      | `0`V      |
| `r002`   | 1,000           | no             | `3.0`V      | `5.0`V    |
| `r003`   | 1,000           | no             | `3.0`V      | NC        |
| `r004`   | 1,000           | yes            | `3.0`V      | NC        |
| `r005`   | 1,000           | yes            | `3.0`V      | `5.0`V    |
NC = Not Connected.
## Remarks and comments
When 1st amp OFF(Vd=0V), reflection was high(with 12.5ns delay = 125cm(single path)).
Without an attenuator, CMTLF1S saturates.

