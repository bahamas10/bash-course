.PHONY: serve
serve:
	python3 -mhttp.server

# deploy the website
.PHONY: deploy
deploy:
	rsync -avh --delete --progress \
	    ./{index.html,style.css} web:/var/www/course.ysap.sh/
