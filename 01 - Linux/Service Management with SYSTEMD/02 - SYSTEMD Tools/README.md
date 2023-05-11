* Let us now look at the tools for managing services working with SYSTEMD targets, logging, and getting information about the overall state of the system. 

* The two major tools are: systemctl and journalctl. 

# systemctl #

* <b>sysytemctl:</b> The main command used to manage services on a SYSTEMD-managed server. It can be used to manage services such as start, restart, stop, reload, enable or disable services to start during the system boot. 

* Let us look at some systemctl commands.

   1. To start a service, 
   ```
   systemctl start docker
   ```
   2. To stop,
   ```
   systemctl stop docker
   ```
   3. To restart,
   ```
   systemctl restart docker
   ```
   4. To reload the service without interrupting normal functionality,
   ```
   systemctl reload docker 
   ```
   5. To enable a service and make it persistent across reboot,
   ```
   systemctl enable docker
   ```
   6. To disable the service at boot,
   ```
   systemctl disable docker
   ```
   7. To get information about the state of service,
   ```
   systemctl status docker
   ```
   8. After making changes to a service unit file, run this command,
   ```
   systemctl deamon-reload 
   ```
   9. To make changes to a service,
   ```
   systemctl edit <service_unit_file_> --full 
   ```
   A text editor will open. Units edited this way apply the changes immidiately without runnung the systemctl daemon-reload.
   10. To see current run-level or the target, 
   ```
   systemctl get-default
   ```
   11. To change the target,
   ```
   systemctl get-default <new_target>
   ```
   12. To list all the units SYSTEMD has loaded or attempted to load,
   ```
   systemctl list-units --all 
   ```
   13. To see information about the active units only,
   ```
   systemctl list-units
   ```
   
# journalctl #
   
* <b>journalctl:</b> This command can query the contents of the SYSTEMD logging system called journal and is a convenient troubleshooting tool to figure out issues such as service failures. 
   
* journalctl is useful when troubleshooting issues with SYSTEMD units as it checks the journal or log entries from all parts of the system. 

* 'journalctl' without any flags prints all the log entries from the oldest entry to the newest. 

* To see the logs from the current boot, 

```
journalctl -b
```

* To see the log entries for a specific unit, 

```
journalctl -u <name_of_unit>
```
