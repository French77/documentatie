

#### 04-09-2020 WireGuard and server location
#### Conky afbeelding

![Screenshot](https://i.imgur.com/Yf48ioV.png"Screenshot")


##### conky.tekst   
    
```ruby }
conky.text = [[
${color #4e6969}${font ConkyColors:size=10}o${font}${color} ${time %X}
${color #4e6969}${font ConkyColors:size=10}n${font}${color} ${time %A %d-%m-%Y Week %V}
${color #4e6969}${font ConkyColors:size=10}b${font}${color}  Desktop: ${alignr}${nodename_short} ${monitor_number}
${color #4e6969}${font conkysymbols:size=10}u${font}${color}  Versie naam: $alignr${execi 3600 lsb_release -c -s}
${color #4e6969}${font conkysymbols:size=10}u${font}${color}  Versie: $alignr${execi 3600 lsb_release -d -s}
${color #4e6969}${font conkysymbols:size=10}a${font}${color} Systeem:$alignr$sysname $machine
${color #4e6969}${font openlogos:size=10}G${font}${color}  Kernel: ${alignr}${kernel}
${color #4e6969}${font ConkyColors:size=10}f${font}${color}  Cinnamon Versie: $alignr${execi 3600 cinnamon --version}
${color #4e6969}${font ConkyColors:size=10}f${font}${color}  Nemo Versie: $alignr${execi 3600 nemo --version}
${color #4e6969}${font openlogos:size=10}P${font}${color}  Firefox Versie: $alignr${execi 3600 firefox --version}
${color #4e6969}${font StyleBats:size=10}6${font}${color} Conky Versie:${alignr}${conky_version} 
${color #4e6969}${font openlogos:size=10}I${font}${color}  Inxi Versie: $alignr${execi 3600 inxi --version}
${color #4e6969}${font openlogos:size=10}p${font}${color}  Pia VPN Versie: $alignr${execi 3600 piactl -v}

${color #4e6969}${font ConkyColors:size=10}i${font}${color} HD: $alignr Seagate 1000GB
${color LightBlue} Percentage: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_used_perc /}%
${color LightBlue} Capaciteit: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_size /}
${color LightBlue} Vrij: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_free }
${color LightBlue} Gebruikt:${color }${voffset 1}${offset 2}${color}${alignr}${fs_used }

${color #4e6969}${font conkysymbols:size=10}f${font}${color}  Intel Core: $alignr i5-7600 ${freq_g}GHz
${color #4e6969}${font conkysymbols:size=10}n${font}${color}  Belasting: ${loadavg} ${alignr}$cpu%
${color #4e6969}${font conkysymbols:size=10}n${font}${color} CPU Freq: ${alignr} ${freq}MHz
${color #4e6969}${font ConkyColors:size=10}g${font}${color LightBlue}${voffset -2} RAM geheugen: ${color  }${voffset 1}${offset 2}${color}${alignr}${memmax}
${color #4e6969}${font conkysymbols:size=10}m${font}${color LightBlue}${voffset -2} In gebruik:${color  }${voffset 1}${offset 2}${color}${alignr}${mem}
 
${color #4e6969}${font conkysymbols:size=10}m${font}${color } Verbruik Applicaties
${color LightBlue} ${top_mem name 1}$alignr${top_mem mem 1}% ${top cpu 1}% 
${color LightBlue} ${top_mem name 2}$alignr${top_mem mem 2}% ${top cpu 2}%
${color LightBlue} ${top_mem name 3}$alignr${top_mem mem 3}% ${top cpu 3}%
${color LightBlue} ${top_mem name 4}$alignr${top_mem mem 4}% ${top cpu 4}%
${color LightBlue} ${top_mem name 5}$alignr${top_mem mem 5}% ${top cpu 5}%
${color LightBlue} ${top_mem name 6}$alignr${top_mem mem 6}% ${top cpu 6}%
                                                                                
${color #4e6969}${font Weather:size=14}c${font}${color } Weersinfo: ${execi 300 curl -s nl.wttr.in/Spijkenisse?format=%l+%c+%C%t+%o+%h+%P+%f,+%w+%p+%m¸▲+%S¸▼+%s}
${color #4e6969}${font Weather:size=14}c${font}${color } Weersinfo: ${execi 300 curl -s nl.wttr.in/Heerenveen?format=%l+%c+%C+%t+%o+%h+%P+%f,+%w+%p+%m¸▲+%S¸▼+%s}

${color #4e6969}${font conkysymbols:size=10}i${font}${color} Netwerk
${color #4e6969}${font ConkyColors:size=10}r${font}${color} ISP: $alignr KPN
${color #4e6969}${font conkysymbols:size=10}I${font}${color} IP adres: $alignr ${addr enp1s0}
${if_up wgpia0}
${color #4e6969}${font conkysymbols:size=10}i${font}${color} VPN
${color #4e6969}${font ConkyColors:size=10}r${font}${color} ISP: $alignr PIA 
${color #4e6969}${font ConkyColors:size=10}r${font}${color} Protocol: $alignr WireGuard
${color #4e6969}${font conkysymbols:size=10}I${font}${color} IP adres: ${alignr}${execi 600 curl -s ipinfo.io/ip}
${color #4e6969}${font conkysymbols:size=10}i${font}${color} Locatie VPN Server: $alignr${execi 600 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="city": ")(\w+)'} - ${execi 600 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="region": ")(\w+)'} - ${execi 600 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="country": ")(\w+)'} 
${else}${color #ff571a}${font ConkyColors:size=10}q${font}${color} ${color #ff571a}${blink PIA-VPN:  Verbroken/Sluimerstand!} 
${endif}
${color #4e6969}${font ConkyColors:size=10}i${font}${color} Router: $alignr H368N Experiabox V9 
${color LightBlue} Overzicht${alignr} Verkeer
$color Uit: ${tcp_portmon 1 32767 count}  In: ${tcp_portmon 32768 61000 count}${alignr} Totaal: ${tcp_portmon 1 65535 count}
${color #4e6969}${font PizzaDude Bullets:size=10}u${font}${color} Router-In ${alignr} Protocol$color
${tcp_portmon 32768 61000 rhost 0} ${alignr} ${tcp_portmon 32768 61000 rservice 0}
${tcp_portmon 32768 61000 rhost 1} ${alignr} ${tcp_portmon 32768 61000 rservice 1}
${color #4e6969}${font PizzaDude Bullets:size=10}n${font}${color} Router-Uit ${alignr}Protocol$color
${tcp_portmon 1 32767 rhost 0} ${alignr} ${tcp_portmon 1 32767 lservice 0}
                                                                                             ${color #4e6969}${font ConkyColors:size=15}c${font}${color}
${color #FDAC53}${font ConkyColors:size=10}q${font}${color } ↔ 25-Oct-2022 Pia Vpn verlengen met 2 jaar 
${color #4e6969}${font conkysymbols:size=10}f${font}${color} BIOS: ${alignr}${execi 7200 inxi -M}
































































































]]




























































































]]
```
