# Disposable Email Domains

Block temporary, throwaway, and disposable email addresses in real time. Free API with 200,000+ known disposable domains, backed by [Sendcorex](https://sendcorex.com).

🔗 **Live site:** [https://disposable.sendcorex.com](https://disposable.sendcorex.com)

## What is this?

A fast, free API to detect and block disposable/temporary email addresses at signup, checkout, or anywhere else you collect emails. Stop fake signups, reduce spam, and keep your user base clean — without maintaining your own blocklist.

- ✅ 200,000+ known disposable domains, updated continuously
- ✅ Simple REST API — one request, instant answer
- ✅ Free to start, no credit card required
- ✅ Works with any language via HTTP (Node.js, PHP, Python, Java, C#, Ruby, Go, cURL)

## Get an API Key

Sign up and generate your free API key here:

👉 [https://disposable.sendcorex.com](https://disposable.sendcorex.com) → **Get Started**

## Quick Start

### cURL

```bash
curl -X POST \
  https://graph.sendcorex.com/v4/mail/isdisposable \
  -H 'Authorization: API_KEY' \
  -d '{"email":"user@mailinator.com"}'
```

### Node.js

```javascript
const response = await fetch("https://graph.sendcorex.com/v4/mail/isdisposable", {
  method: "POST",
  headers: {
    "Authorization": "API_KEY",
    "Content-Type": "application/json"
  },
  body: JSON.stringify({ email: "user@mailinator.com" })
});

const data = await response.json();
console.log(data);
// { email: "user@mailinator.com", disposable: true, domain: "mailinator.com" }
```

### Python

```python
import requests

response = requests.post(
    "https://graph.sendcorex.com/v4/mail/isdisposable",
    json={"email": "user@mailinator.com"},
    headers={"Authorization": "API_KEY"}
)

print(response.json())
# {"email": "user@mailinator.com", "disposable": true, "domain": "mailinator.com"}
```

### PHP

```php
$ch = curl_init("https://graph.sendcorex.com/v4/mail/isdisposable");
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, json_encode(["email" => "user@mailinator.com"]));
curl_setopt($ch, CURLOPT_HTTPHEADER, [
    "Authorization: API_KEY",
    "Content-Type: application/json"
]);

$response = curl_exec($ch);
curl_close($ch);

print_r(json_decode($response, true));
```

## Example Response

```json
{
  "email": "user@mailinator.com",
  "domain": "mailinator.com",
  "disposable": true
}
```

## Documentation

Full API reference, SDKs, and integration guides:
📖 [https://docs.sendcorex.com/disposable](https://docs.sendcorex.com/disposable)

## Support

Questions or feedback? Reach out at [hi.core@reply.sendcorex.com](mailto:hi.core@reply.sendcorex.com)

---

Built and maintained by [Sendcorex](https://sendcorex.com) — reliable email infrastructure for developers.
