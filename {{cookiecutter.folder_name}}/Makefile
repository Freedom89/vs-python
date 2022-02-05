DOCKERNAME=dockerpy
build:
	docker build -t $(DOCKERNAME) .

# Add `CMD jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root`
# to your make file before running this command
notebook:
	docker run --rm -it -p 8888:8888 $(DOCKERNAME)

bash:
	docker run --rm -it -p 8888:8888 \
	--entrypoint bash \
	-v $(shell pwd)/src:/src \
	$(DOCKERNAME)
	