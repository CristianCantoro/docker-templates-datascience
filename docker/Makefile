.PHONY: jupyterlab notebook help

.DEFAULT_GOAL := help

jupyterlab: 					## Build eut-bdds/jupyterlab image
	cd jupyterlab && \
		docker build -t eut-bdds/jupyterlab -f Dockerfile.jupyterlab .


notebook: 						## Build eut-bdds/notebook image
	cd notebook && \
		docker build -t eut-bdds/notebook -f Dockerfile.notebook .


help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | \
		sort | \
		awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'
