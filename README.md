# 01_02-service-containers
Use these files to test a service container.

1. Create a new repo.
2. Add the files from this directory to the root of the new repo; note there may be a .gitignore file that is hidden...add that file as well.
3. Move the file `service-container.yml` into the `.github/workflows` directory in the new repo.
4. Once the file is commited, the workflow should be triggered by a `push` event.
5. Confirm the workflow runs as expected and includes output for a step named `Initialize containers`.

# 01-03-scheduled-triggers
Use these files to test a scheduled trigger.

1. Create a new repo.
2. Upload the file `nightly-build.yml` into the `.github/workflows` directory in the new repo.
3. Once the file is commited, the workflow should be triggered by a `push` event.
4. Confirm the workflow completes and creates an artifact.
5. Modify the schedule in the workflow to run more frequently than once per day to see the results of the schedule.
6. Review the results of the workflow triggered by a schedule and compare it to a workflow triggered by a push.

# 01_04-composite-actions
Use these files to test a composite action.

1. Create TWO new repos:
    - one to host the composite action
    - one to host the workflow that uses the action
1. Upload the file `action.yml` into the root of the compsite action repo.
1. Upload the following files into the root of the workflow repo:
    ```
    main.py
    requirements.txt
    ```
1. Edit the file `composite-action-workflow.yml` to replace the following placeholders with the correct values:
    ```
    YOUR_GITHUB_USER_NAME
    YOUR_COMPOSITE_ACTION_REPO_NAME
    ```
1. If your username is `octocat` and the composite repo name is `awesome-action`, your `composite-action-workflow.yml` should now include a line as follows:
    ```
    uses: octocat/awesome-action@main
    ```
1. Upload the file `composite-action-workflow.yml` into the `.github/workflows` directory of the composite action repo.
1. Once the workflow file is commited, the workflow should be triggered by a `push` event.
1. Confirm the workflow runs as expected and includes output from the composite action.
