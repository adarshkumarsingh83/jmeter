# jmeter

----

### Download link 
* https://jmeter.apache.org/download_jmeter.cgi

## Start jmeter 
* cd apache-jmeter-xx
* apache-jmeter-xx/bin sh jmeter.sh 
```
================================================================================
Don't use GUI mode for load testing !, only for Test creation and Test debugging.
For load testing, use CLI Mode (was NON GUI):
   jmeter -n -t [jmx file] -l [results file] -e -o [Path to web report folder]
& increase Java Heap to meet your test requirements:
   Modify current env variable HEAP="-Xms1g -Xmx1g -XX:MaxMetaspaceSize=256m" in the jmeter batch file
Check : https://jmeter.apache.org/usermanual/best-practices.html
================================================================================
Warning: the fonts "Times" and "Times" are not available for the Java logical font "Serif", which may have unexpected appearance or behavior. Re-enable the "Times" font to remove this warning.
Warning: the fonts "Times" and "Times" are not available for the Java logical font "Serif", which may have unexpected appearance or behavior. Re-enable the "Times" font to remove this warning.
```

### Change the theame to System to save the jmx file Option -> Look and feel -> system 

### Test plan 
* parent for any kind of the test plans 
* Change the namne based on the type of the project test 

### Thread Group 
* it will simuilate the uses for testing the system 
* Right Click on Test Plan -> Add -> Threads -> ThreadGroup 
* Change the namne based on the project type 
* Thread Properties 
	* Number of Threads => number of concurrent user 
	* Ramp up Period => after what time Number of courrent user must be increased 
	* Loop Count  => how many times number of courrent user must be increased 

### Sampler 
* it will give option to add the http request types
* Right Click on Thread Group -> Add -> Sampler -> HttpRequest 
* Change the namne based on the type of the request end point 


### Listenr   
* it will give option to veiw the response 
* Right Click on Thread Group -> Add -> Listner -> View Result Tree  
* Change the namne based on the type of the response end point 

### Adding Header Manger 
* Right Click on Http Request -> Config Element -> Header Manger
* Click on add button -> then add the header and values 


### saveing as file 
* top menu button save -> xxx.jmx 
