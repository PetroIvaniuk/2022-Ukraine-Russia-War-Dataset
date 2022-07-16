# 2022-Ukraine-Russia-War-Dataset

<img src="https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/images/dataset_2022_war_ukraine_russia.png" alt="drawing" width="1000"/>

This is the dataset that describes Equipment Losses & Death Toll & Military Wounded & Prisoner of War of russians in 2022 Ukraine russia War. 
All data are official and additionally structured by myself. 
A lot of civilians and children have already been killed by russia troops. Ukraine is in war flame and under missile attack now. We are strong. Stand with Ukraine. #StandWithUkraine, @StandWithUkraine 

### Application 
- [russia War Equipment Losses Application](https://share.streamlit.io/petroivaniuk/ukraine-russia-war/main/russia_losses.py)

### Related Datasets
- [2022 Ukraine Russia War Equipment Losses Oryx](https://www.kaggle.com/datasets/piterfm/2022-ukraine-russia-war-equipment-losses-oryx) - Ukraine and russia Equipment Losses.
- [russian navy (Military Maritime Fleet)](https://www.kaggle.com/datasets/piterfm/russian-navy) - All Surface Combatants, Submarines, Littoral Warfare Ships, Rescue, and Auxiliary Ships. Ship losses During The 2022 Russian Invasion Of Ukraine are included.
- [Dataset Social Media Athletes from russia & belarus](https://www.kaggle.com/datasets/piterfm/olympic-athletes-social-media-russia-belarus) - Social Media of russia and belarus athletes that took part in Beijing 2022 Olympic Winter Games.
- [Kaggle, Data in CSV format](https://www.kaggle.com/piterfm/2022-ukraine-russian-war) - The same data on Kaggle. You can also look on [Kaggle notebooks](https://www.kaggle.com/datasets/piterfm/2022-ukraine-russian-war/code) with analysis and visualisation.

### Data Sources
1. Main data sources are [Armed Forces of Ukraine](https://www.zsu.gov.ua/en) and [Ministry of Defence of Ukraine](https://www.mil.gov.ua/en/). They gathered data from different points of the country. The calculation is complicated by the high intensity of hostilities.
2. [Invaders](https://invaders-rf.com/) - Russians Prisoner of War (POW).
3. [Oryxspioenkop](https://www.oryxspioenkop.com/2022/02/attack-on-europe-documenting-equipment.html) - Ukraine and russia Equipment Losses. This list only includes destroyed vehicles and equipment of which photo or videographic evidence is available. Therefore, the amount of equipment destroyed is significantly higher than recorded here.
4. [Liveuamap](https://liveuamap.com/) - Live Interactive Map with events that happened.
5. [Live monitoring of all sanctions against Russia](https://correctiv.org/en/latest-stories/2022/03/01/sanctions-tracker-live-monitoring-of-all-sanctions-against-russia/) - Correctiv.
6. [Tracking sanctions against Russia](https://graphics.reuters.com/UKRAINE-CRISIS/SANCTIONS/byvrjenzmve/index.html) - Reuters.
7. [Russia’s Attacks on Civilian Targets Have Obliterated Everyday Life in Ukraine](https://www.nytimes.com/interactive/2022/03/23/world/europe/ukraine-civilian-attacks.html) - NYTimes.
8. [Help to stop Russian war against Ukraine](https://www.kaggle.com/general/310445) - Kaggle Petition.

### Data
**Important.** Each new record is accumulated data from previous days.

**Important.** Data will be updated daily

[Data Personnel](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_personnel.json) 

[Data Equipment](https://github.com/PetroIvaniuk/2022-Ukraine-Russia-War-Dataset/blob/main/data/russia_losses_equipment.json)

### Data Preprocessing
If you need daily bases data I recommend the [Daily Data Notebook](https://www.kaggle.com/code/piterfm/daily-data). It contains a full code that shows how to convert the data or you can adapt the below code snippet.
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
- drones: 
  - UAV - Unmanned Aerial Vehicle, 
  - RPA - Remotely Piloted Vehicle.
