export NAME=ghost
export NAMESPACE=cozylab-ghost

include ../../../hack/package.mk

generate:
	cozyvalues-gen -v values.yaml -s values.schema.json -r README.md

update: generate