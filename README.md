# ansible-role-cfn-route53

## Example playbook
```
- hosts: localhost
  connection: local
  vars:
    route53_stack_name: "test-route53-role"
    route53_stack_description: "testing route53 role"
    route53_tags:
      "something" : "something"
    route53_dns_name: "test.test.com"
    route53_zone_name: "test.com."
    route53_comment: "some commment"
    route53_target_address: "someinstance.us-west-2.compute.amazonaws.com"
    ansible_security_token: "{{ lookup('env', 'AWS_SESSION_TOKEN') }}"

  roles:
    - ansible-role-cfn-route53
```
