# 📊 Sentence Embedding Similarity Visualizer (Manim)

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
