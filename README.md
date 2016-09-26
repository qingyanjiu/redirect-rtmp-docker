#rtmp-nginx-in-docker
<p>基于nginx的rtmp推流服务器，支持把ps4的直播流推送到指定的地址（如斗鱼）</p>
<p>docker build -t IMAGENAME .</p>
<p>docker run -d -p 8099:80 -p 1935:1935 IMAGENAME</p>
<p>iptables -A INPUT -ptcp --dport 1935 -j ACCEPT</p>
<p>iptables -A INPUT -ptcp --dport 8099 -j ACCEPT</p>
<p>sudo iptables -t nat -A PREROUTING -i eth0 -d 192.108.239.0/24 -j REDIRECT </p>
<p>sudo iptables -t nat -A PREROUTING -i eth0 -d 23.160.0.0/24 -j REDIRECT</p>