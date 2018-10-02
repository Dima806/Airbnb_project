# Airbnb_project

Descriptive analysis of Airbnb data from Seattle, Boston and Copenhagen (see also [this Medium post](https://medium.com/@dima806/digging-into-airbnb-data-reviews-sentiments-superhosts-and-prices-prediction-part1-6c80ccb26c6a) for detailed description)

### Used libraries:

* [`collections`](https://docs.python.org/3/library/collections.html)
* [`dateutil`](https://dateutil.readthedocs.io/en/stable/)
* [`eli5`](https://pypi.org/project/eli5/)
* [`geopy`](https://pypi.org/project/geopy/)
* [`matplotlib`](https://matplotlib.org/)
* [`nltk`](http://www.nltk.org/)
* [`numpy`](http://www.numpy.org/)
* [`pandas`](https://pandas.pydata.org/)
* [`scipy`](https://www.scipy.org/)
* [`seaborn`](https://seaborn.pydata.org/index.html)
* [`sklearn`](http://scikit-learn.org/stable/index.html)
* [`skopt`](https://scikit-optimize.github.io/)
* [`tqdm`](https://pypi.org/project/tqdm/)
* [`warnings`](https://docs.python.org/3/library/warnings.html)

### Libraries installation with [Pypi](https://pypi.org/)

`pip install eli5`

`pip install geopy`

`pip install matplotlib`

`pip install nltk`

`pip install numpy`

`pip install pandas`

`pip install scipy`

`pip install seaborn`

`pip install sklearn`

`pip install tqdm`

### Motivation for the project
The aim of the project is to analyze the latest Airbnb data publicly available for three different cities (Seattle, Boston and Copenhagen), to perform sentiment analysis of the reviews for their customers, to reveal the difference between Airbnb superhosts from ordinary hosts, and to understands main factors responsible for the prise of Airbnb apartments.

### Files in the repository

* `airbnb_final_analysis_v3.ipynb` - jupyter notebook with all details about preprocessing and analysis
* `README.md` - this file

### Summary of the results of the analysis

* Overwhelming majority (`> 95%`) of Airbnb reviews are either positive or neutral.
* For Copenhagen, the the technical messages fraction about apartment cancellation is about `3.5%`, or 4-6 times larger than in Boston and Seattle.
* Also, Copenhagen has much smaller fraction of superhosts (`10%`) than Seattle (`40%`) or Boston (`23%`).
* For all these cities, superhosts tend to have larger total and monthly averaged number of reviews, review scores and yearly availability are larger for superhosts than for ordinary hosts. On the other hand, the number of minimum nights, host response time and the host listings counts are smaller for superhosts than for ordinary hosts. This may reflect the higher popularity of superhosts and their higher level of service, compared to ordinary hosts.
* Among the most important features for daily price predictions are the distance to the city center and the type of the room. However, there are also significant differences between largest influencing features between different cities. For example, feature `hosting_listings_count` is valuable for US cities (especially for Boston) but is negligible for Copenhagen.
* Based on model trained by the data from different cities, we are able to predict the prices for a given city with a decent [R2 score](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html) close to 0.7.

### Acknowledgements

None.
