# Configuration items for gitlab-openstack-deploy

This repository contains the group_vars and host_vars for the generic gitlab
omnibus playbook. See https://github.com/coderefinery/gitlab-openstack-deploy for
details.

## Note about SSL certificates

Currently certbot auto-creation does not work inside the omnibus container. To
create a certificate

```
$ sudo su
# docker stop gitlab
# certbot
[ follow instructions ]
[ copy certificates over files in /srv/gitlab/config/ssl/ ]
# sudo docker start gitlab
```

And verify manually that you don't get ssl errors.
