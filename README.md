## lightweight scraper for free parking places in ulm

This is just a simple scraper which collects json-compatible data that is then stored to json files with the filename being the timestamp. 

<br />

## Dependencies
Execute pythonDependencyInstallation.ps1 to install all necessary python packages
```shell script
./pythonDependencyInstallation.ps1
```
<br />

## Run
```shell script
python main.py store
```

to store a snapshot. 

Any error will be written to the `./errors/` directory.

<br />

## Access data

through `util.Storage` and `util.DataSources` or via

```shell script
python main.py load
```

### To run as cron-job

type `crontab -e` and add something like

```crontab
*/15 * * * * /bin/sh -c 'cd /path/to/parking-scraper && ./env/bin/python main.py store'
```
