---
description: Installation of the app
---

# 👊 Quick start

## Automatic installation

{% hint style="warning" %}
Below are tutorials for downloading and installing the app on various operating systems. The tutorials provided are for MEDomicsLab (the parent app), and the instructions remain the same. However, please use the following link to download the assets for the MEDimage-app: [MEDimage-app release](https://github.com/MEDomics-UdeS/MEDimage-app/releases/tag/v0.0.1).
{% endhint %}

{% tabs %}
{% tab title="Windows" %}
{% embed url="https://www.youtube.com/watch?ab_channel=MEDomicsLab&v=MSPWubu8qK8" %}
{% endtab %}

{% tab title="Ubuntu" %}
{% embed url="https://www.youtube.com/watch?ab_channel=MEDomicsLab&v=7OCasKO8zJU" %}
{% endtab %}

{% tab title="MacOS" %}
{% embed url="https://www.youtube.com/watch?ab_channel=MEDomicsLab&v=J9wq_C6PHK0" %}
{% endtab %}
{% endtabs %}

## Manual installation

To manually download, install, and start using the application, please follow these steps:

#### Cloning the project

Via SSH (recommended)

```
git clone -b develop git@github.com:MEDomics-UdeS/MEDimage-app.git
```

Via HTTPS

```
git clone -b develop https://github.com/MEDomics-UdeS/MEDimage-app.git
```

#### Installing [npm ](https://www.npmjs.com/)package

Access the cloned folder

```
cd <.../MEDimage-app/>
```

Install npm packages

```
npm install
```

#### Building [go server](https://go.dev/) files

Manually

```
cd go_server
go build main.go
```

or automatically, by running the following script

{% tabs %}
{% tab title="Windows" %}
```
.\utilScripts\pack_GO.bat
```
{% endtab %}

{% tab title="Ubuntu" %}
```
bash utilScripts/pack_GO_linux.sh
```
{% endtab %}

{% tab title="MacOS" %}
```
bash utilScripts/pack_GO_mac.sh
```
{% endtab %}
{% endtabs %}

Set up the python environment, by running the following script

{% tabs %}
{% tab title="Windows" %}
```
.\pythonEnv\create_conda_env_win.bat
```
{% endtab %}

{% tab title="Ubuntu" %}
Run the following script

```
bash pythonEnv/create_conda_env_linux.sh
```
{% endtab %}

{% tab title="macOS" %}
```
zsh pythonEnv/create_conda_env_mac.sh
```
{% endtab %}
{% endtabs %}

This will create a [conda environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) named `med_conda_env` and install the required packages.

***

_When developing python code, you may need to install new packages. To do so, you can activate the environment and install any package with pip:_

```
conda activate med_conda_env
pip install <package_name>
```

***

### RUN THE APP

```
npm run dev
```

**Now that the app is live and running, it is time to learn how to use the interface, see you on the next page** :wink:
