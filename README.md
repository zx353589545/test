#
#-------------------------------------------------------------#
#  创建者：https://v2rayse.com
#  创建时间：2024-03-13 03:00:06
#  模版：v2rayse默认模版
#  节点数量：6
#-------------------------------------------------------------#
#
port: 7890
socks-port: 7891
allow-lan: true
mode: Rule
log-level: info
external-controller: 0.0.0.0:9090
proxies:
  - {"type":"http","name":"http_proxy","server":"127.0.0.1","port":10900,"udp":true}
  - {"type":"socks5","name":"socks5_proxy","server":"127.0.0.1","port":10010,"udp":true}
proxy-groups:
  - name: 🚀 节点选择
    type: select
    proxies:
      - http_proxy
      - socks5_proxy
rules:
