# ansible-percona84

Installs/configures Percona 8.4

- This role does not modify configuration of the root account
  (recent versions of mysql configure the root account to use `auth_socket`
  plugin, i.e., no need to set up a password for the root account) (Ref. [1],
  [2])
- Wherever possible, by default this role does not change the application default
  values in the configuration files
- Config changes are not written to the `my.cnf` file (which is normally kept
  updated by the distro packages). Instead, a config file is added to the
  appropriate include directory

[1]: [Socket Peer-Credential Pluggable Authentication (MySQL Reference Manual)](https://dev.mysql.com/doc/refman/8.4/en/socket-pluggable-authentication.html)

[2]: [Use MySQL Without a Password (and Still be Secure) (Percona)](https://www.percona.com/blog/use-mysql-without-a-password/)
