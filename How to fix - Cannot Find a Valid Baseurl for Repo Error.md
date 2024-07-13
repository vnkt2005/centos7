This error indicates that yum is not capable of accessing base repository while executing the given command. 
There may be two possibilities of error.

1. Network issues
2. Base url is commented out in the configuration file

try the following command and check whether any network issues is causing the problem.
```sh
  $ping google.com
```

# vi /etc/yum.repos.d/CentOS-Base.repo
Look for the [base] section, try uncommenting the baseurl by removing the leading # on the baseurl line.
