# aws_cloudformation

A collection of AWS CloudFormation templates.

## Requirements

* Python3
* pip3

Setup a Python3 virtual environment and use pip3 to install additional Python module dependencies using the `requirements_prod.txt` file, or `requirements_nonprod.txt` for latest dependency versions:

    $ pip install -r requirements_prod.txt

The `awscli` can also be installed using `pip3`.

See https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html for details on configuring AWS CLI profiles.

## Testing CloudFormation templates

    find . -path ./.venv -prune -o -name '*.cfn_template.yml' -print | xargs -n1 yamllint
    find . -path ./.venv -prune -o -name '*.cfn_template.yml' -print | xargs -n1 cfn-lint
