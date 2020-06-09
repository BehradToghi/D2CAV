# D2CAV
A Maneuver-based Urban Driving Dataset and Model for Cooperative Vehicle Applications

The dataset is publicly available to be used by researchers and collaborators, please cite the paper below if you would like to use D2CAV in your work:
https://arxiv.org/abs/2005.13781

Bibtex:
@misc{toghi2020maneuverbased, title={A Maneuver-based Urban Driving Dataset and Model for Cooperative Vehicle Applications}, author={Behrad Toghi and Divas Grover and Mahdi Razzaghpour and Rajat Jain and Rodolfo Valiente Romero and Yaser P. Fallah}, year={2020}, eprint={2005.13781}, archivePrefix={arXiv}, primaryClass={eess.SP} }

This is a OBD (On-Board Daignosis) dataset collected from a vehicle for the purpose of maneuver classification and driver behavior simulation. The file system of the dataset is quite simple. The dataset root folder has six subfolders with the named according to the maneuver the data belongs to. There are multiple files inside each of those sub-folders, each representing the instance number of that particular maneuver. Each file in the subfolders has the timestamped attributes. The value of an attribute is saved for 20 seconds before and 20 seconds after the maneuver was recorded/made for data analysis. Following are some details of the dataset.

### Attributes
As there were many attributes collected via the OBD connector of the vehicle only the following were recognized as useful for the purpose of the project.

| Attribute                  | Min | Max              |  Unit/measure |
|----------------------------|-----|------------------|---------------|
| accelerator_pedal_position | 0   | 100              | %             |
| steering_wheel_angle       | 450 | -450             | Degrees       |
| vehicle_speed              | 0   | vehicle specific | km/h          |
| brake_pedal_status         | 0   | 1                | binary        |


Along  side the OBD data, GPS data for the vehicle was also collected. It is to note that the data collection campaign was conducted in the Northern hemisphere of the planet and West of the Prime Meridian. Following are the attributes collected from GPS, used in the project.

| Attribute    | Min  | Max              |  Unit/measure |
|--------------|------|------------------|---------------|
| latitude     | -90  | 90               | Degrees       |
| longitude    | -180 | 180              | Degrees       |
| speed (km/h) | 0    | vehicle specific | km/h          |
| heading      | 0    | 360              | Degrees       |


### Maneuvers
The dataset is collected in a right-hand traffic country. Following are the maneuvers recognized for the project.

|  Maneuver  | No of Instances | Description                              |
|:----------:|:---------------:|------------------------------------------|
| hard_brake | 61              | Immediate braking in a case of emergency |
| lane_left  | 97              | Changing to adjacent lane on the left    |
| lane_right | 79              | Changing to adjacent lane on the right   |
| left_turn  | 75              | Turning left on the road                 |
| right_turn | 78              | Truning right on the road                |
| u_turn     | 62              | Making a u-turn over a road divider      |


If the dataset is employed for any purpose in your work, please cite the attached research work with it.
