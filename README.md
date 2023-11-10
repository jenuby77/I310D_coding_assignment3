# I 310D Fall 2023 Coding Assignment 3
### Hypothesis: The Perspective API will fail to mark indirect insulting comments on appearances as toxic.
Through this project, the hypothesis will be tested using the Perspective API with sample test cases from public sources and self-written by the creator. The Perspective API generates a toxicity score for a comment, and in this project, it is said to be toxic if the score is equal to or greater than 50%. 

### Insights
Overall, based on test cases, the API model demonstrated a relatively high accuracy. However, the hypothesis is proven to be valid; many indirect insulting comments were not given a high enough toxicity score. 

During the process, the model tended to give a much higher toxicity score for comments that contained cursing words. Moreover, words commonly known as harmful or insulting (e.g., ugly) led the comment to receive a high toxicity score. This has likely caused the accuracy of direct insulting comments to be 100%.
Unfortunately, the model failed to interpret indirect insulting comments as toxic. It is assumed that the main contributor is the lack of negative words. This is quite problematic as the accuracy of insulting comments without those is likely to be very low. 

It is presumed that these are the reasons why the test cases for non-insulting comments without negative words have a 100% accuracy, whereas non-insulting comments with negative words have a lower accuracy.

Another reason for such a failure is seemingly due to the model's inability to read the nuances of the comments. This raises the question of whether the model is trained in a number of different contexts where a comment could be used with different purposes. 

## Data Source
Disclaimer: comments that are not from a public source are purely written for educational purposes.
- [Bustle](https://www.bustle.com/articles/179754-13-appearance-related-things-people-comment-on-that-are-nobodys-business-but-your-own)
- [BuzzFeed](https://colab.research.google.com/corgiredirector?site=https%3A%2F%2Fwww.buzzfeed.com%2Fvictoriavouloumanos%2Fwomen-share-unsolicited-comments-about-appearance-by-men)
- [Reddit](https://colab.research.google.com/corgiredirector?site=https%3A%2F%2Fwww.reddit.com%2Fr%2Fask%2Fcomments%2Fqzlr6i%2Fwomen_what_is_the_worst_thing_someone_has_said%2F)

## APIs
- [Pandas](https://pandas.pydata.org/docs/reference/index.html)
- [Google API Client](https://github.com/googleapis/google-api-python-client.git)
  - [Perspective](https://developers.perspectiveapi.com/s/?language=en_US)
- [JSON](https://jsonapi.org/)

## License
[MIT License](https://opensource.org/license/mit/)
