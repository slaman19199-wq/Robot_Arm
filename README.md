# Robot_Arm
# تثبيت الأدوات الأساسية
sudo apt update
sudo apt install -y git python3-colcon-common-extensions ros-humble-moveit

# تفعيل بيئة ROS
source /opt/ros/humble/setup.bash

# إنشاء مساحة العمل
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src

# نسخ ملفات ذراع الروبوت من GitHub
git clone https://github.com/smart-methods/Robot_Arm_ROS2.git

# العودة إلى مجلد مساحة العمل
cd ~/ros2_ws

# بناء المشروع
colcon build

# تفعيل إعدادات البيئة بعد البناء
source ~/ros2_ws/install/setup.bash
