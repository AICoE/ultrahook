# Ultrahook Client for OpenShift

This repository contains s2i ready OpenShift application based on Ultrahook Client

## Local build

Build locally as:

```
s2i build --copy . centos/ruby-24-centos7 ultrahook
```

Run locally as:

```
docker run --rm -it -e ULTRAHOOK_API_KEY=<your_api_key> -e ULTRAHOOK_SUBDOMAIN=<some_subdomain> -e ULTRAHOOK_DESTINATION=<destination_url> ultrahook
```

## Deployment

To import the template, run:

```
oc apply -f openshift/template.yaml
```

To deploy the ultrahook client, run:

```
oc process ultrahook ULTRAHOOK_API_KEY=<your_api_key> ULTRAHOOK_SUBDOMAIN=<some_subdomain> ULTRAHOOK_DESTINATION=<destination_url> | oc apply -f -
```

Or you can do the same thing in OpenShift Console UI
