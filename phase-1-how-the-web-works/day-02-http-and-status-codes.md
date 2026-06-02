\# Day 2 — HTTP, HTTPS \& Status Codes



\## What I Learned



\### HTTP — The Language of the Web

HTTP (HyperText Transfer Protocol) is the language clients and servers use to communicate. Every web action is just an HTTP request and response.



\### HTTPS — The Secure Version

HTTPS = HTTP + Secure. The "S" stands for Secure. It encrypts data so even if intercepted on public Wi-Fi, attackers see gibberish.



\### HTTP Methods (CRUD)

\- GET — Read data (load a page, view profile)

\- POST — Create new data (login, signup, post photo)

\- PUT — Update existing data (edit bio, change profile pic)

\- DELETE — Remove data (delete tweet, remove friend)



\### Status Codes

\- 2xx — Success: 200 OK, 201 Created

\- 3xx — Redirect: 301 Moved Permanently

\- 4xx — Client error (YOUR fault):

&#x20; - 400 Bad Request

&#x20; - 401 Unauthorized (don't know who you are)

&#x20; - 403 Forbidden (know you, not allowed)

&#x20; - 404 Not Found

\- 5xx — Server error (SERVER's fault):

&#x20; - 500 Internal Server Error

&#x20; - 503 Service Unavailable



\### Authentication vs Authorization

\- AuthN (Authentication) = Proving WHO you are (login)

\- AuthZ (Authorization) = What you're ALLOWED to do (permissions)



\## My curl Experiments

\- curl https://api.github.com → 200 OK, returned API endpoint list

\- curl -i https://api.github.com → saw full headers including rate limits

\- curl -i https://api.github.com/this-page-doesnt-exist → got 404

\- curl https://api.github.com/users/smaransiwakoti-debug → got my own profile as JSON



\## New Concepts I Discovered



\### Rate Limiting

GitHub limits unauthenticated requests to 60 per hour. Headers like X-RateLimit-Limit and X-RateLimit-Remaining tell you how many requests you have left. This prevents abuse and protects the server.



\### Defense in Depth

I learned this principle while setting up Git privacy:

\- Layer 1 (Client): My laptop labels commits with a no-reply email

\- Layer 2 (Server): GitHub blocks pushes that would expose my real email

Two layers of protection are always better than one.



\## Git Skills Unlocked Today

\- Configured user.name and user.email globally

\- Switched to a no-reply email for privacy

\- Cloned my first repo with git clone

\- Created folder structure inside a local repo

\- First terminal-based commit ever



\## One Lesson I Won't Forget

NEVER paste file content into the terminal — paste it into the EDITOR! The terminal is for commands, the editor is for content.



\## One Question I Still Have

(Write any question you have here)

