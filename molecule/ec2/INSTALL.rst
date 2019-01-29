*******
Amazon Web Services driver installation guide
*******

Requirements
============

* boto or boto3
* awscli
* AWS credentials file (see https://docs.aws.amazon.com/en_us/cli/latest/userguide/cli-configure-files.html)
* AWS region set to "eu-central-1"

Install
=======

.. code-block:: bash

    $ sudo pip install boto boto3
    $ sudo pip install --upgrade awscli
    $ export AWS_REGION="eu-central-1"
