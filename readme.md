# Demo how to run and schedule jupyter notebook(s) using AMLv2 CLI pipelines and papermill command

![image](https://user-images.githubusercontent.com/5873303/206203917-84bec23b-b22c-44c2-8966-24a2ec55b8d3.png)


### DEMO STEPS:

Create a single step job that runs command: papermill -k python train.ipynb

```az ml job create --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default --file job.yml --stream```

Create an aml pipeline  that runs multi-notebooks:


```az ml job create --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default --file pipeline.yml --stream```

Schedule the created aml pipeline:

```az ml schedule create --file schedule.yml  --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default```

List Scheduled jobs:

```az ml schedule list --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default```

Disable the scheduled pipeline job:

```az ml schedule disable --name simple_cron_job_schedule  --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default ```

Delete the scheduled job:

```az ml schedule delete --name simple_cron_job_schedule  --subscription xxxx-xxxx-xxxx-xxxx --resource-group rg_aml --workspace-name aml-default ```
