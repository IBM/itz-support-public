# Content Creator: How to improve your collections search results

Scenario:

- Collection owner or collaborator would like their collection to display higher on the search results page. 

## How collection form fields are weighted 

Collection field weights:
- Collection name: 10
- Collection description: 5
- Collection short description: 3
- Collection Taxonomy_Minor Unit: 1
- Collection Taxonomy_Major Unit: 1
- Collection Taxonomy_Offerings: 1
- Collection Taxonomy_Offering Portfolio: 1
- Collection Brand: 1
- Resource name: 2
- Resource description: 1
- Environment name: 2
- Environment description: 1 
- Collection search tags: 2
- Collection industries: 1
- Collection technology decision points: 1

Query boosting in Elastic search allows us to indicate that some fields in your created collections when searching should be more important than others. Above are the fields on your created collections that we have associated a weight to. The higher the number the higher score when users search and there is a one-to-one match in that field. 

For example: 

User searches "data" in the search bar. If the word "data" is referenced in the title once then assume in this example that a score of 10 is applied based on the match. 1 match of search term "data" X the collection name weight of 10 = a score of 10. Additionally if the search term "data" is also found in collection description field once then the match score on collection description would result a 5. 1 match of search term "data" X the collection description weight of 5 = a score of 5. All of the matches found in the collection by field will produce a match score at each field based on their weight and will result for the search criteria an aggregate of all the scores together when returning collection results back to the end user. The best match scores of your collection and the best match scores of other collections based on the search term "data" will decide which collections to display first on the search page. 

Now let's throw in another layer of weighting that is applied in addition to the above logic.

Badge weights:
- Platinum Collection badge: 100 weight
- Platinum badge:  75 weight
- Gold badge: 50 weight
- Silver badge: 25 weight
- Bronze badge: NULL

Every collection that has a badge associated with it has this additional criteria applied within Elastic search. Imagine the use case mentioned above and the result of two collections best match scores resulted for some odd reason in the exact same scores. 

Collection 1: Best match score was 100 based on the search term "data"

Collecton 2: Best match score was 100 based on the search term "data"

Collection 1 has a platinum badge associated and Collection 2 has a silver badge associated. 

Collection 1 will result a higher best match score since the weight is higher for a platinum badge. The higher the badge, the higher the weight, meaning the higher the score when comparing the search result of what was searched by the user. This weight was added to surface higher quality, higher support engagement, and the most up to date Platinum grade collections first due to the higher quality of standards that apply with platinum content. 

[Learn more about each badges standards here.](https://ibm.box.com/s/rw6lxuoor1q2vvrdy3r194a96bhwjt6u)
Want to learn more about Elastic search scoring framework? [Check out this article.](https://www.compose.com/articles/how-scoring-works-in-elasticsearch/)

### Support

For any questions, contact ITZ support - techzone.help@ibm.com

