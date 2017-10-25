# to-https

## Guinea Pigs

* https://devinteractive.nydailynews.com/quiz/map-quiz/puerto-rico/
* https://devinteractive.nydailynews.com/quiz/
* https://devinteractive.nydailynews.com/quiz/nyc-101/
* https://devinteractive.nydailynews.com/project/
* https://devinteractive.nydailynews.com/project/archive/amazing-history-nyc/

## bash commands
```bash
#find . -name "index.*" -exec sed -i '{}' -e 's###g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://assets.nydailynews#//www.nydailynews#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/includes/js/vendor/jquery.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/js/jquery.min.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/css/foundation.css#/css/foundation.css#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/library/vendor-nav/vendor-include.js#/library/vendor-nav/vendor-include.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/includes/ads/ads.js#/includes/ads/ads.js#g' \; -print
#find . -type d -exec rm -rf {} \;
```
