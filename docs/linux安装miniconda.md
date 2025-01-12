下载Miniconda安装脚本：
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
给安装脚本添加执行权限：
chmod +x Miniconda3-latest-Linux-x86_64.sh
执行安装脚本：
./Miniconda3-latest-Linux-x86_64.sh

安装过程中的注意事项：
按回车键阅读许可协议
输入"yes"同意许可条款
确认安装位置（默认是 ~/miniconda3）
当问到是否初始化Miniconda3时，输入"yes"

使环境变量生效
source ~/.bashrc

验证安装：
conda --version

配置conda国内镜像源（建议添加）：
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes

