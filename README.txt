
# Dataset Description

## Directory Structure

### 1. Scheduler Instances
This directory contains JSON files defining various AGV mission configurations and a layout file. Each mission JSON file includes:

- **Resources**: A list of AGV IDs available for the mission.
- **Locations**:
  - **Pickup**: IDs of pickup points where AGVs collect loads.
  - **Dropoff**: IDs of drop-off points where AGVs deliver loads.
  - **Charging Stations**: IDs of charging stations where AGVs can recharge their batteries.
- **Jobs Load**: An array representing the load associated with each job, which influences battery consumption.
- **AMR Origins**: Starting points for each AGV at the beginning of the mission.

The **layout.json** file describes the physical configuration of the AGV environment:

- **Locations**: Each location is identified by an ID, with specified latitude, longitude, and a descriptive name (e.g., "Start0", "Pickup1", "Dropoff1", "Charging1").
- **Links**: These represent possible paths between locations, defined by source-target pairs, allowing AGVs to navigate between points.



### 2. Soc Time Series
This directory contains time-series CSV file documenting the **State of Charge (SoC)** of AGV over time. The file includes:

- **Time**: Timestamps for each recorded SoC measurement.
- **State of Charge**: The battery level of AGVs at each timestamp, providing insight into energy consumption during missions.


