# Gallery Evaluator Plus (Python)

A Python 3 version of the **Gallery Evaluator Plus** starter project for experimenting with gallery-layout evaluation and simple layout-generation algorithms.

## Features

- Loads 20 paintings from YAML-like data
- Loads 10 predefined layouts from YAML-like data
- Evaluates layouts using:
  - fit score
  - spacing score
  - overlap penalty
  - theme coherence
  - period coherence
  - lighting match
- Generates one random layout
- Generates one greedy layout
- Writes results to `output/scores.csv`

## Project Structure

```text
gallery-evaluator-plus-python/
├── README.md
├── run.py
├── data/
│   ├── paintings.yaml
│   └── layouts.yaml
├── gallery/
│   ├── __init__.py
│   ├── models.py
│   ├── parser.py
│   ├── evaluator.py
│   ├── generators.py
│   └── csv_writer.py
└── output/
```

## Requirements

- Python 3.9+

No external packages are required.

## Run

```bash
python3 run.py
```

The program will:

1. Load paintings from `data/paintings.yaml`
2. Load layouts from `data/layouts.yaml`
3. Evaluate all predefined layouts
4. Generate one random layout
5. Generate one greedy layout
6. Export results to `output/scores.csv`

## Notes on YAML

This project uses a **small custom parser** for a restricted YAML subset, matching the original C++ version.
It is intentionally simple and expects the structure used in the included data files.

## License

Provided as a teaching and experimentation starter project.
