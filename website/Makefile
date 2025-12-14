favicon.ico:
	curl -o favicon.ico https://ysap.sh/favicon.ico

index.txt:
	./make-curl-website > index.txt

.PHONY: serve
serve: favicon.ico index.txt
	python3 -mhttp.server

# deploy the website
.PHONY: deploy
deploy: favicon.ico index.txt
	rsync -avh --delete --progress \
	    ./{index.txt,index.html,style.css,favicon.ico} \
	    web:/var/www/course.ysap.sh/
