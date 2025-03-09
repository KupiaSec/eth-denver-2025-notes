# ETHDenver-2025 Notes

Welcome to the ETHDenver-2025 Notes collection!
This site contains summaries and key insights from presentations at ETHDenver-2025 Notes.

We used google/gemini-flash-1.5-8b to generate summaries from the video transcripts.
All copyrights belong to the presenters; we simply wanted to create a quick way to catch up on all the talks.

## Getting Started

### Prerequisites

- Python 3.x
- pip

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/KupiaSec/eth-denver-2025-notes.git
   cd eth-denver-2025-notes
   ```

2. Create a virtual environment:
   ```bash
   python -m virtualenv venv
   ```

3. Activate the virtual environment:
   ```bash
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

4. Install MkDocs and required plugins:
   ```bash
   pip install mkdocs mkdocs-material
   ```
   Refer to [MkDocs documentation](https://www.mkdocs.org/user-guide/installation/) for more details.

## Development

To run the documentation site locally:

```bash
mkdocs serve
```

This will start a development server at http://127.0.0.1:8000/

## Deployment

### GitHub Pages

To deploy to GitHub Pages:

```bash
mkdocs gh-deploy
```

This command builds the site and pushes it to the `gh-pages` branch of your repository.

## License

This repository is only for educational purposes. All the rights belong to the original presenters.