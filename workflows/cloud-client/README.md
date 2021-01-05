<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# Cloud Workflows Quickstart – Python

This sample shows how to execute a Cloud Workflow and wait for the workflow execution results.

## Setup

1. Read [Prerequisites][prereq] and [How to run a sample][run] first.

1. Deploy the workflow, `myFirstWorkflow`:

    1. Copy the YAML from this file: https://github.com/GoogleCloudPlatform/workflows-samples/blob/main/src/myFirstWorkflow.workflows.yaml
    1. Paste the YAML into a file called `myFirstWorkflow.workflows.yaml`.
    1. Run the command: `gcloud beta workflows deploy $WORKFLOW --source myFirstWorkflow.workflows.yaml`

## Run the Quickstart

Install [`pip`][pip] and [`virtualenv`][virtualenv] if you do not already have them.

You may want to refer to the [`Python Development Environment Setup Guide`][setup] for Google Cloud Platform for instructions.   

1. Create a virtualenv. Samples are compatible with Python 2.7 and 3.4+.

    ```sh
    virtualenv env
    source env/bin/activate
    ```

1. Install the dependencies needed to run the samples.

    ```sh
    pip install -r requirements.txt
    ```

1. Start the application, setting your project name in an environment variable, `GOOGLE_CLOUD_PROJECT`:

    ```sh
    GOOGLE_CLOUD_PROJECT=your-project
    python main.py
    ```

1. Observe the results:

    In stdout, you should see a JSON response from your workflow like the following:

    ```json
    ["Wednesday","Wednesday Night Wars","Wednesday 13","Wednesday Addams","Wednesday Campanella","Wednesdayite","Wednesday Martin","Wednesday Campanella discography","Wednesday Night Hockey (American TV program)","Wednesday Morning, 3 A.M."]
    ```

[prereq]: ../README.md#prerequisities
[setup]: https://cloud.google.com/python/setup
[pip]: https://pip.pypa.io/
[virtualenv]: https://virtualenv.pypa.io/