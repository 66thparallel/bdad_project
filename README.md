Final Project for CSCI-GA.3033 Big Data Application Development

Title: Tourist Attraction Sentiment Analysis with TripAdvisor Reviews

Authors: Yu-Ting Chiu, Jane Liu

Description: This application uses sentiment analysis to create a ranked list of the best offbeat tourist
    attractions for Paris, London, and NYC for travel industry professionals. This program was written in Python
    2.7. It is unknown if it will work correctly for other versions of Python.


FILES
app_code/main.py
data_ingest/scrape.s
data_ingest/scraper.py
etl_code/etl.txt
profiling_code/profile.py
website/attrac/static/london.jpg
website/attrac/static/paris.jpg
website/attrac/static/newyork.jpg
website/attrac/templates/base.html
website/attrac/templates/index.html
website/attrac/db.py
website/attrac/schema.sql
website/instance/flaskr.sqlite
website/output/london.txt
website/output/paris.txt
website/output/nyc.txt
website/hello.py
screenshots/[screenshots of the running application]


REQUIREMENTS
Please copy all files and folders into the working directory (shown above). The following libraries are used: MLlib,
Spark SQL, string library.


INSTRUCTIONS

1. A batch file scrape.s has been included to run the web scrapers on the Prince cluster. We used only one
scraper.py file and updated the URLs to point to different tourist attractions for different cities.

2. It is recommended to run the profiling code (profile.py) line by line in the REPL due to the verbose feedback from
Spark  when running a script.

3. Please update your file path in main.py. It is located in the user-defined function printCity() at the bottom
of main.py.

    # Set the file path for the output files
    filepath = "/home/jl860/bdad/fp/website/output/"

4. To run the executable files: (please modify file paths)

cd /opt/cloudera/parcels/SPARK2/bin/
./spark2-submit --master local /home/jl860/bdad/fp/app_code/main.py

5. The output text files (containing a ranked list of tourist attractions) is output to the file path that
is specified in #3 above. Currently it's set to output to /home/jl860/bdad/fp/website/output/


EXPECTED RESULTS
The binary logistic regression model is expected to have approximately 50% accuracy.
We plan to train a multiple logistic regression model and will submit it in a separate file.

