<h1 align="center">🔍 Mini Search Engine</h1>

<p align="center">
  <em>Complete search engine with web crawler, inverted index, TF-IDF ranking, and PageRank</em>
</p>

<p align="center">
  <a href="https://knight-rule.github.io/search-engine"><img src="https://img.shields.io/badge/demo-live-brightgreen" alt="Live Demo"></a>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black" alt="JavaScript">
</p>

---

## ✨ Features

- [x] **Web Crawler** — Crawl and index web pages automatically
- [x] **Inverted Index** — Fast full-text search with word-to-document mapping
- [x] **TF-IDF Scoring** — Rank results by term frequency and document importance
- [x] **PageRank Algorithm** — Authority-based ranking using link analysis
- [x] **SVG Graph Visualization** — Interactive network graph of crawled pages
- [x] **Search Results Ranking** — Combine TF-IDF and PageRank for best results
- [x] **Analytics Dashboard** — View crawl stats, index size, and query metrics
- [x] **Demo Mode** — Pre-crawled dataset for instant exploration
- [x] **Zero Dependencies** — Pure vanilla JavaScript

## 📸 Screenshot

![screenshot](screenshot.png)

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Search interface and visualization |
| CSS3 | Dashboard styling and graph rendering |
| JavaScript | Crawler, indexer, TF-IDF, PageRank |

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/knight-rule/search-engine.git

# Navigate to the project
cd search-engine

# Open in browser
open index.html
```

No build step or dependencies required — just open the HTML file!

## 📖 Usage

1. **Crawl Pages** — Enter URLs or use demo mode to crawl sample sites
2. **Search** — Type a query and see ranked results instantly
3. **View Graph** — Click "Graph" to see the link structure as an SVG network
4. **Check Analytics** — View crawl stats, index size, and query performance
5. **Compare Rankings** — Toggle between TF-IDF only and combined PageRank results

```javascript
// Search API
const results = engine.search("machine learning", {
  algorithm: "tfidf_pagerank",  // or "tfidf" or "pagerank"
  limit: 10
});

// Results include:
// - title, url, snippet
// - tfidfScore, pagerankScore, combinedScore
// - matchedTerms[]
```

## ⚙️ How It Works

```
┌─────────────┐    ┌──────────────┐    ┌─────────────┐
│  Web Crawler│───▶│  Document    │───▶│  Inverted   │
│  (BFS/DFS)  │    │  Store       │    │  Index      │
└─────────────┘    └──────────────┘    └──────┬──────┘
                                              │
┌─────────────┐    ┌──────────────┐    ┌──────▼──────┐
│  Ranked     │◀───│  TF-IDF +    │◀───│  Query      │
│  Results    │    │  PageRank    │    │  Processor  │
└─────────────┘    └──────────────┘    └─────────────┘
```

The search engine mirrors real search architecture:
1. **Crawling** — BFS spider fetches pages, extracts links and content
2. **Indexing** — Documents are tokenized, stemmed, and added to inverted index
3. **TF-IDF** — Term frequency × inverse document frequency scores relevance
4. **PageRank** — Iterative algorithm computes authority from link structure
5. **Ranking** — Combined score determines final result ordering

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Prashant** — [@knight-rule](https://github.com/knight-rule)

<p align="center">
  Made with ❤️ for search enthusiasts
</p>
