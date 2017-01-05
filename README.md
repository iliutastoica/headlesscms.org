# jamstackcms

[jamstackcms.com](http://www.jamstackcms.com), a leaderboard of top open-source static site content management systems.

## Contributing

Missing a static site generator here? Just fork the repo and add your generator
as a `<name>.md` in the `source/projects` folder.

Make sure to follow the following rules:

*   **Static Site Generation:** No "flat-file CMSs". The program must be able to output a static website that can be hosted in places like Netlify, S3 or Github Pages.
*   **Stick to the format:** Fill out all the same fields as the other CMS's in `source/projects`.
*   **Short description:** Keep all the details for the body text, keep the description for the overview page short and sweet.

## Running locally

jamstackcms is built with Middleman. To install and run locally:

    git clone https://github.com/netlify/staticgen.git
    cd jamstackcms
    bundle install
    bundle exec middleman

You'll run into GitHub's API limits very quickly if you just do this. To avoid this we recommend you create a Github API token with permissions to access public repositories and Gist.

Then create a Gist with a single file `data.json` with an empty javascript object literal as content: {}

Then set these environment variables before running middleman:

    export GITHUB_TOKEN=YOUR_TOKEN
    export GIST_ID=ID_OF_YOUR_GIST

Then middleman will use the Gist you specified to archive stats (stars, forks and issues) for the repositories.

## Netlify

jamstackcms is built and maintained by [Netlify](https://www.netlify.com), a hosting and automation service for static websites and apps.

## License
This project is licensed under the [MIT license](http://opensource.org/licenses/MIT).
