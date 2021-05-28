# nvidia
list:

-  lspci | grep -i nvidia
-  gcc --version
-  
436  uname -r
437  sudo apt-get install linux-headers-$(uname -r)
438  sudo /usr/local/cuda-X.Y/bin/cuda-uninstaller
439  udo /usr/bin/nvidia-uninstall
440  sudo /usr/bin/nvidia-uninstall
441  sudo apt-get install linux-headers-$(uname -r)
442  distribution=$(. /etc/os-release;echo $ID$VERSION_ID | sed -e 's/\.//g')
443  wget https://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64/cuda-$distribution.pin
444  sudo mv cuda-$distribution.pin /etc/apt/preferences.d/cuda-repository-pin-600
445  sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64/7fa2af80.pub
446  echo "deb http://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64 /" | sudo tee /etc/apt/sources.list.d/cuda.list
447  sudo apt-get update
448  sudo apt-get -y install cuda-drivers
449  export PATH=/usr/local/cuda-11.3/bin${PATH:+:${PATH}}
450  sudo systemctl enable nvidia-persistenced

https://docs.nvidia.com/datacenter/tesla/tesla-installation-notes/index.html#runfile
