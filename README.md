Code samples for Chapter 7 The IoT Software Package: Raspberry Pi side
- Code application to run in the IoT Device provisioned in Balena platform

# Bug fix!!!
Replace file `sensehat.js` in folder `./nodered/app/node_modules/node-red-node-pi-sense-hat/sensehat.js` by `node-red-node-pi-sense-hat/sensehat.js`
NOTE: This doesn't force to use Python2.7 but any other version for which Sense Hat python drivers work properly

# How to include your Pusher credentials
Make a copy of the `.env.template` file and add you account credentials:
```
$ cd ./nodered/app
$ cp .env.template .env
```
Then add your Pusher credentials to `.env` file

# Run for 32 bits devices (armhf)
Replace the current version of `Dockerfile.template` by `Dockerfile.template.32bits`
```bash
$ cd ./nodered/app
$ cp Dockerfile.template.32bits Dockerfile.template
```
Log into Balena cloud with your credentials and push the local repository with the changes above:
```
$ balena login
$ balena push Sense-IoT-32bits
```

# Run for 64 bits devices (arm64)
Replace the current version of `Dockerfile.template` by `Dockerfile.template.64bits`
```bash
$ cd ./nodered/app
$ cp Dockerfile.template.64bits Dockerfile.template
```
Then proceed as explain above to push the local repository to Balena cloud.
