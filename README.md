clashprofile：
	自己用的规则


rule-providers:
  apple:
    behavior: "domain" # domain, ipcidr or classical (premium core only)
    type: http
    url: "url"
    interval: 3600
    path: ./apple.yaml
  microsoft:
    behavior: "domain"
    type: file
    path: /microsoft.yaml

==============domain===============
domain
payload:
  - '.blogger.com'
  - '*.*.microsoft.com'
  - 'books.itunes.apple.com'
  =============ipcidr================
ipcidr
payload:
  - '192.168.1.0/24'
  - '10.0.0.0.1/32'
  ============classical=================
classical
payload:
  - DOMAIN-SUFFIX,google.com
  - DOMAIN-KEYWORD,google
  - DOMAIN,ad.com
  - SRC-IP-CIDR,192.168.1.201/32
  - IP-CIDR,127.0.0.0/8
  - GEOIP,CN
  - DST-PORT,80
  - SRC-PORT,7777
  # MATCH is not necessary here