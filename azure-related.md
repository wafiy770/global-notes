#### Azure Function

##### run azure function on local

Make sure to pull the latest version of the functions in github first

- configure functions.json first, to run on startup
```
{
  "scriptFile": "__init__.py",
  "bindings": [
    {
      "name": "mytimer",
      "type": "timerTrigger",
      "direction": "in",
      "schedule": "0 0 18 * * *",
      "runOnStartup": true
    }
  ]
}
```

- on cmd terminal, make sure inside .env 
```
func start --functions <function_name>
```

Ctrl + c to kill the function after receive 'executed function ....'
```
Executed 'Functions.GetEmployeesAttendanceAF' (Succeeded, Id=492fa919-64e2-4197-9cfc-966917ff6b1a, Duration=258517ms)
```


##### getPosSales on specific date

- open init.py inside otherData_GetPosSales

- change the yaml file at first argument in open(), depending on what country to extract
```
    # read configuration.yaml
    with open("otherData_GetPosSales_MY.yaml", "r") as yamlfile:
        data = yaml.load(yamlfile, Loader=yaml.FullLoader)
```

- add "runOnStartup": true inside function.json 
```
{
  "scriptFile": "__init__.py",
  "bindings": [
    {
      "name": "mytimer",
      "type": "timerTrigger",
      "direction": "in",
      "schedule": "0 0 18 * * *",
      "runOnStartup": true
    }
  ]
}
```

- inside yaml file, uncomment the outlet & date filters
```
  take_all: 'getspecificoutletsales'
  #target_outlet: '100010'
  #from_dt: '2023-11-22'
  #to_dt: '2023-11-22'
```

- extracted file is saved as stage configuration in the yaml file
```
stage:
  data_lake_account_name: 'fourfingersadls'
  data_lake_container_name: 'zeoniq-data-malaysia'
  data_lake_directory_name: 'otherData/{stage_table}'
  data_lake_subdirectory_name: '{subDir_date}'
  file_name: '{stage_table}_{date}.csv'
  stage_table: ['getpossales','PosSalesDetails',
  'PosSalesPayments','PosSalesCustomerDtl']
```


##### Deploying local Azure Function to Cloud

- check The4kingVault
https://4fingerspteltd.sharepoint.com/:w:/r/sites/The4kingVault/_layouts/15/Doc.aspx?sourcedoc=%7BE601EC6B-85F0-403B-82B7-8CA7A919F4EB%7D&file=Azure%20Functions.docx&action=default&mobileredirect=true