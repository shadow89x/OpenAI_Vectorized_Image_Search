# Vectorized Image Search
## What is Vectorized Search?
The difference between the conventional search method and vector search is that the latter doesn't just find correlations based on the content labeled with images. Instead, all the characteristics inherent to the image itself are stored as elements of the vector. Therefore, the significant advantage is that all the features inherent to the image (color, texture, relevance to other images, etc.) can be searched without any separate labels.

Live app you can test here (you need Microsoft Azure computer vision subscription key):
[https://shadow89x-openai-vectorized-image-search-appapp-q1zfmy.streamlit.app/](https://shadow89x-openai-vectorized-image-search-appapp-q1zfmy.streamlit.app/)

The app accepts a query from the user, which can be either a URL of an image or a text. It identifies whether the input is a URL or text based on URL validation. Depending on the type of input, it calls Azure's Computer Vision API to convert the input into a vector.

This vector is then compared with a database of precomputed vectors using cosine similarity to find the most similar images. The database is loaded from a CSV file which contains the vector representations and the corresponding URLs of the images. The top 10 images with the highest similarity are displayed to the user.

This project is a Streamlit application that allows users to search for similar images or products using either a URL or text query. It utilizes the Azure Computer Vision API to vectorize input and compares them to a set of precomputed vectors using cosine similarity.

## How it Works

1. The application interacts with the user through a sidebar where key inputs are provided. This involves the Azure Computer Vision API key and endpoint. By default, an error will be displayed until these details are provided.

![Sidebar inputs](https://live.staticflickr.com/65535/53006806297_53bfe1f36f_c.jpg)

2. The user can submit an image URL of their choice. The application vectorizes this image and displays items that are most similar.

![Vectorize Image](https://live.staticflickr.com/65535/53007397506_0d2fb41470_c.jpg)

3. The application can also detect context from the image. For example, it can identify prominent colors such as 'red'.

![Context detection](https://live.staticflickr.com/65535/53007397501_8f87ee767f_z.jpg)

4. A distinctive feature of this application is that the images it displays are clickable. When a user clicks on an image, the application re-initiates a search for items most similar to the selected image.

![Clickable images](https://live.staticflickr.com/65535/53007781995_c85e012144_c.jpg)

Refer to the [Getting Started](#getting-started) section for instructions on how to run the application.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

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

```bash
pip install streamlit pandas pillow requests azure-ai-vision azure-storage-blob numpy
