Works on AWS CodeBuild too. 
![image](https://github.com/kapalulz/docker_pipeline_azureDevOps_AWS_codebuild/assets/17459523/862bf3a8-c7ee-4432-8769-e55ee2c3be12)
![image](https://user-images.githubusercontent.com/17459523/208579707-ee8073ab-906f-41a8-9db4-2d5f47e3cc06.png)

# Project Description

Also compatible with AWS CodeBuild.

* This sample contains the fully implemented program from the tutorial. Please make sure to visit the following link: [Using Flask in Visual Studio Code](https://code.visualstudio.com/docs/python/tutorial-flask). Intermediate steps are not included.

* It also includes the necessary *Dockerfile* and *uwsgi.ini* files required for building a container with a production server. The resulting image functions both locally and when deployed to Azure App Service. Refer to [Deploy Python using Docker containers](https://code.visualstudio.com/docs/python/tutorial-deploy-containers).

* To run the app locally:
  1. Run the command `cd hello_app`, to change into the folder that contains the Flask app.
  2. Run the command `set FLASK_APP=webapp` (Windows cmd) or `FLASK_APP=webapp` (macOS/Linux) to point to the app module.
  3. Start the Flask server with `flask run`.

## The startup.py file

In the root folder, the `startup.py` file is specifically for deploying to Azure App Service on Linux without using a containerized version of the app (that is, deploying the code directly, not as a container).

Because the app code is in its own *module* in the `hello_app` folder (which has an `__init__.py`), trying to start the Gunicorn server within App Service on Linux produces an "Attempted relative import in non-package" error.

The `startup.py` file, therefore, is a shim to import the app object from the `hello_app` module, which then allows you to use startup:app in the Gunicorn command line (see `startup.txt`).

## Contributing

Contributions to the sample are welcome. When submitting changes, also consider submitting matching changes to the tutorial, the source file for which is [tutorial-flask.md](https://github.com/Microsoft/vscode-docs/blob/master/docs/python/tutorial-flask.md).

Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit [https://cla.microsoft.com](https://cla.microsoft.com).

When you submit a pull request, a CLA-bot automatically determines whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

## Additional details

* This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
* For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
* Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.


