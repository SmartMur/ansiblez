# Monit role

The HTTP interface listens on loopback by default. Set `vault_monit_password` in
your encrypted Ansible Vault before running the role. Use a long, random value
without double quotes, backslashes, or line breaks, for example one generated
with `openssl rand -hex 24`. Set the real password as part of any rollout of
this role. Existing installations configured with the former example password
need a password change.

For remote access, use an SSH tunnel to the Monit host or explicitly configure
a trusted interface and an appropriate firewall. Setting a non-loopback address
is an operational choice for that host.
