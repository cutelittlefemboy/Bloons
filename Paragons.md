# Paragon mechanics

A paragon upgrade becomes available when all three tier 5s of a tower are on the map at once. When purchased, **all** towers of this type merge into a single Paragon tower.

The _degree_ of the paragon can vary from 1 to 100, depending on the towers merged. Higher degrees have improved damage, pierce, and attack speed. All paragons additionally have significant damage bonuses against bosses and elite bosses.

Paragons cannot receive any buffs from other towers, but are affected by Monkey Knowledge.

## Degree requirements

The merged towers contribute "power" to the paragon degree as follows:

- 10k per tier 5 tower
    
    - excludes the first 3 tier 5s that are being combined
        
    - maximum 90k (9 additional tier 5s)
        
- 100 per upgrade
    
    - excludes all tier 5 towers
        
    - maximum 10k (100 upgrades = 17 crosspathed tier 4s)
        
- 1 per $25 spent
    
    - excludes the first 3 tier 5s
        
    - maximum 10k ($250k)
        
- 1 per 180 pops
    
    - includes all towers
        
    - generated income also contributes, at a rate of $1 = 4 pops
        
    - maximum 90k (16.2 million damage)
        

A minimum degree of 1 is guaranteed, and a maximum degree of 100 requires all 200k possible power. For all other degrees, the requirement is:

_(50 degree__3_ _+ 5025 degree__2_ _+ 168324 degree + 843000) / 600_

## Bonuses

In these formulas, _d(x)_ is the damage at degree _x_, while _d_ on its own is the base damage as listed in tower-specific Popology. Likewise for other stats.

Damage:

- +1% per degree, +1 per 10 degrees, max +100% + 10
    
    - d(100) = d * 2 + 10
        
    - d(x) = d * (1 + (x-1)*0.01) + floor((x-1)/10)
        
- stacks with other damage, for example
    
    - cd(x) = cd * (1 + (x-1)*0.01)
        
    - total against ceramics is d(x) + cd(x) as usual
        

Boss damage:

- +20% per 20 degrees, applied after all other scaling, as well as to _bd_ directly (so _bd_ is overall double-counted)
    
    - first calculate bd(x) = bd * (1 + (x-1)*0.01) as normal
        
    - total against bosses is (d(x) + md(x) + 2*bd(x)) * (1 + floor(x/20)*0.2) - bd(x)
        
- also affects damage-over-time but without double-counting _bd_
    

Elite boss damage:

- all paragon attacks deal double damage against elite bosses
    
    - total: 2 * (d(x) + md(x) + bd(x)) * (1 + floor(x/20)*0.2)
        
- for degrees 20+, _bd_ is again counted twice
    
    - total: 2 * (d(x) + md(x) + 2*bd(x)) * (1 + floor(x/20)*0.2) - bd(x)
        

Pierce:

- +1% per degree, +1 per degree, max +100% + 100
    
    - p(100) = p * 2 + 100
        
    - p(x) = p * (1 + (x-1)*0.01) + (x-1)
        

Speed:

- s(x) = s / (1 + √((x-1) * 50) * 0.01)
    

Note that the same scaling applies to all attacks on any paragon.

## Summary

Overall requirements and buffs every 10th degree:

|degree|xp|damage|boss damage|pierce|reload|
|---|---|---|---|---|---|
|10|5131|+9% + 0|+0%|+9% + 9|0.8251|
|20|11032|+19% + 1|+20%|+19% + 19|0.7645|
|30|19609|+29% + 2|+20%|+29% + 29|0.7241|
|40|31360|+39% + 3|+40%|+39% + 39|0.6935|
|50|46786|+49% + 4|+40%|+49% + 49|0.6689|
|60|66387|+59% + 5|+60%|+59% + 59|0.6481|
|70|90664|+69% + 6|+60%|+69% + 69|0.6301|
|80|120115|+79% + 7|+80%|+79% + 79|0.6143|
|90|155241|+89% + 8|+80%|+89% + 89|0.5999|
|100|200000|+100% + 10|+100%|+100% + 100|0.5869|

---

# Individual stats

For reference, here are the main stats for each current paragon, at every 20th degree, as well as the maximum achievable degree in single-player — 76, or 79 for Dart Monkey (due to Master Double Cross MK). Note that ceramic/moab/boss damage is listed in total, not as an addition to base damage.

## Dart Monkey — Apex Plasma Master

|°|attack|d|cd|md|bd|p|r|s|
|---|---|---|---|---|---|---|---|---|
|1|triple-jugg|20|50|20|100|200|85|0.3|
||juggernaut|20|50|20|100|200|-|-|
|20|triple-jugg|24.8|60.5|24.8|163.04|257|85|0.2294|
||juggernaut|24.8|60.5|24.8|163.04|257|-|-|
|40|triple-jugg|30.8|72.5|30.8|243.28|317|85|0.2080|
||juggernaut|30.8|72.5|30.8|243.28|317|-|-|
|60|triple-jugg|36.8|84.5|36.8|338.72|377|85|0.1944|
||juggernaut|36.8|84.5|36.8|338.72|377|-|-|
|79|triple-jugg|42.6|96.0|42.6|381.44|434|85|0.1847|
||juggernaut|42.6|96.0|42.6|381.44|434|-|-|
|80|triple-jugg|42.8|96.5|42.8|449.36|437|85|0.1843|
||juggernaut|42.8|96.5|42.8|449.36|437|-|-|
|100|triple-jugg|50|110|50|580|500|85|0.1761|
||juggernaut|50|110|50|580|500|-|-|

## Boomerang Monkey — Glaive Dominus

|°|attack|d|cd|md|bd|p|r|s|
|---|---|---|---|---|---|---|---|---|
|1|glaive|20|20|20|80|100|75|0.04|
||shred|750|-|750|750|-|-|1.0|
||orbital|42|62|62|222|1000|60|0.1|
||press|1|1|20|20|300|100|2.5|
||explosion|2500|2500|2500|7500|20|50|-|
||burn|500|500|500|500|-|-|1.0|
|20|glaive|24.8|24.8|24.8|129.72|138|75|0.0306|
||shred|893.5|-|893.5|1072.2|-|-|1.0|
||orbital|50.98|74.78|74.78|356.296|1209|60|0.0765|
||press|2.19|2.19|24.8|29.76|376|100|1.9113|
||explosion|2976|2976|2976|11901.2|42.8|50|-|
||burn|596|596|596|715.2|-|-|1.0|
|40|glaive|30.8|30.8|30.8|193.24|178|75|0.0277|
||shred|1045.5|-|1045.5|1463.7|-|-|1.0|
||orbital|61.38|89.18|89.18|525.172|1429|60|0.0693|
||press|4.39|4.39|30.8|43.12|456|100|1.7337|
||explosion|3478|3478|3478|17379.2|66.8|50|-|
||burn|698|698|698|977.2|-|-|1.0|
|60|glaive|36.8|36.8|36.8|268.76|218|75|0.0259|
||shred|1197.5|-|1197.5|1916.0|-|-|1.0|
||orbital|71.78|103.58|103.58|725.408|1649|60|0.0648|
||press|6.59|6.59|36.8|58.88|536|100|1.6202|
||explosion|3980|3980|3980|23858.0|90.8|50|-|
||burn|800|800|800|1280.0|-|-|1.0|
|76|glaive|42.0|42.0|42.0|298.2|250|75|0.0248|
||shred|1319.5|-|1319.5|2111.2|-|-|1.0|
||orbital|80.5|115.5|115.5|800.8|1825|60|0.0620|
||press|8.75|8.75|42.0|67.2|600|100|1.5509|
||explosion|4382|4382|4382|26261.2|110|50|-|
||burn|882|882|882|1411.2|-|-|1.0|
|80|glaive|42.8|42.8|42.8|356.28|258|75|0.0246|
||shred|1349.5|-|1349.5|2429.1|-|-|1.0|
||orbital|82.18|117.98|117.98|957.004|1869|60|0.0614|
||press|8.79|8.79|42.8|77.04|616|100|1.5356|
||explosion|4482|4482|4482|31337.6|114.8|50|-|
||burn|902|902|902|1623.6|-|-|1.0|
|100|glaive|50|50|50|460|300|75|0.0235|
||shred|1510|-|1510|3020|-|-|1.0|
||orbital|94|134|134|1228|2100|60|0.0587|
||press|12|12|50|100|700|100|1.4671|
||explosion|5010|5010|5010|40020|140|50|-|
||burn|1010|1010|1010|2020|-|-|1.0|

## Ninja Monkey — Ascended Shadow

|°|attack|d|cd|md|bd|p|r|s|
|---|---|---|---|---|---|---|---|---|
|1|shuriken|32|32|32|64|4|70|0.217|
||flash-bomb|96|96|96|192|50|70|1.5|
||mini-shuriken|80|80|80|160|20|-|-|
||sticky-bomb|16000|-|16000|48000|-|∞|5.5|
||explosion|3500|3500|3500|4900|10|40|-|
|20|shuriken|39.08|39.08|39.08|100.208|23.76|70|0.1659|
||flash-bomb|115.24|115.24|115.24|298.224|78.5|70|1.1468|
||mini-shuriken|96.2|96.2|96.2|248.72|42.8|-|-|
||sticky-bomb|19041|-|19041|68545.2|-|∞|4.2049|
||explosion|4166|4166|4166|7331.6|30.9|40|-|
|40|shuriken|47.48|47.48|47.48|146.536|44.56|70|0.1505|
||flash-bomb|136.44|136.44|136.44|431.208|108.5|70|1.0402|
||mini-shuriken|114.2|114.2|114.2|360.04|66.8|-|-|
||sticky-bomb|22243|-|22243|93412.2|-|∞|3.8141|
||explosion|4868|4868|4868|10318.0|52.9|40|-|
|60|shuriken|55.88|55.88|55.88|201.344|65.36|70|0.1406|
||flash-bomb|157.64|157.64|157.64|588.032|138.5|70|0.9721|
||mini-shuriken|132.2|132.2|132.2|491.36|90.8|-|-|
||sticky-bomb|25445|-|25445|122120.0|-|∞|3.5645|
||explosion|5570|5570|5570|13809.2|74.9|40|-|
|76|shuriken|63.0|63.0|63.0|224.0|82.0|70|0.1346|
||flash-bomb|175.0|175.0|175.0|649.6|162.5|70|0.9305|
||mini-shuriken|147.0|147.0|147.0|543.2|110.0|-|-|
||sticky-bomb|28007|-|28007|134411.2|-|∞|3.4119|
||explosion|6132|6132|6132|15201.2|92.5|40|-|
|80|shuriken|64.28|64.28|64.28|264.632|86.16|70|0.1333|
||flash-bomb|178.84|178.84|178.84|768.696|168.5|70|0.9214|
||mini-shuriken|150.2|150.2|150.0|642.68|114.8|-|-|
||sticky-bomb|28647|-|28647|154668.6|-|∞|3.3784|
||explosion|6272|6272|6272|17805.2|96.9|40|-|
|100|shuriken|74|74|74|340|108|70|0.1273|
||flash-bomb|202|202|202|980|200|70|0.8803|
||mini-shuriken|170|170|170|820|140|-|-|
||sticky-bomb|32010|-|32010|192020|-|∞|3.2277|
||explosion|7010|7010|7010|22420|120|40|-|

## Monkey Buccaneer — Navarch of the Seas

|°|attack|d|cd|md|bd|p|r|s|
|---|---|---|---|---|---|---|---|---|
|1|cannon|60|60|120|180|28|60|0.429|
||grape|25|25|55|85|10|60|0.429|
||forward-dart|44|44|44|88|14|∞|0.15|
||moab-missile|200|200|200|400|10|∞|1.5|
|20|cannon|72.4|72.4|143.8|272.52|52.32|60|0.3280|
||grape|30.75|30.75|66.45|129.72|30.9|60|0.3280|
||forward-dart|53.36|53.36|53.36|137.336|35.66|∞|0.1147|
||moab-missile|239|239|239|620.0|30.9|∞|1.1468|
|40|cannon|86.4|86.4|169.8|387.84|77.92|60|0.2975|
||grape|37.75|37.75|79.45|186.29|52.9|60|0.2975|
||forward-dart|64.16|64.16|64.16|199.912|58.46|∞|0.1040|
||moab-missile|281|281|281|893.8|52.9|∞|1.0402|
|60|cannon|100.4|100.4|195.8|523.16|103.52|60|0.2780|
||grape|44.75|44.75|92.45|252.86|74.9|60|0.2780|
||forward-dart|74.96|74.96|74.96|273.848|81.26|∞|0.0972|
||moab-missile|323|323|323|1216.4|74.9|∞|0.9721|
|76|cannon|112.0|112.0|217.0|578.2|124.0|60|0.2661|
||grape|50.75|50.75|103.25|280.7|92.5|60|0.2661|
||forward-dart|84.0|84.0|84.0|303.8|99.5|∞|0.0931|
||moab-missile|357|357|357|1341.2|92.5|∞|0.9305|
|80|cannon|114.4|114.4|221.8|678.48|129.12|60|0.2635|
||grape|51.75|51.75|105.45|329.43|96.9|60|0.2635|
||forward-dart|85.76|85.76|85.76|359.144|104.06|∞|0.0921|
||moab-missile|365|365|365|1587.8|96.9|∞|0.9214|
|100|cannon|130|130|250|860|156|60|0.2518|
||grape|60|60|120|420|120|60|0.2518|
||forward-dart|98|98|98|460|128|∞|0.0880|
||moab-missile|410|410|410|2020|120|∞|0.8803|