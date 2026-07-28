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
curl -X GET "https://api.sendcorex.com/v1/disposable/check?email=test@mailinator.com" \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### Node.js

```javascript
const response = await fetch(
  "https://api.sendcorex.com/v1/disposable/check?email=test@mailinator.com",
  {
    headers: { Authorization: "Bearer YOUR_API_KEY" }
  }
);

const data = await response.json();
console.log(data);
// { email: "test@mailinator.com", disposable: true, domain: "mailinator.com" }
```

### Python

```python
import requests

response = requests.get(
    "https://api.sendcorex.com/v1/disposable/check",
    params={"email": "test@mailinator.com"},
    headers={"Authorization": "Bearer YOUR_API_KEY"}
)

print(response.json())
# {"email": "test@mailinator.com", "disposable": true, "domain": "mailinator.com"}
```

### PHP

```php
$ch = curl_init("https://api.sendcorex.com/v1/disposable/check?email=test@mailinator.com");
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTPHEADER, [
    "Authorization: Bearer YOUR_API_KEY"
]);

$response = curl_exec($ch);
curl_close($ch);

print_r(json_decode($response, true));
```

## Example Response

```json
{
  "email": "test@mailinator.com",
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
