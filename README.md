# 🏴‍☠️ One Piece NLP Analysis

An NLP project exploring **themes, recurring concepts, and sentiment in reader discussions about *One Piece*** using TF-IDF keyword extraction and VADER sentiment analysis.

## 🎯 Problem

Why do readers repeatedly highlight certain narrative elements when discussing *One Piece*?

This project explores the textual patterns within reader discussions to identify:

* Frequently emphasized narrative concepts
* Recurring themes and phrases
* Overall sentiment toward the series
* Emotional and thematic patterns in reader feedback

> **Scope:** This project analyzes textual patterns in a small sample of reader discussions. It does not establish causal relationships between narrative features and commercial sales.

## 📊 Dataset

The analysis uses a small manually curated corpus of **8 reader discussion/review texts** focused on *One Piece*.

The texts discuss topics such as:

* World-building
* Foreshadowing
* Freedom
* Found family / Nakama
* Character development
* Backstories
* Longevity
* Political and social themes

The corpus is embedded directly in the notebook as a Python list.

### Dataset Characteristics

| Attribute        | Description                             |
| ---------------- | --------------------------------------- |
| Corpus size      | 8 text samples                          |
| Content type     | Reader discussions / review-style texts |
| Language         | English                                 |
| Unit of analysis | Individual review                       |
| Target           | No predefined target variable           |
| Analysis type    | Unsupervised text analysis              |

## 🔬 Method

The project follows a basic NLP pipeline.

### 1. Text Preprocessing

Each text is:

* Converted to lowercase
* Stripped of punctuation and numbers
* Tokenized
* Filtered using English stopwords

The cleaned corpus is then used for downstream text analysis.

### 2. TF-IDF Analysis

**TF-IDF (Term Frequency–Inverse Document Frequency)** is used to identify words and phrases that are relatively important within the corpus.

The analysis uses:

* Unigrams
* Bigrams
* English stopword removal

The mean TF-IDF score across documents is then used to rank the most prominent terms.

### 3. Sentiment Analysis

**VADER (Valence Aware Dictionary and sEntiment Reasoner)** is used to estimate sentiment for each review.

The analysis records:

* Positive sentiment
* Negative sentiment
* Compound sentiment score

Compound scores range from **-1 to +1**, where higher values indicate more positive sentiment.

### 4. Thematic Interpretation

The highest-weighted terms are interpreted qualitatively to identify broader narrative themes.

This combines:

**Quantitative NLP → Keyword extraction → Qualitative thematic interpretation**

## 📈 Results

### 1. Dominant Themes

The highest-ranked TF-IDF terms in the analysis are:

| Rank | Keyword / Phrase          | TF-IDF Score | Interpreted Theme       |
| ---: | ------------------------- | -----------: | ----------------------- |
|    1 | `world building`          |        0.285 | World-building          |
|    2 | `freedom`                 |        0.241 | Philosophy / motivation |
|    3 | `foreshadowing`           |        0.218 | Long-term storytelling  |
|    4 | `found family / nakama`   |        0.204 | Relationships           |
|    5 | `longevity / consistency` |        0.189 | Long-term engagement    |
|    6 | `backstories`             |        0.176 | Emotional storytelling  |

These results suggest that the sampled discussions place substantial emphasis on **world-building, thematic ideas, long-term narrative connections, relationships, and character backstories**.

### 2. Sentiment

The reported average compound sentiment score is approximately:

**+0.78**

This indicates that the sampled reviews are strongly positive in tone.

The individual reviews also show positive sentiment around topics such as:

* World-building
* Freedom
* Character relationships
* Backstories
* Long-term storytelling

The VADER analysis is calculated individually for each of the eight texts.

### 3. Main Thematic Pattern

The analysis suggests three broad themes:

**🌍 Narrative Complexity**

World-building and foreshadowing appear prominently in the sampled discussions.

**❤️ Emotional Connection**

Readers frequently discuss character backstories, found family, and emotional experiences.

**🧭 Thematic Ideas**

Concepts such as freedom, liberation, and inherited will appear as recurring discussion points.

## 📊 Visualization

The notebook combines two visualizations:

### TF-IDF Keyword Importance

A horizontal bar chart ranks the most prominent words and phrases according to their mean TF-IDF scores.

### Reader Sentiment

A second bar chart displays the VADER compound sentiment score for each sampled review.

![One Piece Text Analysis](visualization.png)

The notebook generates the visualization as a high-resolution image for further use.

## 💡 Conclusion

The NLP analysis identifies several recurring themes in the sampled *One Piece* reader discussions.

### Key Takeaways

**1. World-building is highly prominent.**

Terms related to world-building and interconnected storytelling receive high TF-IDF weights.

**2. Freedom is an important recurring concept.**

The theme appears repeatedly in discussions of Luffy, character motivation, and the broader narrative.

**3. Emotional storytelling is central to reader discussions.**

Backstories and found-family relationships appear among the prominent themes.

**4. The sampled corpus is strongly positive.**

The average VADER compound score of approximately **+0.78** indicates a strongly positive sentiment profile.

### Important Limitation

The findings should **not** be interpreted as proof that these narrative characteristics caused *One Piece*'s commercial success.

The corpus contains only **8 manually constructed texts**, and the analysis does not include:

* Actual manga sales by chapter or volume
* Reader population data
* A control group
* Longitudinal reader data
* Comparison with other manga
* Statistical testing of commercial outcomes

Therefore, the project is best understood as an **exploratory NLP and thematic-analysis study** rather than a causal explanation of commercial success.

## 🚀 Future Improvements

A stronger version of this project could:

* Collect thousands of authentic reviews
* Scrape publicly available Reddit/forum discussions where permitted
* Compare *One Piece* with other major manga
* Perform topic modeling with LDA or BERTopic
* Analyze sentiment over time
* Track themes by manga arc
* Compare narrative themes with sales data
* Build a supervised model for review classification
* Use word embeddings or transformer-based models

A particularly interesting extension would be:

> **Narrative Themes × Reader Sentiment × Manga Sales**

This would connect the current NLP analysis with your separate manga-market-analysis project.

## 🛠️ Technologies

* **Python**
* **Pandas** — data manipulation
* **NumPy** — numerical computation
* **NLTK** — text processing and VADER sentiment
* **Scikit-learn** — TF-IDF feature extraction
* **Matplotlib** — visualization
* **Seaborn** — visualization
* **Jupyter Notebook** — analysis

### Methods

`Natural Language Processing` `TF-IDF` `Sentiment Analysis` `VADER` `Text Mining` `Thematic Analysis` `Feature Extraction`

## 📁 Repository Structure

```text
one-piece-nlp-analysis/
│
├── one-piece-nlp-analysis.ipynb
├── visualization.png
└── README.md
```

## 📌 Topics

`Python` `NLP` `Natural Language Processing` `Text Mining` `TF-IDF` `Sentiment Analysis` `VADER` `Manga` `One Piece` `Data Analysis` `Data Visualization`
