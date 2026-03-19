---
title: "Home Server"
date: 2026-03-19T00:00:00-06:00
draft: false
unsafe: true
#layout: single
---

CaddyCloudflare

    services:
    caddy:
        image: ghcr.io/caddybuilds/caddy-cloudflare:latest
        restart: unless-stopped
        cap_add:
        - NET_ADMIN
        ports:
        - 80:80
        - 443:443
        - 443:443/udp
        volumes:
        - ./conf:/etc/caddy
        - ./site:/srv
        - caddy_data:/data
        - caddy_config:/config
        environment:
        - CF_API_TOKEN=ZZzqWvKNVHLjRqt4EQxuZrz-TUvyhtwB-mXxYDY6
    volumes:
    caddy_data: null
    caddy_config: null
    networks:
    dockge_default:
        external: true

Caddyfile

    # basic_auth {
    # 	admin $2a$14$ek4L2GdCQjT7BhKHzq9jvOQ7OimIIuHNTeuPxEN3tdQ1iAcZWTK9e
    # 	manager $2a$14$CHD8SYiEfNduM0yMHCNEQeoKkL1DYUz8DoL8aEHVUhOUFv0xxZNpq
    # 	guest $2a$14$vdL73wHBm7W1CgqYkpl9huy7lXjRZlvQhRIcKh8olkYLBqyP7A1oO
    # }

    mentalflower.com {
            root * /usr/share/caddy
            file_server

            tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }
    }

    dockge.mentalflower.com {
        reverse_proxy http://192.168.x.x:5001
            tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }

    }

    nextcloud.mentalflower.com {
            reverse_proxy http://192.168.x.x:8080
            tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }

    }

    jellyfin.mentalflower.com {
            reverse_proxy http://192.168.x.x:8096

            tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }

    }

    wg.mentalflower.com {
        reverse_proxy http://192.168.x.x:51821
        tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }
    }

    pihole.mentalflower.com {
            #basicauth {
            #        admin $2a$14$ek4L2GdCQjT7BhKHzq9jvOQ7OimIIuHNTeuPxEN3tdQ1iAcZWTK9e
            #}
            reverse_proxy http://192.168.x.x:7080
            tls {
                    dns cloudflare {env.CF_API_TOKEN}
                    resolvers 1.1.1.1
            }
    }


-------------------------------------------

Ddclient

    services:
    ddclient:
        image: lscr.io/linuxserver/ddclient:latest
        container_name: ddclient
        environment:
        - PUID=1000
        - PGID=1000
        - TZ=Etc/UTC
        volumes:
        - ./conf:/config
        restart: unless-stopped
    networks: {}

conf


    ######################################################################
    ##
    ## Define default global variables with lines like:
    ## 	var=value [, var=value]*
    ## These values will be used for each following host unless overridden
    ## with a local variable definition.
    ##
    ## Define local variables for one or more hosts with:
    ## 	var=value [, var=value]* host.and.domain[,host2.and.domain...]
    ##
    ## Lines can be continued on the following line by ending the line
    ## with a \
    ##
    ##
    ## Warning: not all supported routers or dynamic DNS services
    ##          are mentioned here.
    ##
    ######################################################################
    daemon=300				# check every 300 seconds
    syslog=yes				# log update msgs to syslog
    #mail=root				# mail all msgs to root
    #mail-failure=root	    # mail failed update msgs to root
    pid=/var/run/ddclient/ddclient.pid	# record PID in file.
    ssl=yes 				# use ssl-support.  Works with
                            # ssl-library
    # postscript=script		# run script after updating.  The
                            # new IP is added as argument.
    #
    #use=watchguard-soho,        fw=192.168.111.1:80	# via Watchguard's SOHO FW
    #use=netopia-r910,           fw=192.168.111.1:80	# via Netopia R910 FW
    #use=smc-barricade,          fw=192.168.123.254:80	# via SMC's Barricade FW
    #use=netgear-rt3xx,          fw=192.168.0.1:80		# via Netgear's internet FW
    #use=linksys,                fw=192.168.1.1:80		# via Linksys's internet FW
    #use=maxgate-ugate3x00,      fw=192.168.0.1:80		# via MaxGate's UGATE-3x00  FW
    #use=elsa-lancom-dsl10,      fw=10.0.0.254:80		# via ELSA LanCom DSL/10 DSL Router
    #use=elsa-lancom-dsl10-ch01, fw=10.0.0.254:80		# via ELSA LanCom DSL/10 DSL Router
    #use=elsa-lancom-dsl10-ch02, fw=10.0.0.254:80		# via ELSA LanCom DSL/10 DSL Router
    #use=alcatel-stp,            fw=10.0.0.138:80           # via Alcatel Speed Touch Pro
    #use=xsense-aero,            fw=192.168.1.1:80          # via Xsense Aero Router
    #use=allnet-1298,            fw=192.168.1.1:80          # via AllNet 1298 DSL Router
    #use=3com-oc-remote812,	     fw=192.168.0.254:80	# via 3com OfficeConnect Remote 812
    #use=e-tech,                 fw=192.168.1.1:80          # via E-tech Router
    #use=cayman-3220h,           fw=192.168.0.1:1080        # via Cayman 3220-H DSL Router
    #
    #fw-login=admin,             fw-password=XXXXXX		# FW login and password
    #
    ## To obtain an IP address from FW status page (using fw-login, fw-password)
    #use=fw, fw=192.168.1.254/status.htm, fw-skip='IP Address' # found after IP Address
    #
    ## To obtain an IP address from Web status page (using the proxy if defined)
    ## by default, checkip.dyndns.org is used if you use the dyndns protocol.
    ## Using use=web is enough to get it working.
    ## WARNING: set deamon at least to 600 seconds if you use checkip or you could
    ## get banned from their service.
    #use=web, web=checkip.dyndns.org/, web-skip='IP Address' # found after IP Address
    #
    #use=ip,                     ip=127.0.0.1	# via static IP's
    #use=if,                     if=eth0		# via interfaces
    #use=web					# via web
    #
    #protocol=dyndns2				# default protocol
    #proxy=fasthttp.sympatico.ca:80			# default proxy
    #server=members.dyndns.org			# default server
    #server=members.dyndns.org:8245			# default server (bypassing proxies)

    #login=your-login				# default login
    #password=test					# default password
    #mx=mx.for.your.host				# default MX
    #backupmx=yes|no				# host is primary MX?
    #wildcard=yes|no				# add wildcard CNAME?


    ##
    ## CloudFlare (www.cloudflare.com)
    ##
    use=web # get IP with website below
    web='https://cloudflare.com/cdn-cgi/trace'
    protocol=cloudflare,        \
    zone=mentalflower.com,            \
    ttl=1,                      \
    #login=your-login-email,     \ # Only needed if you are using your global API key. If you are using an API token, set it to "token" (without double quotes).
    password=ZZzqWvKNVHLjRqt4EQxuZrz-TUvyhtwB-mXxYDY6             \ # This is either your global API key, or an API token. If you are using an API token, it must have the permissions "Zone - DNS - Edit" and "Zone - Zone - Read". The Zone resources must be "Include - All zones".
    mentalflower.com, www.mentalflower.com, *.mentalflower.com


-------------------------------------------

Jellyfin

    services:
    jellyfin:
        image: jellyfin/jellyfin
        container_name: jellyfin
        # Optional - specify the uid and gid you would like Jellyfin to use instead of root
        # user: uid:gid
        ports:
        - 8096:8096/tcp
        - 7359:7359/udp
        volumes:
        - /path/to/config:/config
        - /path/to/cache:/cache
        - type: bind
            source: /path/to/media
            target: /media
        - type: bind
            source: /path/to/media2
            target: /media2
            read_only: true
        - type: bind
            source: /path/to/fonts
            target: /usr/local/share/fonts/custom
            read_only: true
        restart: unless-stopped
        # Optional - alternative address used for autodiscovery
        environment:
        - JELLYFIN_PublishedServerUrl=http://example.com
        # Optional - may be necessary for docker healthcheck to pass if running in host network mode
        extra_hosts:
        - host.docker.internal:host-gateway
    networks:
    nginx_default:
        external: true
        name: jellyfin


-------------------------------------------

Nextcloud

    volumes:
    nextcloud: null
    db: null
    services:
    db:
        image: mariadb:10.6
        restart: always
        command: --transaction-isolation=READ-COMMITTED --log-bin=binlog --binlog-format=ROW
        volumes:
        - db:/var/lib/mysql
        environment:
        - MYSQL_ROOT_PASSWORD=YourPassword
        - MYSQL_PASSWORD=YourPassword
        - MYSQL_DATABASE=nextcloud
        - MYSQL_USER=nextcloud
    app:
        image: nextcloud
        restart: always
        ports:
        - 8080:80
        links:
        - db
        volumes:
        - nextcloud:/var/www/html
        # needs to be absolute path to use as a file
        - ${PWD}/conf/config.php:/var/www/html/config/config.php
        environment:
        - MYSQL_PASSWORD=YourPassword
        - MYSQL_DATABASE=nextcloud
        - MYSQL_USER=nextcloud
        - MYSQL_HOST=db
    networks:
    ingress:
        external: true

config.php

    <?php
    #testststst
    $CONFIG = array (
    'htaccess.RewriteBase' => '/',
    'memcache.local' => '\\OC\\Memcache\\APCu',
    'apps_paths' => 
    array (
        0 => 
        array (
        'path' => '/var/www/html/apps',
        'url' => '/apps',
        'writable' => false,
        ),
        1 => 
        array (
        'path' => '/var/www/html/custom_apps',
        'url' => '/custom_apps',
        'writable' => true,
        ),
    ),
    'upgrade.disable-web' => true,
    'instanceid' => 'oci0xgxyxbz0',
    'passwordsalt' => '5ylBnLLXhXeOzL02g2r8OOAud19sz4',
    'secret' => '9sNG+Cpd+9dGhVoXKCyzSTVri+ZALzSxLgABdgVFOhaTZJXQ',
    'trusted_domains' => 
    array (
        0 => 'nextcloud.mentalflower.com'
    ),
    'overwriteprotocol' => 'http',
    'datadirectory' => '/var/www/html/data',
    'dbtype' => 'mysql',
    'version' => '33.0.0.16',
    'overwrite.cli.url' => 'http://192.168.x.x:8080',
    'dbname' => 'nextcloud',
    'dbhost' => 'db',
    'dbtableprefix' => 'oc_',
    'mysql.utf8mb4' => true,
    'dbuser' => 'nextcloud',
    'dbpassword' => 'YourPassword',
    'installed' => true,
    );


-------------------------------------------


Pihole

    # More info at https://github.com/pi-hole/docker-pi-hole/ and https://docs.pi-hole.net/
    services:
    pihole:
        container_name: pihole
        image: pihole/pihole:latest
        ports:
        # DNS Ports
        - 53:53/tcp
        - 53:53/udp
        # Default HTTP Port
        - 7080:80/tcp
        # Default HTTPs Port. FTL will generate a self-signed certificate
        - 7443:443/tcp
        # Uncomment the below if using Pi-hole as your DHCP Server
        #- "67:67/udp"
        # Uncomment the line below if you are using Pi-hole as your NTP server
        #- "123:123/udp"
        environment:
        # Set the appropriate timezone for your location from
        # https://en.wikipedia.org/wiki/List_of_tz_database_time_zones, e.g:
        TZ: America/New_York
        
        # Set a password to access the web interface. Not setting one will result in a random password being assigned
        # Set to IP of host running the docker container
        FTLCONF_LOCAL_IPV4: 192.168.x.x
        FTLCONF_webserver_api_password: YourPassword
        
        # If using Docker's default `bridge` network setting the dns listening mode should be set to 'ALL'
        FTLCONF_dns_listeningMode: ALL
        # Volumes store your data between container upgrades
        volumes:
        # For persisting Pi-hole's databases and common configuration file
        - ./etc-pihole:/etc/pihole
        # Uncomment the below if you have custom dnsmasq config files that you want to persist. Not needed for most starting fresh with Pi-hole v6. If you're upgrading from v5 you and have used this directory before, you should keep it enabled for the first v6 container start to allow for a complete migration. It can be removed afterwards. Needs environment variable FTLCONF_misc_etc_dnsmasq_d: 'true'
        #- './etc-dnsmasq.d:/etc/dnsmasq.d'
        cap_add:
        # See https://github.com/pi-hole/docker-pi-hole#note-on-capabilities
        # Required if you are using Pi-hole as your DHCP server, else not needed
        - NET_ADMIN
        # Required if you are using Pi-hole as your NTP client to be able to set the host's system time
        - SYS_TIME
        # Optional, if Pi-hole should get some more processing time
        - SYS_NICE
        restart: unless-stopped
    networks:
    dockge_default:
        external: true
    caddycloudflare_default:
        external: true


-------------------------------------------


Wiregaurd Easy

    volumes:
    etc_wireguard: null
    services:
    wg-easy:
        environment:
        - WG_HOST=vpn.mentalflower.com # your public DNS name / static IP
        - WG_ALLOWED_IPS=0.0.0.0/ # ← split-tunnel to your home LAN
        - WG_DEFAULT_DNS=1.1.1.1
        - WG_PERSISTENT_KEEPALIVE=25
        #environment:
        #  Optional:
        #  - PORT=51821
        #  - HOST=0.0.0.0
        #  - INSECURE=false

        image: ghcr.io/wg-easy/wg-easy:15
        container_name: wg-easy
        networks:
        wg:
            ipv4_address: 10.42.42.42
            ipv6_address: fdcc:ad94:bacf:61a3::2a
        volumes:
        - etc_wireguard:/etc/wireguard
        - /lib/modules:/lib/modules:ro
        ports:
        - 51820:51820/udp
        - 51821:51821/tcp
        restart: unless-stopped
        cap_add:
        - NET_ADMIN
        - SYS_MODULE
        # - NET_RAW # ⚠️ Uncomment if using Podman
        sysctls:
        - net.ipv4.ip_forward=1
        - net.ipv4.conf.all.src_valid_mark=1
        - net.ipv6.conf.all.disable_ipv6=0
        - net.ipv6.conf.all.forwarding=1
        - net.ipv6.conf.default.forwarding=1
    networks:
    wg:
        driver: bridge
        enable_ipv6: true
        ipam:
        driver: default
        config:
            - subnet: 10.42.42.0/24
            - subnet: fdcc:ad94:bacf:61a3::/64
    dockge_default:
        external: true


-------------------------------------------

