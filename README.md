# Song Similarity App(AI/ML)

# Images of the App :memo:
![Image 1](https://github.com/Neel-max-cpu/Aiml-project-Finding-similar-song/blob/main/public/1.png?raw=true)
![Image 2](https://github.com/Neel-max-cpu/Aiml-project-Finding-similar-song/blob/main/public/2.png?raw=true)
![Image 3](https://github.com/Neel-max-cpu/Aiml-project-Finding-similar-song/blob/main/public/3.png?raw=true)


# References
- **Chat GPT**
- **V0(by vercel)**
- **YouTube**
- **Shadcn documentation**
- **GeekForGeeks**
-**MillionSongDataset**
-**Google Developer Console**

## Overview
This project is an Admin Dashboard that enables efficient user management with role-based access control (RBAC). The dashboard allows administrators to manage user accounts, view statistics, and access data visualizations. It includes two roles: Admin and User, each with specific permissions. The interface is fully responsive, ensuring usability across desktop and mobile devices.
Admin is automatically created with admin as username and password (using a create admin function - can change accordingly)

This project is an Ai/Ml based project where one can find similar songs based on the track/song they uploaded. File can be of the
format of .mp3/.wav.
Based on that top 5 results will be shown, along with their youtube link if available(api taken from YouTube Data API v3).

## Check the video for the brief of the project without running here  -> [Link]() ⭐

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [How to Run](#how-to-run)

## Features
- **Upload**:  Users can uplod their track(.mp3/.wav) format.
-**View**: Users can see the top 5 similar track along with the youtube link(if available).
- **Responsive Design**: Optimized for various screen sizes, providing a seamless experience on both mobile and desktop devices.

## Technologies Used
- **Frontend**: React.js+vite
- **Backend**: python
- **Api**: Google's (for youtube api)
- **Styling**: Shadcn Ui and custom Tailwind CSS for responsive design
- **Version Control**: Git & GitHub

## Installation

### Prerequisites
Ensure you have the following installed on your machine:
- Node.js (v14 or later)
- npm (Node Package Manager)
- Python(v3)

### Step 1: Clone the Repository
```bash
git clone [https://github.com/Neel-max-cpu/Aiml-project-Finding-similar-song.git](https://github.com/Neel-max-cpu/AdminDashboard.git)
```

### Step 2: Navigate to the Project Directory
Change into the project directory:
```
cd frontend
```

```
cd backend
```

### Step 3: Install Dependencies
Run the following command to install the necessary dependencies for the frontend:
```
npm install
```

For the backend you need to check and install the dependencies directly

Important to, download the dataset you can go to MillionSongData's website [Link](http://millionsongdataset.com/) here.
I have used the million song subset(1.8gb) the full data set if of 280gb. Download it and keep the file in the public folder of the backend.

### Step 4: Set Up the Environment Variables
Create the .env file, just paste your api(can be fetched from here [Link](https://console.cloud.google.com/apis/dashboard)link).
Create an account and enable YouTube Data API v3 and create an api key.


### Usage
After setting up the environment variables, you can start the application.


### How to Run
### Step 1: Start the Backend Server
Before running the backend build/precompute your faiss index.
Nvaigate to the corefolder then build_faiss_index.py run that command or directly run the command, wait for it as it can take sometime!
```
cd backend\app\core
python build_faiss_index.py
```
or

```
python app/core/build_faiss_index.py

```

Navigate to the server directory and start the backend server, set it to virtual environment and start the server:
```
cd backend
.\venv\Scripts\activate
uvicorn app.main:app --reload
```

### Step 2: Start the Frontend
In a new terminal window, navigate to the client directory and start the React application:
```
cd frontend
npm run dev
```

### Step 3: Access the Application
Open your web browser and go to http://localhost:5173/ to access the App.