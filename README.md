# Kaggle_Titanic

for getting started with Titanic

入门项目，主要是为了熟悉Kaggle流程，所以主要跟随Discussion中的baseline和Top进行，为之后的ICR做准备


## 数据集获取
```kaggle
pip install kaggle
kaggle competitions download -c spaceship-titanic
```
## 数据集介绍
* PassengerId => 乘客ID  yyyy_xx  yyyy表示一个group，通常为家庭
* HomePlanet => 家乡星球
* CryoSleep => 是否处于休眠状态
* Cabin => 入住舱室号 甲板/数字/边  其中边分为P左舷和S右舷
* Destination => 目的地
* Age => 年龄
* VIP => 是否为VIP
* RoomService, FoodCourt, ShoppingMall, Spa, VRDeck => 乘客在泰坦尼克号宇宙飞船的众多豪华设施中所支付的费用
* Name => 乘客姓名
* Transported => 乘客是否被传送到另一个维度

有部分问题：(似乎不用弄懂实际的语境意义，但对理解题目还是有一定帮助)
- 乘客来源星球是否是实际价值，earth europa mars
- 入住舱室号中哪些甲板和数字更有价值
- 目的地的不同是否能区分乘客的价值
- 乘客的年龄是否能区分乘客的价值
- 各种豪华设施是否是等价的而没有排名次序的
- 乘客姓名是否无用

## 总流程
数据集获取 &rarr; 特征工程 &rarr; 模型选择 &rarr; 模型训练 &rarr; 模型评估 &rarr; 模型调优 &rarr; 模型融合

## 待优化
看了Top方案，发现对数据的理解还是不到位
- 乘客应该按照年龄段分类
- 乘客的同行数量还是有一定影响，可以添加一个特征表示乘客是否是solo
- 乘客的来源地会影响乘客的甲板位置
- 甲板上房间的数量越少，说明改甲板越高级，越有可能是VIP
- 甲板两侧房间分布应该是均匀的
- 甚至能根据姓名得出家庭人数？
- 穷举模型20多个+穷举超参数，逆天
- 交叉验证后，选择十个模型进行融合

## 总结
大概了解了kaggle的比赛流程和常用方法，对于大部分Top方案，最重要的部分都在特征工程和预处理上面，模型的话都是用库，其实都差不多，如果不追求rank10%，其实慢慢手动调参也行
