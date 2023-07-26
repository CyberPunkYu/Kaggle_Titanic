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

