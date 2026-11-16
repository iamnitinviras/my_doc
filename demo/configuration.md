# Configuration

Demo reads its settings from `demo.config.json` in the project root.

```json
{
  "title": "My Project",
  "theme": "light",
  "port": 3000
}
```

## Options

| Option | Type | Default | Description |
| --- | --- | --- | --- |
| `title` | string | `"Demo"` | Site title. |
| `theme` | string | `"light"` | `light` or `dark`. |
| `port` | number | `3000` | Local preview port. |

{% hint style="warning" %}
Restart `demo serve` after changing the config.
{% endhint %}
