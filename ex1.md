# Exercise 1: Setting Up Your Environment

## Before You Start

Azure Machine Learning is a Microsoft Azure-based service for running data science and machine learning workloads at scale in the cloud. To use Azure Machine Learning, you will need an Azure subscription. If you do not already have one, you can sign up for a free trial at [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)

## Task 1: Create an Azure ML Workspace

As its name suggests, a workspace is a centralized place to manage all of the Azure ML assets you need to work on a machine learning project.

1. Sign into the [Azure portal](https://portal.azure.com) and create a new **Azure Machine Learning service workspace** resource in a new resource group. You can use any available region.
2. When the workspace and its associated resources have been created, view the workspace in the portal.

## Task 2: Open the Azure ML Web Interface

You can manage workspace assets in the Azure portal, but for data scientists, this tool contains lots of irrelevant information and links that relate to managing general Azure resources. An alternative, Azure ML-specific web interface for managing workspaces is available.

1. In a new browser tab, open [https://ml.azure.com](https://ml.azure.com) and sign in using the Microsoft account you used to sign into Azure.
2. Select your Azure subscription and the workspace you created in the previous task.

## Create a Notebook VM

You can run code to work with your workspace in many tools, including locally installed tools like Visual Studio Code or Jupyter Notebooks, or hosted environments like the Azure Data Science VM, Azure NOtebooks, or a JupyterHub server. Additionally, Azure ML includes the ability to create and manage Notebook VMs in your workspace, and that's what we'll use in this lab.

1. In your workspace, create a new **Notebook VM** using the *STANDARD_DS3_V2* VM type template.
2. After the Notebook VM has been created, verify that it is running, and then click the **Jupyter** or **JupyterLab** link, depending on the notebook environment you want to use in this lab (you can experiment with both, they have acess to the same file system in the Notebook VM).
3. In the notebook environment, open a new **Terminal**, and in the **Users** folder, run the following command:

    ```bash
    git clone https://github.com/GraemeMalcolm/azureml-primers
    ```

4. After the comand has completed, close the terminal and view the home folder in your notebook file explorer - it should contain an **azureml-primers** folder, containing the files you will use in the rest of this lab.

> **Note**: If you intend to continue straight to the next lab, leave your Notebook VM running. If you're taking a brereak, you might want to close the Jupyter tabs and **Stop** your notebooks VM to avoid incurring unnecessary costs.
