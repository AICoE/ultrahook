# ultrahook-openshift
Ultrahook Client for OpenShift

This repository contains s2i ready OpenShift application based on Ultrahook Client

Build locally as:

```
s2i build --copy . centos/ruby-24-centos7 ultrahook
```

Run locally as:

```
docker run --rm -it -e ULTRAHOOK_API_KEY=<your_api_key> -e ULTRAHOOK_SUBDOMAIN=<some_subdomain> -e ULTRAHOOK_DESTINATION=<destination_url> ultrahook
```

