
This repository contains AWS VPC Infrasturcture as Code (IaC) in the form of AWS Cloudformation templates. These are a collection of general purpose Cloudformation templates.

## Requirements

* Python3
* pip3

Setup a Python3 virtual environment and use pip3 to install additional Python module dependencies using the `requirements_production.txt` file, or `requirements_nonproduction.txt` for latest dependency versions:

    $ pip install -r requirements_production.txt

See https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html for details on configuring AWS CLI profiles.

## Testing
    find . -path ./.venv -prune -o -name '*.cfn_template.yml' -print | xargs -n1 yamllint
    find . -path ./.venv -prune -o -name '*.cfn_template.yml' -print | xargs -n1 cfn-lint
