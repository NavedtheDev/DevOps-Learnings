* Cron is used to schedule jobs in Linux. 

* With a Cron job, a user can specify any date, time, or frequency to schedule a task. Once defined, the system will execute the task at the set time.

* This functionality is enabled by the crond service that runs in the background. 

* To schedule a task, run the command,

```
crontab -e 
```
We will be in the VI Editor now. Navigate to the bottom of the file and add the configuration for our job to be scheduled.

* The first five fields are used to specify the exact schedule to run the task. The sixth field is the command to run.

<b>NOTE:</b> Do not use sudo with crontab command, or you will find that the job will be scheduled for the root user. 
