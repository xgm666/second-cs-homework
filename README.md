# second-cs-homework学号：102101344结对成员学号：102101335
# 数独功能完善及并发求解数独的实现
## 单独数独求解函数
* 先调用函数找到需要求解的数独格子，得到相应坐标后，采用回溯算法，不断填入数字进行尝试，满足要求则求解下一个数独，不满足则回溯递归，从而得到正确数独答案

![在这里插入图片描述](https://img-blog.csdnimg.cn/53ab656f642e40e395a8b7a7e2c4e6fd.png)
## 寻找空位数独函数如下
* 找到可填入数独格子后，先进行条件判断，若为空或者是当前输入的数字不满足数独要求则返回该格子的坐标进行重新尝试求解，若当前输入的数字已满足数独要求（即所在行，所在列，所在九宫格无重复数字），则对该格子标绿方便识别

![在这里插入图片描述](https://img-blog.csdnimg.cn/7b328775b81e40029c933d357369a9f6.png)
## 检查当前填充数字是否满足数独要求的函数
* 该函数会分别检查，所填数字在所在行，所在列，所在九宫格是否有重复数字，若发现重复数字，则返回假值false，否则返回真值true，用于数独求解函数的条件判断

![在这里插入图片描述](https://img-blog.csdnimg.cn/78adb5581d8547229f911da52d0f091f.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/0f862ed24ea1452db677232efb485f0b.png)
## 并发求解九个数独函数实现
* 这次我们仍采取promise.all并发求解九个九宫格数独，为其数独求解提供性能保证，并新增加求解所有数独时间的计算，具体函数如下

![在这里插入图片描述](https://img-blog.csdnimg.cn/4c96141711264fdbb2dbec409798df6d.png)
##  选中可输入单元格的文字放大效果实现
![image](https://github.com/grealuffy/homework-2/assets/143927752/32f0afb1-6cae-4c81-9e24-bf921c7fa37b)
![image](https://github.com/grealuffy/homework-2/assets/143927752/ed1122cf-deed-4ce1-a1ed-10ebad77f5f4)

# 代码运行
## 点击解压后的html文件夹，从页面一开始，右键在菜单栏中找到打开选择浏览器打开（建议用Edge），如果页面没有声音，可在设置调网站自动播放，才会出现背景音乐，如下图（以edge为例）
![%%V0WUNY6Z)%%616R`~PNRL](https://github.com/grealuffy/-/assets/143927752/e057a208-1d0d-4a10-a184-2ca6b05fcf4f)
![image](https://github.com/grealuffy/-/assets/143927752/30cc4ccc-2f05-4c37-9664-016a8dae390f)
![image](https://github.com/grealuffy/-/assets/143927752/c3d3f2b7-9d11-44d1-ae42-3175be86f13a)
## 进入游戏后运行界面如下图
![image-4](https://github.com/grealuffy/-/assets/143927752/0bc09bfc-ca61-493c-937e-d8271a8d2b9c)
![image-5](https://github.com/grealuffy/-/assets/143927752/d6cd02e6-6e4d-40b6-9af1-18d2e15800fd)
### 完善后的简单模式界面
![image](https://github.com/grealuffy/homework-2/assets/143927752/83f634cf-013c-40f1-8895-86e7a18dc93b)
![image](https://github.com/grealuffy/homework-2/assets/143927752/b9bcec6b-64ae-4771-a214-0e2b4784c5f1)
![image](https://github.com/grealuffy/homework-2/assets/143927752/91e4ac72-f49d-44d0-b4e9-eeb09a1f3658)
![image](https://github.com/grealuffy/homework-2/assets/143927752/01da77b3-d136-4d48-a216-1db3bd9e157e)

### 完善后的困难模式界面
![image](https://github.com/grealuffy/homework-2/assets/143927752/9452312d-bfb3-49af-9805-a00c32f25593)
![image](https://github.com/grealuffy/homework-2/assets/143927752/f5618103-c290-48f9-9ba6-684ded9f3eed)

