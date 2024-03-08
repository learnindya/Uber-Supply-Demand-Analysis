# Uber-Supply-Demand-Analysis

## Objectives
- Identify trends in booking
- Analyse demand and supply
- Predict the demand in a region at an hour

## Data Pre-processing
### Feature extraction
- 'start_month'
- 'start_day'
- 'start_hour'
- 'start_minute'
- 'start_dayofweek'
- 'pickup_distance'
- 'pickup_duration'

## Booking trend
<img width="413" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/99470364-2b4e-4c0a-887d-e14e2805e225">

<img width="416" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/defae6d8-1716-486e-b179-e48823720cad">

<img width="539" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/d87f0f8c-dc14-4339-bb67-c0c736dd2e90">

## Riders & Drivers Distribution 
<img width="564" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/129b33c8-919f-4dd5-a9f0-d55e5d42f5c1">

Riders cancel their orders throughout the region, with Surquillo and San Borja having the most cancellation.

Drivers cancel their orders in Jorge Chavez airport, Mall Aventura Plaza Bellavista, Brena, Surquillo, San Isidro, San Borja, Miraflores, Santiago de Surco, and La Mollina districts.

## Trip Status
<img width="454" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/00a38455-f449-4c8d-b0be-449a07e88464">

<img width="454" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/55083b3d-b6d2-4e09-ba32-87188ab6eb09">

<img width="519" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/6b80914e-9f67-49d8-b5e5-41444672d264">

From all seasonal trend, it can be inferred that the top reason for a failed order is due to rider cancellation. This could be analysed further by calculating the distance between rider and driver for cancelled orders, and determine if pickup_duration affects rider's decision to cancel.

## Rider Cancellation
Riders cancel their bookings because of high pickup duration.

## Driver Cancellation
It turns out that the average price for driver cancel is indeed lower than the average price for drop off. This seems to indicate that drivers are more interested to pick up riders with higher price. There is a positive moderate correlation between price and drop off, which supports the previous hypothesis. But the correlation between price and driver cancel is weaker (-0.10), so price may not be the sole reason for drivers to cancel booking.

## Supply-Demand Gap
<img width="530" alt="image" src="https://github.com/learnindya/Uber-Supply-Demand-Analysis/assets/105585813/5ca4e917-6a76-488c-b9b7-065cb4d674e5">

23:00 has the highest supply-demand gap. This is primarily caused by riders cancelling their booking because they have to wait for a long time to be picked up.

At peak hours, there were high orders in San Isidro, Miraflores, Surquillo and San Borja, but there is not enough rider around to fulfill requests timely.

There are orders almost every hour at Jorge Chavez Airport, but not enough drivers nearby. In this area, drivers often cancel their orders. Price may be one reason for drivers to cancel booking. To address this, drivers need to be surveyed.

## Data Pre-processing
- Selected features: hour, dayofweek, month, cluster, order_count
- Standardization

## Modeling
RandomForestRegressor()
MAPE (test): 0.471803127678629
MAPE (train): 0.37119477861396055
r2 (test): 0.8606767132297307
r2 (train): 0.8896822728559621
