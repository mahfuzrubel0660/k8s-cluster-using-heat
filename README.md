# k8s-example-via-gui

Prerequisite:
~~~
1. openstack python client
2. Openstack python heat client
3. openstack credential
~~~

Ubuntu
~~~
apt install python-openstackclient
pip install python-heatclient
~~~

Change the following as per your environment

## vi creds
~~~
export OS_USERNAME=
export OS_PASSWORD=
export OS_PROJECT_NAME=
export OS_USER_DOMAIN_NAME=Default
export OS_PROJECT_DOMAIN_NAME=Default
export OS_AUTH_URL=http://cloud.brilliant.com.bd:5000/v3
export OS_IDENTITY_API_VERSION=3
export OS_IMAGE_API_VERSION=2
export OS_AUTH_TYPE=password
~~~

$ source creds

$ openstack stack create -t stack_full.yaml -e env.yaml k8s-cluster --wait
