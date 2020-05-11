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

#### Step 4: Run the script titled "DataframeProcessing.ipynb"
To make sure that this script runs properly, ensure that the file titled "zillow-neighborhoods.geojson" is in the current folder. This script accepts the pickle file created by "QProjections.ipynb" called "output.pkl" and then does a web scrape of the available listings on Craigslist. Then the script takes the Craigslist data and applies the model factors to the listed price using the neighborhood conversion from the GeoPandas and Shapely modules. Once all is said and done, this script outputs a dataframe of all the craigslist listings and their respective future price predictions. This will be saved in the pickle file titled "craigslist_df.quinn"

#### Step 5: Run the script titled "ProjectFlaskUI-Final.ipynb"
This script actually runs the User Interface allowing the user to interractively find their best real estate investing option. The script first accepts the dataframe created in step 4, and then adds to it the actual address of the listing by using the geopy module package (the script may take up to 2-3 minutes to run this portion of the script). Finally, at the bottom of the script, there is a kernal that should be running with text in red displaying *Running on http://127.0.0.1:5000/ 

#### Step 6: Run the UI
Note that in order for the UI to run properly it is necessary to download the folders titled "static" and "templates". From here, click on the link under app.run() listed in Step 5. This will take you to the user interface. Now you can use the input and output pages to give preferences and then see what is the best real estate option by clicking "See your Results!"


