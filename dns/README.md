# DNS(Domain Name Server)란? 
-  사람이 읽을 수 있는 도메인 이름(예: www.amazon.com)을 머신이 읽을 수 있는 IP 주소(예: 192.0.2.44)로 변환해 주는 서버


## 웹서비스 접근을 위한 DNS 요청 흐름
![웹서비스 접근을 위한 DNS 요청 흐름](https://github.com/JinYongHwa/operating_system/raw/master/dns/dns_aws.png)

[참고링크](https://aws.amazon.com/ko/route53/what-is-dns/)

## 도메인의 구조
![도메인의 구조](https://github.com/JinYongHwa/operating_system/raw/master/dns/domain.jpg)



## bind9 설치

```
sudo apt-get install bind9
```

## bind9 설정

### named.conf.options
```
options {
        directory "/var/cache/bind";

        // If there is a firewall between you and nameservers you want
        // to talk to, you may need to fix the firewall to allow multiple
        // ports to talk.  See http://www.kb.cert.org/vuls/id/800113

        // If your ISP provided one or more IP addresses for stable
        // nameservers, you probably want to use them as forwarders.
        // Uncomment the following block, and insert the addresses replacing
        // the all-0's placeholder.

         forwarders {
                8.8.8.8;
         };

        //========================================================================
        // If BIND logs error messages about the root key being expired,
        // you will need to update your keys.  See https://www.isc.org/bind-keys
        //========================================================================
        dnssec-validation auto;
        allow-transfer { none; };
        auth-nxdomain no;    # conform to RFC1035
        listen-on-v6 { any; };
};
```

### copy db.local 
```
sudo cp db.local db.test.com
```

### db.test.com
```
$TTL    30
@       IN      SOA     test.com. root.test.com. (
                              3         ; Serial
                         604800         ; Refresh
                          86400         ; Retry
                        2419200         ; Expire
                         604800 )       ; Negative Cache TTL
;
@       NS              ns.test.com.
@       IN      A       127.0.0.1
@       IN      AAAA    ::1
ns      IN      A       127.0.0.1
www     IN      A       127.0.0.1
```

### named.conf.local
```
zone "test.com" {
        type master;
        file "/etc/bind/db.test.com";
};
```




## bind9 실행

```
sudo service bind9 start
```
