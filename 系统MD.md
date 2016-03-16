# WIN10
## 安装时输入激活码
**VK7JG-NPHTM-C97JM-9MPGT-3V66T**

# 解决Win7 USB/DVD Download Tool无法写入U盘
1. WIN键+R 启动出“运行”对话框，键入cmd，启动命令提示符。输入diskpart，启动DISKPART工具  

2. 在DISKPART窗口中输入以下命令：

		>list disk （此命令是列出所有磁盘驱动器，请务必看清楚你的U盘前面的数字编号，例如1）
		>select disk # （#是上一步中所显示的U盘编号数字，不要写成硬盘编号）
		>clean
		
3. 开始给U盘创建主分区，进入并激活主分区：
		
		>create partition primary
		>select partition 1
		>active
		
4. 快速初始化U盘为FAT32格式，并重新加载U盘，然后退出DISKPART；

		>format quick fs=fat32
		>assign
		>exit