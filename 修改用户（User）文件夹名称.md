> 情景：Windows 11 的用户名与 C 盘（系统盘）中的文件夹名称不对应（可能是由于重装系统导致的），例如我笔记本中系统用户名是 “fly”，但文件夹名称却是“16490”。

#### Step 1：打开Administrator账户

“搜索”→ cmd → 右键：“以管理员身份运行”→ 输入命令“net user administrator /active:yes”后回车

<img src="C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106154050492.png" alt="image-20230106154050492" style="zoom:80%;" />

![image-20230106154229992](C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106154229992.png)

#### Step 2：切换至Administrator账号

如图：

![image-20230106154354389](C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106154354389.png)

#### Step 3：修改用户文件夹

​	找到“用户（或User）”中的文件夹，修改为你计划的名称（图略，例如我的就是将“16490”修改为“fly”）。

> 附：如不能修改名称，重启电脑后再尝试修改。

#### Step 4：修改注册表信息

* 快捷键“win + R”，打开“运行”，输入“regedit”。

![image-20230106154756443](C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106154756443.png)

* 回车，依次找：HKEY_LOCAL_MACHINE → SOFTWARE → Microsoft → Windows NT → CurrentVersion → ProfileList → ProfileImagePath → 自己的用户名

  <img src="C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106155348872.png" alt="image-20230106155348872" style="zoom:50%;" />

* 双击 ProfileList，修改计划的用户名

  ![image-20230106155500577](C:\Users\MyPhoenix\AppData\Roaming\Typora\typora-user-images\image-20230106155500577.png)

#### Step 5：切换至原账号（参考Step2）

注销 Administrator 账号，切换到原账号。

#### Step 6：关闭Administrator账户

“搜索”→ cmd → 右键，“以管理员身份运行”→ 输入命令“net user administrator /active:no”后回车，以关闭 Administrator 账户





