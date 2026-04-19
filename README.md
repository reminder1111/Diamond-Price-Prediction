# Diamond Price Prediction

A Flask-based machine learning web app that predicts diamond prices from key physical and quality attributes such as carat, depth, table, dimensions, cut, color, and clarity.

## Deploy Link

- Deploy link: [https://diamond-price-prediction-t9mm.onrender.com](https://diamond-price-prediction-t9mm.onrender.com)
- GitHub repository: [reminder1111/Diamond-Price-Prediction](https://github.com/reminder1111/Diamond-Price-Prediction)

## Features

- Predicts diamond prices from a trained scikit-learn model
- Simple Flask UI with an input form for manual testing
- Saved preprocessing pipeline and model artifacts included in the repo
- Ready for local development and Render deployment

## Tech Stack

- Python
- Flask
- pandas
- numpy
- scikit-learn
- seaborn

## Project Structure

```text
.
|-- application.py
|-- artifacts/
|-- notebooks/
|-- src/
|   |-- components/
|   |-- pipelines/
|   |-- exception.py
|   |-- logger.py
|   `-- utils.py
|-- templates/
|-- requirements.txt
`-- render.yaml
```

## Input Features

The prediction form uses these fields:

- `carat`
- `depth`
- `table`
- `x`
- `y`
- `z`
- `cut`
- `color`
- `clarity`

## Run Locally

1. Clone the repository:

```bash
git clone https://github.com/reminder1111/Diamond-Price-Prediction.git
cd Diamond-Price-Prediction
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Start the app:

```bash
python application.py
```

5. Open in your browser:

```text
http://127.0.0.1:5000/predict
```

## Render Deployment

This repo includes a `render.yaml` blueprint, so Render can create the service directly from the repository.

1. Open the deploy link above.
2. Connect your GitHub account to Render if prompted.
3. Approve the new web service.
4. Render will install dependencies from `requirements.txt` and start the app with `gunicorn application:app`.

After the first deployment, Render will generate your public live app URL.

## Example Prediction Flow

1. Open `/predict`
2. Enter the diamond attributes
3. Submit the form
4. View the predicted price on the page

## Notes

- The repository includes trained model artifacts inside `artifacts/`
- The app now reads the deployment port from the `PORT` environment variable, which is required by most cloud platforms
- Dependency versions are pinned to the versions verified in the local environment
