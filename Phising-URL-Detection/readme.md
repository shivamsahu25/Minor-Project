

## Phishing URL Detection
![image](images/Screenshot%202025-05-18%20145211.png)
---
![image](images/Screenshot%202025-05-18%20145245.png)
---
![image](images/Screenshot%202025-05-18%20145328.png)

## Installation


### 1. **Clone the Repository**

```bash
git clone https://github.com/shivamsahu25/Minor-Project.git
cd Minor-Project 
```

---

### 2. **Check Python Version Requirements**

* Look inside `requirements.txt`, `README.md` for the supported Python version.
* If not mentioned, Python 3.8–3.10 is usually safe for most older ML/Flask projects.

---

### 3. **Create a Virtual Environment**

#### Ubuntu/Linux/macOS:

```bash
sudo apt update && sudo apt install python3.8 python3.8-venv python3.8-dev build-essential -y
python3.8 -m venv venv
source venv/bin/activate
```

#### Windows:

```cmd
python -m venv venv
venv\Scripts\activate
```

---

### 4. **Install Project Dependencies**

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

🔁 **If `requirements.txt` fails due to version issues**:

Install major packages manually:

```bash
pip install numpy pandas flask
# Then install others
pip install -r requirements.txt --no-deps
```

---

### 5. **Run the Project**

Check if there's an entry point file like `app.py`, `main.py`, or a Flask app.
Usually:

```bash
python app.py
```

Or, for Flask:

```bash
export FLASK_APP=app.py  # use `set` instead of `export` on Windows
flask run
```

---

### 6. **Access the Web App**

* Open browser and go to:

  ```
  http://127.0.0.1:5000
  ```

---
## Result

Accuracy of various model used for URL detection
<br>

<br>

||ML Model|	Accuracy|  	f1_score|	Recall|	Precision|
|---|---|---|---|---|---|
0|	Gradient Boosting Classifier|	0.974|	0.977|	0.994|	0.986|
1|	CatBoost Classifier|	        0.972|	0.975|	0.994|	0.989|
2|	XGBoost Classifier| 	        0.969|	0.973|	0.993|	0.984|
3|	Multi-layer Perceptron|	        0.969|	0.973|	0.995|	0.981|
4|	Random Forest|	                0.967|	0.971|	0.993|	0.990|
5|	Support Vector Machine|	        0.964|	0.968|	0.980|	0.965|
6|	Decision Tree|      	        0.960|	0.964|	0.991|	0.993|
7|	K-Nearest Neighbors|        	0.956|	0.961|	0.991|	0.989|
8|	Logistic Regression|        	0.934|	0.941|	0.943|	0.927|
9|	Naive Bayes Classifier|     	0.605|	0.454|	0.292|	0.997|
---

### 7. **Troubleshooting Tips**

| Problem                          | Solution                                                     |
| -------------------------------- | ------------------------------------------------------------ |
| `numpy` / `pandas` install fails | Run: `sudo apt install python3-dev build-essential`          |
| Flask shows "Module not found"   | Run: `pip install flask`                                     |
| Using Python 3.12 or higher               | Downgrade to Python 3.8 or 3.10 for compatibility            |

---

### Optional: Use `conda` if pip fails a lot (especially on Windows)

```bash
conda create -n myenv python=3.8
conda activate myenv
conda install numpy pandas flask
pip install -r requirements.txt --no-deps
```

---
