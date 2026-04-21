+++
date = '2026-04-19T17:28:41+01:00'
title = 'Firefox Browser Extensions'
categories = ["Privacy"]
tags = ["Firefox", "Browser", "Browser Extensions"]
+++
Here is a list of of Firefox browser extensions I really like, especially for privacy.
# [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) ![](ublock.svg)
Truly one of the best ad-blockers of all time. It is lightweight and has some extra features to give you control over your web browser.

## Disable JavaScript by Default
uBlock allows you to disable JavaScript as a default behavior in the settings menu. This allows you to manually whitelist domains which should use JS on the extension pop-up menu when you press "More". This gives you uMatrix-lite control over browser requests. It's a nice middle ground between simplicity and control.

## Block Remote Fonts
You can also prevent web fonts from being downloaded to reduce further the amount of requests to external connections.

## Block Outsider Intrusion into LAN
This is a filter list that you should absolutely enable. It blocks suspicious actions such as port scanning your local network.

# [LocalCDN](https://addons.mozilla.org/en-US/firefox/addon/localcdn-fork-of-decentraleyes/) ![](localcdn.svg)
This extension emulates Content Delivery Networks (CDNs) so when a website requests resources from a large CDN like jQuery, it instead grabs it locally and injects it into the environment.

## Ruleset for uBlock Origin
To properly redirect CDN connections to LocalCDN with an adblocker you need to generate rule sets from the extension settings. Go to "Advanced" then scroll to the bottom and select your uBlock Origin. Copy the ruleset then in uBlock Origin settings go to "My Rules", paste the ruleset into "Temporary rules" and press Save then Commit.

# [LibRedirect](https://addons.mozilla.org/en-US/firefox/addon/libredirect/) ![](libredirect.svg)

LibRedirect used to be an extremely useful extension for redirecting mainstream sites to privacy-friendly alternatives but due to the [The Downfall of Alternative Frontends](https://denshi.org/blog/the-downfall-of-alternative-frontends/) it's extremely finnicky to find a working redirect link and may only work for nicher services in current year.
