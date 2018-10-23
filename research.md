## ensemble GAssist
![image](https://cdn.someecards.com/someecards/usercards/1331054374953_8341913.png)

- 比較は個体数を固定して島の数で割る，そこから今後の評価を行う．
- 総評価回数を同じにすればいい？ crazy.

#### defaultクラスをなくす
- how about setting default class to auto
- default setting of keel disabled default class sucks

##### how to do
1. 给每一个数据中添加一个其他pattern，只添加在训练集就可以么？
    - 这个pattern 需要读取数据的属性数然后定义
    - 添加这个pattern后设定default class为minor
    - 在计算的时候应该是不带入这个pattern的计算，感觉比较麻烦.

##### why need default class
- refer to [GAssist2014](http://ico2s.org/data/papers/Bacardit2004.pdf) 
- use default class can drastically reduce the number of rules inside a classifier.
- only need to learn one class (in a two-class data), so search space is reduced.
- less rules may lead to not like to over-fitting which leads to better test acc.
- [imp] if disable default class we may need to loose the strict of number of rules in each classifier.

#### パターン移動
##### 属性のサンプリング

- 違う島の間で違う属性を使う．
- 普通にサンプリング

#### Random Forest
- 并行集成学习的著名代表
- 基于自助采样法(bootstrap sampling)
- 对于结果bagging通常对分类任务使用简单投票法，对回归任务使用简单平均法。
- 与AdaBoost只适用于二分类任务不同，Bagging可以用于多分类，回归等任务.
- Bagging的另一个优点是由于每一个base classifier只使用了初始训练集中月63.2%的样本，剩下约36.8%的样本可用作验证集来对泛化性能进行out-of-bag estimate.

##### 结合策略
1. 由于学习任务的假设空间大，可能有多个假设在训练集上达到同等性能。此时若使用单学习器可能会因误选而导致泛化性能不佳，结合多个学习器会减小风险。
2. 

##### build diversity between base classifiers


##### diversity measure


###### disagreement measure
- dis = (b+c) / m

###### correlation coefficient
- pij = (ad - bc) / root{(a+b)(a+c)(c+d)(b+d)}

###### q-statisticc
- qij = (ad - bc) / (ad + bc)
