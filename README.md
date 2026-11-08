# Student Task Prioritizer

Streamlit web app that helps students decide what to do first. An ML model predicts a
**High / Medium / Low** priority for every study task from four features:
difficulty (1–5), days left, estimated hours, importance (1–5).

## Pages
Dashboard · My Tasks · Calendar · Study Schedule · AI Assistant · Analytics · Settings

## Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
```

## Project structure
```
app.py                                 # UI (module 3)
task_manager.py                        # task management (module 4)
ml_model.py, model.joblib              # ML model (module 2)
student_task_prioritizer_dataset.csv   # dataset (module 1)
ml_outputs/                            # metrics, confusion matrix
tests/                                 # tests (module 5)
requirements.txt, README.md            # module 6
```

## ML integration
`app.py` calls `predict_priority(difficulty, days_left, estimated_hours, importance)`.
Out-of-range input raises `ValueError`; the app catches it and falls back to a simple
weighted formula. The sidebar shows which mode is active.

## ML model
<!-- paste sections 1–4 from ML_PART.md: data, model, metrics (accuracy 0.70), limitations -->

## Deploy (Streamlit Community Cloud)
Push to GitHub, create an app pointing at `app.py`. `requirements.txt` must be in the repo root.

## Team
<!-- names and modules -->
