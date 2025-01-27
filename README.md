<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>
    <header>
        <h1>Customer Churn Prediction Streamlit App</h1>
    </header>

  <section>
        <h2>Overview</h2>
        <p>This repository contains a Streamlit app that predicts whether a customer is likely to churn (leave a service) based on their profile data. The model is a machine learning model built using TensorFlow and Keras, and it is deployed using Streamlit to make predictions in real-time. The app takes customer details such as credit score, geography, gender, and other features to predict the likelihood of churn.</p>
    </section>

  <section>
        <h2>Features</h2>
        <ul>
            <li><strong>User Input</strong>: The user inputs customer information such as geography, gender, age, balance, and more.</li>
            <li><strong>Prediction Output</strong>: The app returns a probability of whether the customer will churn or not.</li>
            <li><strong>Data Preprocessing</strong>: The app handles one-hot encoding for categorical variables, scaling numerical features, and transforming the inputs into a format compatible with the trained model.</li>
        </ul>
    </section>

  <section>
        <h2>Technologies Used</h2>
        <ul>
            <li><strong>Python</strong>: The primary programming language for the app and model.</li>
            <li><strong>TensorFlow/Keras</strong>: Used for building and loading the machine learning model.</li>
            <li><strong>Streamlit</strong>: For building the interactive user interface.</li>
            <li><strong>Pandas</strong>: For handling data manipulation.</li>
            <li><strong>Scikit-learn</strong>: For preprocessing the data (scaling and encoding).</li>
            <li><strong>Pickle</strong>: For saving and loading encoders and scaler objects.</li>
            <li><strong>NumPy</strong>: For numerical operations.</li>
        </ul>
    </section>

  <section>
        <h2>Installation</h2>
        <p>To run the Streamlit app locally, follow the steps below:</p>
        <ol>
            <li><strong>Clone the repository</strong>
                <pre><code>git clone https://github.com/yourusername/customer-churn-prediction.git
cd customer-churn-prediction</code></pre>
            </li>
            <li><strong>Create a virtual environment</strong> (optional but recommended)
                <pre><code>python -m venv venv</code></pre>
            </li>
            <li><strong>Install dependencies</strong>
                <pre><code>pip install -r requirements.txt</code></pre>
            </li>
            <li><strong>Run the Streamlit app</strong>
                <pre><code>streamlit run app.py</code></pre>
                The app will be available in your browser at <a href="http://localhost:8501">http://localhost:8501</a>.
            </li>
        </ol>
    </section>

  <section>
        <h2>How the Model Works</h2>
        <h3>1. Data Preprocessing</h3>
        <p>Before feeding the data to the machine learning model, we preprocess it by:
            <ul>
                <li>Encoding categorical features like <strong>Geography</strong> and <strong>Gender</strong>.</li>
                <li>Scaling numerical features such as <strong>Balance</strong>, <strong>CreditScore</strong>, and <strong>EstimatedSalary</strong>.</li>
                <li>Combining all features into a data frame ready for prediction.</li>
            </ul>
        </p>
        <h3>2. Model Prediction</h3>
        <p>The user input is passed through preprocessing steps, including encoding and scaling, and then passed into the trained machine learning model for prediction. The model predicts the likelihood of the customer churning, and this probability is displayed to the user.</p>
        <h3>3. Result Interpretation</h3>
        <p>If the probability is greater than 0.5, the customer is likely to churn. If the probability is less than or equal to 0.5, the customer is not likely to churn.</p>
    </section>

  <section>
        <h2>Data Story: Customer Churn Prediction</h2>
        <h3>Problem Statement</h3>
        <p>In this project, we aim to predict the likelihood of a customer churning based on several features such as:</p>
        <ul>
            <li><strong>CreditScore</strong>: A numerical score that reflects the creditworthiness of the customer.</li>
            <li><strong>Geography</strong>: The customer's region (e.g., France, Germany, Spain).</li>
            <li><strong>Gender</strong>: The gender of the customer (Male/Female).</li>
            <li><strong>Age</strong>: The age of the customer.</li>
            <li><strong>Balance</strong>: The account balance of the customer.</li>
            <li><strong>Tenure</strong>: How long the customer has been with the company (in years).</li>
            <li><strong>NumOfProducts</strong>: Number of products the customer has with the company.</li>
            <li><strong>HasCrCard</strong>: Whether the customer has a credit card (1 or 0).</li>
            <li><strong>IsActiveMember</strong>: Whether the customer is an active member of the company (1 or 0).</li>
            <li><strong>EstimatedSalary</strong>: The salary of the customer.</li>
        </ul>
        <h3>Approach</h3>
        <p>1. Data Preprocessing: We preprocess the data by encoding categorical variables and scaling numerical variables.</p>
        <p>2. Model: A <strong>TensorFlow</strong> neural network model is used to predict churn based on the input data.</p>
        <p>3. Prediction: The trained model outputs a probability representing the likelihood of the customer churning.</p>
        <h3>Insights</h3>
        <p>By deploying this churn prediction model, businesses can:</p>
        <ul>
            <li><strong>Identify high-risk customers</strong>: Those likely to churn, allowing the company to focus retention efforts on them.</li>
            <li><strong>Analyze churn trends</strong>: Understand which customer demographics are most likely to churn.</li>
            <li><strong>Personalize retention strategies</strong>: Offer targeted promotions or incentives to high-risk customers.</li>
        </ul>
        <h3>Next Steps</h3>
        <ul>
            <li><strong>Model Improvement</strong>: Continuously retrain the model with updated data to improve its accuracy.</li>
            <li><strong>Feature Expansion</strong>: Include additional customer behavior data, such as transaction history or customer service interactions, to improve prediction quality.</li>
            <li><strong>Deployment</strong>: Deploy the model into production environments where businesses can use it for real-time predictions.</li>
        </ul>
    </section>

  <footer>
        <h2>License</h2>
        <p>This project is licensed under the MIT License - see the <a href="LICENSE">LICENSE</a> file for details.</p>
    </footer>
</body>
</html>
