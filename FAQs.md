I'll add more to these soon. If you have other issues not mentioned here or suggestions, [ask away](https://github.com/Sank6/Discord-Bot-List/issues)

## How can I host this?

This is an [express](https://expressjs.com/) server like many others, and to host it, you'll need to install and run the file on a VPS (virtual private server) and use a DNS server, to point an A-Name record of your VPS's IP address to your domain. This isn't designed to be hosted on [glitch](https://glitch.com/) free tier.

## "Invalid OAuth2 redirect URI"

In your Discord [developer settings](https://discord.com/developers) for the application, make sure you only have **one redirect URI** and it is your domain followed by `/api/callback`. Eg, `https://botlist.com/api/callback`.
Also make sure that in your config file, your domain, contains the protocol and does **NOT** end with a `/`. Eg, `https://botlist.com` and not like these: `https://botlist.com/` `botlist.com`