# turbo-shy
Fork of https://turbo.hotwired.dev

## Differences from original

Each page visited via Turbo Drive **must** contain the following meta tag:

```html
<meta name="turbo-visit-control" content="allow">
```

Otherwise, a full page reload will be triggered.

In other words, Turbo Drive is a full opt-in. "Focus on 10% of pages where users spend 90% of their time" and all that.

## Background

This fork was created when we tried to use Turbo in our Django project. Django project consist of several "apps", each one of each includes their own independent CSS and HTML templates. Moreover, we used a lot of third-party apps (Django Admin, OpenAPI explorer). So, we wanted an easy way to enable Turbo Drive on our own app while not breaking the others. We could have used `turbo-root` but our app was living on `/`. Hence the fork.

So, now it's enough to include the `<meta>` tag where you want the Turbo Drive to work, and no need to worry about all the other Turbo-unaware pages.
