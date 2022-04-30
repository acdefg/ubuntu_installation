# ubuntu_installation
## write iso into USB disk to build a system disk
- iso mirror link: https://mirrors.tuna.tsinghua.edu.cn/#
![image](https://user-images.githubusercontent.com/48377634/166099113-ba4c3834-4e28-4ba3-ac4a-86e46f14d7ce.png)
![image](https://user-images.githubusercontent.com/48377634/166099131-a6621a96-2d60-42d8-969f-1e42739594eb.png)
- ultraiso download link: https://ultraiso.en.softonic.com/
选试用就行
1. 文件-> 打开->选择下载好的iso
2. 启动-> 写入硬盘映像
3. 格式化->写入

![image](https://user-images.githubusercontent.com/48377634/166101218-67cabc3a-7503-4a50-9c05-da1a5f459c09.png)
![image](https://user-images.githubusercontent.com/48377634/166101201-fedacbe4-20f5-4e9b-be35-d4769398d95a.png)
![image](https://user-images.githubusercontent.com/48377634/166101243-b9170479-59dd-4173-bc4a-9c03d30dba19.png)

## reference link
1. https://zhuanlan.zhihu.com/p/355314438
2. https://zhuanlan.zhihu.com/p/407175785
3. https://blog.csdn.net/codeHonghu/article/details/111940656 - good


# delete double system
## change grub option
1. boot interface
2. use easyUEFI
## delete the disk at disk manager
## delete the option at EFI
1. 输入【Win】+【R】，输入【diskpart】打开diskpart；

2. 输入【list disk】，显示磁盘列表

3. 输入【select disk 0】，选择磁盘0，即win10系统所在磁盘；

4. 输入【list partition】，查看磁盘0的分区列表；

5. 输入【select partition 3】，选择wind10启动引导项所在分区（即Type=System，容量一般较小为100M的那一个分区）；

6. 为win10的EFI启动引导项所在分区分配盘符，输入【assign letter = p】，这里p为盘符名称，字母A~Z应该都可以，注意不要和已有盘符名重复即可；
7. 以管理员方式运行记事本，打开p盘，EFI文件夹，删除ubuntu文件夹

## reference link
https://www.cnblogs.com/arxive/p/11749770.html


