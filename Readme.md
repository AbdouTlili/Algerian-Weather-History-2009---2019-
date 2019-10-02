# Welcome to the Algerian Weather History (2009-2019) DataSet**

this dataSet is a part of our Project [Umbrella (weather prediction)](https://github.com/AbdouTlili/Umbrella-opensouece-weather-prediction-project-)

the dataBase contains Algerian weather information for 10 years ( 2009 - 2019 ), it has been used for a desktop application for weather prediction  by : 

  * [Tlili abderahman errached](https://github.com/AbdouTlili)
  * [Dokkar rachid reda](https://github.com/DokkarRachidReda)
  * [Ben messaoud issam](https://github.com/Issamoh)
  * [Kadri mohamed el said](https://github.com/iDOVICSA)
  * [Saoudi abderraouf](https://github.com/saoudiabderraouf)
  * [Mimene younes](https://github.com/younes38)
     
 The data has been found and cleaned by [Saoudi abderraouf](https://github.com/saoudiabderraouf) and [Tlili abderahman errached](https://github.com/AbdouTlili)
 
 the final dataset contien  :
 
 * 44 out of 48 Algerian divisions ( Wilayas ) .
 * up to 8 records per day in different hours .
 * 10 meteorological parameters :
     1. the exact date and hour of the record.
     2. the recorded temperature (Celsius degree).
     3. the min and max temperature of the day (Celsius degree).
     4. the recorded pressure (millibars).
     5. the wind direction.
     6. the wind force.
     7. the cloud density.
     8. the cloud height 
     9. the recorded precipitation (millimeter).
     10.the humidity (percentage)
     
  you can find the ```.db``` file and the cleaned ```.csv``` in this repo 
    

## Meteorological parameters encoding :

  * DT : date in the format  YYYY.MM.DD HH:MM <br>
  * T : temperature in Celsius.<br>
  * Po : the atmosphere pressure in Millibars.<br>
  * DD : wind direction encoded <br>

  | code  | Meaning |
  | --- | --- |
  |  clm-pas-vent | calm, no wind  |
  | est | east |
  | nord | nord |
  | ouest | west |
  | sud | south |

       P.S : you may find combined directions like : "ouest-nord-ouest" which means that the wind direction is "west to northwest" 
  * Ff : the wind force, integers starts from 0 ( no wind ) represents the wins speed ( km/h)
  * N : This is a percentage that shows the Density of the Cloud in the sky, for example: 20-30%,
50% or no cloud if the sky is totally clear 0%. And to simplify the management of these different
rates, they are treated as doubles between 0.0 (if there is no cloud) and 10.0 (if the sky is
totally covered by the cloud), and for that we code them as follows:

|initial percentage  | 	DB coding |
 | --- | --- |
|no clouds |	0.0|
|10% or less, but not 0% |	0.5|
|10% 	|1.0|
|10–20%	|1.5|
|20%	|2|
|.	|.|
|.	|.|
|90%	|9.0|
|90 or more, but not 100%|	9.5|
|100%	|10.0|

  * H (the clouds height):  The initial data of this meteorological variable are given as strings for example: 2500 or more, or no clouds, 1500-2000 which represent the height of the cloud on the earth's surface, whereas it is easier to manage them as integers, hence our coding:

|initial value  |DB coding|
 | --- | --- |
|100-300 	|0|
|300-600	|1|
|600-1000	|2|
|1000-1500	|3|
|1500-2000	|4|
|2000-2500	|5|
|2500 ou plus, ou pas de nuages.	|6|

  * Tn : the minimum temperature in the day.
  * Tx : the maximum temperature in the day.
  * h : the percentage of the humidity.
  * Tn : the precipitation quantity in Millimeter. 


  
  
please don't hesitate to contact us if you have any question or you need any clarifications

email : ha_tlili@esi.dz - ha_saoudi@esi.dz
