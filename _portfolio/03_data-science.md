---
title: "Data science: is HK facing depopulation?"
excerpt: "Some data dashboarding and plotting to understand a question I had"
header:
  teaser: https://miro.medium.com/v2/resize:fit:720/format:webp/0*H1MD2lTwgxdPAAaX
sidebar:
  - title: "Timeframe"
  - text: "July 2021, updated Jan 2025 with more features"

mathjax: true
---

_This work was previously written and published on Medium in 2021, several updates were made in 2025 as a plotting service I've used has become outdated._.

The past several years have been particularly challenging for Hong Kong, but the decisive blow was dealt by various new laws, which made many residents seriously consider leaving permanently.

I have definitely heard more Cantonese being spoken on the streets of London and Manchester, and have seen more social media groups popping up offering a helping hand to new immigrants.

Recently, there have been new schemes to attract Hong Kongers to travel to the mainland for consumption, entertainment, as well as work.

Quantifying how many people that plan to leave or have left is a difficult task. But what is the trend?

Bloomberg Opinion have looked at proxies such as the withdrawal of money from the Mandatory Provident Fund and the application for certificates of no criminal conviction, which have all increased. What I am interested in is Immigration data.

![Photo by Ryan McManimie on Unsplash](https://miro.medium.com/v2/resize:fit:720/format:webp/0*H1MD2lTwgxdPAAaX)

### Data dashboard

<!-- ![alt text](/files/immigration/dashboard.png) -->

<iframe src="https://kwokkenton-hongkong-immigration-frontend-vwwzsh.streamlit.app/?embed=True" style="width: 100%; height: 800px; border: none;">
  <p>Your browser does not support iframes.</p>
</iframe>

[Visit the dashboard here](https://kwokkenton-hongkong-immigration-frontend-vwwzsh.streamlit.app/){: .btn .btn--success target="\_blank"}

### Data Science Technicalities

The work here is as much a Python exercise on Web-scraping and Data Visualisation as a study on Hong Kong society. Web-scraping is basically retrieving data from websites, specifically their HTML code. I wish to point out that some others have done a [similar project](https://webb-site.com/dbpub/hkpax.asp) but I wish to go into more depth.

![alt text](/files/immigration/table.png)

_Screenshot of the Immigration Department’s website, showing an example table of data_

I scraped data from the Hong Kong Immigration Department’s website, where they provide daily updates on the number of passengers who have entered and left different ports in the city. Data is provided by the HK Government and the relevant rights are theirs. This was done by finding all relevant cells with the <td> tag. Afterwards, I used more features from Pandas to wrangle the data into a more appropriate (long) format suitable for analysis. I stored this in a cloud-based PostgreSQL database (from Neon), which has a generous free tier.

## Skills developed

**Programming**: Selenium, SQL, PostgreSQL, Streamlit
