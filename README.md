# DataFrameWorkerAgent
The DataFrame Worker Agent is a JupyterLab-based tool for processing free-text queries about DataFrames. It converts these queries into Python code to retrieve the requested information. Additionally, it uses Tavily as a tool to fetch detailed information related to the retrieved data.

## Intallation

<b>Prerequisites</b>

* Access to <b>JupyterLab, Google Colab</b>, or another interactive computing environment to run this Jupyter Notebook.
* To run the notebook, ensure the following frameworks are installed: LangChain, LangGraph, Pandas, python-dotenv
* [Tavily](https://www.tavily.com) is used as a tool invoked by the LLM to fetch additional data.
* Access to a Large Language Model API.

### Step 1: Clone the Repository

Clone this repository to your local machine:
```
git clone <REPOSITORY_URL>
cd <PROJECT_FOLDER>
```

### Step 2: Open Jupyter Notebook in JupyterLab

Ensure that ```<PROJECT_FOLDER>``` is accessible in JupyterLab by setting it as your working directory in JupyterLab.
 * In JupyterLab, use the "Open from Path" option to load ```ProductMuse_v1.ipynb```.
 * Similarly, load ```.env``` and populate the variable keys with appropriate values.

### Step 3: Run the Jupyter Notebook

To execute the notebook, select each cell and press ```Shift + Enter```.
