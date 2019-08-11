= newboat =
RSS/Atom feed reader for text consoles


$ newsboat -h
help
$ newsboat -r
refresh feeds on start

= urls =
add urls in ~/.newsboat/urls

url format:
http://url.to/feed "tag"


= shortcuts =
n: got to next unread entry
o: open the selected entry in default web browser
r: reload the currently selected feed
R: reload all feeds
A: mark as read
/: search
s: save single entry
e: enqueue
?: help
q: go back and exit


= subscriptions =
- reddit: <reddit_url>/r/<sub_reddit>/.rss
- youtube: https://www.youtube.com/subscription_manager (export subscriptions)
  newsboat -i=<path_to_xml_file>


= sources =
https://newsboat.org/
https://www.mankier.com/1/newsboat
https://newsboat.org/releases/2.16.1/docs/faq.html#
https://newsboat.org/releases/2.16.1/docs/newsboat.html
