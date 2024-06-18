---
description: Installation of the app
---

# 👊 Quick start

{% hint style="warning" %}
Currently, the installation process is not automated, but it is straightforward and requires only a few steps.
{% endhint %}

To download, install, and start using the application, please follow these steps:

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

or automatically

{% tabs %}
{% tab title="Windows" %}
Run the following script

```
.\utilScripts\pack_GO.bat
```
{% endtab %}

{% tab title="Linux" %}
Run the following script

```
bash utilScripts/pack_GO_linux.sh
```
{% endtab %}
{% endtabs %}

Setting up the python environment

{% tabs %}
{% tab title="Windows" %}
Run the following script

```
.\pythonEnv\create_conda_env_win.bat
```
{% endtab %}

{% tab title="Linux" %}
Run the following script

```
bash pythonEnv/create_conda_env_linux.sh
```
{% endtab %}
{% endtabs %}

This will create a [conda environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) named `med_conda_env` and install the required packages.

When developing python code, you may need to install new packages. To do so, you can activate the environment and install any package with pip:

```
conda activate med_conda_env
pip install <package_name>
```

### RUN THE APP

```
npm run dev
```

**Now that the app is live and running, it is time to learn how to use the interface, see you on the next page** :wink:
