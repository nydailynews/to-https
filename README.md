# to-https

## Guinea Pigs

* https://devinteractive.nydailynews.com/quiz/map-quiz/puerto-rico/
* https://devinteractive.nydailynews.com/quiz/
* https://devinteractive.nydailynews.com/quiz/nyc-101/
* https://devinteractive.nydailynews.com/project/
* https://devinteractive.nydailynews.com/project/archive/amazing-history-nyc/

find . -name "index.*" -exec sed -i '{}' -e 's#assets.adobedtm.com/4fc527d6fda921c80e462d11a29deae2e4cf7514/satelliteLib-774d60efeb80c8b9f62cea9078508154c4f534ff.js#assets.adobedtm.com/4fc527d6fda921c80e462d11a29deae2e4cf7514/satelliteLib-c91fdc6ac624c6cbcd50250f79786de339793801.js#g' \; -print

## bash commands
```bash
#find . -name "index.*" -exec sed -i '{}' -e 's###g' \; -print
# JS mostly
find . -name "index.*" -exec sed -i '{}' -e 's#http://assets.nydailynews#//www.nydailynews#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/includes/js/vendor/jquery.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/js/jquery.min.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://cdnjs.cloudflare.com/ajax/libs/jquery/1.7.1/jquery.min.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js#/js/jquery.min.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/css/foundation.css#/css/foundation.css#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/library/vendor-nav/vendor-include.js#/library/vendor-nav/vendor-include.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/includes/ads/ads.js#/includes/ads/ads.js#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#src="http://interactive.nydailynews.com/#src="/#g' \; -print


# CSS
find . -name "index.*" -exec sed -i '{}' -e 's#type="text/css" href="http:#href="https:#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#link href="http:#link href="https:#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#rel="stylesheet" href="http:#rel="stylesheet" href="https:#g' \; -print
find . -name "*.css" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/#/#g' \; -print
find . -name "*.css" -exec sed -i '{}' -e 's#http://assets.nydailynews.com/#https://www.nydailynews.com/#g' \; -print
find . -name "index.*" -exec sed -i '{}' -e 's#url(http://assets.nydailynews.com/#url(https://www.nydailynews.com/#g' \; -print


# IMG
find . -name "index.*" -exec sed -i '{}' -e 's#src="http://poladm.nydailynews.com:8080#src="https://www.nydailynews.com#g' \; -print

# FINALLY
find . -name "index.*" -exec sed -i '{}' -e 's#http://interactive.nydailynews.com/#https://interactive.nydailynews.com/#g' \; -print

#find . -name "index.*" -exec grep 'href="http://interactive' '{}' \; -print
find . -name "index.*" -exec grep 'src="http:' '{}' \; -print
find . -name "index.*" -exec grep 'href="http:' '{}' \; -print
find . -name "*.css" -exec grep 'http:' '{}' \; -print

#find . -type d -exec rm -rf {} \;

find . -name "index.*" -exec sed -i '{}' -e 's#includes/ads/ads.js#includes/template/template.js#g' \; -print

```
