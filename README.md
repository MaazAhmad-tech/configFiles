# configFiles

Externalized configuration files for the `accounts`, `cards`, and `loans` microservices.

The `contactDetails.email` values are stored in encrypted form with Spring Cloud Config's `{cipher}` format so the public repository does not expose them in plain text.

To generate new encrypted values locally, start the config server with the same `ENCRYPT_KEY` and call:

```bash
curl -X POST http://localhost:8071/encrypt \
  -H "Content-Type: text/plain" \
  --data-urlencode "=plain-text-value"
```
