favicon.ico:
	curl -o favicon.ico https://ysap.sh/favicon.ico

.PHONY: index
index:
	./make-curl-website > index.txt

.PHONY: serve
serve: favicon.ico
	python3 -mhttp.server

# deploy the website
.PHONY: deploy
deploy: favicon.ico index
	rsync -avh --delete --progress \
	    ./{index.txt,index.html,style.css,favicon.ico,download.html} \
	    web:/var/www/course.ysap.sh/
