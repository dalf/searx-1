# Searx

builds custom searx container with a changed simple theme and settings.yml; This project builds on top of https://github.com/searxng/searxng (searxng vs searx: https://github.com/searxng/searxng/issues/46).

Check out https://start.paulgo.io for a deployed server with this container


### Environment Variables (all optional: if not set -> using default settings)

* ```MORTY_KEY``` : set the morty key in the settings.yml file (it also enables/disables image proxy)

* ```DOMAIN``` : set the domain for instance name and morty, as well as the base url (for example example.org would have `https://example.org/` as base and `https://example.org/morty` as morty url)

* ```CONTACT``` : set instance maintainer contact (for example `mailto:user@example.org`)

* ```ISSUE_URL``` : set issue url for custom searx repo (for example `https://github.com/paulgoio/searx/issues` !Without trailing /)


### Basic Example

* ```docker run -it --rm -p 8080:8080 paulgoio/searx:production```

* After that just visit http://127.0.0.1:8080 in your browser and stop the server with ctrl-c


### Production Setup

Check out the `docker-compose.yml` file in this repo for reference (it also uses a custom filtron image for a complete stateless setup)
