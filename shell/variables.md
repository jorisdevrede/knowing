# Environment variables

## Create / Update

*Powershell* 
```
> $env:Variable = "Value"`
```
*Bash* 
```
$ export Variable = "Value"
```


## Delete

*Powershell*
```
> Remove-Item Env:\Variable
```

*Bash*
```
$ unset Variable
```


## List

*Powershell*
```
> dir env:
```

*Bash*
```
$ env
```
