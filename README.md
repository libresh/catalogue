# Catalog
A placeholder to tackle the FLOSS catalog standardization.

In the rest of the document, application will refer to Free and Libre Web Application. But you can also use it for the broad sense of software, and you can use the same solutions for the same problems.

## Problem space

### Application problem:
```
As a an application maintainer, I want to list service providers.
```

### Hoster problem:
```
As a hoster, I want to list applications I host.
```

## Current Solution space

### Application solutions:

These are examples of catalog of service providers:
 - [Mastodon](https://instances.social/)
 - [Nextcloud](https://nextcloud.com/providers/)
 - [librehosters](https://github.com/libresh/awesome-librehosters)
 - [CHATONS](https://chatons.org/fr/find)
 - [Radical Tech Collectives](https://www.autistici.org/links)

These are 5 examples among many on how to solve the problem.
As you can see these solutions are customs, and not reusable by say, [matrix](https://github.com/matrix-org/matrix.org/issues/95) which has to yet solve the problem one more time.

### Hoster solutions

There is a really nice attempt to solve that with [libreho.st](https://lab.libreho.st/librehosters/librehost-api)

A catalog of application, can also be called [store](https://indieweb.org/store).

 - [yunohost](https://github.com/YunoHost/apps/blob/master/official.json)
 - [disroot](https://disroot.org/en#_white-bar)
 - [Indie.Host](https://indie.host/shop/)

Again, all these solutions are custom, and not really usable.

## Proposed Solution

As you grasp the scale of the problem, now, let's dig deeper.
What if WordPress wants to change the logo?
Yes, it would mean that each store where there is a WordPress logo around the world has to be updated.
As a hoster, I have the same issue, if I want to update my tagline, I have to go everywhere I am listed, and update it.

Let's use [json-ld with Linked Data](https://json-ld.org/), on the official website of those objects, and get the metadata when needed.

### Application Solution:

Let's take the example of mastodon.
Indie.Host has an instance of mastodon. Yet, I have to go to https://instances.social/admin to update the metadata of my instance.

We could imagine a mastodon admin interface to either:
 - fill metadata
 - link to my [website](https://indie.host) where there would be the necessary `json-ld`.

### Hoster Solution:

Let's PR main applications to add a `json-ld` with metadata used by yunohost (maybe the most advanced store so far.)
