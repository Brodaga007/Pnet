# Pnet
Настройка конфига nftables
table ip nat {
  chain postrouting {
    type nat hook postrouting priority 100; policy accept
    meta l4proto {gre, ipip, ospf} counter return
    masquerade
  }
}




  
