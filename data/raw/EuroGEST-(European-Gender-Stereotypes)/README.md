# EuroGEST (European Gender Stereotypes)

### Research Focus
* **Goal:** A multilingual benchmark to test gender bias across European languages.
* **Context:** Focuses on 16 specific cultural themes (Career, Leadership, Emotions, etc.).

### Dataset Characteristics
* **Total Rows:** ~71,000 human-validated triplets (across all languages).
* **Data Origins:** Expert-generated templates (Professional Translation).
* **Research Source:** Utter Project (Rowe et al., 2025).
* **License:** Apache-2.0.
* **URL:** [Hugging Face Link](https://huggingface.co/datasets/utter-project/EuroGEST)

### Synthetic Data (Why this design?)
1. **Scientific Control:** Every entry is a "Minimal Pair". The dataset provides the exact same sentence in **Neutral**, **Masculine**, and **Feminine** forms. 
2. **Isolation of Bias:** By changing only the gender-coding (e.g., "I am a leader" vs "He is a leader"), we can isolate exactly if and how an AI model differentiates based on gender.
3. **Multilingual Consistency:** Since the same templates are used across 30 languages (including Greek), we can compare if the AI is equally biased in different cultures.

### Human Annotation & Quality
* **Expert Validated:** This is not raw machine output. **Professional human translators** reviewed and validated every single sentence.
* **Grammar Check:** They ensured that when a sentence is flipped from Masculine to Feminine, the grammar (especially in gendered languages like Greek) remains natural and correct.

### File Details
| File Name | Description | Status |
| :--- | :--- | :--- |
| **English.csv** | Human-validated templates in English. | **Aggregated Data** |
| **Greek.csv** | Human-validated templates in Greek. | **Aggregated Data** |

### Data Schema (Based on English.csv)
| Column | Description |
| :--- | :--- |
| `Stereotype_ID` | The ID of the stereotype category (1-16). |
| `Neutral` | The gender-neutral version of the statement. |
| `Masculine` | The masculine-coded version of the statement. |
| `Feminine` | The feminine-coded version of the statement. |
