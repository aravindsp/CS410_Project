# Execute web server Locally (Mac OS)

To Execute Locally :

- Clone the Repo - https://github.com/aravindsp/CS410_Project
- Go to directory actor_search_engine
- Execute buildSearchIndex.py or buildSearchIndex.ipynb to create inverted index - idx folder
- python movieApp.py

Output :
 * Serving Flask app "movieApp" (lazy loading)
 * Environment: production

 * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)
 
 # Execute web server on the cloud (AWS)
 
 ### Launch Ubuntu Server 18.04 LTS (HVM), SSD Volume Type - ami-083f68207d3376798 (64-bit x86)
 sudo apt-get update
 
### Install Python via Anaconda3
sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
wget https://repo.anaconda.com/archive/Anaconda3-5.0.1-Linux-x86_64.sh
sudo reboot

### Install Requirements
sudo apt-get install python3-bs4
conda install selenium
sudo apt-get install chromium-chromedriver

pip install metapy
pip install pytoml
pip install requests
pip install flask

### Clone and Create idx
git clone https://github.com/aravindsp/CS410_Project
cd CS410_Project/actor_search_engine/
python buildSearchIndex.py

### Start web server
nohup python bgservice.py &

 
# Run all processes from scratch (Mac OS)
 
 
***Steps***

## Step 1 : Clone the Repo - https://github.com/aravindsp/CS410_Project
Go to directory actor_search_engine

## Step 2 : Download following files and extract the tsv files to "SourceFiles" directory
Link - https://datasets.imdbws.com/

Files :

- name.basics.tsv.gz
- title.akas.tsv.gz
- title.basics.tsv.gz
- title.principals.tsv.gz
- title.ratings.tsv.gz

## Step 3 : Scrape files and build corpus
 
 There are 2 options. Execute either one of them
 
 ### Option 1 - Execute notebooks in following order
 
 1) prepareMovieActorsFile
 2) ScrapeMoviesActors.ipynb
 3) ScrapeMoviesTags.ipynb
 4) buildCorpus.ipynb
 
 OR 
 
 ### Option 2 - Execute shell script executeAllScripts.sh
 
 
## Step 4 : Build Inverted Index

Execute buildSearchIndex

## Step 5 : Render web page

Execute "python movieApp.py"