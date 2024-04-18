default: testacc

# Run local build
.PHONY: build
build:
	goreleaser build --snapshot --clean

# Run acceptance tests
.PHONY: testacc
testacc: build
	TF_ACC=1 go test ./... -v $(TESTARGS) -timeout 120m
