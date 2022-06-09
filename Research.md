# GRAD22 Research

We took a number of different routes in this investigation in order to find a way to store and add modules to GitHub. Like the Scott Logic blog, we wanted to be able to store our content in markdown files via github that would be displayed on the main site. This would allow easy adding and editing of modules. Each module needed to include information that the user would require, such as a list of modules that needed to be completed before starting the current one, labels which could be used to easily sort similar modules and a link to the repo that graduates will work off of. Some of the approaches we took include:

## Markdown to JSX

A tool was found that would allow us to convert the markdown files containing each module into JSX which would be displayable in the base react app. Whilst this was a good way to display the modules, it would lack functionality with tagging.

## Github Pages

GitHub pages was initially dismissed as the it wouldn’t be possible to use a custom url without a premium version of github. However, it was discovered that it was possible to display pages on an iframe within the react app. A quick demo was put together which would swap between pages on a button press on the app.

## Markdown to JSON with GitHub actions

GitHub actions allowed any markdown file to be converted to a JSON file when it was committed. This allowed the creation of a file that could easily be used in the main application, complete with labels to sort the modules and a list of dependencies for each.
