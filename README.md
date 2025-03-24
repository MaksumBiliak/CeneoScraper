# CeneoScraper MaksymBiliak
https://www.ceneo.pl/84514582#tab=reviews_scroll
## Ceneo scraping algorithm
1. Analysis  of the structure of the webpage
2. Send Http request to acces first page with options
3. Check the code of Http responce
4. Parse the Httm code of first page
5. Extract required data from parsed code
6. If there are more pages, move to the next page and repeat steps 2-6
7. Save extracted data

## Analyzis of teh structure of the webpage
|component|selector|variable|
|---------|--------|--------|
|opinion| div.js_product-review|opinion |
|opinion ID |[data-entry-id] |opinion_id |
|author |user-post__author-name| author|
|recomendation |span.user-post_author-recomendation > em|recommendation |
|number of stars |user-post__score-count |stars |
|content of opinion |div.user-post__text |content |
|list of advantages |review-feature__item review-feature__item--positive |pros |
|list of disadvantages |review-feature__item review-feature__item--negative |cons |
|for how many helpfull |button.vote-yes[data-total-vote] |vote_yes |
|for how many unhelpfull  |button.vote-no[data-total-vote]  |vote_no |
|publishig date |span.user-post__published > time:nth-child(1)[datetime]|published |
|purchase date |span.user-post__published > time:nth-child(2)[datetime] |purchased |