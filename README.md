<h1> <img src="https://raw.githubusercontent.com/shsarv/Cardio-Monitor/main/static/heartlogo.png" width="50px" /> Cardio-Monitor</h1>

**Ongoing Project**

Cardio Monotor is a web app that helps you to find out whether you are at a risk of developing a heart disease. **the model used for prediction has the accuracy of 92%.**

This is the course project of subject Big Data Analytics (BCSE0158). THe Core Project is available... [here](https://github.com/shsarv/Heart-Disease-Prediction). 

<h3> <img src="https://raw.githubusercontent.com/simple-icons/simple-icons/49314d89b6a54b2750a130e2b56d5da310aa6552/icons/abstract.svg" width="30px" /> Abstract -  </h3> 
Over the last few decades, heart disease is the most common cause of global death. So early detection of heart disease and continuous monitoring can reduce the mortality rate. The exponential growth of data from different sources such as wearable sensor devices used in Internet of Things health monitoring, streaming system and others have been generating an enormous amount of data on a continuous basis. The combination of streaming big data analytics and machine learning is a breakthrough technology that can have a significant impact in healthcare field especially early detection of heart disease. This technology can be more powerful and less expensive. To overcome this issue,realtime heart disease prediction system based on apache Spark/ real time input data which stand as a strong large scale distributed computing platform that can be used successfully for streaming data event against machine learning through in-memory computations. 

<h3> <img src="https://st.depositphotos.com/1008768/4671/i/950/depositphotos_46719249-stock-photo-demo-icon.jpg" width="30px" /> Demo </h3> 
will be attatched soon.

![]()

<h3> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/27/Flow_logo.svg/846px-Flow_logo.svg.png" width="30px" /> general working of this web application.</h3> 

![](https://raw.githubusercontent.com/shsarv/Cardio-Monitor/main/Input%20Data.png)


<h3>Technology Used. </h3> 
<code><img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-ar21.svg" width="120px" /></code>
<code><img src="https://www.vectorlogo.zone/logos/python/python-ar21.svg" width="120px" /></code>
<code><img src="https://www.vectorlogo.zone/logos/mongodb/mongodb-ar21.svg" width="120px" /></code>
<code><img src="https://raw.githubusercontent.com/scikit-learn/scikit-learn/main/doc/logos/scikit-learn-logo.png" width="120px" /></code>
<code><img src="https://raw.githubusercontent.com/rasbt/mlxtend/master/docs/sources/img/logo.png" width="120px" /></code>
<br>
<br>

<h3>Future Technology to be Used. </h3> 
<code><img src="https://miro.medium.com/max/1838/1*qgkjkj6BLVS1uD4mw_sTEg.png" width="120px" /></code>
<code><img src="https://bigdatapath.files.wordpress.com/2019/04/1-4.jpg?w=698" width="120px" /></code>
<code><img src="https://www.vectorlogo.zone/logos/mongodb/mongodb-ar21.svg" width="120px" /></code>
<code><img src="https://www.vectorlogo.zone/logos/deepl/deepl-ar21.svg" width="120px" /></code>
<br>
<br>


<h3>Local Setup</h3>

1. Clone the repo and create a virtual environment:
   ```
   git clone https://github.com/vikash2103/Cardio-Monitor.git
   cd Cardio-Monitor
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # macOS/Linux
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Configure MongoDB (see below), then run the app:
   ```
   python app.py
   ```
   Visit `http://127.0.0.1:5000` in your browser.

> **Note:** `requirements.txt` originally pinned 2021-era package versions (numpy 1.20, scikit-learn 0.24, Flask 1.1, ...) that no longer have installable wheels on current Python. It now pins modern, tested-compatible versions instead. `heartmodel.pkl` was retrained against the new scikit-learn, since a model pickled with the old version won't load under the new one.

<h3>MongoDB Configuration</h3>

The app reads its connection string from the `DATABASE_LINK` environment variable (loaded from a local `.env` file via `python-dotenv`) and stores prediction records in the `Heartpatientdatabase.Heart_Data` collection.

Create a `.env` file in the project root (it's git-ignored, so it stays local):
```
DATABASE_LINK=<your-mongodb-connection-string>
```

**Option A — Local MongoDB.** If you have MongoDB installed and running (default port), use:
```
DATABASE_LINK=mongodb://localhost:27017
```
No database or collection needs to be created up front — MongoDB creates `Heartpatientdatabase` and `Heart_Data` automatically on the first prediction saved.

**Option B — MongoDB Atlas (free tier).** If you don't have MongoDB installed locally:
1. Create a free account at [mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas) and create a free (M0) cluster.
2. Under **Database Access**, create a database user with a username/password.
3. Under **Network Access**, add your current IP address (or `0.0.0.0/0` for unrestricted access during local development).
4. Click **Connect** on your cluster → **Drivers**, and copy the connection string, e.g.:
   ```
   mongodb+srv://<username>:<password>@<cluster-url>/?retryWrites=true&w=majority
   ```
5. Paste it into `.env` as `DATABASE_LINK`, substituting your actual username and password.

<h3>License</h3> 
<img src="https://www.vectorlogo.zone/logos/mitedu/mitedu-ar21.svg" width="100px" />

 **Created By - Sarvesh Kumar Sharma**
