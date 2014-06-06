# Ansible Ansible Role #

Ansible role to install and configure AWS Command Line Interface. Feedback, 
bug-reports, requests, is welcomed and can be done via
[github issues](https://github.com/New-Edge-Engineering/ansible-aws_cli/issues).

## Requirements & Dependencies ##
- Tested on Mac OS X with Ansible 1.5.

## Variables ##
**aws_cli_credentials** a list of credentials for a particular user identified 
by their name that is another dictionary wth the key and secret. Use default if 
only one, otherwise the first becomes the default. For example:

    aws_cli_credentials:
      -
        user: root
        dev:
          key: AKIAI0RPNNAJ0GYAAIYA
          secret: pQosD7Y0jagsfdljApXcvHjU7vx89RsHgw6j3044GS
        test:
          key: AKIAI0RPNNAJ0GYAAIBB
          secret: pQosD7Y0jagsfdljApXcvHjU7vx89RsHgw6j304400
        live:
          key: AKIAI0RPNNAJ0GYAACCC
          secret: pQosD7Y0jagsfdljApXcvHjU7vx89RsHgw6j308888

**aws_cli_archives** a list of directories to be continuously backupped. It made 
up of archive of name, credentials (name, optional falling back to default), 
region, bucket (name), remote (directory), local (directory). This will sync down 
files and continuously sync up files.

## License ##

Licensed under the MIT License. See the LICENSE file for details.
