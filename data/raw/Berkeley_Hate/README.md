# Measuring Hate Speech (UC Berkeley D-Lab)

### Research Focus
* **Goal:** A high-precision scale for measuring the severity of hate speech using social science methodologies.
* **Context:** Large-scale analysis of real-world toxicity across YouTube, Reddit, and Twitter.

### Dataset Characteristics
* **Total Rows:** 135,556 annotated comments.
* **Data Origins:** Real-world Social Media Data.
* **Research Source:** Kennedy et al. (2020) - UC Berkeley D-Lab.
* **License:** CC-BY-4.0.

### Real-World Data (Why this design?)
1. **Mathematical Severity:** It provides a continuous **Hate Score** based on Item Response Theory (IRT), moving beyond binary classifications.
2. **Granular Targeting:** It identifies victims across multiple protected categories (Race, Religion, Sexual Orientation, Gender, Disability).
3. **Multi-dimensional Labels:** Each post is evaluated on sub-dimensions like Insult, Humiliation, and Dehumanization.

### Human Annotation & Quality
* **Annotator Density:** Each post was reviewed by an average of **2.2 annotators** (ranging from 2 to 5 per post).
* **IRT Methodology:** The dataset uses **Item Response Theory** to resolve disagreements between annotators, ensuring the final score is statistically robust.

### The Hate Speech Score (Interpretation)
The `hate_speech_score` is a logit-scale value where:
* **Score < 0:** Non-hate / Neutral language.
* **Score > 0:** Increasing levels of hate speech.
* **Threshold:** A score of **0.5 or higher** is typically used to classify a post as "Hate Speech" in binary tasks.

### File Details
| File Name | Description | Status |
| :--- | :--- | :--- |
| **measuring_hate_speech.csv** | The full dataset with multi-dimensional toxicity scores. | **Aggregated Data** |

### Data Schema
| Column | Description |
| :--- | :--- |
| `text` | The raw comment text from social media platforms. |
| `hate_speech_score` | Continuous IRT score (Negative = Neutral, Positive = Hate). |
| `target_race` | Binary indicator (0/1) if the post targets a racial group. |
| `target_gender` | Binary indicator (0/1) if the post targets a gender. |
| `annotator_count` | Number of humans who reviewed this specific post. |
