# Provision VM and install docker

## Run the setup.sh bash script

You wil be asked about the project name.

```bash
./setup.sh
```

## SSH into the new VM

Visit https://console.cloud.google.com/compute/instances and click the `Connect SSH` button.

## Install docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

## Add your user to the docker group

This is done not having to sudo each docker command. Note to put this change into effect you have to re-open the cloud shell.

```bash
sudo usermod -aG docker $USER
```
