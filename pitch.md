# Brief Description
A web system designed to identify trends by scanning news sources to find common topics. 
---
# Problem
- It would be very useful to have a way to determine trends in a very fine grain way, confined to the sources you choose. Currently, existing free options only provide a very wide scope causing trends to become less.
# Appetite 
- The API and interface should be finished in 6 weeks or less.
# Solution
Here's the process:
1. Connect with many RSS feeds from various news sources. If you were interested in a particular topic, 
   you would only provide news sources that deal with that topic. 
2. Retrieve the RSS feeds and filter out commonly used words. A JSON format file containing many 
   commonly used words can be found here: https://github.com/dariusk/corpora/blob/master/data/words/common.json
   however, it must be pruned of some entries like "war."
3. Count the number of times each word is used across all sources and order them.
4. To that list, add the number of times specific pairs of words are used in those sources. 
5. Collect the top 30 (number subject to change) words/word-pairs and infer them as trends.

Design will be implemented in a way that is mobile first seeing as this would be the most common use.

# Rabbit Holes
- RSS feeds are an aging technology.
- RSS feeds could become unavailable in the future.
- Some sources might not offer an RSS feed.
- If RSS feeds are not sufficient for this application, I may have to explore web scraping pages.
# No-goes
- The system's ability to accurately identify trends is dependent on the amount/quality of the sources provided.
-  This is not a news site, all content comes from other sources

# Note On Scope
- Initially there will be a list of popular sources that will be used for the trending topic search. From this list the user will be allowed to add and or remove sources to their liking. A more user refined catalog of sources being the eventual outcome.

![one](https://user-images.githubusercontent.com/46355366/154315760-2f7f8aec-568f-46df-9efe-d0bb38c7cbfd.png)

![two](https://gist.github.com/dantiberi/d5f655be60b248f4f2e4df9335e47b0d?permalink_comment_id=4073412#gistcomment-4073412)

![three](https://gist.github.com/dantiberi/d5f655be60b248f4f2e4df9335e47b0d?permalink_comment_id=4073412#gistcomment-4073412)
