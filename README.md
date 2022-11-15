# Dopomoha.ro - Built with Website Factory

[![GitHub contributors](https://img.shields.io/github/contributors/code4romania/website-factory.svg?style=for-the-badge)](https://github.com/code4romania/website-factory/graphs/contributors) [![GitHub last commit](https://img.shields.io/github/last-commit/code4romania/website-factory.svg?style=for-the-badge)](https://github.com/code4romania/website-factory/commits/master) [![License: MPL 2.0](https://img.shields.io/badge/license-MPL%202.0-brightgreen.svg?style=for-the-badge)](https://opensource.org/licenses/MPL-2.0)

In times of crisis, it is crucial that the necessary resources reach those that are most in need in the simplest and most efficient way. The people who are now displaced by a terrifying conflict need all the support that Romania can offer. But one thing they need before anything else is reliable, timely and straightforward information in response to all the questions and worries they might have about safely entering Romania and navigating the reality of a new country.

Dopomoha (Help) is a web support and information platform for migrants fleeing the war in Ukraine. On this platform they will find information on the entry requirements at the border, the procedure for seeking asylum in Romania, their rights and obligations as asylum seekers and useful resources for their stay in Romania. Dopomoha is available in Romanian, Ukrainian, English and Russian and can be accessed through a browser from any device. 

This platform will be updated regularly with verified information from official sources, for all the displaced migrants in Romania.

Dopomoha is a project created by Code for Romania in partnership with the Department for Emergency Situations(DSU), The UN Refugee Agency, International Organization for Migration (OIM) and the National Romanian Council for Refugees (CNRR). 

[Contributing](#contributing) | [Built with](#built-with) | [Development](#development) | [Deployment](#deployment) | [Feedback](#feedback) | [License](#license) | [About Commit Global](#about-commit-global)

## Contributing

This project is built by amazing volunteers and you can be one of them! Here's a list of ways in [which you can contribute to this project](.github/CONTRIBUTING.md).

## Built with
-   Laravel 8
-   Tailwind CSS
-   Inertia.js
-   Vue.js
-   Alpine.js

### Requirements
-   PHP 8.0+
-   Apache or Nginx
-   MySQL or PostgreSQL

## Development
This project uses Laravel Sail, Laravel's default Docker development environment.

After running the [initial setup](#initial-setup), run this command to start up the environment:
```sh
./vendor/bin/sail up -d
```

and then this command to rebuild the css / js assets on change:

```sh
./vendor/bin/sail npm run watch
```

### Initial setup

```sh
# 1. Install composer dependencies
docker run --rm -v ${PWD}:/app -w /app composer:latest composer install --ignore-platform-reqs --no-scripts --no-interaction --prefer-dist --optimize-autoloader

# 2. Copy the environment variables file
cp .env.example .env

# 3. Start the application
./vendor/bin/sail up -d

# 4. Install npm dependencies
./vendor/bin/sail npm ci

# 5. Build the frontend
./vendor/bin/sail npm run dev

# 6. Generate the app secret key
./vendor/bin/sail artisan key:generate

# 7. Migrate and seed the database
./vendor/bin/sail artisan migrate:fresh --seed
```

For more information on Laravel Sail, check out the [official documentation](https://laravel.com/docs/8.x/sail).

## Deployment

TBD

## Feedback

-   Request a new feature on GitHub.
-   Vote for popular feature requests.
-   File a bug in GitHub Issues.
-   Email us with other feedback contact@commitglobal.org

## License

This project is licensed under the MPL 2.0 License - see the [LICENSE](LICENSE) file for details

## About Code4Ro

The team behind Commit Global has a robust and celebrated track record in the tech for social good field since 2015. We have built the fastest growing organization in the space, Code for Romania and set it up as a model of good practices on how to design and build technology that helps at scale. Our tools have served governments, UN agencies and large and small CSOs during crisis and peace time. Most recently we have built, deployed and maintained a first of its kind humanitarian ecosystem in support of refugees fleeing from Ukraine, ensuring their safe and uninterrupted access to information, healthcare and services, while equipping NGOs with the tools they need to be more effective.

All throughout our activity we have been one of the champions of cooperation and co-creation in the the civic tech field, constantly investing efforts and resources in working with and supporting the work of similar organizations around the world. As part of these efforts we created, curated and hosted the largest civic tech strategic event in history, the 2018 Code for All Global Summit: a 4 days offline event where hundreds of delegates from all continents exchanged ideas and digital solutions for the benefit of humanity.

Find more details on https://www.commitglobal.org/en
