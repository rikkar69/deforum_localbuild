# Easy Windows Environment Setup For Local Deforum Stable Diffusion

## Update!
Since the local branch of deforum has been developed, please follow these instructions/branch: https://github.com/deforum/stable-diffusion/tree/local

Video tutorial: https://www.youtube.com/watch?v=xzeENkbpX_w

1. Download and install Anaconda (https://www.anaconda.com/)
2. Open the official deforum Stable Diffusion notebook (https://colab.research.google.com/github/deforum/stable-diffusion/blob/main/Deforum_Stable_Diffusion.ipynb)
## Create Local folder structures
1. Create this folder path in a drive ``E:/Deforum/content`` (if not using ``E:`` drive, replace with the appropriate letter in this and subsequent steps).
2. Create two sub folders in the path called ``output`` and ``models`` to match the defaults in the deforum Colab notebook, ending up with ``E:/Deforum/content/output`` and ``E:/Deforum/content/models``.
3. Download the Stable Diffusion model ckpt and save into the ``models`` folder (https://huggingface.co/CompVis/stable-diffusion-v-1-4-original) or copy the model from your Google Drive if you have already downloaded the model for use with cloud GPUs. 
## Create Conda Environment
1. Download the ``environment.yml`` file and save into ``E:/Deforum``
2. Open Start menu and open ``Anaconda Powershell Prompt``
3. Navigate to the ``Deforum`` folder using the command ``cd e:\Deforum``
4. Execute the command ``conda env create -f environment.yml`` to create the conda environment and install the needed dependancies
5. Activate the new environment using the command ``conda activate deforumlocal``

## Connect and run the notebook

1. Start a Jupyter session using the command ``jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8889 --NotebookApp.port_retries=0`` in Anaconda Powershell Prompt.
2. Close the browser tab that opens and copy the localhost address that displays in Anaconda Powershell. Ex. ``http://localhost:8889/?token=42c7da12d8acb14c512979d882414e569b363ceb9815974a``

![image](https://user-images.githubusercontent.com/95973743/192117810-c9595da0-0337-478b-afed-6702e36b1ea1.png)

3. In the deforum Colab notebook, click on the connect menu and select ``Connect to a local runtime``

![image](https://user-images.githubusercontent.com/95973743/192116684-e81e6f1d-6bdd-4dca-9c34-797a943bd63a.png)

4. Paste the copied localhost address into the ``Backend URL`` field and click ``Connect``

![image](https://user-images.githubusercontent.com/95973743/192116724-fa37957d-a3c5-4d60-a322-17c10d4cdff3.png)

5. After a successful connection, remove the ``/`` from the ``model_path`` and ``output_path`` in the ``Model and Ouput Paths`` code cell and uncheck ``mount_google_drive:``

![image](https://user-images.githubusercontent.com/95973743/192117254-45583193-5422-4227-956a-5a2ec1b55672.png)

6. Continue running all cells like you would with a cloud session and start dreaming!
