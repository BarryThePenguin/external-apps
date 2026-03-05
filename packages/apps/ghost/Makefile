NAMESPACE=cozy-system
NAME=ghost

include ../../../hack/package.mk

generate:
	cozyvalues-gen -v values.yaml -s values.schema.json -r README.md
		../../../hack/update-crd.sh

image: image-ghost

image-ghost:
	docker buildx build images/ghost \
		--tag 
