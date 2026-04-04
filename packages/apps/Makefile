OUT=../../_out/repos/apps
CHARTS := $(shell find . -maxdepth 2 -name Chart.yaml | awk -F/ '{print $$2}')

repo:
	rm -rf "$(OUT)"
	helm package -d "$(OUT)" $(CHARTS)
	helm repo index "$(OUT)"