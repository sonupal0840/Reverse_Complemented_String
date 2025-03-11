# Reverse_Complemented_String
#**Overview**

This is a FastAPI-based file processing service that allows users to upload CSV files, process their contents, and download processed files. The application supports extracting data from structured CSV files and applying transformations like reverse complementing sequences.

#**Features**

Upload CSV Files: Users can upload .csv files via FastAPI endpoints.

Data Parsing: Extracts sections like [Header], [Reads], [Settings], and [Data] from the file.

Reverse Complement Processing: Computes the reverse complement of sequences found in a specific column.

Download Processed Files: Users can download the processed CSV files.

CORS Enabled: Allows communication with a React frontend.

**Installation**

Prerequisites

Ensure you have the following installed:

Python 3.8+

pip

Steps

Clone this repository:

git clone https://github.com/yourusername/your-repo.git
cd your-repo

Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies:

pip install -r requirements.txt

Running the Application

Start the FastAPI server:

uvicorn main:app --reload

The API will be accessible at http://127.0.0.1:8000.

API Endpoints

1. Upload a File

POST /upload/

Uploads a CSV file and processes it.

2. Reverse Complement Processing

POST /reverse_complement/

Applies reverse complement transformation to the index2 column of the uploaded file.

3. Download Processed File

GET /download/?file_name=processed_filename.csv

Downloads the processed CSV file.

Deployment

Deploy FastAPI Backend on Render

Push your code to GitHub.

Go to Render, create an account.

Create a new Web Service and connect your GitHub repository.

Set the Start Command to:

uvicorn main:app --host 0.0.0.0 --port 8000

Deploy!

Deploy React Frontend on Vercel

Push your React app to GitHub.

Go to Vercel and create a new project.

Connect your GitHub repository and deploy.

License

This project is licensed under the MIT License
