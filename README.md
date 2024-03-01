# Leveraging EDGAR Filings in Portfolio Construction

Applied Finance Project Code for Group 2:
1. Ayushi Garg
2. Anjali Jha
3. Abhilasha Dey
4. Anuj Choudhury
5. Santhosh Kumar

This project builds long short strategy using sentiment score and similarity score between quarterly reports. 
The webscraped 10K/10Q raw filings can be found at . 
We also have frequency based dictionaries at https://sraf.nd.edu/sec-edgar-data/10x-document-dictionaries/ . 
To extract frquency based dictionary for whole text or a particular section, look at edgar_filings_portfolio/bert/-----. 

Frequency based dictionary downloaded from EDGAR website needs to be processed to make a dictionary with keys as words and frquency count as values. Stop words are removed. Use edgar_filings_portfolio/bag_of_words/data_processing.ipynb  for doing that. We store processed dictionaries in parquet files bucketed by year.

Compute similarity scores - jaccard similarity and cosine similarity between current quarter filing and prior quarter filing using edgar_filings_portfolio/bag_of_words/similarity_scores.ipynb and store these files in parquet files bucked by Filing Date since portfolios are constructed based on that date.

Construct quintile and long short portfolios using edgar_filings_portfolio/bag_of_words/similarity_scores.ipynb






 
