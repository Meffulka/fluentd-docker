# Fluentd

## Purpose

It push the logs [nginx-proxy] (https://github.com/jwilder/nginx-proxy) into elastic.

## docker image

It is based on [the official image of fluentd] (https://hub.docker.com/r/fluent/fluentd/).

Additionally installed plugins:

* `fluent-plugin-rewrite-tag-filter` - for rewriting tags (used to separate stdout and stderr)
* `fluent-plugin-geoip-filter` - to search for geo-location by ip
* `fluent-plugin-record-modifier` - for adding static fields (contour (dev / uat / prod), type (access_log / error_log))
* `fluent-plugin-elasticsearch` - for unloading into elastic
* `fluent-plugin-color-stripper` - uncolored ANSI logs.
