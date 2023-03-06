## Introduction
The Internet Monitoring and Action Project (iMAP) will promote and defend Internet freedoms in South and Southeast Asia by pursuing the following interconnected objectives: (1) establish in-country networks that will monitor network interference and restrictions to the freedom of expression online; (2) promote legal advocacy to expand Internet freedoms; and (3) enable civil society action for a freer Internet.

The project will operate in Malaysia, Indonesia, Philippines, Cambodia, Vietnam, Thailand, Hong Kong, Myanmar and India.

This website will contain further details about the IMAP project: 
* Country page summary
* Activities
* Development of test lists
* The IMAP team and partners

### To run test site:
- Install zc.buildout: `pip install wheel zc.buildout`
- Update add-on folders `bin/develop update`
- Run buildout: `buildout -vv`
- Start debug session with `bin/instance fg` 

### On live server
- Change directory to `/opt/imap`
- Update iMAP folder `sudo -u www-data git pull`
- Run buildout `sudo -u www-data venv/bin/buildout -v`
- Start/stop services `sudo -u www-data bin/instance start` or `sudo -u www-data bin/instance stop`
- To debug use `sudo -u www-data bin/instance fg`

#### To automate restarting of services after reboot:
 Install cron job (using `crontab -e`): `@reboot sleep 10; cd /opt/imap/; sudo -u www-data bin/instance start`.
(Note that this job will start 10 seconds after reboot)
