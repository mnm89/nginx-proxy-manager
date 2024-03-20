This is an example of serving 3 angular applications with nginx proxy manager under 3 different pathnames

 - /first-app
 - /second-app
 - /third-app

Note that there is a custom configuration for the proxy host as configuring a custom location with the nginx proxy manager is not working ... 

Open Issue: https://github.com/NginxProxyManager/nginx-proxy-manager/issues/3512 

PS: every angular application has a baseHref configured respectively within its angular.json file
