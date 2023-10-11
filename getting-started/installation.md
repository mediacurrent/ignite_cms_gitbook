# Installation

### Checkout codebase <a href="#newprojectsetup-checkoutinitialcodebase" id="newprojectsetup-checkoutinitialcodebase"></a>

The Ignite packages are available for you to clone in a modified version of the [recommended Drupal composer template](https://github.com/drupal/recommended-project).

The project is hosted on a public Bitbucket repo which can be cloned using the following command:

```
git clone git@bitbucket.org:mediacurrent/drupal-project.git shortcode_project
```

Change to the project folder and run the following command to initialize the codebase.

```
composer install
rm web/sites/default/.gitignore
```

This runs composer install. As this is the first time being run, it is a composer update and calculates all dependencies.

### Spin-up your local environment <a href="#newprojectsetup-checkoutinitialcodebase" id="newprojectsetup-checkoutinitialcodebase"></a>

Any local development tool should work, at [Mediacurrent](https://www.mediacurrent.com) we use DDEV. \
DDEV users can use the setup instructions below:

<details>

<summary>DDEV Configuration</summary>

#### Run DDEV’s configuration tool

You can pass in defaults (recommended options below), or you can run it without arguments for an interactive configuration tool.

```
# Option 1: Non-interactive configuration. Project names must be alphanumeric and/or hyphenated.
ddev config --docroot=web --project-name="project" --project-type=drupal10 --webserver-type="nginx-fpm" --create-docroot

# Option 2: Interactive configuration
ddev config
```

* Project name ( as above this is typically the first part of the domain name.)
* Docroot Location = web
* Project Type = drupal10

#### Start DDEV <a href="#newprojectsetup-startddev" id="newprojectsetup-startddev"></a>

After configuration has been completed, start the ddev containers.

```
ddev start
```

</details>

### Initialize Project <a href="#newprojectsetup-initializeproject" id="newprojectsetup-initializeproject"></a>

Run the following commands to initialize the project.

```
./scripts/hobson project:init project.ddev.site
```

* This command ensures the `config/config.yml` is in place and has the domain set.

### Restart environment <a href="#newprojectsetup-restartddev" id="newprojectsetup-restartddev"></a>

If DDEV is being used as the local environment, run the following command:

```
ddev restart
```

### Advanced Configuration <a href="#newprojectsetup-restartddev" id="newprojectsetup-restartddev"></a>

For additional configuration options, see our [Advanced configuration guide](advanced-configuration.md).

### &#x20;<a href="#newprojectsetup-restartddev" id="newprojectsetup-restartddev"></a>

{% hint style="success" %}
### Install the Ignite Demo (optional) <a href="#newprojectsetup-restartddev" id="newprojectsetup-restartddev"></a>

The following command will run a full Composer install and site installation using the Ignite Demo profile.

**`./scripts/build.sh`**

This will install the full Ignite Demo experience with sample content.&#x20;
{% endhint %}

Congratulations, you have installed Ignite CMS!&#x20;
