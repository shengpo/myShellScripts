turnOff_wl11n.sh
================

這個 shell script 是為了因應有時連上wireless時，連線速度過慢的問題。


script修改原理如下：
--------------------
- wireless慢的話，打開terminal輸入以下指令：
	sudo rmmod iwlwifi && sudo modprobe iwlwifi 11n_disable=1

- kernel更新至3.7.1-030701-generic時，必須改成下列方式：
	sudo rmmod iwldvm && sudo rmmod iwlwifi && sudo modprobe iwlwifi 11n_disable=1
(refernece: https://bbs.archlinux.org/viewtopic.php?pid=1176708)
