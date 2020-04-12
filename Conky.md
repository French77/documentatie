![Screenshot](https://i.imgur.com/3FcACYm.png"Screenshot")




##### Conky script Dutch Language using StyleBats,ConkyColors,conkysymbols,openlogos and PizzaDude Fonts.Free to use,distribute or modify to your own needs.

```ruby conky.config = {
	-- Use double buffering (eliminates flickering)
	double_buffer = true,

        -- Overide local settings
        override_utf8_locale = true,

	-- Run conky in the background
	background = false,
  
	-- Update interval in seconds
	update_interval = 2.5,

	-- Set to zero to run forever
	total_run_times = 0,

	-- Subtract file system buffers from used memory
	no_buffers = true,

	-- Number of samples to take for CPU and network readings
	cpu_avg_samples = 2,
	net_avg_samples = 2,

	-- Use Xft (anti-aliased font and stuff)
	use_xft = true,
	font = 'Ubuntu Bold:size=8,8',
	xftalpha = 0.9,
	uppercase = false,
  
	-- Prevent text from moving around while using a mono font
	use_spacer = 'left',
  
	-- Default color and border settings
	default_color = 'LightBlue',
	draw_shades = true,
	draw_outline = true,
	draw_borders = false,

	-- Makes conky window transparent
	own_window = true,
	own_window_class = 'Conky',
	own_window_argb_visual = true,
	own_window_argb_value = 127,
	own_window_transparent = true,
	own_window_type = 'desktop', 
	own_window_hints = 'undecorated,below,skip_taskbar,sticky,skip_pager',
  
	-- Window size and position
	minimum_width = 400,
	minimum_height = 400,
	maximum_width = 700,
    alignment = 'top_middle',
    gap_y = 85
```    
##### conky.tekst   
    
```ruby }
 conky.text = [[
                                                           
${color #4e6969}${font ConkyColors:size=10}o${font}${color} ${time %X}
${color #4e6969}${font ConkyColors:size=10}n${font}${color} ${time %A %x Week %V}
${color #4e6969}${font ConkyColors:size=10}b${font}${color}  Desktop: ${alignr}$nodename_short
${color #4e6969}${font conkysymbols:size=10}u${font}${color}  OS: $alignr${execi 3600 lsb_release -d -s}
${color #4e6969}${font conkysymbols:size=10}a${font}${color} Systeem:$alignr$sysname $machine
${color #4e6969}${font openlogos:size=10}G${font}${color}  Kernel: ${alignr}${kernel}
${color #4e6969}${font ConkyColors:size=10}f${font}${color}  Cinnamon Versie: $alignr${execi 3600 cinnamon --version}
${color #4e6969}${font ConkyColors:size=10}f${font}${color}  Nemo Versie: $alignr${execi 3600 nemo --version}
${color #4e6969}${font openlogos:size=10}P${font}${color}  Firefox Versie: $alignr${execi 3600 firefox --version}
${color #4e6969}${font StyleBats:size=10}6${font}${color} Conky Versie:${alignr}${conky_version}
${color #4e6969}${font openlogos:size=10}I${font}${color}  Inxi Versie: $alignr${execi 3600 inxi --version}

${color #4e6969}${font conkysymbols:size=10}k${font}${color } HD: $alignr Seagate 1000GB
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

${color #4e6969}${font conkysymbols:size=10}b${font}${color} Netwerk
${color #4e6969}${font ConkyColors:size=10}r${font}${color} ISP: $alignr KPN
${color #4e6969}${font StyleBats:size=10}I${font}${color} IP adres: $alignr ${addr enp1s0}
${if_up tun0}
${color #4e6969}${font conkysymbols:size=10}b${font}${color} VPN
${color #4e6969}${font ConkyColors:size=10}r${font}${color} ISP: $alignr PIA
${color #4e6969}${font StyleBats:size=10}I${font}${color} IP adres: ${alignr}${execi 60 curl ipinfo.io/ip 2>/dev/null}
${color #4e6969}${font conkysymbols:size=10}i${font}${color} Locatie VPN Server: $alignr${execi 9001 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="city": ")(\w+)'} - ${execi 9001 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="region": ")(\w+)'} - ${execi 9001 wget -qO- ipinfo.io 2> /dev/null | grep -oP '(?<="country": ")(\w+)'}   
${else}${color DC143C}${font ConkyColors:size=10}r${font}${color} ISP: $alignr PIA-VPN Verbroken
$endif
${color #4e6969}${font ConkyColors:size=10}i${font}${color} Router: $alignr H368N Experiabox V9 
${color LightBlue} Overzicht${alignr} Verkeer
$color Uit: ${tcp_portmon 1 32767 count}  In: ${tcp_portmon 32768 61000 count}${alignr} Totaal: ${tcp_portmon 1 65535 count}
${color #4e6969}${font PizzaDude Bullets:size=10}u${font}${color} Router-In ${alignr} Protocol$color
${tcp_portmon 32768 61000 rhost 0} ${alignr} ${tcp_portmon 32768 61000 rservice 0}
${tcp_portmon 32768 61000 rhost 1} ${alignr} ${tcp_portmon 32768 61000 rservice 1}
${tcp_portmon 32768 61000 rhost 2} ${alignr} ${tcp_portmon 32768 61000 rservice 2}
${color #4e6969}${font PizzaDude Bullets:size=10}n${font}${color} Router-Uit ${alignr}Protocol$color
${tcp_portmon 1 32767 rhost 0} ${alignr} ${tcp_portmon 1 32767 lservice 0}
${tcp_portmon 1 32767 rhost 1} ${alignr} ${tcp_portmon 1 32767 lservice 1}
                                                           ${color #4e6969}${font ConkyColors:size=15}c${font}${color}  
${color #ff571a}${font ConkyColors:size=10}q${font}${color } 1] 25-Oct-2020 Pia Vpn verlengen met 2 jaar 
${color #ff571a}${font ConkyColors:size=10}q${font}${color } 2] Image OSMC RPI-4 maand ?-2020
${color #ff571a}${font ConkyColors:size=10}q${font}${color } 3] 

${color #4e6969}${font openlogos:size=10}X${font}${color} BIOS: ${alignr}${execi 3600 inxi -xx-M}




































































































]]
```
