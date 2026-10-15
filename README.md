# Graduate Admission Prediction with Flask

A Python machine learning web application that loads a serialized regression model and displays an estimated admission percentage from applicant inputs.

**Stack:** Flask, scikit-learn, NumPy, HTML templates.

## Application flow

1. Enter GRE and TOEFL scores, university rating, statement-of-purpose rating, recommendation rating, CGPA, and research experience.
2. Flask converts the form values into the model's input feature order.
3. The saved model generates a prediction, which is displayed as a rounded percentage.

This is an educational model demonstration; its output is not an admissions decision or a validated probability.

## Run locally

```bash
git clone https://github.com/yashwanthp21/MLlinregHeroku.git
cd MLlinregHeroku
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

On Windows PowerShell, activate with `.venv\Scripts\Activate.ps1`.

Open http://127.0.0.1:5000 and submit the form. Run from the repository root so the app can locate `finalized_model.pickle`.

## Repository guide

| File or directory | Purpose |
| --- | --- |
| `app.py` | Form handling, model loading, and prediction |
| `finalized_model.pickle` | Serialized model used by the app |
| `templates/` | Input and results pages |
| `static/` | Frontend assets |
| `requirements.txt` | Pinned Python dependencies |
| `MLForCloudDeployment_Heroku.pdf` | Included deployment reference |

## Compatibility and deployment

Dependencies are pinned to older versions, including scikit-learn 0.21.3 and NumPy 1.17.4. They may not install on current Python releases, and the serialized model may require the original library versions. The commands above describe the intended startup flow; a compatible environment is required.

The included `Procfile` and `runtime.txt` are empty, so the repository does not currently provide complete Heroku deployment configuration. The app's direct entry point enables Flask debug mode and is intended for local development.

## Author

[Yashwanth Pulimi](https://github.com/yashwanthp21)
