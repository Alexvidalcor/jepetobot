
**CURRENT STATUS: BETA**

<img src="https://raw.githubusercontent.com/Alexvidalcor/jepetobot/master/src/images/Readme-logo1.png" width="500" />

_Telegram bot developed to explore the AI possibilities of OpenAI_

_Support for deployment on AWS is included through Github Actions_

## Main features :fire:

### AWS cloud deployment support.

* IaC (Infrastructure as Code) support for cloud infrastructure on Amazon Web Services is included through the AWS CDK.

* Support for local execution is also included.

### Automated deployment of cloud infrastructure and code.

* The deployment of cloud infrastructure on AWS has been automated through Github Actions (See [cdk_deploy_resources.yaml](https://github.com/Alexvidalcor/jepetobot/blob/master/.github/workflows/cdk_deploy_resources.yaml))

* New code releases have also been automated via github actions and docker containers (See [update_application.yaml](https://github.com/Alexvidalcor/jepetobot/blob/master/.github/workflows/update_application.yaml))

### Easy access to ChatGPT (GPT3.5-turbo) from Telegram

Adapted to the latest chatgpt model | 'Identity' change from bot options | 'Temperature' change from bot options
--- | --- | --- |
 | <img src="https://raw.githubusercontent.com/Alexvidalcor/jepetobot/master/src/images/Readme-image1.gif" height="400" width="300"/> | <img src="https://raw.githubusercontent.com/Alexvidalcor/jepetobot/master/src/images/Readme-image2.gif" height="400" width="300"/> | <img src="https://raw.githubusercontent.com/Alexvidalcor/jepetobot/master/src/images/Readme-image3.gif" height="400" width="300"/> |
 
### Management system of users

* A system has been added to enable or deny access to specific user IDs

* The user management system can also be applied to the configuration access.


## Getting started 🚀


### Debian-based/Fedora Linux distribution 

_Manual Installation (terminal commands):_

```
git clone https://github.com/Alexvidalcor/jepetobot
cd jepetobot/
python3 src/installation/install.py
./src/installation/execute.sh
```

_Installation using Docker (it is required to have Docker installed previously):_

```
git clone https://github.com/Alexvidalcor/jepetobot
cd jepetobot/
docker build -t jepetobot . 
docker run -d -it --name jepetobot_cont jepetobot
```

_Get Telegram Token_

It is necessary to obtain a token from the Telegram Bot API.

Instructions for it are [HERE](https://core.telegram.org/bots#how-do-i-create-a-bot)

_Get OpenAI Token_

It is necessary to obtain a token from the OpenAI API.

Instructions for it are [HERE](https://platform.openai.com/docs/introduction/tokens)


| :exclamation:  Check the [Wiki](https://github.com/Alexvidalcor/jepetobot/wiki) for more info!  |
|-----------------------------------------|

## Cloud Deployment 📦

**Manual deploy in AWS:**

Need to have CDK pre-installed (Click [here](https://aws.amazon.com/getting-started/guides/setup-cdk/) for more information). 

Once CDK is installed and configured, run the following commands:

```
cdk synth

cdk deploy --all
```

**Automatic deploy in AWS via Github Actions:**

Currently there are two Github Actions workflows prepared to automate the deployment:

* _cdk_deploy_resources.yaml_

Resources | EC2 | S3| secretmanager | codedeploy |
--- | --- | --- | --- |--- |
Purpose | Machine where the application is hosted | Bucket where application versions are stored | Secret Manager inside AWS | Automates the deployment of new versions of the application | 

* _update_application.yaml_

Update cloud app code with every push to master branch. It generates a slight service downtime of a few seconds.

| :zap:        All use of cloud generates costs, use it at your own risk!   |
|-----------------------------------------|

## Wiki :closed_book:

For detailed information, check the project [Wiki](https://github.com/Alexvidalcor/jepetobot/wiki)


## Built with 🛠️

* [AWS-CDK](https://aws.amazon.com/es/cdk/) - Deploy on AWS.
* [Python-Telegram-Bot](https://python-telegram-bot.org) - Telegram Api Wrapper.
* [OpenAI-Api](https://openai.com/api/) - AI api


## Disclaimer :memo:

* I'm not responsible for bricked devices or software misconfigurations.
* I'm not responsible for possible high cloud costs generated by using the code of this project.
    * **You are free to use the software of this project and it is your decision**. As I explain in the [wiki](https://github.com/Alexvidalcor/jepetobot/wiki), this project originates from an experiment and fully stable operation is not guaranteed.


## License :pushpin:

This project is licensed under the License (GNU GPL-V3) - see the [LICENSE.md](LICENSE.md) file for details.


---

⌨️ with ❤️ by [Alexvidalcor](https://github.com/Alexvidalcor) 😊
