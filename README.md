# My-Object-Detection
Only runs on Raspberry pi 3 and 4
## List of Commands for OpenCv setup:
sudo apt-get update && sudo apt-get upgrade && sudo rpi-update <br>
sudo nano /etc/dphys-swapfile <br>
 CONF_SWAPSIZE=2048 <br>
sudo apt-get install build-essential cmake pkg-config<br>
sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev<br>
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev<br>
sudo apt-get install libxvidcore-dev libx264-dev<br>
sudo apt-get install libgtk2.0-dev libgtk-3-dev<br>
sudo apt-get install libatlas-base-dev gfortran<br>
wget -O opencv.zip <br>
https://github.com/opencv/opencv/archive/4.1.0.zip<br>
wget -O opencv_contrib.zip <br>
https://github.com/opencv/opencv_contrib/archive/4.1.0.zip<br>
unzip opencv.zip<br>
unzip opencv_contrib.zip<br>
sudo pip3 install numpy<br>
cd ~/opencv-4.1.0/ <br>
mkdir build <br>
cd build <br>
cmake -D CMAKE_BUILD_TYPE=RELEASE \ <br>
-D CMAKE_INSTALL_PREFIX=/usr/local \ <br>
-D INSTALL_PYTHON_EXAMPLES=ON \ <br>
-D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-4.1.0/modules \ <br>
-D BUILD_EXAMPLES=ON .. <br>
make -j4<br>
sudo make install && sudo ldconfig<br>
sudo reboot<br>
## Test Code
python3<br>
import cv2<br>
cv2.__version__<br>
## Open up terminal and clone the repo:
bash cd /home/pi <br>
git clone https://github.com/akashdeepchand/My-Object-Detection.git
## Launch the web cam:
sudo python3 /home/pi/My-Object-Detection/ObjectDetectionModule.py
### Now we can use the Project in Raspberry Pi
