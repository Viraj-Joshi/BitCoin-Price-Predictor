# Bitcoin-Price-Predictor
Predict Bitcoin Prices from 2016 and on; TODO: aggregate sources like Reddit and Google Searches for sentiment + additional regressors like other stocks/ cryptos

# Cloud Services

After running the LSTM model and Prophet several times on my computer, I really wanted to find a way to lower the downtime waiting for the model to be constructed and seeing whether my error decreased after adjusting paramters.

* I found Azure Notebooks the easiest to setup( pasting the git repo and you are done) but also much slower than my desktop.
* I found installing Anaconda and the required packages on a AWS EC2 instance to be hard to setup, and was not keen on ssh'ing into a server every time I wanted look at my notebook.
* I settled on Amazon SageMaker as a way to load an existing Jupyter Notebook as well as learn to build,train, and deploy new ML models
in one localized space.

# Methods

* LSTM
* Random Walk
* Facebook Prophet
  * Used seasonalities
  * Find a n length cycle with experimentally lowest found MAPE and highest found returns (In Progress)
  
# Returns
* Each method seeks to generate buy-sell dates starting from 2019. As of now, LSTM generates about $80000. FB Prophet Method 2 generates about $2000 dollars. FB Prophet Method 1 generates a negative amount, but predicates a postive amount.
* FB Prophet Method 2 is a work in progress.
