# Exercise 1: Setting Up Your Environment

## Before You Start

Azure Machine Learning is a Microsoft Azure-based service for running data science and machine learning workloads at scale in the cloud. To use Azure Machine Learning, you will need an Azure subscription. If you do not already have one, you can sign up for a free trial at [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)

## Task 1: Create an Azure ML Workspace

As its name suggests, a workspace is a centralized place to manage all of the Azure ML assets you need to work on a machine learning project.

1. Sign into the [Azure portal](https://portal.azure.com) and create a new **Machine Learning** resource, specifying a unique workspace name and creating a new resource group. You can create the resource in any region that supports the *NC-series* of virtual machines, which you can determine in the [Azure Products Available by Region page](https://azure.microsoft.com/en-us/global-infrastructure/services/?products=virtual-machines)

    **Note**: Machine Learning workspaces aren't restricted to these regions, but if you plan to use GPU-enabled compute for your machine learning workloads, you need to create the workspace in a region where GPU VMs are supported.

2. When the workspace and its associated resources have been created, view the workspace in the portal.

> **More Information**: To learn more about workspaces, see the [Azure ML Documentation](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-workspace).

## Task 2: Explore the Azure ML Studio Interface

You can manage workspace assets in the Azure portal, but for data scientists, this tool contains lots of irrelevant information and links that relate to managing general Azure resources. An alternative, Azure ML-specific web interface for managing workspaces is available.

> **Note**: The web-based interface for Azure ML is named *Studio*, which you may find confusing as there is also a free *Azure Machine Learning Studio* product for creating machine learning models using a visual designer. A more scalable version of this visual designer is included in the new Studio interface.

1. In the portal blade for your workspace, click the link to launch Studio; or alternatively, in a new browser tab, open [https://ml.azure.com](https://ml.azure.com),  sign in using the Microsoft account you used to sign into Azure in the previous task, and select your Azure subscription and the workspace you created in the previous task.
2. View the Studio interface for your workspace - you can manage all of the assets in your workspace from here.

## Task 3: Create a Notebook VM

You can run code to work with your workspace in many tools, including locally installed tools like Visual Studio Code or Jupyter Notebooks, or hosted environments like the Azure Data Science VM, Azure Notebooks, or a JupyterHub server. Additionally, Azure ML includes the ability to create and manage Notebook VMs in your workspace, and that's what we'll use in this lab.

1. In your workspace, create a new **Notebook VM** using the default VM type template.
2. After the Notebook VM has been created, verify that it is running, and then click the **Jupyter** or **JupyterLab** link, depending on the notebook environment you want to use in this lab (you can experiment with both, they have access to the same file system in the Notebook VM).
3. In the notebook environment, open a new **Terminal**, and in the **Users** folder, run the following command:

    ```bash
    git clone https://github.com/GraemeMalcolm/azureml-primers
    ```

4. After the comand has completed, close the terminal and view the home folder in your notebook file explorer - it should contain an **azureml-primers** folder, containing the files you will use in the rest of this lab.

## Task 4: Connect to Your Workspace using the Azure ML SDK

1. In the **/azureml-primers/notebooks** folder, open the **01 - Setting up Your Environment.ipynb** notebook.
2. Read the notes in the notebook, running each code cell in turn.

> **Note**: If you intend to continue straight to the [next exercise](ex2.md), leave your Notebook VM running. If you're taking a break, you might want to close the Jupyter tabs and **Stop** your Notebook VM to avoid incurring unnecessary costs.
