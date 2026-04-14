# Hate Speech and Offensive Language (Davidson et al.)

### Research Focus
* **Goal:** Distinguishing between actual **Hate Speech** and generic **Offensive Language** (e.g., profanity or slang).
* **Context:** Real-world Twitter data containing nuances of everyday language.

### Why this Dataset? (Bias Detection Focus)
I included this dataset because it evaluates a specific type of AI bias:
1. **Linguistic Bias:** It tests if a model wrongly labels slang or African American Vernacular English (AAVE) as "Hate Speech" just because it contains offensive words.
2. **Contextual Understanding:** It helps determine if an AI can distinguish between a toxic attack and informal/aggressive social media talk.

### Dataset Characteristics
* **Total Rows:** ~24,800 tweets.
* **Data Origins:** Real-world Twitter posts (2017).
* **Research Source:** Davidson et al.
* **License:** MIT / Open Access.

### Human Annotation
* **Crowdsourced:** Annotated by multiple humans (min. 3 per tweet).
* **Labels:**
    * **0**: Hate Speech
    * **1**: Offensive Language
    * **2**: Neither (Neutral)

### File Details
| File Name | Description | Status |
| :--- | :--- | :--- |
| **labeled_data.csv** | Tweets categorized into Hate, Offensive, or Neutral. | **Aggregated Data** |

### Data Schema
| Column | Description |
| :--- | :--- |
| `class` | 0: Hate, 1: Offensive, 2: Neither. |
| `tweet` | The raw text of the tweet. |
| `count` | Number of users who coded each tweet. |
