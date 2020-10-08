# Feature Policy

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Feature_Policy)

Enable or disable certain browser features and APIs.

## Example

### HTTP Header

```ini
feature-policy:
    # Disable geolocation
    geolocation 'none';

    # Allow camera for current origin
    camera 'self';

    # Allow fullscreen for content from example.com
    fullscreen https://example.com
```

### iframe

```html
<!-- Allow fullscreen and PiP for this iframe -->
<iframe
    src="https://example.com/video"
    allow="fullscreen; picture-in-picture"
></iframe>
```
