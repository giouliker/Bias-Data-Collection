# Social Bias Frames (SBIC)
### Research Focus
The original research introduces a framework to distill social bias and offensive stereotypes from language into structured explanations, resulting in a model that can automatically detect targeted demographics and the underlying intent of biased posts.
### Dataset Characteristics
* **Total Rows:** ~131,000 annotated posts
* **Data Origins:** Social media platforms (Reddit, Twitter, Gab)
* **Research Source:** Allen Institute for AI (Sap et al., 2020)
* **License:** CC-BY
* **URL:** [Hugging Face Link](https://huggingface.co/datasets/allenai/social_bias_frames)
### Human Annotations
* **Annotator Diversity:** Labeled by a diverse group of human annotators (varying age, gender, and race).
* **Multi-Labeling:** Each post often has multiple annotations to capture different human perspectives on bias.
### File Details
| File Name | Description | Status |
| :--- | :--- | :--- |
| **SBIC.v2.trn.zip** | The main raw dataset (compressed). Contains all individual annotations. | **Primary Raw Data** |
| **SBIC.v2.agg.trn.csv** | Training set with aggregated labels (averaged scores per post). | **Aggregated Data** |
| **Note:** | Dev and Test splits are omitted for repo but can be merged later. |  |
### Data Schema
| Attribute | Description | Role |
| :--- | :--- | :--- |
| `post` | Raw social media text | **Primary Text** |
| `offensiveYN` | Likelihood of being offensive | **Bias Score** |
| `targetCategory` | Target demographic group | **Category Label** |
