# Leveraging EDGAR Filings in Portfolio Construction

Applied Finance Project Code for Group 2:
1. Ayushi Garg
2. Anjali Jha
3. Abhilasha Dey
4. Anuj Choudhury
5. Santhosh Kumar

This project develops a long-short investment strategy leveraging sentiment and similarity scores derived from quarterly financial reports (10K/10Q). The raw filings are obtained through web scraping, with frequency-based dictionaries accessible from SRAF's EDGAR data (Loughran-McDonald_10X_DocumentDictionaries_1993-2023.txt). To construct a word-frequency dictionary from the raw filings or specific sections, refer to the data_processing.ipynb notebook within the edgar_filings_portfolio/bag_of_words directory. This process involves removing stop words and converting the data into a structured dictionary format, subsequently stored in yearly bucketed parquet files.

## Bag of Words
Similarity scores, specifically Jaccard and cosine similarities, are calculated between a company's current and previous quarter filings using the similarity_scores.ipynb notebook found in the same directory. These scores are archived in parquet files, organized by the filing date to facilitate portfolio construction based on temporal criteria.

Portfolio construction, including the formation of quintiles and the determination of long-short positions, is also executed through the 'portfolio_construction.ipynb' notebook, employing the derived similarity metrics as a basis for investment decisions.

Portfolio returns are calculated using the 'save_port_returns.ipynb' notebook and saved in parquet files. These computations are applicable to both the broader stock market and specifically to S&P 500 constituents.

Further analysis of the portfolio, including the calculation of Sharpe ratios, overall returns, and quintile alphas within the frameworks of the Capital Asset Pricing Model (CAPM) and Fama-French (FF) three- and five-factor models, is conducted in the 'portfolio_analysis.ipynb' notebook.

## BERT

## Sentiment Analysis
Portfolio analysis is available in 'edgar_filings_portfolio/sentiment_analysis/sentiment_analysis.ipynb'. For forming portfolios you can construct portfolios using files in 'edgar_filings_portfolio/bag_of_words' directory and using similarity_score instead of sentiment_score


EDA.ipynb file contains some exploratory data analysis.










 
