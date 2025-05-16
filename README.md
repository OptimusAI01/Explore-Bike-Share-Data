# US Bikeshare Data Explorer & Analyzer 🚲📊

Welcome to the US Bikeshare Data Explorer! This interactive Python script allows you to dive into bikeshare data from three major US cities: Chicago, New York City, and Washington. Filter data by month and day, uncover fascinating statistics, and even visualize trip patterns!

## 🚀 Features

*   **Interactive Filtering:** Choose a city (Chicago, New York, Washington), month (January - June, or all), and day of the week (Monday - Sunday, or all) to analyze specific datasets.
*   **Time Statistics:**
    *   Most common month for travel.
    *   Most common day of the week for travel.
    *   Most common start hour for trips.
*   **Station Statistics:**
    *   Most commonly used start station.
    *   Most commonly used end station.
    *   Most frequent combination of start and end stations.
*   **Trip Duration Statistics:**
    *   Total travel time for the filtered data.
    *   Average (mean) travel time.
*   **User Statistics:**
    *   Counts of different user types (e.g., Subscriber, Customer).
    *   Counts of gender (for Chicago & New York City).
    *   Earliest, most recent, and most common year of birth (for Chicago & New York City).
*   **Data Visualization:** Generates a bar chart showing the number of bike trips by start hour for your filtered selection.
*   **Raw Data Display:** Option to view 5 rows of raw data at a time.

## 📂 Files in this Repository

*   `bikeshare_analyzer.py`: The main Python script to run the analysis.
*   `README.md`: This file! Providing an overview and instructions.

## 🛠️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

*   Python 3.x
*   pip (Python package installer)

### Installation

1.  **Clone the repository (or download the ZIP):**
    ```bash
    git clone https://github.com/BinarySkull/bikeshare-data-explorer.git
    cd bikeshare-data-explorer
    ```
    
2.  **Install required Python libraries:**
    The script uses `pandas` for data manipulation and `matplotlib` for plotting.
    ```bash
    pip install pandas matplotlib
    ```
    If you're using a virtual environment (recommended):
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows: env\Scripts\activate
    pip install pandas matplotlib
    ```
3. **Download the datasets:**
   You can find them [here.](https://drive.google.com/drive/folders/1gO6AhEnageESHc4S6vgg3PugsxQ5ecpl?usp=sharing)
   
### Running the Script

1.  Navigate to the project directory in your terminal.
2.  Run the script:
    ```bash
    python bikeshare_analyzer.py
    ```
3.  The script will then prompt you to enter your desired city, month, and day filters. Enjoy exploring the data!

## 📝 How It Works

1.  **User Input (`get_filters`):** The script first greets you and asks for your preferences:
    *   City (Chicago, New York, or Washington)
    *   Month (January to June, or 'all')
    *   Day of the week (Monday to Sunday, or 'all')
2.  **Data Loading (`load_data`):**
    *   Based on your city selection, the corresponding CSV file is loaded into a pandas DataFrame.
    *   The 'Start Time' column is converted to datetime objects.
    *   New columns for 'month', 'day_of_week', and 'hour' are extracted.
    *   The DataFrame is filtered according to your month and day selections.
3.  **Calculating Statistics:**
    *   `time_stats`: Calculates and displays the most frequent travel times.
    *   `station_stats`: Calculates and displays the most popular stations and trips.
    *   `trip_duration_stats`: Calculates and displays total and average trip durations.
    *   `user_stats`: Calculates and displays statistics about bikeshare users (types, gender, birth year where available).
4.  **Plotting Data (`plot_trips_by_hour`):**
    *   A bar chart is generated and displayed showing the distribution of trips by the start hour for the filtered data.
5.  **Displaying Raw Data (`show_row_data`):**
    *   You'll be asked if you want to see 5 rows of the filtered data. You can continue viewing more rows in chunks of 5.
6.  **Restart Option:** After an analysis run, you can choose to restart and explore different filters.

## 💡 Example Interaction
- Hello! Let's explore some US bikeshare data!
- Enter a city from (Chicago, New York, Washington) that you want to get data about
- chicago
- Ok, Please wait a moment
- Which month do you need the data on?...(all, january , february , ... , june
- may
- Ok, please wait a moment.
- Which day do you need the data on?...(all, monday, tuesday, ... sunday)
- monday
- Ok, Please wait a moment
- Calculating The Most Frequent Times of Travel...
- The most common month is :5
- The most common day of week is :Monday
- The most common start hour is :17
- This took 0.02 seconds.
- Calculating The Most Popular Stations and Trip...
- ... (and so on) ...

## 🙏 Acknowledgements

*   Data provided by Udacity for their Data Analyst Nanodegree program.

*   Enjoy exploring the bikeshare data! If you have any suggestions or find any bugs, feel free to open an issue or submit a pull request.
