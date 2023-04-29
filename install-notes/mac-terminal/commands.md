# macOS Terminal Commands

## View Running Processes
The equivalent to `systemctl` in linux, for macOS it is to use `launchctl`

### To view running processes: 
```
launchctl list
```

### To find a running process (e.g. docker):
```
launchctl list | grep -i docker
```

Example Output: 
```
launchctl list | grep -i docker

-	    0	com.docker.helper
82051	0	application.com.docker.docker.8198157.8198456
```

### To kill a process via pid (process id):
```
kill <pid>
```

Example Usage:
```
kill 82051
```

### To kill a process via name (e.g. docker):
```
pkill docker
```


