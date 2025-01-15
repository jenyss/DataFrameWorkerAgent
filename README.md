# DataFrameWorkerAgent
The DataFrame Worker Agent is a JupyterLab-based tool for processing free-text queries about DataFrames. It converts these queries into Python code to retrieve the requested information. Additionally, it uses Tavily as a tool to fetch detailed information related to the retrieved data. _**This last step can be done from the LangGraph framework without invoking an LLM and was implemented just to illustrate LLM tool calling.**_

## Agent Workflow

1. **Input Node:** Converts free-text user input into a DataFrame query using an LLM.

   - **Input:** `"task"`
   - **Output:** `"query"`

2. **Execution Node:** Runs the query on a DataFrame loaded from an Excel sheet and formats the output.

   - **Input:** `"query"`
   - **Output:** `"result"`

3. **Get Company Data Node:** Takes the formatted `"result"` and passes it to an LLM. The LLM extracts specified data (in this case: a list of company tickers) and iterates over them, calling a tool (Tavily) to fetch recent company information for each ticker. Outputs the aggregated result from all iterations in a structured format.

   - **Input:** `"result"`
   - **Output:** `"company_info"`
  
   _**You can easily disconnect or customize this node to suit your specific needs.**_

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
 * In JupyterLab, use the "Open from Path" option to load ```DataFrameWorkerAgent.ipynb```.
 * Similarly, load ```.env``` and populate the variable keys with appropriate values.

### Step 3: Run the Jupyter Notebook

To execute the notebook, select each cell and press ```Shift + Enter```.
