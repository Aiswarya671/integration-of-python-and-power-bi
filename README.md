# integration-of-python-and-power-bi
**COMPANY**: CODTECH IT SOLUTIONS
**NAME**: AISWARYA.R
**INTERN ID**:CODHC214
**DOMAIN**: POWER BI
**DURATION**: 4 WEEKS
**MENTOR**: NEELA SANTHOSH
# DESCRIPTION OF TASK:
Enable Python in Power BI
Open Power BI Desktop.
Go to File → Options and Settings → Options.
Under Python scripting, set up your Python home directory (e.g., where Anaconda or Python is installed).
2. Load Data Using Python in Power BI
In Power BI Desktop, go to Home → Transform Data.

Click New Source → Python Script.

Write a Python script 
Click OK, and Power BI will execute the script.

Click Load to bring the transformed data into Power BI.

3. Use Python for Data Visualization in Power BI
Go to Report View.

Click Python Visual from the Visualizations panel.

Drag and drop the required fields into the values section.

Write a Python script to visualize the data
Click Run script, and Power BI will render the visualization.

4. Automate Python Workflows in Power BI
Use Power BI Service for scheduling automatic refreshes.
Store Python scripts in a dedicated folder or database and reference them in Power BI.
If working with large datasets, consider using Azure Notebooks or Jupyter Notebooks for pre-processing before importing into Power BI.
5. Advanced Integration (Power BI API + Python)
If you want to push data dynamically into Power BI dashboards, use Power BI REST API with Python:

Install Power BI API package:

bash
Copy code
pip install requests
Use Python to push data to Power BI:

python
Copy code
import requests
import json

# Power BI API URL and dataset details
url = "https://api.powerbi.com/beta/your_workspace/datasets/your_dataset/rows?key=your_api_key"

# Sample data payload
data = json.dumps([{"Category": "Electronics", "Sales": 2000}])

# Send data to Power BI
response = requests.post(url, data=data, headers={"Content-Type": "application/json"})

print(response.status_code, response.text)
