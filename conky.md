#### Conky script made by Freñiçh Dutch Language using StyleBats and PizzaDude Fonts.Free to use,distribute or modify to your own needs.Copy/paste this script to your own .conkyrc(~) ####

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
	font = 'Ubuntu Bold:size=8',
	xftalpha = 0.8,
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
	minimum_width = 220,
	minimum_height = 690,
	maximum_width = 320,
	alignment = 'top_right',
	gap_y = 85

> conky.text = [[
${color 52c700}${font PizzaDude Bullets:size=12}h${font}${color } Conky script gemaakt door:${font PizzaDude Bullets:size=10}3${font} Freñiçh.

> ${color 52c700}${font StyleBats:size=10}X${font}${color } ${time %X}
> ${color 52c700}${font PizzaDude Bullets:size=9}J${font}${color } ${time %A %x Week %V}
> ${color 52c700}${font StyleBats:size=10}C${font}${color } PC naam: ${alignr}$nodename

> ${color 52c700}${font StyleBats:size=10}Q${font}${color} Sonya Mint 18.2 Cinnamon 64-bit${font}
> ${color 52c700}${font StyleBats:size=10}F${font}${color} Intel Core i5-7600 ${font}
> ${color 52c700}${font StyleBats:size=10}6${font}${color} Conky Versie:${alignr}${conky_version}

> ${voffset 2}${color 52c700}${font StyleBats:size=10}k${font}${color}${voffset -2} Kernel: ${alignr}${kernel}
> ${voffset 2}${color 52c700}${font StyleBats:size=10}8${font}${color}${voffset -2} PC Aktief: ${alignr}${uptime_short}
> ${voffset 4}${color 52c700}${font StyleBats:size=10}I${font}${color} IP adres: $alignr ${addr enp1s0}

> #${hr 2}
> ${color 52c700}${font StyleBats:size=10}O${font}${color } HD Seagate 1000GB
> ${color LightBlue}Percentage: ${fs_used_perc /}%${alignr} Capaciteit: ${fs_size /}
> ${color LightBlue}Vrij: ${fs_free /home} ${alignr}${fs_bar 5,60 /}
> {color LightBlue}Gebruikt:${fs_used /home}${color}${alignr}${fs_bar 5,60 /}

> ${color 52c700}${font StyleBats:size=10}M${font}${color }${color LightBlue} /home   $color${fs_used /home}/${fs_size /home}${alignr}${color LightBlue}${fs_bar 5,60 /home}

> ${voffset 2}${color 52c700}${font StyleBats:size=10}A${font}${color LightBlue}${voffset -2} CPU1: ${color }${voffset 1}${offset 2}${cpubar cpu1 5,60}${color}${alignr}${cpu}%
> ${voffset 2}${color 52c700}${font StyleBats:size=10}A${font}${color LightBlue}${voffset -2} CPU2: ${color }${voffset 1}${offset 2}${cpubar cpu1 5,60}${color}${alignr}${cpu}%
> ${voffset 2}${color 52c700}${font StyleBats:size=10}U${font}${color LightBlue}${voffset -2} Fysiek RAM geheugen: ${color  }${voffset 1}${alignr}$memmax 
> In gebruik:${alignr}$mem($memperc%) ${membar 5,60}

> ${color 52c700}${font StyleBats:size=10}E${font}${color } Verbruik Applicaties
> ${color LightBlue} ${top_mem name 1}$alignr${top_mem mem 1}%
> ${color LightBlue} ${top_mem name 2}$alignr${top_mem mem 2}%
> ${color LightBlue} ${top_mem name 3}$alignr${top_mem mem 3}%
> ${color LightBlue} ${top_mem name 4}$alignr${top_mem mem 4}%

> ${color 52c700}${font StyleBats:size=10}S${font}${color} Netwerk
> ${color 52c700}${font PizzaDude Bullets:size=10}N${font}${color} Upload Snelheid ${upspeed eth0}${alignr}${upspeedgraph eth0 5,60}
> ${color 52c700}${font PizzaDude Bullets:size=10}T${font}${color} Download Snelheid ${downspeed eth0} ${alignr}${downspeedgraph eth0 5,60}
> ${color 52c700}${font PizzaDude Bullets:size=10}U${font}${color} Totale Snelheid${alignr}${totaldown eth0}

> ${color 52c700}${font StyleBats:size=10}L${font}${color} ROUTER<->POORTEN
> ${color LightBlue}Poort(en)${alignr}#Verbinding
> $color Uitgaand: ${tcp_portmon 1 32767 count}  Inkomend: ${tcp_portmon 32768 61000 count}${alignr}Totaal: ${tcp_portmon 1 65535 count}
> ${color 52c700}${font PizzaDude Bullets:size=10}n${font}${color} Routerpoort->Uitgaand ${alignr} <-Poort$color
> ${tcp_portmon 1 32767 rhost 0} ${alignr} ${tcp_portmon 1 32767 lservice 0}
> ${tcp_portmon 1 32767 rhost 1} ${alignr} ${tcp_portmon 1 32767 lservice 1}
> ${color 52c700}${font PizzaDude Bullets:size=10}u${font}${color} Routerpoort->Inkomend ${alignr} <-Poort$color
> ${tcp_portmon 32768 61000 rhost 0} ${alignr} ${tcp_portmon 32768 61000 rservice 0}
> ${tcp_portmon 32768 61000 rhost 1} ${alignr} ${tcp_portmon 32768 61000 rservice 1}

> ${if_running radiotray}
> ${color 52c700}${font PizzaDude Bullets:size=10}Y${font}${color} RADIO TRAY AAN
> ${execi 15 qdbus net.sourceforge.radiotray /net/sourceforge/radiotray net.sourceforge.radiotray.getCurrentRadio}: 
> ${execi 15 qdbus net.sourceforge.radiotray /net/sourceforge/radiotray getCurrentMetaData| fold -s -w35}
> ${else}${voffset -5}${color0}${font PizzaDude:size=6}${font}${color DC143C}${font PizzaDude Bullets:size=10}Z${font} ${color} RADIO TRAY UIT
> ${endif}
> ${if_running spotify}
> ${color 52c700}${font PizzaDude Bullets:size=10}Y${font}${color} SPOTIFY AAN
> ${else}${voffset -5}${color0}${font PizzaDude:size=6}${font}${color DC143C}${font PizzaDude Bullets:size=10}Z${font} ${color} SPOTIFY UIT
> ${endif}
> ]]

![Screenshot](https://i.imgur.com/fYDkPav.png"Screenshot")





