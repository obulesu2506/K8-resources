Secrets:

Secret is an API object storing confidential data of the containers.

syntax:

```
apiVersion: v1
kind: secret

```
To encode the password & username

```
echo -n <username> | base64

echo -n <password> | base64

```
To decode the username & password

```
echo -n <username> | base64 --decode

echo -n <password> | base64 --decode

```