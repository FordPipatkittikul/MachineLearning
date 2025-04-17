# Anaconda, Miniconda and Conda

Quick overview: https://www.mrdbourke.com/get-your-computer-ready-for-machine-learning-using-anaconda-miniconda-and-conda/

Download: https://www.anaconda.com/download

Command to create a custom environment within the project folder: `conda create --prefix ./env pandas numpy matplotlib scikit-learn`

Command to activate: `conda activate C:\yourpath\yourpath\yourpath\sample_project_1\env`

Command to deactivate: `conda deactivate`

Command to install some packages: `conda install jupyter`

# Sharing your Conda Environment

1. Share your entire project folder (including the environment folder containing all of your Conda packages).

2. Share a .yml (pronounced YAM-L) file of your Conda environment.

The benefit of 1 is it's a very simple setup, share the folder, activate the environment, run the code. However, an environment folder can be quite a large file to share.

That's where 2 comes in. A .yml is basically a text file with instructions to tell Conda how to set up an environment.

For example, to export the environment we created earlier at /Users/daniel/Desktop/project_1/env as a YAML file called environment.yml we can use the command:

`conda env export --prefix /Users/daniel/Desktop/project_1/env > environment.yml`

After running the export command, we can see our new .yml file stored as environment.yml.

A sample .yml file might look like the following:

    name: my_ml_env
    dependencies:
        - numpy
        - pandas
        - scikit-learn
        - jupyter
        - matplotlib

Of course, your actual file will depend on the packages you've installed in your environment.

For more on sharing an environment, check out the [Conda documentation on sharing environments.](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment)


Finally, to create an environment called env_from_file from a .yml file called environment.yml, you can run the command:

`conda env create --file environment.yml --name env_from_file`

For more on creating an environment from a .yml file, check out the [Conda documentation on creating an environment from a .yml file.](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)

# Jupyter notebook

An interactive web application that allows you to create and share documents containing live code, equations, visualizations, and narrative text.

benefits:
- Iterative Experimentation: Easily test different approaches and parameters.
- Visualization: Ideal for visualizing data, model performance, and intermediate steps.
- Documentation: Combine explanations and code in one environment.
- Collaboration: Share notebooks with colleagues or clients.
- Reusability: The workflow is recorded, making it easier to debug, reproduce, and improve.