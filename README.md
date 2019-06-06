# Bitcoin-Price-Predictor
Predict Bitcoin Prices from 2016 and on; TODO: aggregate sources like Reddit and Google Searches as part of NN.

# Cloud Services

After running the LSTM model and Prophet several times on my computer, I really wanted to find a way to lower the downtime waiting for the model to be constructed and seeing whether my error decreased after adjusting paramters.

* I found Azure Notebooks the easiest to setup( pasting the git repo and you are done) but also much slower than my desktop.
* I found installing Anaconda and the required packages on a AWS EC2 instance to be hard to setup, and was not keen on ssh'ing into a server every time I wanted look at my notebook.
* I settled on Amazon SageMaker as a way to load an existing Jupyter Notebook as well as learn to build,train, and deploy new ML models
in one localized space.
