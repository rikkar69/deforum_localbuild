# Easy Environment Setup For Local Deforum Stable Diffusion
1. Download and install Anaconda (https://www.anaconda.com/)
2. Download and install GIT (https://git-scm.com/download/win)
## Create Local folder structures
1. Create this folder path in a drive ``E:/Deforum/content``
2. Create two folders in the path called ``content`` and ``models`` to match the defaults in the deforum Colab notebook.
3. Download the Stable Diffusion model ckpt and save into the ``models`` folder (https://huggingface.co/CompVis/stable-diffusion-v-1-4-original) or copy the model from your Google Drive if you have already downloaded the model for using with cloud GPUs. 
## Create Conda Environment
1. Download the ``environment.yml`` file and save into ``E:/Deforum``
2. Open Start menu and open ``Anaconda Powershell Prompt``
3. Navigate to the ``Deforum`` folder using the command ``cd e:\Deforum``
4. Execute the command ``conda env create -f environment.yml`` to create the conda environment and install the needed dependancies
5. Activate the new environment using the command ``conda activate deforumlocal``
6. Start a Jupyter sessions using the command ``jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8889 --NotebookApp.port_retries=0``
7. Close the browser tab that opens and copy the localhost address that displayes in Anaconda Powershell Ex. ``http://localhost:8889/?token=42c7da12d8acb14c512979d882414e569b363ceb9815974a``
8. In the deforum Colab notebook, click on the connect menu and select ``Connect to a local runtime``

![image](https://user-images.githubusercontent.com/95973743/192116684-e81e6f1d-6bdd-4dca-9c34-797a943bd63a.png)

9. Paste the copied localhost address into the ``Backend URL`` field and click ``Connect``

![image](https://user-images.githubusercontent.com/95973743/192116724-fa37957d-a3c5-4d60-a322-17c10d4cdff3.png)

10. After a successful connection, remove the ``/`` from the ``model_path`` and ``output_path`` in the ``Model and Ouput Paths`` code cell and uncheck ``mount_google_drive:``

![image](https://user-images.githubusercontent.com/95973743/192117254-45583193-5422-4227-956a-5a2ec1b55672.png)

11. Continue running cells like you would with a cloud session and start dreaming!
