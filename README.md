# CS410_Project

To Execute Locally :

- Clone the Repo
- Go to directory actor_search_engine
- Execute buildSearchIndex.py or buildSearchIndex.ipynb to create inverted index - idx folder
- python movieApp.py

Output :
 * Serving Flask app "movieApp" (lazy loading)
 * Environment: production

 * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)
 
***Steps***

# Step 1 : Scrape files and generate Corpus
 
 There are 2 options. Execute either one of them
 
 ###Option 1 - Execute notebooks in following order
 
 1) prepareMovieActorsFile
 2) ScrapeMoviesActors.ipynb
 3) ScrapeMoviesTags.ipynb
 4) buildCorpus.ipynb
 
 OR 
 
 ###Option 2 - Execute shell script executeAllScripts.sh
 
 
# Step 2 : Build Inverted Index

Execute buildSearchIndex

# Step 3 : Render web page

Execute "python movieApp.py"