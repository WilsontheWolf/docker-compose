# Watchtower

Create `.env`

You can optionally setup notifcations, by filling as so:

```env
WATCHTOWER_NOTIFICATIONS=shoutrrr
WATCHTOWER_NOTIFICATION_URL="url"
WATCHTOWER_NOTIFICATION_TEMPLATE: "{{range .}}{{.Time.Format \"2006-01-02 15:04:05\"}} ({{.Level}}): {{.Message}}{{println}}{{end}}"
```

See: https://containrrr.dev/watchtower/notifications/