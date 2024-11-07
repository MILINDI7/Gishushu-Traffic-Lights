# Gishushu-Traffic-Lights
Gishushu Traffic Lights State Machine

## Welcome! 👋

This document contains a folder [Designs](https://github.com/MILINDI7/Gishushu-Traffic-Lights/tree/main/Designs) that illustrates the navigation of vehicles and pedestrians on the main road of Gishushu [#KN-5-Rd](https://www.google.com/maps/place/KN+5+Rd,+Kigali/@-1.9536348,30.1021243,18.91z/data=!4m6!3m5!1s0x19dca69adbd0ffcd:0x8cb9848cdf13613c!8m2!3d-1.9610367!4d30.1209166!16s%2Fg%2F12vtj54db?entry=ttu&g_ep=EgoyMDI0MTAyOS4wIKXMDSoASAFQAw%3D%3D)by the traffic lights.

## Specification
**1. Intersection structure:**
    - There are four(4) main roads
    - Each road has two(2) directions
    - There are four(4) main traffic lights at the intersection each facing a specific road, and 3*2 pedestrian's lights

**2. Roads Structure:**
    **the first Road has 3 directions:**
        - 1 : the straight path
        - 1.1 : the turn left path via the fourth(4th) road. 
        - 1.2 : the turn right path via the second(2nd) road.
     **the second Road has 3 directions:**
        - 2 : the straight path
        - 2.1 : the turn right path ahead of the first(1st) road
        - 2.2 : the turn left path ahead the third(3rd) road
    **the third Road has 3 directions:**
        - 3 : the straight path
        - 3.1 : the turn left path via the second(2nd) road
        - 3.2 : the turn right path via the fourth(4th) road
    **The fourth Road has 3 directions:**
        - 4 : the straight path
        - 4.1 : the turn right path ahead of the third(3rd) road
        - 2.2 : the turn left path ahead the first(1st) road
    **The pedestrians crossing areas are marked by dashed lines, with the following symbols:**
        -P1
        -P2
        -P3

⚠️consider that in Rwanda we use the right side for traffic

**3. Traffic Lights States:**
    **The are only three states for each traffic light:**
        - 🟢 Green: Vehicles can proceed/ can go.
        - 🟡 Yellow: Vehicles must be ready to stop; Red is appearing in a few.
        - 🔴 Red: Vehicles must stop.

**4. Phases of Operations**
        - **Phase 1** : Roads **1, 1.2, 3, 3.2** are 🟢 green allowing vehicles from them to proceed, other roads are 🔴 red, vehicles are on standby.
        - **Transition Phase** : Roads **all roads** are 🟡 yellow allowing pedestrians **P1, P2, P3** to cross the roads wherever possible.
        - **Phase 2**: Roads **1.1, 2, 2.2, 2.2, 3.1, 4, 4.1, 4.2** are 🟢 allowing vehicles from them to proceed, other roads are on 🔴 red light, vehicles are on standby.
        - **This cycle repeats unless a police officer overrides the traffic lights use**

**5. Time Sequence**
    - The first transition will take 20 seconds in total, 10 seconds beeping yellow and from steady yellow to next phase(red).

**6. Pedestrian Crossing**
    - Pedestrians crossing phase is included whenever the zebra crossing is connected to road that has a yellow or red light on.

## Thank you for going through this project, suggestions, feedbacks and reviews are welcomed! 🚀