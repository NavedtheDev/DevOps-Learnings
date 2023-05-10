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

* Let us see how the schedule works and see the meaning of the first five columns in the crontab. Here is an example,


![Screenshot (150)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/00a47245-eafd-484b-82e9-dc653370110f)


* A star in these fields indicates any value.

* If you want to run your job every 5 mins, you can configure that using step values with a slash. Here is how,

```
*/2 * * * *
```
Same can be used for other options as well.

* To list all the jobs scheduled in cron, 

```
crontab -l
```

* To check if the job was successfully run is to inspect the logfile /var/log/syslog. 
