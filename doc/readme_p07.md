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
| period | 7 | 
| run | 1-10 | 
| Location | UTokyo, building 9,  room 9-210 |
| Date of measurement (yyyy-mm-dd) | 2025-07-02~13 | 
| Operators | Ryutaro Matsumoto, Dr.Yuki Mitsuya   | 
| Goal of measurement | Readout of TES both timing and PNR Signal at O(1) level photons w/ hybrid setup. w/ 1 amp in the Fridge. w/ large data for averaging (timing signal) |
| | |

## Experimental setup description
Used 100mK for TES. HBT amp **CMTLF1S**  was set in 3K chamber and touched◊ tight to the Cu for thermal release.<br>
Long Ni-Ti cabling deployed between TES and HBT amps, also tightly fixed on the 3K stage with Cu boards.<br>
Wave length of the light source was `1547`nm and `1310`nm.<br>
 With Variable Optical Attenuator, ranging from 0dB to -45dB, number of photons was controlled.  <br>
For better PNR and speed of reaction, new TES(12nm thickness) was introduced by Nagahara-san. <br>
2nd stage amp was ejected for better PNR (contamination from amp to SQUID signal (**need to confirm**)
For now, 2nd amp was not deployed, but in the near future, we are trying to put it in the housing of LN(77K) outside of the ADR for better Nt and gain.
## TES detector
| | |
|:----------------| :----------------|
| Type | Ir TES 12nm thickness (from Daizo Nagahara)| 
| Name | NA | 
| Size | 10µm square |
| Bias Current(Ib) | Various Values | 
| FLL Resistance(Rf) | `100`kΩ |
| GBW | `0.55-0.23`GHz |
| | |
## SQUID
| | |
|:----------------| :----------------|
| Name | F39 A| 
| Ib | `10.364`µA | 
| Vb | `173.03`µV | 
| Phib | `16.48`µA | 
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
detail data is in: ./../hardware/scope/p07

## Runs
First, we conducted IV curve measurement at 100mK for this TES.<br>
All runs in this period are taken with voltage signal from **TES(w/ SQUID)** amplified by the **CMTLF1S + AE-ADL** SiGe HBTs (same as `p02`) and **NAMEOFAMP**(3rd Amp at room temperture). Swept OAT value.
|          |          |             |       |           |         |       |        |             |                          |
| :------- | :------- |:------------|:----  |:-----     |:----    | :-----| :----- | :---------  |:----------------------   |
| **runs** |**Target**|**waveforms**|**Tb** |**Ib(TES)**|**WL**   |**OAT**|**Amps**|**Format**   |**Short description**     |
|`r001`    |Timing    |`10,000`     |`150`mK|`70`µA     |`1547`nm |`45`dB | ON     |`20`µs/`50`ps| data not found               |
|`r002`    |Timing    |`10,000`     |`150`mK|`70`µA     |`1547`nm |`45`dB | ON     |`20`µs/`50`ps|O(1) level photon for timing, delay was 175ns from the trigger     |
|`r003`    |Timing    |`5,000`      |`150`mK|`70`µA     |`1547`nm |`35`dB | ON     |`20`µs/`50`ps|O(5) level signal for timing reference           |
|`r004`    |Timing    |`5,000`      |`150`mK|`70`µA     |`1547`nm |`--`dB | ON     |`20`µs/`50`ps|Noise measurement for timing                |
|`r005`    |PNR       |`3,000`      |`150`mK|`70`µA     |`1547`nm |`--`dB | ON     |`20`µs/`20`ns|Noise for PNR     |
|`r006`    |PNR       |`10,000`     |`150`mK|`70`µA     |`1547`nm |`45`dB | ON     |`20`µs/`20`ns|O(1) level PNR      |
|`r007`    |PNR       |`10,000`     |`150`mK|`70`µA     |`1547`nm |`35`dB | ON     |`20`µs/`20`ns|O(5) level PNR reference               |
|`r008`    |PNR       |`10,000`     |`175`mK|`40`µA ?   |`1547`nm |`45`dB | ON     |`20`µs/`20`ns|O(1) level PNR, in search for better PNR             |
|`r009`    |PNR       |`3,000`      |`175`mK|`40`µA ?   |`1547`nm |`--`dB | ON     |`20`µs/`20`ns|Noise for PNR  |
|`r010`    |PNR       |`10,000` ?   |`200`mK|`45`µA     |`1310`nm |`40`dB | ON     |`20`µs/`4`ns |O(1) level PNR, in search for better PNR       |
|`r011`    |PNR       |`10,000` ?   |`200`mK|`37.6`µA   |`1310`nm |`40`dB | ON     |`20`µs/`4`ns |O(1) level PNR, in search for better PNR       |
|`r012`    |PNR       |`10,000` ?   |`200`mK|`37.6`µA   |`1310`nm |`37.5`dB| ON    |`20`µs/`4`ns |O(5)? level PNR, in search for better PNR      |
|`r013`    |PNR       |`5,000`      |`200`mK|`37.6`µA   |`1310`nm |`--`dB | ON     |`20`µs/`4`ns |Noise for PNR       |
|`r014`    |Timing    |`30,000`     |`200`mK|`37.6`µA   |`1310`nm |`37.5`dB| ON    |`20`µs/`50`ps|Timing data @ same condition          |
|`r015`    |PNR       |`15,000`     |`260`mK|`55`µA     |`1310`nm |`40`dB | ON     |`20`µs/`5`ns |O(2)? level PNR, in search for better PNR      |
|`r016`    |PNR       |`3,000`      |`260`mK|`55`µA     |`1310`nm |`--`dB | ON     |`20`µs/`5`ns |Noise for PNR     |
|`r017`    |PNR       |`10,000`     |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`20`µs/`20`ns|O(2) level PNR, Operated by Dr.Mitsuya    |
|`r018`    |PNR       |`3,000`      |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`20`µs/`20`ns|Noise for PNR, Operated by Dr.Mitsuya     |
|`r019`    |PNR       |`10,000`     |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`20`µs/`20`ns|O(2) level PNR, Operated by Matsumoto, confirmation exp  |
|`r020`    |PNR       |`3,000`      |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`20`µs/`20`ns|Noise for PNR, Operated by Matsumoto, confirmation exp   |
|`r021`    |Timing    |`6,000`      |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`10`µs/`50`ps|Timing for condition above. Relatively small data point      |
|`r022`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`10`µs/`50`ps|Timing for condition above.           |
|`r023`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`32.5`dB| ON    |`10`µs/`50`ps|Reference data  w/ O(10) level photons            |
|`r024`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`--`dB | ON     |`10`µs/`50`ps|Noise data for Timing            |
|`r025`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`0`dB  | ON     |`1`µs/`50`ps|Reference1 for Timing(C4:DC50Ω)            |
|`r026`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`40`dB | ON     |`1`µs/`50`ps|2.5 level photons Timing(C4:DC50Ω)            |
|`r027`    |PNR       |`10,000`     |`300`mK|`35.9`µA   |`1310`nm |`32.5`dB| ON    |`20`µs/`20`ns|PNR at 12 level photons            |
|`r028`    |PNR       |`3,000`      |`300`mK|`35.9`µA   |`1310`nm |`--`dB | ON     |`20`µs/`20`ns|Noise for PNR           |
|`r029`    |Timing    |`30,000`     |`300`mK|`35.9`µA   |`1310`nm |`--`dB | ON     |`1`µs/`50`ps|Noise data for Timing            |

## Remarks and comments
After struggling with 300kHz noise, we concluded that was coming from outside of the room, apparently magnetic noise. So we added a Pb (super conducting material) shield around TES and SQUID, cooled down to 100mK, but we couldn't properly keep down to 100mK.  We suggested it was because of Pb shield superconductivity, even it was covered with Cu tape. At 293K and 3K, 300kHz noise was not observed.<br>
After this failure, we conducted this measurement just to clarify the insufficient cool down was because of Pb shield or the fridge. During this using the original cupper housing for TES, the stage was cooled down properly, so we concluded the Pb shield was the cause. We assumed without the magnetic shield 300kHz noise would be visible again, but it didn't appear. It seemed like a temporary noise from other experiment in the building. <br>
With new TES and w/o magnet shielding, we got timing data properly, and went for PNR check. Then with contamination from SiGe amplifier, SQUID signal was poor at PNR. So, we searched a num of configs and found 300mK(close to Tc) and relatively low TES bias(35µA) was suitable. This is because Ib vibration and thermal loss from TES to the bath were supressed we guess.<br> 

However with TES(24nm thickness) and without 2nd amp, gain had been insufficient for O(1) photons level, this time with TES(12ns thickness), we got timing signal with 2.4 photons just with SiGe amp in 3K stage.<br>