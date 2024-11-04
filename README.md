# AOAI ChatGPT Demo using Streamlit

A fully python based Streamlit development harness for ChatGPT hosted in Azure OpenAI Service.

## Getting Started

## Setup

1. **Clone the repository**:
   ```sh
   git clone https://github.com/ddesonier/ChatGPT_USGov.git
   cd ChatGPT_USGov
   ```

2. **Create a virtual environment and activate it**:
   ```sh
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   source .venv/bin/activate  # On macOS/Linux
   ```

3. **Install the required libraries**:
   ```sh
   pip install -r requirements.txt
   ```

### Running the App

To run the app, simply run the `streamlit run app.py`.  This will start the app on port 8501.  You can then access the app at `http://localhost:8501`. If running in a container, you will need to forward the port to your local machine if VSCode does not do it for you automatically.

### Devcontainer

This project is designed to be used with VSCode and the Remote Containers extension.  Once you have the extension installed, open the project in VSCode and you will be prompted to open the project in a container.  This will build the container and install all the dependencies.

### Python Dependencies

The `requirements.txt` file contains all the python dependencies for this project.  The `devcontainer.json` file will automatically install these dependencies when the container is built.


### Docker

```bash
$ docker login myregistry.azurecr.io

$ docker build --no-cache -t yourusername/app .

$ docker run -p 8501:8501 yourusername/app

$ docker tag yourusername/app myregistry.azurecr.io/app:v1

$ docker push myregistry.azurecr.io/app:v1
```