.. _faq:

FAQs
====

Insula
------

Q: What resources are available for my projects at Insula?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

The available *default* resources are:

* 5000 MB of persistent storage, for processing outputs or uploaded data. Data will be retained indefinitely (forever).
* 5 jobs in parallel
* 20 usage credits. Each credit is consumed when you:
   * Download data from :ref:`processing_outputs` or :ref:`uploaded_data` collections.
   * Execute a Processing Service (see :ref:`run_service`). 

Please note that not all downloads or actions will consume credits and a clear prompt will inform when you are about to consume credits.

If you need additional resources for your projects, please contact us at insula-ops.it@cgi.com. 

Insula Code Lab
-----------------

Q: How to remove a kernel from the Insula Code Lab?
++++++++++++++++++++++++++++++++++++++++++++++++++++

* Access the Code Lab
* Open a Terminal
* Type *jupyter kernelspec uninstall <environment to remove>*

Q: Will my personal storage be preserved in the Insula Code Lab?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Your personal storage in Insula Code Lab is designed to be persistent, meaning it survives server shutdowns. It is located under `/home/jovyan`. This ensures your data remains available when the server restarts.
However, Insula Code Lab currently does not perform automatic backups of your personal storage. While your data is unlikely to be lost during a server shutdown, it's crucial to take responsibility for backing up your critical information.

Q: Are R and Julia (incl. Pluto) supported?
+++++++++++++++++++++++++++++++++++++++++++

While you may see R and Julia (including Pluto) listed as kernels, it's important to understand that currently there is limited support for these languages and their packages. This means you might encounter issues running R or Julia code or using their specific packages.

Q: Why ipyleaflet maps are not rendered on the browser?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

After successfully following the instructions here https://ipyleaflet.readthedocs.io/en/latest/installation/index.html#using-pip, ipyleaflet maps are not rendered on the browser. This is likely a cache issue on your browser. To fix, you can try an hard refresh of the browser. See https://www.gavel.io/resources/what-is-a-hard-refresh-how-to-do-a-hard-refresh-in-any-browser for more details.

Q: Is it possible to use conda in the Insula Code Lab?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

While conda is a powerful tool for managing Python environments, it's currently not the recommended approach within Insula Code Lab.

Here's why:

* **Dependency Conflicts:** Insula Code Lab manages its own environment to ensure smooth operation and compatibility. Introducing conda might lead to conflicts with pre-installed packages or dependencies within the Lab's environment.
* **Package Stability:** The Lab strives to provide a stable and consistent experience. Using conda could introduce external packages with potential stability issues.

Insula Code Lab offers built-in mechanisms for managing dependencies within your projects (see :ref:`python_new_package`).

If you have specific requirements that necessitate conda, it's technically possible to use it. However, we recommend consulting Insula's support team beforehand to discuss potential compatibility issues and ensure a smooth workflow.

Q: Why my installed Python packages are no longer there?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

The Insula Code Lab persists files and folders located in the `/home/jovyan`. This applies also to the Python's Virtual Environments (see :ref:`python_env`). On the other hand, if a package is installed via a command like `pip install package`, this will be installed under the main Python installation, that is not persisted. Therefore, it is recommended to use Python environments as described in :ref:`python_new_package`, if one wants to persist installed packages.

Q: What are the resources available to my server in the Insula Code Lab
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

The available resources are:

* 500m CPU (*m* stands for millicores)
* 4 GB of RAM
* 250 GB of persistent storage. Data will be retained indefinitely (forever).
