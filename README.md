# Personal-Projects

# Create a virtual environment named venv
python3 -m venv venv

# Activate it (macOS/Linux)
source venv/bin/activate

# Register the Virtual Environment with Jupyter

Even if the venv is active in the terminal, notebooks will not automatically use it.
You must register it as a Jupyter kernel:

python -m ipykernel install --user --name=personal-projects-env --display-name "Python (personal-projects)"

This makes the environment selectable in your IDE (Cursor/VS Code).

Relaod cursor -> open the notebook -> In the top-right, click Select Kernel → Jupyter Kernel…

Now your notebook is running on the virtual environment.

# To verify, if the notebook is running on the venv, run:

!which python

You should see something like:
.../Personal-Projects/venv/bin/python

# Save Dependencies

To capture your environment:

pip freeze > requirements.txt

# To run streamlit app

You have to copy the model file in artifact created by the .ipynb folder to the app folder  so streamlit can access it 

Go to app folder > then run "streamlit run main.py"