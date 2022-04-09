# turbo-shy

Fork of https://turbo.hotwired.dev

#### CDN

```html
<script type="module" src="https://cdn.jsdelivr.net/gh/m1kc/turbo-shy/turbo-shy-7.1.0.js"></script>
```

## Differences from original

Each page visited via Turbo Drive **must** contain the following meta tag:

```html
<meta name="turbo-visit-control" content="allow">
```

Otherwise, a full page reload will be triggered.

In other words, Turbo Drive is a per-page opt-in. "Focus on 10% of pages where users spend 90% of their time" and all that.

## Background

This fork was created when we tried to use Turbo in our Django project. Django projects consist of several "apps", each one includes their own independent CSS and HTML templates. Moreover, we use a lot of third-party apps (Django Admin, OpenAPI explorer). So, we wanted an easy way to enable Turbo Drive on our own app while not breaking the others. We could have used `turbo-root` but our app was living on `/` so that wasn't an option. Hence the fork.

So, now it's enough to include the `<meta>` tag where you want the Turbo Drive to work, and no need to worry about all the other Turbo-unaware pages.
