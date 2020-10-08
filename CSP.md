# Content Security Policy (CSP)

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)

Mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks.

## Example

```ini
Content-Security-Policy:
    # Allow content from current origin
    default-src 'self';

    # Allow images from all origins
    img-src *;

    # Allow audio and video from media.example.com
    media-src media.example.com;

    # Allow JS from scripts.example.com
    script-src scripts.example.com;

    # Report violations to this URL
    report-uri https://csp.example.com
```

## Real-world use

### [ING](https://banking.ing.de/app/obligo)

```ini
content-security-policy:
    # Allow content from current origin and a list of cross-origins
    default-src
        'self'
        *.ing.de
        *.ing-diba.de
        ing-diba.scalable.capital

        # Allow inline scripts
        'unsafe-inline'

        # Allow JS eval()
        'unsafe-eval'
```

### [HEY](https://app.hey.com)

```ini
content-security-policy:
    # Allow scripts from current origin and a list of cross-origins
    script-src
        'self'
        https://production.haystack-assets.com
        stats.hey.com
        *.braintreegateway.com
        *.braintree-api.com
        hcaptcha.com
        *.hcaptcha.com;

    # Block legacy features that don't have <iframe>'s security
    object-src 'none';

    # Block <base> element
    base-uri 'none';

    # Restrict form action URLs
    form-action 'self';

    # Disallow embedding
    frame-ancestors 'none';

    # Report violations to this URL
    report-uri https://sentry.io/api/…
```
