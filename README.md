prometheus-coloudformation
==================

Overview
--------

This repository contains a set of nagios plugins for AWS Cloudformation service

Usage
-----

* Install python-boto3
* Create a dedicated key pair via AWS IAM (read-only access for EC2 and ELB)
* Put this key pair in nagios home .aws/config file
* Launch the scripts with --help for more help
* running the application with the --exporter (and optiona --exporter_port) start a small http server that server prometheus metric on /metrics

AWS Config file
---------------

```config
[profile nagios_checker]
aws_access_key_id = key_id
aws_secret_access_key = private_key
region = eu-west-1
```

License
-------

Copyright (c) Camptocamp 2015 All rights reserved.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
