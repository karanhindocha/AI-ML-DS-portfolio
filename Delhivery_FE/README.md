## 🚚 Delhivery - Data Feature Engineering

## One-line summary:
This project focuses on cleaning, aggregating, and feature engineering logistics data from Delhivery to prepare it for downstream forecasting and analytical models.

## 🧩 Problem Statement:

Delhivery, India’s largest fully integrated logistics company, processes massive volumes of shipment data through its data engineering pipelines.
The objective is to:
- Process raw trip-level logistics data
- Aggregate multi-segment shipment records
- Engineer relevant time, distance, and location-based features
- Prepare a clean and model-ready dataset

## 📁 Dataset:
- The dataset contains detailed shipment-level information generated from Delhivery’s logistics operations.

https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/551/original/delhivery_data.csv?1642751181

   Key Features:

- data: tells whether the data is testing or training data
- trip_creation_time – Timestamp of trip creation
- route_schedule_uuid – Unique Id for a particular route schedule
- route_type – Transportation type
- FTL – Full Truck Load: FTL shipments get to the destination sooner, as the truck is making no other pickups or drop-offs along the way
- Carting: Handling system consisting of small vehicles (carts)
- trip_uuid - Unique ID given to a particular trip (A trip may include different source and destination centers)
- source_center - Source ID of trip origin
- source_name - Source Name of trip origin
- destination_cente – Destination ID
- destination_name – Destination Name
- od_start_time – Trip start time
- od_end_time – Trip end time
- start_scan_to_end_scan – Time taken to deliver from source to destination
- is_cutoff – Unknown field
- cutoff_factor – Unknown field
- cutoff_timestamp – Unknown field
- actual_distance_to_destination – Distance in Kms between source and destination warehouse
- actual_time – Actual time taken to complete the delivery (Cumulative)
- osrm_time – An open-source routing engine time calculator which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) and gives the time (Cumulative)
- osrm_distance – An open-source routing engine which computes the shortest path between points in a given map (Includes usual traffic, distance through major and minor roads) (Cumulative)
- factor – Unknown field
- segment_actual_time – This is a segment time. Time taken by the subset of the package delivery
- segment_osrm_time – This is the OSRM segment time. Time taken by the subset of the package delivery
- segment_osrm_distance – This is the OSRM distance. Distance covered by subset of the package delivery
- segment_factor – Unknown field

## 🛠️ Tools & Technologies Used:
- Programming Language: Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy
- Techniques: Feature Engineering, Aggregation, Normalization, Standardization
- Environment: Jupyter Notebook

## 🔍 Approach & Methodology:
- The project follows a structured data preparation and feature engineering workflow:
1. Data loading and structural inspection
2. Data type correction and categorical handling
3. Missing value analysis and treatment
4. Aggregation of multi-row trip records
5. Feature extraction from timestamps and location fields
6. Comparison of actual vs OSRM time and distance metrics
7. Outlier detection and treatment using IQR
8. Encoding categorical variables
9. Feature normalization and standardization

## 📈 Key Analysis:
- Dataset structure, shape, and statistical summary
- Aggregation of shipment segments at trip level
- Time-based feature creation (year, month, day, duration)
- Location feature extraction from source and destination names
- Visual and statistical comparison between Actual time vs OSRM time, Actual distance vs OSRM distance, Segment-level vs aggregated metrics
- Outlier detection using boxplots and IQR method

## 🧠 Feature Engineering:
- Aggregation of rows using: trip_uuid, Source and destination centers
- Creation of delivery duration features
- Extraction of city, state, and corridor information
- One-hot encoding of route types
- Scaling numerical features using:
- StandardScaler / MinMaxScaler

## 💡 Key Insights and 📌 Business Recommendations:
- Most trips use carting as delivery type compared to Full Truck Load.
- Bengaluru, Mumbai and Gurgaon are both the top contributors along with Bhiwandi, Delhi, Hyderabad, Chennai, Pune and Chandigarh thereby indicating that the Southern, Western and Northern corridors as the top performing ones.
- The top states with intra - state trips are Maharashtra, Karnataka,Tamil Nadu, Telengana, UP and among inter-state trips are Karnaataka, Maharashtra, Tamil Nadu, Telengana and Andhra Pradesh.
- The top cities in intra - city trips are Bangalore, Mumbai, and Hyderabad while the top cities for inter - city trips are Mumbai, Bhiwandi and Guragon.
- Due to delays caused by unprecedented traffic or other delays, OSRM seems to be calculating time and distance less than what actual scenario.
- Carting is prefered more in midnight orders.
- Most of the products were delivered on Wednesday followed by Saturday and Thursday. Least number of products were delivered on Sunday thereby indicating that customers prefer the deliveries of orders during weekdays.
- Many features show right-skewed distributions, particularly time and distance-related variables. Strong positive correlations observed between actual time, OSRM time, and distance-related features.
- Since there is significant dfference between the time and distances calculated by OSRM with actual time and distances, it might make sense to revisit the information which is fed to the routing engine for trip planning.
- The number of hubs could be increased in the states/cities which have highest contribution to traffic. FTL should be executed more for faster and on time deleveries.
