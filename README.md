# Sisly
A framework for scraping images/video. Works with aria2



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
  aria2.queue(url, filename, [on-complete])
}
