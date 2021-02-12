# Drip Managed8 Composer Template
A project template for Drupal 8 sites on Managed Hosting with a docroot directory and modified .gitignore to allow all site files to be committed and tagged for release.

## Starterlight Theme
Our front-end developer team has put together a Drupal 8 starter theme called [Starterlight](https://github.com/zivtech/starterlight) to use for starting new Drupal 8 theming projects. See the [Starterlight](https://github.com/zivtech/starterlight) project page on GitHub for documentation.

## Lando Integration
This repository is ready to use out of the box in Lando for local development. Make sure to rename the Lando project in the .lando.yml file.

## Probo Integration
This repository is ready to be integrated with [Probo.CI](https://probo.ci/) to install a fresh copy of Drupal 8. Additional configuration to the .probo.yaml file is required to manage configuration imports after the site has been installed.
