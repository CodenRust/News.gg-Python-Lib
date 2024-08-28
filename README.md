
# 📰 News.gg API

News.gg is a robust Python library designed to provide seamless access to the official News.gg API, an advanced alternative to GoogleNews. This library empowers developers to effortlessly integrate real-time news data into their applications, featuring optimized functions for fetching, filtering, and managing news articles. With a focus on performance and ease of use, News.gg is the ideal choice for developers seeking a reliable and efficient news API solution.









## Installation

This section will guide you on how to install News.gg libary

```bash
  pip install news.gg
```

After installation, you must import the libary in your code:
```bash
  import news
```


## Example Code/Docs

In this section you will learn on how to use the libary fully:

Example Code:
```bash
from news import News, NewsAPIError

# Instantiate the News class with your API key
news = News(api_key="e99b0814-ec9e-477c-9d71-e25e68b7dd5b")

try:
    # Fetch news articles for a specific country (e.g., "in" for India)
    articles = news.get_news_by_country("TWOLETTERCOUNTRYCODE")
    # articles = news.get_news_by_country("TWOLETTERCOUNTRYCODE", lang="2LETTERLANGUAGECODE")
    # Iterate over the fetched articles and print the title and publication date
    for article in articles:
        print(article["title"], article["publishedAt"])
except NewsAPIError as e:
    # Handle errors that occur during the API request
    print(f"Error fetching news: {e}")
```
- Ensure your API key is valid and has the necessary permissions for accessing the news data.
- The country code should be a valid ISO 3166-1 alpha-2 code (e.g., "us" for the United States).

- To create an API key click [here](http://46165.site.bot-hosting.net/index_api)
## Authors

- [Coden](https://www.github.com/nrgiazo)


## License

[MIT](https://github.com/nrgiazo/News.gg/blob/main/LICENSE.txt)

