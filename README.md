
## About

This is the status site for the BCDevX Platform Services technical operations. It is used to communicate the status of shared services, hosted on and including the OpenShift Container Platform (OCP). When a service disruption is detected this site will be updated with relevant information. Once the service disruption is address, we'll post an incident report here.

This site is served via github.io and can be viewed at two URLs:

[github.io](https://bcgov.github.io/platform-services-status)

[Vanity URL](https://status.devops.gov.bc.ca/)

## How to Update

Below are instructions on how to update the relevant components of this site.

**Pro Tip** 🤓

Its a good idea to test your changes before you publish them. See them `Development` section below. If your YAML above is malformed the site may present itself incorrectly.

### Update Service Status

In the event of a service disruption you will want to update the file `index.md`. Open the file in your favorite editor, or in a pinch you can use the GitHub Web UI and change the `frontmatter`; that's the little blurb of YAML at the top of the file:

```yaml
---
# Use the following two color codes for status box background
# colours a.k.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "All services are operating normally"
bgcolour: "#d2f8d2"
description: ""
status:
    ocp: "Operational"
    sso: "Operational"
    rc: "Operational"
    mss: "Operational"
---
```

Edit it to reflect the ongoing incident. Keep the `message` very short, it does not have much space to expand. Use the `description` to add meaningful updates. Once the outage is over reset this section and add an incident report (see below).

```yaml
---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "Platform wide service disruption"
bgcolour: "#ff9999"
description: |
    We are investigating what appears to be a system wide outage effecting a wide range of services including OCP, SSO and
    RocketChat.
status:
    ocp: "Down"
    sso: "Down"
    rc: "Down"
    mss: "Down"
---
```

When this change is merged into the `master` branch it will take about 60 seconds before it is widely available. 

### Add an Incident Report

Once an incident is complete it is good platform etiquette to publish an incident report so the wider user base can better understand the current state of things. To do this just create a new markdown file in the `_posts` directlry following the naming convection of existing files.

Once your have merged your update into the `master` branch it will take about 60 seconds before it is widely available.

## Development

The best way to do local development is to use docker. Follow the instructions below and you should be up-and-running in no time:

1. Clone the repo, and change to the newly minted directory;
2. Fire up the Jekyll docker container:

```console
docker run -it --rm --name jekyll -v $(pwd):/srv/jekyll -p 4000:4000 jekyll/jekyll /bin/bash
```
3. Update the bundler:

```console
gem install bundler
```
4. Run the local Jekyll server:

```console
jekyll serve --watch --force_polling
```

That's it. It'll install some packages. When done, you'll see something that looks the output below. Point your browser to `http://localhost:4000` and you should see the site! Because you're running in watch mode every time you change a file it will re-compile the site and immediately serve out your changes.

```console
ruby 2.6.5p114 (2019-10-01 revision 67812) [x86_64-linux-musl]
Configuration file: /srv/jekyll/_config.yml
            Source: /srv/jekyll
       Destination: /srv/jekyll/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.585 seconds.
 Auto-regeneration: enabled for '/srv/jekyll'
    Server address: http://0.0.0.0:4000
  Server running... press ctrl-c to stop.
  ```

## Project Status / Goals / Roadmap

This project is ongoing.

## Getting Help or Reporting an Issue

Send a note to bcdevexchange@gov.bc.ca and you'll get routed to the right person to help you out.

## How to Contribute

This project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## License

Text components of this site are licensed Creative Commons Attribution 4.0 International License where as code components are Apache 2.0.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">platform-services-status</span> by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">the Province of British Columbia</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
