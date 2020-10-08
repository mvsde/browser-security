# Definition of “Origin”

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Glossary/origin)

The **origin** is defined by:

* Scheme (`https`)
* Host (`example.com`)
* Port (`:443`)

## Same origin

| Site A                    | Site B                    | Reason                |
| ------------------------- | ------------------------- | --------------------- |
| https://example.com/hello | https://example.com/world | Same scheme and host  |
| https://example.com       | https://example.com:443   | Port `443` is default |

## Different origin

| Site A              | Site B                   | Reason            |
| ------------------- | ------------------------ | ----------------- |
| https://example.com | http://example.com       | Different schemes |
| https://example.com | https://www.example.com  | Different hosts   |
| https://example.com | https://example.com:8080 | Different ports   |
