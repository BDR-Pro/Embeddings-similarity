# 🧠 Sentence Embedding Similarity (Local)

This simple Python script uses `sentence-transformers` to compute and visualize sentence embeddings and their cosine similarity.

## 🔍 Features

- Loads a small, efficient embedding model: `all-MiniLM-L6-v2`
- Encodes a set of example sentences into dense vector embeddings
- Computes **pairwise cosine similarity matrix**
- Performs a **semantic search** for the most similar sentences to a query
- Outputs a ranked list of closest matches

## 🚀 Run Instructions

### 1. Install Dependencies

```bash
pip install sentence-transformers scikit-learn pandas
````

### 2. Run the Script

```bash
python sentence_similarity.py
```

Or use a Jupyter Notebook if you're working interactively.

## 🧾 Output Example

Example query:

```
"Hot pizza from the oven"
```

Top similar sentences:

```
A pizza is baking in the oven  (score: 0.57)
The oven is very hot           (score: 0.47)
I like pizza                   (score: 0.37)
```

## 📊 Pairwise Similarity Matrix (visual in notebook)

|              | I like pizza | The dog... | A pizza... | He enjoys... | The oven... | She loves... |
| ------------ | ------------ | ---------- | ---------- | ------------ | ----------- | ------------ |
| I like pizza | 1.000        | 0.057      | 0.409      | ...          | 0.244       | 0.284        |
| ...          | ...          | ...        | ...        | ...          | ...         | ...          |

Styled with a blue gradient using Pandas.

## 💡 Notes

* This is a fully **local** setup – no API or external service calls
* Uses cosine similarity to reflect **semantic closeness** of sentences
* Useful for quick NLP prototyping or exploring sentence relationships

## 📊 Sentence Embedding Similarity Visualizer (Manim)

This project visualizes **cosine similarity** between sentence embeddings using the [Manim](https://docs.manim.community/) animation engine.

## 🎯 Features

- Shows sentence vectors as arrows in 2D space
- Animates sentence labels
- Annotates cosine similarity between selected vectors
- Uses **precomputed cosine similarity** (no model required)

## 🛠️ Requirements

```bash
pip install manim
````

(Use a virtualenv if needed)

## 🚀 Run

```bash
python -m manim -pql embeddings.py VisualizeCosineSimilarity
```

* `-pql`: Preview in low quality (for faster rendering)
* You can also use `-pqh` for high quality or `-qm` for medium

## 🧠 How It Works

* Positions of arrows are **manually defined** to reflect semantic similarity visually
* Cosine similarity is precomputed and displayed during the animation
* No need to load or compute SentenceTransformer models at runtime

## 🧾 Example Output

You’ll see 6 arrows, each representing a sentence like:

```
I like pizza
The oven is very hot
She loves climbing rocks
...
```

And similarity score annotations like:

```
cosine = 0.41
```

## 📁 Files

* `embeddings.py`: Manim animation script
* `README.md`: You are here

## 🧩 To Extend

* Animate angles using `Angle()` in Manim
* Import sentence embeddings and do PCA live
* Add fade-in comparisons or a slider over time

---

MIT License – Use and modify freely!
