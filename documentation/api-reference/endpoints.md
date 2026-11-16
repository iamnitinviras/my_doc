# Endpoints

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/items` | List items. |
| `GET` | `/items/{id}` | Get one item. |
| `POST` | `/items` | Create an item. |
| `DELETE` | `/items/{id}` | Delete an item. |

## Example: create an item

```bash
curl -X POST https://api.example.com/v1/items \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"name": "Widget", "price": 9.99}'
```

Response:

```json
{
  "id": "itm_123",
  "name": "Widget",
  "price": 9.99
}
```

{% hint style="warning" %}
`DELETE` cannot be undone.
{% endhint %}
