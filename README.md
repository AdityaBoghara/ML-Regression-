# 🔥 FWI (Fire Weather Index) Prediction Web App

This project is a machine learning–powered web application built using **Flask** that predicts the **Fire Weather Index (FWI)** based on various meteorological parameters. It uses a pre-trained **Ridge Regression** model to process inputs such as temperature, humidity, wind speed, and more.

---

## 🚀 Features

- 📊 **ML Model**: Ridge Regression with Scikit-learn
- 🧪 **Inputs**: 9 real-time features including temperature, humidity, and wind speed
- 💡 **Standardized Inputs** using `StandardScaler`
- 🖥️ **User Interface**: Beautiful, responsive HTML form
- 🔄 **Dynamic Prediction** rendered on the same page
- ⚙️ **Runs on Flask** (localhost or public IP)

---

## 🧠 Prediction Parameters

| Feature     | Description                 |
| ----------- | --------------------------- |
| Temperature | Ambient temperature (°C)    |
| RH          | Relative Humidity (%)       |
| Ws          | Wind Speed                  |
| Rain        | Rainfall (mm)               |
| FFMC        | Fine Fuel Moisture Code     |
| DMC         | Duff Moisture Code          |
| ISI         | Initial Spread Index        |
| Classes     | Fire danger class           |
| Region      | Encoded regional identifier |

---

## 📁 Project Structure

```bash
.
├── app.py                    # Flask application logic
├── models/
│   ├── ridge.pkl             # Trained Ridge Regression model
│   └── scaler.pkl            # StandardScaler object
├── templates/
│   ├── index.html            # Input form UI
│   └── home.html             # Result display UI
├── README.md
├── requirements.txt         # Python package requirements
```

## Project Link: http://ml-regression-env.eba-t42jwn2p.us-east-1.elasticbeanstalk.com/

---

## ▶️ How to Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/fwi-prediction-app.git
cd fwi-prediction-app
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Flask app

```bash
python app.py
```

Or, if you're using `application` as the entry object:

```bash
python -m flask run --host=0.0.0.0 --port=5001
```

The app will be available at [http://localhost:5001](http://localhost:5001)

---

## 🔍 How It Works

1. **User inputs 9 weather-related features** in the form.
2. Flask **receives POST request** and extracts values using `request.form.get`.
3. Input is **scaled using StandardScaler** loaded from `scaler.pkl`.
4. Scaled input is **fed into the Ridge Regression model** (`ridge.pkl`).
5. **Prediction result is rendered** on `home.html`.

---

## 📊 Dataset Source

This project uses the **Algerian Forest Fires Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset).

- **Dataset Name:** Algerian Forest Fires
- **Source:** UCI Machine Learning Repository
- **URL:** [https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset)
- **Description:** The dataset contains meteorological data for forest fire prediction collected from two regions in Algeria between June and September 2012.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Acknowledgements

- [Scikit-learn](https://scikit-learn.org/)
- [Flask](https://flask.palletsprojects.com/)
- [Algerian Forest Fires Dataset – UCI](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset)

---

**Built with ❤️ using Flask, ML, and a passion for forest fire prediction**
