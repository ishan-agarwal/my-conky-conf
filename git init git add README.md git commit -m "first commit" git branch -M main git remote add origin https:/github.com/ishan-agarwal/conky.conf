-- vim: ts=4 sw=4 noet ai cindent syntax=lua
--[[
Conky, a system monitor, based on torsmo

Any original torsmo code is licensed under the BSD license

All code written since the fork of torsmo is licensed under the GPL

Please see COPYING for details

Copyright (c) 2004, Hannu Saransaari and Lauri Hakkarainen
Copyright (c) 2005-2012 Brenden Matthews, Philip Kovacs, et. al. (see AUTHORS)
All rights reserved.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
]]
conky.config = {
    alignment = 'top_right',
    background = false,
    border_width = 1,
    cpu_avg_samples = 2,
	default_color = 'white',
    default_outline_color = 'white',
    default_shade_color = 'white',
    draw_borders = false,
    draw_graph_borders = true,
    draw_outline = false,
    draw_shades = false,
    use_xft = true,
    font = 'DejaVu Sans Mono:size=9',
    gap_x = 10,
    gap_y = 60,
    minimum_height = 5,
	minimum_width = 5,
    net_avg_samples = 2,
    no_buffers = true,
    out_to_console = false,
    out_to_stderr = false,
    extra_newline = false,
    own_window = true,
    own_window_class = 'Conky',
    own_window_type = 'desktop',
    own_window_hints = 'undecorated,below,sticky,skip_taskbar,skip_pager',
	own_window_transparent = false,
	own_window_argb_visual = true,
	own_window_argb_value = 0,
	own_window_colour = '000000',
    stippled_borders = 0,
    update_interval = 2,
    uppercase = false,
    use_spacer = 'none',
    show_graph_scale = false,
    show_graph_range = false
}

conky.text = [[
#------------+
# Distro     |
#------------+
${color}Today is:${color green}$alignr${time %A,}$alignr ${time %e %B %G}
${color}Distribution:${color green}$alignr ${execi 6300 cat /etc/issue.net} $machine
${color}Kernel:$alignr${color green} $kernel
${color orange}${voffset 2}${hr 1}
${color2}${voffset 5}Intel i7-10510U (8) @ 4.900GHz: ${color1}@  ${color green}${freq} MHz
#${cpugauge cpu1 20,40}
#${cpugraph 1 15,200 555555 AAAAAA -l}
${color}${goto 13}CPU 0 ${goto 110}${color green}${cpu cpu1}% ${goto 150}${color3}${cpubar cpu1 18}
${color}${goto 13}CPU 1 ${goto 110}${color green}${cpu cpu2}% ${goto 150}${color3}${cpubar cpu2 18}
${color}${goto 13}CPU 2 ${goto 110}${color green}${cpu cpu3}% ${goto 150}${color3}${cpubar cpu3 18}
${color}${goto 13}CPU 3 ${goto 110}${color green}${cpu cpu4}% ${goto 150}${color3}${cpubar cpu4 18}
${color}${goto 13}CPU 4 ${goto 110}${color green}${cpu cpu5}% ${goto 150}${color3}${cpubar cpu5 18}
${color}${goto 13}CPU 5 ${goto 110}${color green}${cpu cpu6}% ${goto 150}${color3}${cpubar cpu6 18}
${color}${goto 13}CPU 6 ${goto 110}${color green}${cpu cpu7}% ${goto 150}${color3}${cpubar cpu7 18}
${color}${goto 13}CPU 7 ${goto 110}${color green}${cpu cpu8}% ${goto 150}${color3}${cpubar cpu8 18}
#------------+
# Temperature|
#------------+
# Next line is for Skylake temperature when none of the other methods work.
#${color1}All CPUs ${color green}${cpu}% ${goto 131}${color1}Temp: ${color green}${execpi .001 cat /sys/class/thermal/thermal_zone7/temp | cut -c1-2}°C ${alignr}${color1}Up: ${color green}$uptime
# Next line is for kernel >= 4.13.0-36-generic
#${color1}All CPUs ${color green}${cpu}% ${goto 131}${color1}Temp: ${color green}${hwmon 1 temp 1}°C ${alignr}${color1}Up: ${color green}$uptime
# Next line is for temperature with Kerenel 4.4
#${color1}All CPUs ${color green}${cpu}% ${goto 131}${color1}Temp: ${color green}${hwmon 0 temp 1}°C ${alignr}${color1}Up: ${color green}$uptime
${color green}$running_processes ${color1}running of ${color green}$processes ${color1}loaded processes.
#------------+
# Intel iGPU |
#------------+
${color orange}${hr 1}${if_existing /sys/class/drm/card0/gt_cur_freq_mhz}
${color2}${voffset 5}Intel i7-10510U(8)@ 4.900GHz @${alignr}${color green}${execpi .001 (cat /sys/class/drm/card0/gt_cur_freq_mhz)} MHz
${color orange}${hr 1}${else}
#------------+
# Prcoesses  |
#------------+
${color1}${voffset 5}Process Name: ${goto 300}PID ${goto 450}CPU% ${goto 600}Mem%
${color}${goto 13}${top name 1} ${goto 290}${top pid 1} ${goto 425}${color green}${top cpu 1} ${goto 575}${top mem 1}
${color}${goto 13}${top name 2} ${goto 290}${top pid 2} ${goto 425}${color green}${top cpu 2} ${goto 575}${top mem 2}
${color}${goto 13}${top name 3} ${goto 290}${top pid 3} ${goto 425}${color green}${top cpu 3} ${goto 575}${top mem 3}
${color}${goto 13}${top name 4} ${goto 290}${top pid 4} ${goto 425}${color green}${top cpu 4} ${goto 575}${top mem 4}
${color}${goto 13}${top name 5} ${goto 290}${top pid 5} ${goto 425}${color green}${top cpu 5} ${goto 575}${top mem 5}
${color}${goto 13}${top name 6} ${goto 290}${top pid 6} ${goto 425}${color green}${top cpu 6} ${goto 575}${top mem 6}
${color}${goto 13}${top name 7} ${goto 290}${top pid 7} ${goto 425}${color green}${top cpu 7} ${goto 575}${top mem 7}
${color}${goto 13}${top name 8} ${goto 290}${top pid 8} ${goto 425}${color green}${top cpu 8} ${goto 575}${top mem 8}
${color}${goto 13}${top name 9} ${goto 290}${top pid 9} ${goto 425}${color green}${top cpu 9} ${goto 575}${top mem 9}
${color orange}${voffset 2}${hr 1}
#------------+
# Storage    |
#------------+
${color1}RAM Use/Free:${goto 240}${color green}$mem ${color green} ${goto 380}${membar 15,200} $alignr${color}${memeasyfree}
${color1}Linux Root:${goto 240}${color green}${fs_used /} ${color green} ${goto 380}${fs_bar 15,200 /} $alignr${color}${fs_free /}
#------------+
# Network    |
#------------+
#${color1}Network using vnStat "-i", "-w" and "-m"
${color}${goto 5}Today ${goto 200}Yesterday ${goto 400}Week ${goto 600}Month ${color green}
# vnstatd updates database every five minutes
${execi 300 vnstat -i wlp0s20f3 | grep "today" | awk '{print $8" "substr ($9, 1, 1)}'} ${goto 200}${execi 300 vnstat -i wlp0s20f3 | grep "yesterday" | awk '{print $8" "substr ($9, 1, 1)}'} ${goto 400}${execi 300 vnstat -i wlp0s20f3 -w | grep "current week" | awk '{print $9" "substr ($10, 1, 1)}'} ${goto 600}${execi 300 vnstat -i wlp0s20f3 -m | grep "`date +"%b '%y"`" | awk '{print $9" "substr ($10, 1, 1)}'}
${color}Down: ${color green}${downspeed wlp0s20f3}/s ${color}${alignr}Up: ${color green}${upspeed wlp0s20f3}/s
${downspeedgraph wlp0s20f3 50,700 000000 ff0000} 
Total: ${color green}${totaldown wlp0s20f3} $color${alignr}Total: ${color green}${totalup wlp0s20f3}
#Bit Rate:$color ${wireless_bitrate wlp0s20f3}
]]
