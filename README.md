# UAA Helm Chart

The purpose of this chart is to provide a reference for deploying UAA into Kubernetes and configuring UAA to be a SAML Service Provider and lookup users via LDAP. 

Included in the chart is a test SAML IdP (SimpleSAMLPHP) and an openldap server. 

With these configured UAA can be setup via OIDC\OAUTH to provide authentication flows for concourse, credhub or pinniped. 

~~~sh 
git clone git@github.com:miclip/uaa-chart.git
cd ./uaa-chart 
helm dependency build  
helm install uaa . -n uaa --create-namespace
~~~
