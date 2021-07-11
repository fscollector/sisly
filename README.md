# Sisly
A framework for scraping images/video. Works with aria2. Ideally this project is just to piece together some other projects into something functional.



# TODO List
Requirements:
- Site Detector - Ex: tumblr.com, pinterest.com, twitter.com
- Simulate Auto Scroll
- Queue up w/ Aria2
- Minimal footprint

Components:
- Framework / Scraper Engine (this)
- Framework / API / CLI [REST]
- Orechestrator (spawn up until reaching max, queue thereafter)
- Selenium Webkit Docker Container(s) [Low Profile]

Bonus:
- Auto Check For Updates (Polling Sites / Blogs)
- Web UI


# Example Usage
var sisly = require('sisly')
var options = { "autoscroll": "1", "parser":"default" }
//var options = { "autoscroll": "1", "parser":"custom.yml" }
sisly.scan('feed.xml', [options], [event]);

[event] = function () {
  aria2.queue(url, filename, [on-complete-event])
}


# Containers
- Sisly (REST API w/ CLI Frontend to compliment and abstract youtube-dl)
- Nodes of Selenium (1 per site/blog, max ram limit to force GC?)
- Aria2 (Downloader)
- Single File (HTML5/Websocket) Aria2 management in a Caddy server
