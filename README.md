# Austin Incident Interactive Dashboard

Demo: https://steve-yuan-8276.github.io/Austin_accidents_interactive_dashboard/

In this project, I performed data cleaning using Pandas, addressing missing values, correcting data types, and removing anomalies to ensure the dataset was robust for analysis. The cleaned data was saved in CSV format for further use during the visualization stages.

In the visualization part, I focused on the spatial and temporal dimensions of traffic accident data and utilized Plotly to create interactive and dynamic visualizations. Each visual component was exported as JSON, enabling seamless integration with HTML and CSS for a responsive, user-friendly dashboard. This approach allowed me to effectively present the temporal and spatial dimensions of traffic accidents, providing clear insights into patterns and trends within the city.

## Instructions for Use

The demo includes five views:

### 1. Accident Severity Distribution Map (Scatter Map)

Combines a scatter plot with a map to show the distribution of accidents in Austin. Accidents are categorized into four levels based on severity, represented by gray, light blue, yellow, and red. Hovering over points reveals detailed information including latitude, longitude, postal code, street name, county, city district, severity level, accident duration, and traffic impact.

**Analysis**:

- **Red and yellow dots**: These dots are concentrated along major highways (such as I-35), showing a high density of traffic accidents in these areas, particularly along north-south highways. This indicates higher traffic pressure or a frequent occurrence of accidents in these locations.

### 2. Annual Accident Time Trend in Austin (Line Chart)

Displays the time trend of accidents from 2016 to 2023. A slider at the bottom allows users to zoom in on specific time periods, while clicking on the legend reveals trends for each county.

**Analysis**:

- The number of accidents fluctuated significantly from 2016 to 2023. There were noticeable declines from February to August 2020 and November 2021 to July 2022, likely related to COVID-19 travel restrictions. Starting in August 2022, accident rates rose sharply as society resumed normal operations.

### 3. Monthly Distribution of Accidents per Year (Distribution Chart)

Presents the number of accidents per month across multiple years. Users can choose "Show All" for a full-period view or select specific years to compare via the legend.

**Analysis**:

- Accidents tend to peak in the autumn and winter months (August to December), while the first half of the year (February to July) sees fewer incidents.
- 2020, the pandemic year, had noticeably fewer accidents, particularly in the spring and summer, reflecting reduced travel.

### 4. Average Number of Accidents by Hour (Distribution Chart)

Displays the average number of accidents by hour. Users can toggle between "Show All" for the entire dataset or "Details" to view weekday vs. weekend patterns.

**Analysis**:

- Accident peaks occur during the morning rush (7-9 AM) and evening rush (4-6 PM).
- On weekends, fewer accidents happen during early morning hours (6-9 AM), but there is a gradual rise through the afternoon (12-6 PM), coinciding with weekend travel habits.

### 5. Traffic Accident Numbers by Postal Code Area Over Time (Bubble Chart)

Uses a bubble chart to display monthly aggregated traffic accident data by postal code. Clicking the play button animates the data, showing dynamic trends over time.

**Analysis**:

- Areas such as **78741** and **78753** consistently show higher accident numbers, indicating these postal codes experience more frequent traffic incidents compared to others.

## View Switching with Buttons

### 1. **Styling with Bootstrap**:

- The design utilizes Bootstrap 4.5.2 for simple and uniform button styling. By default, the map view (`plot5`) is displayed while other views are hidden. Users can switch between different chart containers by clicking the corresponding buttons, activating the `showView()` function.

### 2. **Button Group Layout**:

- Buttons are grouped using `div class="btn-group"`, ensuring a consistent layout. This design allows users to easily switch between views using Bootstrap's responsive layout.

### 3. **Interactive Button Functions**:

- Each button triggers an `onclick` event that dynamically switches the view. This ensures that different visualizations are easily accessible without reloading the page.

## Project Structure
    

    
    Data_Viz_V3_Steve.ipynb
    demo.html
    plots.js
    styles.css
    
    README.md
    
    Data_Source/
        AustinTXAccidentsData.csv
        TravisCoAccidentsData.csv
        TXAccidentsData2022.csv
        WacoTXAccidentsData.csv
    
    JSON/
        fig1.json
        fig2.json
        fig3.json
        fig4.json
        fig5.json
    
    Output_data/
        austin_accident_df.csv
        austin_cleaned_data.csv
        austin_time_trends_data.csv
    

### File Descriptions:

- **HTML Files**: `demo.html` contains the structure for displaying the charts and interactive visualizations.
- **JavaScript Files**: `plots.js` handles chart rendering and interaction logic.
- **CSS Files**: `styles.css` provides styling for the entire web page.
- **JSON Files**: Stores the configuration and data for each visualization.
- **Data_Source**: Contains original traffic accident data for Austin, Travis County, Waco, and other regions.
- **Output_data**: Contains cleaned and transformed datasets, including time trend data and filtered Austin accident data.
- **Jupyter Notebook**: `Data_Viz_V3_Steve.ipynb` documents the data cleaning, exploration, and visualization process.



