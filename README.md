<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Linear Regression Using Machine Learning</title>
</head>

<body>

<h1>📊 Simple Linear Regression Using Machine Learning</h1>

<p>
    A beginner-friendly Machine Learning project that demonstrates how to build,
    evaluate, save, and deploy a <strong>Simple Linear Regression model</strong>
    using Python, Scikit-learn, Flask, and Render.
</p>

<h2>🎯 Project Objective</h2>

<p>
    The main objective of this project is to understand the complete
    Machine Learning lifecycle using a simple Linear Regression problem.
</p>

<h2>🚀 Project Overview</h2>

<p>
    <strong>Simple Linear Regression using Machine Learning</strong> is a
    supervised Machine Learning project where a model learns the relationship
    between:
</p>

<ul>
    <li><strong>Independent Variable (X):</strong> Years of Experience</li>
    <li><strong>Dependent Variable (Y):</strong> Salary</li>
</ul>

<h2>🔄 Complete Workflow</h2>

<pre>
Data Collection
      ↓
Data Understanding
      ↓
Exploratory Data Analysis
      ↓
Train-Test Split
      ↓
Linear Regression Model
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Prediction
      ↓
Model Serialization
      ↓
Flask Web Application
      ↓
Gunicorn
      ↓
Render Cloud Deployment
      ↓
Public Web Application
</pre>

<h2>📁 Dataset</h2>

<p>The dataset used in this project is:</p>

<pre><code>salary.csv</code></pre>

<p>
    The dataset contains <strong>30 rows</strong> and two important columns.
</p>

<table border="1">
    <thead>
        <tr>
            <th>Column</th>
            <th>Description</th>
            <th>Type</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Years of Experience</td>
            <td>Number of years of professional experience</td>
            <td>Numerical</td>
        </tr>
        <tr>
            <td>Salary</td>
            <td>Salary corresponding to the experience</td>
            <td>Numerical</td>
        </tr>
    </tbody>
</table>

<h2>📈 Why Linear Regression?</h2>

<p>
    Linear Regression is one of the simplest and most important supervised
    Machine Learning algorithms.
</p>

<p>
    The basic equation of Simple Linear Regression is:
</p>

<pre><code>y = mx + c</code></pre>

<p>Where:</p>

<ul>
    <li><code>y</code> = predicted salary</li>
    <li><code>x</code> = years of experience</li>
    <li><code>m</code> = slope/coefficient</li>
    <li><code>c</code> = intercept</li>
</ul>

<h2>✂️ Train-Test Split</h2>

<p>The dataset contains:</p>

<pre>
Total Records = 30

Training Data = 24 rows
Testing Data  = 6 rows
</pre>

<p>
    The training data is used to teach the Machine Learning model.
    The testing data is kept separate so that we can evaluate how well
    the trained model performs on previously unseen data.
</p>

<pre><code>
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
</code></pre>

<h2>🤖 Building the Linear Regression Model</h2>

<pre><code>
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, y_train)
</code></pre>

<p>
    At this stage, the algorithm learns the relationship between
    Years of Experience and Salary.
</p>

<h2>🧮 Linear Regression Equation</h2>

<pre><code>y = mx + c</code></pre>

<p>
    The model can therefore be represented as:
</p>

<pre><code>
Predicted Salary = m × Years of Experience + c
</code></pre>

<h2>📊 Model Performance</h2>

<h3>Training Performance</h3>

<pre>
Training Data = 24 rows
Training Performance ≈ 96%
Training Loss ≈ 5,000
</pre>

<h3>Testing Performance</h3>

<pre>
Testing Data = 6 rows
Testing Performance ≈ 90%
Testing Loss ≈ 2,000
</pre>

<h2>📌 Important Note About Accuracy in Regression</h2>

<p>
    Linear Regression is a <strong>regression problem</strong>, where the
    target is a continuous numerical value such as salary.
</p>

<p>Regression-specific evaluation metrics include:</p>

<ul>
    <li>R² Score</li>
    <li>Mean Absolute Error (MAE)</li>
    <li>Mean Squared Error (MSE)</li>
    <li>Root Mean Squared Error (RMSE)</li>
</ul>

<h2>📉 Loss</h2>

<p>A common regression loss is:</p>

<pre><code>Mean Squared Error (MSE)</code></pre>

<pre><code>
MSE = (1/n) Σ(y_actual - y_predicted)²
</code></pre>

<h2>🔮 Making Predictions</h2>

<p>
    After finalizing the model, new data can be provided to predict salary
    for previously unseen experience values.
</p>

<pre><code>
prediction = model.predict([[12]])

print(prediction)
</code></pre>

<p>Another example:</p>

<pre><code>
prediction = model.predict([[15]])

print(prediction)
</code></pre>

<h2>💾 Saving the Machine Learning Model</h2>

<p>
    The trained model was saved as a <strong>pickle file</strong>.
</p>

<pre><code>
import pickle

with open("model.pkl", "wb") as file:
    pickle.dump(model, file)
</code></pre>

<p>The saved model can later be loaded using:</p>

<pre><code>
with open("model.pkl", "rb") as file:
    model = pickle.load(file)
</code></pre>

<h2>🐍 Python Virtual Environment</h2>

<p>
    A virtual environment provides an isolated Python environment
    for a particular project.
</p>

<h3>Benefits</h3>

<ol>
    <li>Dependency Isolation</li>
    <li>Avoid Version Conflicts</li>
    <li>Reproducibility</li>
    <li>Cleaner Development Environment</li>
</ol>

<h2>🛠️ Creating a Virtual Environment</h2>

<pre><code>python -m venv venv</code></pre>

<h2>📦 requirements.txt</h2>

<pre><code>
Flask
numpy
pandas
scikit-learn
gunicorn
</code></pre>

<p>Install dependencies using:</p>

<pre><code>pip install -r requirements.txt</code></pre>

<h2>🌐 Flask Web Application</h2>

<p>
    Flask was used to convert the Machine Learning model into a web application.
</p>

<pre>
Frontend
   ↓
Flask Backend
   ↓
Machine Learning Model
   ↓
Prediction
   ↓
Frontend
</pre>

<h2>🎨 Frontend — index.html</h2>

<p>
    The frontend is written using HTML and is placed inside the Flask
    <code>templates</code> directory.
</p>

<pre>
templates/
└── index.html
</pre>

<h2>⚙️ Backend — app.py</h2>

<p>The <code>app.py</code> file is responsible for:</p>

<ol>
    <li>Starting the Flask application.</li>
    <li>Loading the trained Machine Learning model.</li>
    <li>Receiving user input.</li>
    <li>Passing the input to the model.</li>
    <li>Generating the prediction.</li>
    <li>Returning the result to the frontend.</li>
</ol>

<h2>🖥️ Running the Application Locally</h2>

<pre><code>python app.py</code></pre>

<p>The Flask server provides a local address similar to:</p>

<pre><code>http://127.0.0.1:5000/</code></pre>

<h2>📂 Project Structure</h2>

<pre>
Simple-Linear-Regression/
│
├── app.py
├── model.pkl
├── salary.csv
├── requirements.txt
├── Procfile
├── README.md
│
├── templates/
│   └── index.html
│
└── venv/
</pre>

<h2>☁️ Deployment Using Render</h2>

<p>
    The application can be deployed using <strong>Render Cloud</strong>.
</p>

<pre>
Local Project
      ↓
GitHub Repository
      ↓
Render
      ↓
Build Environment
      ↓
Install Dependencies
      ↓
Start Flask Application
      ↓
Public URL
</pre>

<h2>📄 Procfile</h2>

<pre><code>web: gunicorn app:app</code></pre>

<h2>🦄 Gunicorn</h2>

<p>
    Gunicorn is a production WSGI server commonly used when deploying
    Flask applications.
</p>

<pre><code>gunicorn app:app</code></pre>

<h2>🌍 Making the Application Public</h2>

<p>
    After successful deployment, Render provides a public URL.
</p>

<p>
    <a href="https://afternoon-slr-deployment.onrender.com">
        View Deployed Application
    </a>
</p>

<h2>🧰 Technologies Used</h2>

<table border="1">
    <thead>
        <tr>
            <th>Technology</th>
            <th>Purpose</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Python</td><td>Programming Language</td></tr>
        <tr><td>Pandas</td><td>Data Manipulation</td></tr>
        <tr><td>NumPy</td><td>Numerical Computing</td></tr>
        <tr><td>Matplotlib</td><td>Data Visualization</td></tr>
        <tr><td>Scikit-learn</td><td>Machine Learning</td></tr>
        <tr><td>Linear Regression</td><td>Prediction Algorithm</td></tr>
        <tr><td>Pickle</td><td>Model Serialization</td></tr>
        <tr><td>Flask</td><td>Web Application Framework</td></tr>
        <tr><td>HTML</td><td>Frontend</td></tr>
        <tr><td>Gunicorn</td><td>Production WSGI Server</td></tr>
        <tr><td>Git/GitHub</td><td>Version Control</td></tr>
        <tr><td>Render</td><td>Cloud Deployment</td></tr>
        <tr><td>PyCharm</td><td>Development Environment</td></tr>
    </tbody>
</table>

<h2>💡 Key Concepts Learned</h2>

<h3>Machine Learning</h3>
<ul>
    <li>Supervised Learning</li>
    <li>Regression</li>
    <li>Simple Linear Regression</li>
    <li>Independent and dependent variables</li>
    <li>Train-Test Split</li>
    <li>Model Training</li>
    <li>Model Evaluation</li>
    <li>Prediction</li>
</ul>

<h3>Data Science</h3>
<ul>
    <li>Dataset understanding</li>
    <li>Exploratory Data Analysis</li>
    <li>Data visualization</li>
    <li>Actual vs predicted values</li>
</ul>

<h3>Web Development</h3>
<ul>
    <li>Flask</li>
    <li>HTML</li>
    <li>Frontend-backend integration</li>
    <li>HTTP request/response flow</li>
</ul>

<h3>Deployment</h3>
<ul>
    <li>GitHub</li>
    <li>Requirements management</li>
    <li>Gunicorn</li>
    <li>Procfile</li>
    <li>Render Cloud</li>
    <li>Production deployment</li>
</ul>

<h2>📌 Future Improvements</h2>

<ul>
    <li>Multiple Linear Regression</li>
    <li>Additional salary-related features</li>
    <li>Better data preprocessing</li>
    <li>Cross-validation</li>
    <li>MAE, MSE and RMSE comparison</li>
    <li>R² score evaluation</li>
    <li>Model comparison</li>
    <li>Better frontend design</li>
    <li>Input validation</li>
    <li>Error handling</li>
    <li>REST API endpoint</li>
    <li>Docker deployment</li>
    <li>CI/CD pipeline</li>
    <li>Database integration</li>
    <li>Cloud monitoring</li>
    <li>Advanced Machine Learning algorithms</li>
</ul>

<h2>👨‍💻 Author</h2>

<p><strong>Kamal</strong></p>

<p>Founder &amp; Managing Director Vihara Tech</p>

<ul>
    <li>Data Analytics</li>
    <li>Data Science</li>
    <li>Machine Learning</li>
    <li>Generative AI</li>
    <li>Large Language Models</li>
    <li>Agentic AI</li>
</ul>

<h2>🔗 Project Links</h2>

<h3>🌐 Deployment</h3>

<p>
    <a href="">
        Render Deployment
    </a>
</p>

<h3>💼 LinkedIn</h3>

<p>
    <a href="">
        LinkedIn Profile
    </a>
</p>



<h2>⭐ Conclusion</h2>

<p>
    The <strong>Simple Linear Regression Using Machine Learning</strong>
    project demonstrates how a basic Machine Learning algorithm can be taken
    from a raw dataset to a publicly accessible cloud application.
</p>

<pre>
Dataset
   ↓
EDA
   ↓
Train-Test Split
   ↓
Linear Regression
   ↓
Model Evaluation
   ↓
Prediction
   ↓
Pickle Model
   ↓
Flask Application
   ↓
Gunicorn
   ↓
Render Cloud
   ↓
Public Machine Learning Application
</pre>

<h2>🚀 Machine Learning → Web Application → Cloud Deployment</h2>

<p>
    <strong>Build it. Train it. Test it. Deploy it. Share it.</strong>
</p>

</body>
</html>
