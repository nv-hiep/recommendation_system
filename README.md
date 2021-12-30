# Hoola_RecommendationSystem
Course Recommender with Python, Pandas, Cosine Similarity, ngrok, Streamlit and colab.

##### 1. Recommendation_System_DataAnalysis_R.ipynb
Data Wrangling / Data Cleaning with R. A full exploratory data analysis of Courses.

##### 2. Recommendation_System_Model.ipynb
Build a model (Cosine Similarity Matrix) for the Recommendation System.

##### 3. app.ipynb
Build a webapp of the Recommendation System using ngrok, Streamlit and Colab (including the details for connecting Colab and Streamlit via ngrok).

Refer to /images for some images of examples.


![fig1](https://user-images.githubusercontent.com/13595525/147733311-ce99bf8f-5af7-492c-85f9-5cc48e26e2e6.jpg)

![fig2](https://user-images.githubusercontent.com/13595525/147733318-c66881af-7dfd-4035-91d5-c0fd196cbd58.jpg)

![fig3](https://user-images.githubusercontent.com/13595525/147733327-b37aa2b5-a6d2-482e-8d23-7a26876c3699.jpg)

![fig4](https://user-images.githubusercontent.com/13595525/147733331-380724d4-63dc-4715-bd6a-d7b6da5086ea.jpg)

![fig5](https://user-images.githubusercontent.com/13595525/147733338-fbef3b53-e3d7-4a88-89a7-4a48b7d31ac6.jpg)

![fig6](https://user-images.githubusercontent.com/13595525/147733347-c28e3489-ad4b-426d-8334-5f7ef1de6586.jpg)

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
