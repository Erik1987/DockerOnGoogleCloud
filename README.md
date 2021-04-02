# DockerOnGoogleCloud

## Initializing docker

// use these commands to set up docker user

$ sudo groupadd docker

$ sudo usermod -aG docker ${USER}

$ su - ${USER}

$ sudo usermod -a -G docker ${USER}


$ docker login -u _json_key -p "$(cat keyfile.json)" https://HOSTNAME

where HOSTNAME is gcr.io, us.gcr.io, eu.gcr.io, or asia.gcr.io.

// push

$ docker push eu.gcr.io/PROJECT_ID/myapp-client:latest

// Google sdk

$ gcloud auth login

$ gcloud auth activate-service-account ACCOUNT --key-file=KEY-FILE

ACCOUNT is the service account name in the format [USERNAME]@[PROJECT-ID].iam.gserviceaccount.com. You can view existing service accounts on the Service Accounts page of Cloud Console or with the command gcloud iam service-accounts list
KEY-FILE is the service account key file. See the Identity and Access Management (IAM) documentation for information about creating a key.

$ gcloud auth configure-docker
