# Module.md to JSON tool

> ⚠️ **The repository MUST have write permissions enabled for workflows for this to work on push**

## What does this tool do?

Our training modules are stored in the folder `modules` and each module has its own `moduleFolder` where a `markdown.md` file is used to write each module.

When a change is made to a `module.md` or a new `module.md` is made in the correct directory, on push to the github repo or tool is activated.

A gitHub action is started which will process all the `module.md` files and consolodate them into a single `output.json` ready to be grabbed and processed by the main application.

## Requirments

As this will be used in a separate Scott Logic repository that will be used for storing and editing modules there are a few requirements that the repository must have.

**GitHub actions must be enabled** on the repository as this is where the conversion of the markdown files into the JSON takes place, currently this is set to be on push to main or on pull request to main but this can be updated to meet other requirements.

The repository needs to allow GitHub workflows to have **write permissions** so that when the JSON has been generated it can be pushed into the repo.

## Style guide

In the style guide folder a template for what a module should look like along with a more detailed explanation of individual parts can be found.

## To run conversion tool locally

This tool will only run in github actions if a change or new file is detected. If for whatever reason it doesnt run these commands can be run manually locally before push to update the `output.json`
<br />

```
npm install
npx markdown-json -c settings.json
```
