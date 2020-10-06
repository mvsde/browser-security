# Definition of “Origin”

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Glossary/origin)

The **origin** is defined by:

* Scheme (protocol): `https`
* Host (domain): `example.com`
* Port: `:80`

## Same origin

| Site A                    | Site B                    | Reason               |
| ------------------------- | ------------------------- | -------------------- |
| https://example.com/hello | https://example.com/world | Same scheme and host |
| https://example.com       | https://example.com:80    | Port `80` is default |

## Different origin

| Site A              | Site B                   | Reason            |
| ------------------- | ------------------------ | ----------------- |
| https://example.com | http://example.com       | Different schemes |
| https://example.com | https://www.example.com  | Different hosts   |
| https://example.com | https://example.com:8080 | Differen ports    |
