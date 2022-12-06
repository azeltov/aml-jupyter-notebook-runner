az ml job create --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default --file /home/azureuser/cloudfiles/code/Users/alex/papermill/iris/job.yml --stream

az ml job create --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default --file /home/azureuser/cloudfiles/code/Users/alex/papermill/iris/pipeline.yml --stream
   
az ml schedule create --file schedule.yml  --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default 

az ml schedule list --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default

az ml schedule disable --name simple_cron_job_schedule  --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default 

 az ml schedule delete --name simple_cron_job_schedule  --subscription f1ea6ed8-82f3-416d-881b-8b376218bc85 --resource-group rg_aml --workspace-name aml-default 