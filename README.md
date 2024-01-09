# LinuxOC
Overclocking tools for Linux

- [CPU](#cpu)
- [RAM](#ram)
- [GPU](#gpu)

# CPU
### Monitoring:
- htop, [btop](https://github.com/aristocratos/btop) - per core usage, freq and temps
- [ryzen_monitor](https://github.com/hattedsquirrel/ryzen_monitor) -  **(RYZEN ONLY!)** - per core usage, freq, temps, power, voltage, SoC temps and power, fabric clock, PPT + Stats (peak, avg)
- [CoreFreq](https://github.com/cyring/CoreFreq), [Archlinux Live CD image](https://github.com/cyring/CoreFreq/wiki/Live-CD)
- CoreFreq has direct CPU overclocking capabalities
### Overclocking
- in UEFI settings
- [CoreFreq](https://github.com/cyring/CoreFreq), [Archlinux Live CD image](https://github.com/cyring/CoreFreq/wiki/Live-CD)
### Stress testing:
- **Low stress** - Kernel compilation
- **Medium stress** - `ffmpeg -y -f rawvideo -video_size 1920x1080 -pixel_format yuv420p -framerate 60 -i /dev/urandom -c:v libx265 -preset placebo -f matroska /dev/null`
- **High stress** - [GIMPS](https://www.mersenne.org/download/) (prime95/mprime)

# RAM
### Monitoring:
[ryzen_monitor](https://github.com/hattedsquirrel/ryzen_monitor) -  **(RYZEN ONLY!)** - SoC, VDDCR_SOC, VDDG, L3 VDDM, VDDIO, VDDP power, memory and fabric clocks, cLDO_(VDDM, VDDP, VDDG) voltages
### Overclocking
- exclusively in UEFI
### Stress testing:
- **Low stress** - MemTest86+ - 64bit Linux ISO Downlaod: [here](https://www.memtest.org/download/v7.00/mt86plus_7.00_64.iso.zip) (it is also provided in Gentoo's [LiveGUI USB image](https://www.gentoo.org/downloads/))
- **Medium stress** - [GIMPS](https://www.mersenne.org/download/) (prime95/mprime)
- **High stress** - [Stressapptest](https://github.com/stressapptest/stressapptest) `stressapptest - M <~90+% of free memory> -s <time in seconds> -m <thread count> -W` - run for 30min+

# GPU
- No GPU still :'(
