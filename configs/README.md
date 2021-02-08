# upstreams

I couldn't find this in the docs, but upstreams.conf has to have the format

```nginx
upstream subdomain-name {
    server subdomain-name.rest.of.domain
}
```

lest confusing behaviour result.

For example

```nginx
upstream other-name {
    server subdomain-name.rest.of.domain
}
```

ends up going to other-name.rest.of.domain.