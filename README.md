# Drip Managed8 Composer Template
A project template for Drupal 8 sites on Managed Hosting with a docroot directory and modified .gitignore to allow all site files to be committed and tagged for release.

## Starterlight Theme
Our front-end developer team has put together a Drupal 8 starter theme called [Starterlight](https://github.com/zivtech/starterlight) to use for starting new Drupal 8 theming projects. See the [Starterlight](https://github.com/zivtech/starterlight) project page on GitHub for documentation.

## Lando Integration
This repository is ready to use out of the box in [Lando](https://docs.lando.dev/) for local development. Make sure to rename the Lando project in the .lando.yml file.

## Probo Integration
This repository is ready to be integrated with [Probo.CI](https://probo.ci/) to install a fresh copy of Drupal 8. Additional configuration to the .probo.yaml file is required to manage configuration imports after the site has been installed.

## How to Use This Template
Below you can find step by step documentation for creating a new Drupal 8 project repository controlled by Composer that lives on GitHub and is hosted on a Managed hosting environment.

*Requirements:* [Lando](https://github.com/lando/lando/releases)

1. Create a new GitHub repository for the project site using this repository as a template.
2. Clone the new repository and rename the project's name value in the [.lando.yaml](https://github.com/zivtech/drip-managed8/blob/main/.lando.yml) file.

        name: cooldrupalproject
3. Start the Lando project.

        lando start
4. [Connect Probo.CI](https://docs.probo.ci/) to the new GitHub repository for testing changes in Pull Requests.
5. Composer require any additional contrib projects and commit the changes to a Feature Branch.

        lando composer require drupal/webform
6. Create a Pull Request based on the Feature Branch on GitHub to test the new project site on Probo.CI.
7. Create a git Tag for code releases when applicable.

        git tag 1.0.0
        git push --tags
8. Pull the site code down to the desired server(s) as needed.

        git fetch
        git checkout 1.0.0
