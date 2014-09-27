Twitter Clustering/Grouping
============================
- Original work of **MARCEL CARACIOLO** [http://aimotion.blogspot.in/2010/02/playing-with-twitter-data-final.html]
- Run *twitterCollector.py* first

Dependencies
==============
- 	$ pip install python-twitter [ https://pypi.python.org/pypi/python-twitter/2.0]
-   install nltk, then import nltk, nltk.download --> to download 'stopwords' package
-   install Ubigraph Server in Linux or Mac ( no Windows version available http://ubietylab.net/ubigraph/)
- 	modify *twitterCollector.py* to have correct Twitter OAuth credentials 
while calling twitter.Api() of Step-1
-  api.GetFriendsIds takes almost 10-15minutes even in a decent network
run once and pickle.dump(list,open('data.pk','wb'))
-  read/pickle later to avoid network delay, as we are interested more in the user ids of friends which won't 		be stale inspite of offline network mode
-  	pickle dump the above list to data.pk  for future use
#usersIDList = pickle.load(open('data.pk', 'rb'))
- Set the IP (kmeans.open_ubigraph_server) of Ubigraph server in twitterOrganizer.py 