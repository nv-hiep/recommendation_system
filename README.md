# Hoola_RecommendationSystem
Course Recommender with Python, Pandas, Cosine Similarity, ngrok, Streamlit and colab.

##### 1. Recommendation_System_DataAnalysis_R.ipynb
Data Wrangling / Data Cleaning with R. A full exploratory data analysis of Courses.

##### 2. Recommendation_System_Model.ipynb
Build a model (Cosine Similarity Matrix) for the Recommendation System.

##### 3. app.ipynb
Build a webapp of the Recommendation System using ngrok, Streamlit and Colab (including the deatils for connecting Colab and Streamlit via ngrok). 


## Prerequisite
- Create an account on Ngrok (https://ngrok.com/). ngrok provides a real-time web UI where you can introspect all HTTP traffic running over your tunnels.

- Get Authentication Token (https://dashboard.ngrok.com/get-started/your-authtoken).

- The Auth token is in this format: ./ngrok authtoken xxxxxxxxxxxxxxxxxxxxxxxxxx

- Use the auth token to connect your Ngrok account.

## Run Streamlit from Colab using ngrok
- Connect to ngrok: !ngrok authtoken xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
- Run the processes in the background: !streamlit run --server.port 80 app.py &>/dev/null&
- Check the process: ! pgrep streamlit
- Setup a tunnel using streamlit port 80: pub_url = ngrok.connect(port='80')
- A public URL (https://<abcxyz>.ngrok.io ) will be created, and your app will be running on it.

## Terminate the App
!pgrep streamlit
  
! kill <id>

ngrok.kill() # Disconnect ngrok
