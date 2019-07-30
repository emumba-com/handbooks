Logging helps in debugging and can be a powerful tool in developer's toolkit when done properly.
*  Never use raw print statements (`console.log` in Node.JS, `print` in python).
*  Always define the logging configuration in the log config files.
*  Use instance of logging class/library in your module/class for logging. For example you can use `Winston` for Node.JS, `Log4J` for Java, and builtin-in Logging class of Python. 
* First choice should be to send logs (using config files) into standard output and let the environment handle the logs in whatever way it wants. 
*  Second best solution is to dump log statements into some log files which should be rotated date-wise.
*  Never log sensitive information