GitHub Actions
==============

Core Concepts
-------------
- [Github Actions][1] enables Continuous Deployment (CD) and Continuous Integration (CI) capability to GitHub.
- `Workflow` is the top level construct used to automate build, test, and deployment of the code/application. 
  - It consists of one or more `Jobs`. 
  - It is defined as a YAML file in the `.github/workflows` directory at the root of the GitHub repo. There can be more than one workflows for a repository each defined in its `.yaml` file.
  - `Workflow` is triggered by a `GitHub Event`, an `external Event`, or based on a `Schedule`. More than one workflows (if exists) can be mapped to different events.
- Each `Job` runs on an individual `Virtual Machine`. 
  - Jobs run in parallel or sequentially (in case Job2 depends on status or Job1). 
  - Each `Job` contains one or more `Steps`.
- Each `Step` contains one or more `Actions`.

```
Build-Test-Workflow  (Top level construct for CDCI automation)
|-- Job1-Linux  (Each Job runs on fresh virtual machine, either in parallel or sequential)
|-- Job2-Windows  ()
    |-- Step1
    |-- Step2
        |-- Action1
        |-- Action2
```





## Reference Links
- [GitHub Actions Documentation][2]
- [Workflow File Syntax Reference][3]
















[1]: https://help.github.com/en/articles/about-github-actions#about-github-actions
[2]: https://help.github.com/en/categories/automating-your-workflow-with-github-actions
[3]: https://help.github.com/en/articles/workflow-syntax-for-github-actions
