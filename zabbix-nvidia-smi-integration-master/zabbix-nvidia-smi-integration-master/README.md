<<<<<<< HEAD
# zabbix-nvidia-smi-integration




* GPU Utilisation
* GPU Power Consumption
* GPU Memory (Used, Free, Total)
* GPU Temperature
* GPU Fan Speed






UserParameter=gpu.temp,nvidia-smi --query-gpu=temperature.gpu --format=csv,noheader,nounits -i 0
UserParameter=gpu.memtotal,nvidia-smi --query-gpu=memory.total --format=csv,noheader,nounits -i 0
UserParameter=gpu.used,nvidia-smi --query-gpu=memory.used --format=csv,noheader,nounits -i 0
UserParameter=gpu.free,nvidia-smi --query-gpu=memory.free --format=csv,noheader,nounits -i 0
UserParameter=gpu.fanspeed,nvidia-smi --query-gpu=fan.speed --format=csv,noheader,nounits -i 0
UserParameter=gpu.utilisation,nvidia-smi --query-gpu=utilization.gpu --format=csv,noheader,nounits -i 0
UserParameter=gpu.power,nvidia-smi --query-gpu=power.draw --format=csv,noheader,nounits -i 0

The following code was developed from https://gist.github.com/bhcopeland/b54d3c678a0cb6e87119 and further refined to avoid the need to directly parse output from nvidia smi with grep and cut.

Alongside the template monitorgraphics.sh is an alternative monitoring script that outputs nvidia-smi information to disk. This is not needed for the Zabbix template but it remains useful for monitoring NVidia GPUs.

It is possible to use this Zabbix template within a Docker container, please see the following [repository](https://github.com/wangmuy/zabbix-agent-nvidia) for how this can be accomplished.
=======
devops branhc
>>>>>>> devops
