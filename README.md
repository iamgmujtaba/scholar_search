# Google Scholar Search Analytics: A Tool for Analyzing Historic Occurrence of Academic Papers
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1hB1Rod0KfG_Ov3lXKdM7HlvJjK8N5ZWF)

## Summary
This particular code is designed to extract the number of results returned from Google Scholar for a given search query. The code then compiles this data into a CSV file, which can be used for further analysis or reference. Additionally, the code has built-in functionality to generate graphs and charts based on the data in the CSV file, making it easier to visualize trends or patterns in the search results. Overall, this code is a useful tool for researchers or academics looking to gain insight into the quantity and distribution of scholarly articles related to a particular topic or field.

## Requirements
The code requires Python 3.0 or later and the following packages:
- beautifulsoup4
- urllib3
- matplotlib
- pandas

## Usage
By customizing these search parameters, you can tailor the tool to your specific research needs and generate more targeted results.
- `query`: the search query you wish to use. In this example, the query is set to 'deep learning'.
- `start_year`: the year from which you wish to start searching. In this example, the search is set to start in the year 2018.
- `end_year`: the year at which you wish to stop searching. In this example, the search is set to end in the year 2023.
- `as_occt`: this parameter determines where the search query should be found within the article. Set to 'any' to search for the query anywhere within the article or set 'title' for the query in the title.
- `as_sdt`: include patents in the search (set to null for no patents and 7 for patents).
- `visibility`: include citations in the search (set to null for no citations and 0 for citations).

Additionally, the tool offers advanced search options like google scholar:
- `as_epq`: return articles with the exact phrase.
- `as_oq`: return articles with at least one of the words.
- `as_eq`: return articles without the specified words.
- `as_sauthors`: return articles authored by specific authors.
- `as_publication`: return articles published in specific publications.


## Example
To search for articles related to 'deep learning' published between 2016 and 2023, with the query limited to article titles and published in IEEE
 
```python
search_options = {
    'query': 'deep learning',
    'start_year': 2016,
    'end_year': 2023,
    'as_occt': 'title',
    'as_epq': '',
    'as_oq': '',
    'as_eq': '',
    'as_sauthors': '',
    'as_publication': 'IEEE'
}
```

| year | results |
|------|---------
| ...  |    ...  |	|
| 2016 |    619  |
| 2017 |    1510  |
| 2018 |    2760  |
| 2019 |    4690 |
| 2020 |    5880 |
| 2021 |    7470 |
| 2022 |    8430 |
| 2023 |    1480 |

## Results

The following figures show the results of the search query:

![Figure 1](/bar_chart.png)

![Figure 2](/line_chart.png)

## Cite
The code is used in the paper [ChatGPT in the Age of Generative AI and Large Language Models: A Concise Survey](https://arxiv.org/abs/2307.04251)

### Acknowledgement:
This code is inspired by [Historic word occurrence in academic papers
](https://github.com/Pold87/academic-keyword-occurrence)
