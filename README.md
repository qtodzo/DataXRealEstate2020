# DataXRealEstate2020
Predicting Real Estate Values for Strategic and Responsible Investment. All instructions on how to use this prediction model are found in the README
## Instructions on how to run the UI
#### Step 1: Make sure your environment is complete with the necessary modules. Your environment must contain the following:
- Numpy (numerical operations)
- Pandas (organizing various data into readable data tables)
- GeoPandas (organizing and manipulating geotagged data, which when installed should come with Shapely and other geoprocessing   packages)
- requests (web scrape)
- BeautifulSoup 
- regular expression
- warnings
- Pickle (for transfering outputs between code scripts)
- Datetime (dealing with dates and time operations)
- PyAstronomy (for converting dates to decimals for plotting purposes)
- geopy (for getting the specific address of each listing)
- Flask (for running the actual UI)
- wtforms (for helping build the user input)
- matplotlib (for building the plots used)

#### Step 2: Clone the repository on your PC, and open the files using Jupyter Notebook

#### Step 3: Run the script titled "QProjections.ipynb"
This script will take the scaling factors created by the model and put them into a pandas dataframe. This dataframe is then saved into the pickle file titled "output.pkl"

#### Step 4: Run the script titled "
