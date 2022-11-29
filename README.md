# Pedestrian mobility experiment in Granollers (Spain)

This repository contains the code used to study the mobility data in [1] used for the scientific publication. The data was collected through a citizen science experiment 
in which participated 19 groups of 3-5 people (72 people in total) from three different communities in the small neighborhood of "Primer de Maig" in Granollers city (Spain). The participating groups tracked their journey using a tablet device and the Wikiloc [2] app., while walking and exploring the neighborhood and completing a set of missions (e.g.: "Find a place to play the ball with your group"). The trajectories and the chosen locations by the participants have a strong urbanistic interest for the researchers (specially for the designers and architects) in order to improve urban furniture and activate the neighborhood and identify possible intervention areas.

The three participating communities are:
  - The school "Escola Ferrer i Guàrdia" (4 groups of professors and 7 groups of students, 41 people in total)
  - The neighborhood association "Associació de Veïns Sota el Cami Ral". 
  - The elderly people association "Espai Actiu de la Gent Gran". (8 groups from the two associations, 31 people in total).
  
 
The experiment took place on April, 2022. The groups from the school performed the experiment on Friday, 29th April and the other groups on Saturday, 30th April under the same experimental protocol and conditions.

The data in the repository [1] consist of three folders containing the original collected data, the processed data and the information about the stops to complete the missions.

  1. The folder "original data" contains the raw data collected in the experiment, composed of 18 gpx-files (corresponding to each participant group journey, less for one who did not record the track due to technical issues) and 3,532 GPS locations. The data-files contain 7 columns, which are:
      - course: the direction in which the device is travelling, mesured in degrees and relative to the north.
      - haccuracy: radius of uncertainty for the location, mesured in metres.
      - speed: instantaneous velocity of the device (obtained by the Android/IOS servers) in metres/second.
      - latitude: latitude coordinate in degrees
      - longitude: longitude coordinate in degrees
      - time: timestamp in which the geo-location is recorded
      - nickname: anonymous nickname of the participant
  

  
