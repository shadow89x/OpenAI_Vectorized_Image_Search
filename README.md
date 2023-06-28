Vectorized Image Search

Live app you can test here(you need Microsoft Azure computer vision subscription key):
https://shadow89x-openai-vectorized-image-search-appapp-q1zfmy.streamlit.app/

How it Works

The app accepts a query from the user, which can be either a URL of an image or a text. It identifies whether the input is a URL or text based on URL validation. Depending on the type of input, it calls Azure's Computer Vision API to convert the input into a vector.

This vector is then compared with a database of precomputed vectors using cosine similarity to find the most similar images. The database is loaded from a CSV file which contains the vector representations and the corresponding URLs of the images. The top 10 images with the highest similarity are displayed to the user.

This project is a Streamlit application that allows users to search for similar images or products using either a URL or text query. It utilizes the Azure Computer Vision API to vectorize input and compares them to a set of precomputed vectors using cosine similarity.

Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites

To run this project, you will need:

- Python 3.7 or later
- An Azure account with Computer Vision API enabled

Python libraries required:

- streamlit
- pandas
- PIL
- requests
- azure.ai.vision
- azure.storage.blob
- numpy

You can install these libraries using pip:

pip install streamlit pandas pillow requests azure-ai-vision azure-storage-blob numpy

Running the App

1. Clone the repository:
   
   git clone https://github.com/<your-github-username>/<your-repo-name>.git

2. Go to the cloned directory:

   cd <your-repo-name>

3. Run the Streamlit app:

   streamlit run app.py

In the app, you'll need to input your Azure Computer Vision Endpoint and API Key in the sidebar.



Contributing

Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/AmazingFeature)
3. Commit your Changes (git commit -m 'Add some AmazingFeature')
4. Push to the Branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

License

Distributed under the MIT License. See LICENSE for more information.
