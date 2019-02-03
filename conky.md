#### Conky script Dutch Language using StyleBats,ConkyColors,conkysymbols and PizzaDude Fonts.Free to use,distribute or modify to your own needs. .conkyrc(~) ####

        conky.config = {
	-- Use double buffering (eliminates flickering)
	double_buffer = true,

        -- Overide local settings
        override_utf8_locale = true,

	-- Run conky in the background
	background = true,
  
	-- Update interval in seconds
	update_interval = 2.0,

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
	own_window_class = 'desktop',
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
}
* conky.text = [[

                                                         ${color #c9fe99}${font conkysymbols:size=15}u${font}${color }
${color #a6ff4d}${font ConkyColors:size=10}o${font}${color } ${time %X}
${color #a6ff4d}${font ConkyColors:size=10}n${font}${color } ${time %A %x Week %V}
${color #a6ff4d}${font ConkyColors:size=10}b${font}${color }  Desktop: ${alignr}$nodename
${color #a6ff4d}${font conkysymbols:size=10}u${font}${color}  OS: $alignr${execi 3600 lsb_release -d -s}
${color #a6ff4d}${font ConkyColors:size=10}f${font}${color}  Cinnamon Versie: $alignr${execi 3600 cinnamon --version}
${color #a6ff4d}${font ConkyColors:size=10}f${font}${color}  Nemo Versie: $alignr${execi 3600 nemo --version}
${color #a6ff4d}${font openlogos:size=12}P${font}${color}  Firefox Versie: $alignr${execi 3600 firefox --version}
${color #a6ff4d}${font openlogos:size=10}G${font}${color}  Kernel: ${alignr}${kernel}
${color #a6ff4d}${font StyleBats:size=10}6${font}${color} Conky Versie:${alignr}${conky_version} 

${color #a6ff4d}${font conkysymbols:size=10}k${font}${color } HD Seagate 1000GB
${color LightBlue} Percentage: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_used_perc /}%
${color LightBlue} Capaciteit: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_size /}
${color LightBlue} Vrij: ${color }${voffset 1}${offset 2}${color}${alignr}${fs_free }
${color LightBlue} Gebruikt:${color }${voffset 1}${offset 2}${color}${alignr}${fs_used }
${color #a6ff4d}${font conkysymbols:size=10}f${font}${color}  Intel Core i5-7600 ${freq_g}GHz
${color #a6ff4d}${font conkysymbols:size=10}n${font}${color}  Belasting: ${loadavg} ${alignr}$cpu%
${color #a6ff4d}${font ConkyColors:size=10}g${font}${color LightBlue}${voffset -2} RAM geheugen: ${color  }${voffset 1}${offset 2}${color}${alignr}${memmax}
${color #a6ff4d}${font conkysymbols:size=10}m${font}${color LightBlue}${voffset -2} In gebruik:${color  }${voffset 1}${offset 2}${color}${alignr}${mem}
 
${color #a6ff4d}${font conkysymbols:size=10}m${font}${color } Verbruik Applicaties
${color LightBlue} ${top_mem name 1}$alignr${top_mem mem 1}%
${color LightBlue} ${top_mem name 2}$alignr${top_mem mem 2}%
${color LightBlue} ${top_mem name 3}$alignr${top_mem mem 3}%
${color LightBlue} ${top_mem name 4}$alignr${top_mem mem 4}%
${color #a6ff4d}${font conkysymbols:size=10}b${font}${color} Netwerk
${color #a6ff4d}${font ConkyColors:size=10}v${font}${color} Upload Snelheid: ${color }  ${voffset 1}${offset 2}${color}${alignr} ${upspeed eth0}
${color #a6ff4d}${font ConkyColors:size=10}u${font}${color} Download Snelheid: ${color }${voffset 1}${offset 2}${color}${alignr} ${downspeed eth0} 
${color #a6ff4d}${font PizzaDude Bullets:size=10}U${font}${color} Totale Snelheid: ${color }  ${voffset 1}${offset 2}${color}${alignr} ${totaldown eth0}
${if_up tun0}
${color #a6ff4d}${font ConkyColors:size=10}r${font}${color} PIA-VPN Verbonden
${color #a6ff4d}${font StyleBats:size=10}I${font}${color} IP adres: $alignr ${texeci 60 wget -qO- https://ipecho.net/plain ; echo | tail}

${else}${color DC143C}${font ConkyColors:size=10}q${font}${color} PIA-VPN Verbroken
$endif
${color #a6ff4d}${font ConkyColors:size=10}i${font}${color} Router KPN
${color #a6ff4d}${font StyleBats:size=10}I${font}${color} IP adres: $alignr ${addr enp1s0}
${color LightBlue} Overzicht${alignr} Verkeer
$color Uit: ${tcp_portmon 1 32767 count}  In: ${tcp_portmon 32768 61000 count}${alignr} Totaal: ${tcp_portmon 1 65535 count}
${color #a6ff4d}${font PizzaDude Bullets:size=10}u${font}${color} Router-In ${alignr} Protocol$color
${tcp_portmon 32768 61000 rhost 0} ${alignr} ${tcp_portmon 32768 61000 rservice 0}
${tcp_portmon 32768 61000 rhost 1} ${alignr} ${tcp_portmon 32768 61000 rservice 1}
${tcp_portmon 32768 61000 rhost 2} ${alignr} ${tcp_portmon 32768 61000 rservice 2}
${color #a6ff4d}${font PizzaDude Bullets:size=10}n${font}${color} Router-Uit ${alignr}Protocol$color
${tcp_portmon 1 32767 rhost 0} ${alignr} ${tcp_portmon 1 32767 lservice 0}
${tcp_portmon 1 32767 rhost 1} ${alignr} ${tcp_portmon 1 32767 lservice 1}
${color #ff571a}${font ConkyColors:size=10}q${font}${color } Aandachts punten:
${color LightBlue} -> !!! 25-Oct-2020 Pia Vpn verlengen met 2 jaar !!!

${if_running radiotray}
${color #a6ff4d}${font ConkyColors:size=10}r${font}${color} RADIO TRAY AAN ${alignr} ${execi 15 qdbus net.sourceforge.radiotray /net/sourceforge/radiotray net.sourceforge.radiotray.getCurrentRadio}
${color #a6ff4d}${font ConkyColors:size=10}G ${font}${color}${color LightBlue}${execi 15 qdbus net.sourceforge.radiotray /net/sourceforge/radiotray getCurrentMetaData| fold -s -w35}
${else}${voffset -5}${color0}${font PizzaDude:size=6}${font}${color DC143C}${font ConkyColors:size=10}r${font} ${color} RADIO TRAY UIT
${endif}
${if_running spotify}
${color #a6ff4d}${font ConkyColors:size=10}r${font}${color} SPOTIFY AAN ${alignr}Spotify
${color #a6ff4d}${font ConkyColors:size=10}G ${font}${color LightBlue}Daily - Mix
${else}${voffset -5}${color0}${font PizzaDude:size=6}${font}${color DC143C}${font ConkyColors:size=10}r${font} ${color} SPOTIFY UIT
${endif}
${if_mounted /media/french/Backup}
${color #a6ff4d}${font conkysymbols:size=10}k${font}${color }${color LightBlue} Timeshift Backup${tab 30,0}${color} ${alignr} ${fs_used /media/french/Backup} / ${fs_size /media/french/Backup} 
${else}\
${color DC143C}${font conkysymbols:size=10}k${font} ${color} SDHC Card Ontkoppeld\
${endif}
${if_mounted /media/french/FREECOM}
${color #a6ff4d}${font conkysymbols:size=10}k${font}${color }${color LightBlue} HD Freecom${tab 30,0}${color} ${alignr} ${fs_used /media/french/FREECOM} / ${fs_size /media/french/FREECOM}
${else}\
${color DC143C}${font conkysymbols:size=10}k${font} ${color} Externe HD Ontkoppeld\
${endif}*


]]

![Screenshot](https://i.imgur.com/pXDMFIp.png"Screenshot")
![](https://img.shields.io/badge/Linux-CC0-brightgreen.svg?style=social&label=Afbeeldingen)




