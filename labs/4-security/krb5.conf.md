[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = MAJEDALI
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true

[realms]
 MAJEDALI = {
  kdc = vm1
  admin_server = vm1
 }

[domain_realm]
 .MAJEDALI = MAJEDALI
 MAJEDALI = MAJEDALI