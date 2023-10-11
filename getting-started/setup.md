# Setup

As noted in our Installation guide, the project build script will install the full Ignite Demo experience by default. This is great for evaluating Ignite CMS.

Some developers will want to start with just the basics. To create a new install profile without any features enabled you can use our hobson "project:create-profile" command.

#### Create custom profile <a href="#newprojectsetup-clonemis_profileusinghobson" id="newprojectsetup-clonemis_profileusinghobson"></a>

This command will automatically create a basic custom Ignite profile with no optional features enabled.

```
./scripts/hobson project:create-profile --name="example"
```

**Update config.yml**

After you have created your new install profile you can change the "drupal\_install\_profile" value in config/config.yml to your new profile name.

Once you have made this change you can re-run build.sh.

**Enabling features**

Once you have installed your site you can enable content type and block features individually.

<figure><img src="../.gitbook/assets/Screen Shot 2023-05-24 at 11.18.12 AM.png" alt=""><figcaption><p>Ignite Features</p></figcaption></figure>
