# 2022-Ukraine-Russia-War-Dataset

[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner-direct-single.svg)](https://stand-with-ukraine.pp.ua)

<img src="https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/images/dataset_2022_war_ukraine_russia.png" alt="drawing" width="1200"/>

This is the dataset that describes Equipment Losses & Death Toll & Military Wounded & Prisoners of War of russians in 2022 Ukraine russia War. 
All data are official and additionally structured by myself. 
A lot of civilians and children have already been killed by russia troops. Ukraine is in war flame and under missile attack now. [![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://stand-with-ukraine.pp.ua) [![Russian Warship Go Fuck Yourself](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/RussianWarship.svg)](https://stand-with-ukraine.pp.ua)

### Application 
- [russian losses application](https://ukraine-russia-war.streamlitapp.com/) - a monitoring dashboard that describes russian Equipment Losses during the 2022 russia invasion of Ukraine.
- [Cargo200rus](https://t.me/Cargo200rusBot) - a telegram bot that represent official losses of the russian armed forces in Ukraine. [GitHub.](https://github.com/MadMan2k/TelegramBot-Cargo200rus)

### Related Datasets
- [Massive Missile Attacks on Ukraine](https://www.kaggle.com/datasets/piterfm/massive-missile-attacks-on-ukraine) - a dataset containing available information about launched and shot down missiles and drones during russian massive missile and drone (UAV) strike on infrastructure (since October 2022) as part of its invasion of Ukraine. The dataset also contains information about some single shot-down UAVs.
- [2022 Ukraine Russia War, Losses, Oryx + Images](https://www.kaggle.com/datasets/piterfm/2022-ukraine-russia-war-equipment-losses-oryx) - Ukraine and russia Equipment Losses based on Oryx Investigation.
- [russian navy (Military Maritime Fleet)](https://www.kaggle.com/datasets/piterfm/russian-navy) - all Surface Combatants, Submarines, Littoral Warfare Ships, Rescue, and Auxiliary Ships. Ship losses During The 2022 russian Invasion Of Ukraine are included.
- [Social Media Athletes from russia & belarus](https://www.kaggle.com/datasets/piterfm/olympic-athletes-social-media-russia-belarus) - Social Media of russia and belarus athletes that took part in Beijing 2022 Olympic Winter Games.
- [Kaggle, Data in CSV format](https://www.kaggle.com/piterfm/2022-ukraine-russian-war) - the same data on Kaggle. You can also look at the variety of [Kaggle notebooks](https://www.kaggle.com/datasets/piterfm/2022-ukraine-russian-war/code) with analysis and visualization.

### Data Sources
1. Main data sources are [General Staff of the Armed Forces of Ukraine](https://www.zsu.gov.ua/en) and [Ministry of Defence of Ukraine](https://www.mil.gov.ua/en/). Data from different battlefields are gathered. The calculation is complicated by the high intensity of hostilities. Data are being updated.
2. [Invaders](https://invaders-rf.com/) - Russians Prisoner of War (POW). The project is not active since May of 2022.
3. [Oryxspioenkop](https://www.oryxspioenkop.com/2022/02/attack-on-europe-documenting-equipment.html) - Ukraine and russia Equipment Losses. This list only includes destroyed vehicles and equipment of which photo or videographic evidence is available. Therefore, the amount of equipment destroyed is significantly higher than recorded here.
4. Interactive Maps:
 - [Liveuamap](https://liveuamap.com/) - Live Interactive Map with events that happened.
 - [DeepStateMap](https://deepstatemap.live/#6/49.438/32.053), [Wiki page](https://en.wikipedia.org/wiki/DeepStateMap.Live) - an interactive open-source intelligence online map run by the non-governmental and volunteer-led Deep State UA, which focuses primarily on the military operations of the Russian and Ukrainian armies in the Russian invasion of Ukraine.
 - [Alerts Map](https://alerts.in.ua/en) - Air Raid Alert Map of Ukraine
 - [eMap](https://vadimklimenko.com/map/) - Air Raid Alert Map of Ukraine
5. Sanctions Databases:
 - [Ukraine Russia related sanctions](https://ofac.treasury.gov/sanctions-programs-and-country-information/ukraine-russia-related-sanctions) by USA Office of Foreign Assets Control
 - [Sanction Lists](https://sanctions.nazk.gov.ua/en/sanction-lists/) by the Ministry of Foreign Affairs of Ukraine and the National Agency on Corruption Prevention
 - [RUPEP.ORG](https://rupep.org/en/) - a public database of domestic politically exposed persons of russia and belarus
 - [Open Sanctions](https://www.opensanctions.org/) - helps investigators find leads, allows companies to manage risk, and enables technologists to build data-driven products
 - [Correctiv](https://correctiv.org/en/latest-stories/2022/03/01/sanctions-tracker-live-monitoring-of-all-sanctions-against-russia/) - live monitoring of all sanctions against Russia
 - [Tracking sanctions against Russia](https://graphics.reuters.com/UKRAINE-CRISIS/SANCTIONS/byvrjenzmve/index.html) - Reuters project.
6. [Russia’s Attacks on Civilian Targets Have Obliterated Everyday Life in Ukraine](https://www.nytimes.com/interactive/2022/03/23/world/europe/ukraine-civilian-attacks.html) by NYTimes.
7. [Help to stop Russian war against Ukraine](https://www.kaggle.com/general/310445) - Kaggle Petition.

### Data
**Important.** Each new record is accumulated data from previous days.

**Important.** Data will be updated daily
- [Personnel Losses JSON](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_personnel.json) - contains Personnel Losses during the war
- [Equipment Losses JSON](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_equipment.json) - contains Equipment Losses during the war
- [Equipment Losses Correction JSON](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_equipment_correction.json) - contains some data correction in Equipment Losses Dataset (date: 2022-10-13, date: 2023-05-27)
- [Equipment Losses Oryx JSON](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_equipment_oryx.json) - contains more  granular data of Equipment Losses during the war based on Oryx

### Data Preprocessing
If you need daily bases data I recommend the [Daily Data Notebook](https://www.kaggle.com/code/piterfm/daily-data). 
It contains a full code that shows how to convert the data or you can adapt the below code snippet.
```
df = df.diff().fillna(df).fillna(0).astype(int)
```

### Tracking
- Personnel
- Prisoner of War (POW) - has not been tracked since 2022-04-28
- Aircraft
- Helicopter
- Tank
- Armored Personnel Carrier (APC)
- Multiple Rocket Launcher (MRL)
- Field Artillery
- Military Auto - has not been tracked since 2022-05-01; joined with `Fuel Tank` into `Vehicles and Fuel Tanks`
- Fuel Tank - has not been tracked since 2022-05-01; joined with `Military Auto` into `Vehicles and Fuel Tanks`
- Anti-aircraft warfare
- Drone - UAV+RPA
- Naval Ship - Warships, Boats
- Anti-aircraft Warfare
- Mobile SRBM System - has not been tracked since 2022-05-01; joined into `Cruise Missiles`
- Vehicles and Fuel Tanks - appear since 2022-05-01 as a sum of `Fuel Tank` and `Military Auto`
- Cruise Missiles - appear since 2022-05-01
- Direction of Greatest Losses - appear since 2022-04-25

### Acronyms
- POW - Prisoner of War,
- MRL - Multiple Rocket Launcher,
- APC - Armored Personnel Carrier,
- UAV - Unmanned Aerial Vehicle, 
- RPA - Remotely Piloted Vehicle.
