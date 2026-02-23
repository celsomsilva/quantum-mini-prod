# quantum-mini-prod


A minimal, production-style **Quantum Machine Learning API**, extending my own mlops-mini-prod MLOps architecture using PennyLane.

This project demonstrates how Quantum Machine Learning models can be trained, packaged, and served in a real production-like environment.

The goal is not quantum advantage.

The goal is production readiness.

---
---

## Project Status

This project is under active maintenance, with ongoing improvements to documentation, structure, and models.


---
---

## Purpose

Most Quantum ML examples stop at notebooks.

This project focuses on what real-world ML systems require:

- reproducible training
- saved model artifacts
- inference API
- containerization-ready
- testable endpoints
- deploy-ready architecture

This repository applies the same production principles used in classical ML to Quantum ML.

---

## Architecture

Workflow:

1. Train quantum model (PennyLane)

2. Save model artifact

3. API loads model

4. Serve predictions via FastAPI

5. Ready for Docker and cloud deployment

---

## Tech stack

- Python
- FastAPI
- PennyLane
- NumPy
- scikit-learn
- pytest

---

## Project Structure

quantum-mini-prod/

  src/
   quantum_api/
        __init__.py
        api.py              #FastAPI application (/health, /predict)
        train.py            #training script that generates the model     
        predict.py          #inference logic
  
  models/                  #saved artifacts (quantum_model.joblib + metadata.json)
  
  tests/                   #automated tests using pytest
  
  Dockerfile              #application container
  compose.yaml            #local docker execution
  .github/workflows/ci.yml       # CI pipeline (GitHub Actions)
  Makefile                #shortcut commands
  requirements.txt       #dependencies
  pyproject.toml         # package configuration (src-layout)
  LICENSE
  README.md
  .gitignore


## Relationship with mlops-mini-prod

This repository builds upon **mlops-mini-prod**, my production-style MLOps template, and extends it into Quantum Machine Learning.

Think of this project as its quantum counterpart.

---

## Author

This project was developed by an engineer and data scientist with a background in:

* Postgraduate degree in **Data Science and Analytics (USP)**
* Bachelor's degree in **Computer Engineering (UERJ)**
* Special interest in statistical models, interpretability, and applied AI
* Strong interest in algorithmic reasoning, correctness, and performance evaluation

---

## Contact

* [LinkedIn](https://linkedin.com/in/celso-m-silva)
* Or open an [issue](https://github.com/celsomsilva/quantum-mini-prod/issues)
