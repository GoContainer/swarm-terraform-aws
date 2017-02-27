.DEFAULT_GOAL := help

validate: terraform-fmt terraform-validate	## Validate syntax

plan:	terraform-validate terraform-get terraform-plan ## Plan changes

apply: terraform-validate terraform-get terraform-apply ## Apply Changes

destroy: terraform-destroy	## Destroy infrastructure

output: terraform-output		## Display State Output

terraform-validate:
	terraform validate

terraform-get:
	terraform get

terraform-plan:
	terraform plan

terraform-apply:
	terraform apply

terraform-fmt:
	terraform fmt -list

terraform-destroy:
	terraform destroy

terraform-output:
	terraform output

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'