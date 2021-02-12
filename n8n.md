# n8n

<img src="https://docs.n8n.io/assets/img/n8n-logo.png" style="height: 64px;">

[n8n](https://n8n.io/), the "extendable workflow automation", a personal [IFTTT](https://ifttt.com) if like [/self-hosting]().

n8n makes it possible to solve some tasks in a *"No-Code"* manner (a [very polular](https://nocodelist.co/) thing nowadays):

- CI/CD
- [/Telegram]() bots ([how to](https://medium.com/n8n-io/creating-telegram-bots-with-n8n-a-no-code-platform-fdf1f0928da7))
- sanding of EMails
- ...

You have a bunch of *triggers* (GitHub push, Web-hook, schedule) some *actuators* ("Send a message to Telegram", "ping a host", "POST some request") and a couple of ways to connect formers to letters.

For example, I ([/who/astynax]()) have a Telegram Bot that posts a random piece from ["100 Quotes Every Geek Should Know"](https://www.wired.com/2010/01/100-quotes-every-geek-should-know/) (from WIRED) daily. The quotes themselves I store in [AirTable](https://airtable.com/) - yep, more "No-Code"!

# Hosting with Dokku

I have n8n deployed on a Digital Ocean droplet under control of [/Dokku]().

## Run

1.
    ```bash
    dokku apps:create n8n
    ```
1.
    ```bash
    dokku storage:mount n8n ~/.n8n:/root/.n8n
    ```
1.

    ```bash
    dokku config:set n8n \
      N8N_BASIC_AUTH_ACTIVE=true \
      N8N_BASIC_AUTH_USER=foo \
      N8N_BASIC_AUTH_PASSWORD=bar
    ```

1.
    ```bash
    docker pull n8nio/n8n:latest
    ```
1.
    ```bash
    docker tag n8nio/n8n:latest dokku/n8n:latest
    ```
1.
    ```bash
    dokku tags:deploy dokku/n8n:latest
    ```

## Update

```bash
docker pull n8nio/n8n:latest \
  && docker tag n8nio/n8n:latest dokku/n8n:latest \
  && dokku ps:restart n8n
```