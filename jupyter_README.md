## Prequisites

    1. Python installation

### Step for jupyter notebook installation:

    pip install notebook


### Step for Run jupyter notebook via (GUI):
 
    jupyter notebook

### Step for Run jupyter notebook without (GUI):
   
> How to Run a Jupyter Notebook (.ipynb) from Command Prompt

    If you want to run all cells of a notebook directly from terminal without opening the UI, use nbconvert:

    cmd:\> jupyter nbconvert --to notebook --execute my_notebook.ipynb


    👉 This executes all cells and saves the results inside the same .ipynb file.
    If you want a separate executed output file:

    cmd:\> jupyter nbconvert --to notebook --execute my_notebook.ipynb --output executed_notebook.ipynb
    
> How to Convert Notebook to Python Script

    You can convert .ipynb to .py (plain Python script) like this:

    cmd:\> jupyter nbconvert --to script my_notebook.ipynb

    This creates my_notebook.py, containing all code cells. (Markdown/comments are turned into Python comments.)

✅ Summary

    Install: pip install notebook

    Start UI: jupyter notebook

    Run notebook headlessly:
    jupyter nbconvert --to notebook --execute my_notebook.ipynb

    Convert to Python script:
    jupyter nbconvert --to script my_notebook.ipynb
