storm-twitter-word-count
========================

Sample project based on https://github.com/abh1nav/dvto1 demonstrating real-time computation Storm framework (https://github.com/nathanmarz/storm).

See my blog post for mor details on this project: http://kaviddiss.com/2013/05/17/how-to-get-started-with-storm-framework-in-5-minutes/.

The code subscribes to Twitter's Sample feed, keeps stats on words occuring in tweets and logs top list with of words with most count in every 10 seconds.

This project contains a simple storm topology that connects to the sample stream of the Twitter Streaming API and keeps stats on words occuring in tweets and prints top list of words with highest count in every 10 seconds.

To get started:
* Clone this repo
* Import as existing Maven project in Eclipse/IntilliJ 

To run the project:

``` shell
mvn clean install package 
storm jar target/storm-twitter-word-count-*.jar com.kaviddiss.storm.Topology 
```
* Run Topology.java with your twitter credentials as VM args (see http://twitter4j.org/en/configuration.html#systempropertyconfiguration)

To get a new Twitter API key go to: https://apps.twitter.com/app/new and then place the credentials in the TwitterSampleSpout class

You'll need to have valid Twitter OAuth credentials to get the sample working.
For the exact steps on how to do that, visit https://dev.twitter.com/discussions/631.
