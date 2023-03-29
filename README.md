# FEM-IOT-Col

Datasets of vehicle collisons in Barcelona.
The datasets cointains information regarding the position
of the vehicles in every step of the simulation, with a 
parameter determining if they are part of a collision or not. 

There are two datasets: positions_v1 and positions_v2. The first one, 
enfacises with reckless drivers with majority of back to front collisions. 
On the other hand, the second dataset is and upgrade with more diversity
in the kinds of vehicles driving, and at the same time they can skip 
traffic lights this way generating more lateral collisions in junctions. 

## Positions_v1

This dataset is generated with reckless vehicles. The majority of the collisions
are fornt to back. The parameters that are in the dataset are the following ones: 

|    **time**    | Time instant of the simulation, in seconds                                                                            |
|:--------------:|-----------------------------------------------------------------------------------------------------------------------|
| **vehicle_id** | Vehicle identifier. If a collision occurs is the one collisioning.                                                    |
|  **victim_id** | Identifier of the vehicle victim if a collision has occured.  If none collision has occurred de default value is -1.  |
|  **latitude**  | Position of the vehicle in geographical coordinates: latitude.                                                        |
|  **longitude** | Position of the vehicle in geographical coordinates: longitude                                                        |
|    **speed**   | Velocity of the vehicle in m/s                                                                                        |
|   **heading**  | Direction of the vehilce in respect to the north                                                                      |
|  **collision** | Boolean, it indicats if a collision has occurred or not:  1 collision ocurred 0 no collision ocurred                  |



## Positions_v2

This dataset has more diversity of vehicles than the previous one, and our objective was to increment the number of lateral collisions. 
To do it, the vehicles in the simulation can skip traffic lights. The diferent kinds of vehicles introduced in the simulation are the 
ones listed in the table below. Moreover, the simulation steps in this dataset are every 100ms in contrast to the 1s of the Positions_v1. 

| Vehicle Class | Length width height | mingap | acceleration | deceleration | emergency deceleration | Max speed | Speed Deviation |
|:-------------:|:-------------------:|:------:|:------------:|:------------:|:----------------------:|:---------:|:---------------:|
| passeger      |      5 1.8 1.5      |   2.5  |      2.6     |      4.5     |            9           |    200    |       0.1       |
| delivery      |    6.5 2.16 2.86    |   2.5  |      2.6     |      4.5     |            9           |    200    |       0.05      |
| bus           |      12 2.5 3.4     |   2.5  |      1.2     |       4      |            7           |     85    |        0        |
| motorcycle    |     2.2 0.9 1.5     |   2.5  |       6      |      10      |           10           |    200    |       0.1       |
| moped         |     2.2 0.9 1.5     |   2.5  |      1.1     |       7      |           10           |     45    |       0.1       |

Moreover, two new parameters are beeing observed in the dataset. 
  1. Acceleration: it indicates the acceleration of the vehicle.
  2. VehicleClass: it indicates the shape of the vehicle (passenger, bus, motorcycle, delivery or moped). 


## Positions_v3

This dataset is the same as the Postions_v2, however the simulations steps performed are every 1s as the Positions_v1.

## Positions_v5

This dataset uses the same scenario as Positions_v2, but with larger routes for the vehilces and a larger time of simulation.

## Barcelona_v2

Dataset generated in a new and bigger scenario. It is located in Sant Gervasi Barcelona. Dataset provided with a realistic approax,
with the vehicles beeing loger times in the simulation and circulating more in the principal hayways. 

Each simulation step of the simulation is every 1s. 

The dataset is divided in two but they can be glued together again after downloading and decomprising. 
