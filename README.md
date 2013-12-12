# Kick it!

Create Kickstarter apps with a snap.

![Kick-it](https://raw.github.com/kostia/kick-it/master/kick-it.png)

## Big fat warning

Until version `0.1.*` (everything starting with `0.0.`) this tool should be assumed as instable
and will be changing __dramatically__.

## Installation

`brew install kick-it`. See https://github.com/kostia/homebrew-infopark.

## Configuration

Create a project in the Infopark-Console at https://console.infopark.net/ with CMS and CRM.
For security reasons a project used with this tool __must__ include a special string `kickme`
in it's name, e.g. `fookickme123`.

Download the configuration ZIP and unpack the files to `~/.config/kick-it`:

```bash
unzip fookickme123-config.zip -d ~/.config/kick-it/
```

### Configuring local repositories

You can use local repositories of the `infopark_cloud_connector` or the `infopark_kickstarter`.
Change the corresponding keys in `~/.config/kick-it/config.yml`.

### Persisting generated apps

By default the apps will be generated in `/tmp/kicks` and thus would not survive a reboot.
In order to "persist" the generated apps you have to change the
corresponding key in `~/.config/kick-it/config.yml`.

## Usage

```
kick-it APP_NAME [OPTIONS]
    -c, --local-cc                   Use local repo for Infopark Cloud Connector gem
    -k, --local-ks                   Use local repo for Infopark Kickstarter gem
    -l, --local                      Use local repos for all Infopark gems
    -f, --force                      Skip all confirmations (assume as confirmed)
    -q, --quiet                      Minimize the output
    -v, --version                    Print the version number
```

## Version

`0.0.4`
