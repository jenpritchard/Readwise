# Readwise/Reader helper scripts
 
Currently official support from Reader is lacking when it comes to things like detecting or removing duplicate articles, or easier ways to curate tags.

## ReaderDedupe
The purpose of this script is to crawl your Reader account for any potential duplicate articles, as defined by an article's title. Because there is the possibility that multiple articles have the same title but are not duplicates, you can create a note on the article called "not a dupe" and it will be excluded. For my purposes, further limiting the match by author etc resulted in too many false negatives (mainly when articles from Medium, or or articles from certain feeds), but future enhancements could be made to suit your personal use cases.

### Note
This does not automatically delete duplicates, because
1. The Reader API does not currently allow that, and
2. Even if it did, you'd want to have control over what you consider the right copy to delete

### Prerequisites
Your own API key for your Reader account. API key is obtained at #https://readwise.io/reader_api
A file named .env in the same directory, containing "API_KEY=yourkeyhere"