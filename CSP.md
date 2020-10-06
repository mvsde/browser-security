# Content Security Policy (CSP)

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)

Mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks.

## Example

```ini
Content-Security-Policy:
    # Allow content from current origin
    default-src 'self';

    # Allow all images
    img-src *;

    # Allow audio and video from media.example.com
    media-src media.example.com;

    # Allow JS from scripts.example.com
    script-src scripts.example.com;

    # Report violations
    report-uri https://csp.example.com
```

## Real-world use

### [ING](https://banking.ing.de/app/obligo)

```ini
content-security-policy:
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
    # Allow scripts from current origin and a few third-parties
    script-src
        'self'
        https://production.haystack-assets.com
        stats.hey.com
        *.braintreegateway.com
        *.braintree-api.com
        hcaptcha.com
        *.hcaptcha.com;

    # Block legacy features that may not have <iframe>'s security
    object-src 'none';

    # Block <base> element
    base-uri 'none';

    # Restrict ofrm action URLs
    form-action 'self';

    # Disallow embedding
    frame-ancestors 'none';

    report-uri https://sentry.io/api/…
```
