favicon.ico:
	curl -o favicon.ico https://ysap.sh/favicon.ico

.PHONY: serve
serve: favicon.ico
	python3 -mhttp.server

# deploy the website
.PHONY: deploy
deploy: favicon.ico
	rsync -avh --delete --progress \
	    ./{index.html,style.css,favicon.ico} \
	    web:/var/www/course.ysap.sh/
