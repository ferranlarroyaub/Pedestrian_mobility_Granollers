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
    
      - lat: latitude coordinate of each record in degrees.
      - lon: longitude coordinate of each record in degrees.
      - name: code that identifies the group.
      - cmt: GPS comment of the waypoint.
      - desc: a text description of the element.
      - ele: timestamp in which the geo-location is recorded.
      - time: elevation in meters of the record.
  
  
  2. The folder "processed data" contains the processed and cleaned data (a .csv file for each participanting group, with the same file-name as the raw data but adding the suffix "processed" to each .csv file. The data is reduced to 2,981 GPS locations. 4 new columns are added corresponding to the time increment, the instantaneous velocity, the distance between GPS records and the label of each record as "stop" (if is stopped) or "flight" (if it is moving).

       - $\Delta t$: time difference between consecutive records in seconds (computed in advance: $\Delta t (i) = t(i+1) - t(i)$. So the last element is NaN).
       - d: distance between consecutive GPS records in metres (computed in advance, so the last element is NaN).
       - v: instantaneous velcocity of each record in metres/second (distance over time difference). Again, the last element is NaN.
       - stops: string indicating if the record at position "i" is stopped ("stop") or moving ("flight"). 

  3. The folder "stops" contains 19 csv-files for each participating group, containing information of the stops due to the missions that the groups had to complete. The files include 4 columns with the code of the mission, the latitude and the longitude of the mission location and the duration of the action in seconds. The list of missions is:

    - Dance (code: B). Explore and choose a place to dance using the speaker via Bluetooth.
    - Play (code: J). Explore and choose a place to play with the ball.
    - Chat (code: X). Explore and choose a place to sit and share personal neighborhood stories.
    - Lunch (code: M). Explore and choose a place to lay out the carpet and sit down to eat/snack.
    - Celebration toast (code: C). Explore and choose a place to celebrate a special occasion with a champagne toast.
    - Celebration confetti (code CC). Explore and choose a place to celebrate a special occasion by shooting the confetti gun
