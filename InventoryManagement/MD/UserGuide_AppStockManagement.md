## USERGIDE

| 版本 | 日期      | 作者 | 修改注释 |
| ---- | --------- | ---- | -------- |
| 1.0  | 2018-9-12 | 张玉 |          |
|      |           |      |          |
|      |           |      |          |
|      |           |      |          |

[TOC]



### 1.用户背景概述

本文档适用于上海优家家具SAP Business One项目。

上海优家家具是一家致力于打造让中国大众消费者买得起的优质美式家具公司。公司负责产品设计、品牌营销、供应链管理。产品是由国外工厂代工生产。

### 2.用户需求

优家的仓库非常的大，货品种类也非常繁多且基本都是打包的状态，所以在采购入库和销售出库的过程中由于仓管人员的疏忽会存在漏发多发甚至错发的情况，以至于给企业造成了损失，因此优家急需一套仓库信息管理系统来解决这些问题。下图是我在优家仓库现场考察时拍下的图片。

![20180829_094904](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\20180829_094904.jpg)

![20180829_094946](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\20180829_094946.jpg)

![20180829_112133](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\20180829_112133.jpg)

### 3.用户场景分析

场景1.供应商发给仓库一批货，仓管员根据货品清单对这些货品进行清点和确认，面对种类繁多以及全都是带着包装的货品，有些货品甚至相似，仓管人员在入库的时候可能会出错，给仓库的管理带来非常大的麻烦。

场景2.仓管人员要发一批货给客户，在出库之前，仓管人员照例依旧拿着货品清单为客户进行配货，在配货的过程中由于仓管人员的失误可能出现数量或者货品种类出错，给公司带来了损失，面对这种情况公司很苦恼。

### 3.解决方案

面对优家的需求，奥维奥研发了仓库管理APP，通过条码管理的方式为每件货品贴上条码，APP通过接口将优家的SAP B1端连接起来，APP端将会显示B1端的草稿单据，仓管人员在货品入库和出库之前对照着APP上的单据进行扫描，在扫描的过程中系统会识别这个货物是否属于当前订单，以及数量是否正确。这样面对种类繁多的货品只需要通过移动端的扫描就可以将后台和前端结合在一起，数据也能够互相的传递，如此一来便实现了仓库的信息化管理。

覆盖范围：产成品。

覆盖业务：采购、销售、调拨、盘点

### 4.产品简介

#### 4.1产品结构

![仓库管理系统](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\仓库管理系统.png)

#### 4.2 核心功能

1.接收B1端的库存任务：仓库主管在B1端创建库存任务下达给前端APP。

2.汇报库存任务：根据库存任务对即将出库或者入库的货品进行扫描

3.将汇报过的库存任务同步到B1中：汇报完毕之后点击同步在B1端生成单据，任务结束。

#### 4.3 产品核心目标

1.帮助企业实现移动端的信息化管理

2.帮助企业节省管理成本

### 5.业务场景

#### 5.1 采购收货草稿业务场景

#### 5.1.1 操作步骤

1.创建收货单，并将库存任务的状态改为下达，在库存任务编码处选择指派的仓管员，最后将单据另存为草稿，生成了草稿4077

![MDP01](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MDP01.png)

2.点击库存任务查看已下达的库存任务。

![MD02](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD02.png)

3.任务列表已经显示了在B1端的订单 ‘4068’。

![MD03](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD03.png)

4.左滑点击查看

![MD05](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD05.png)



5.任务行上显示了要进行出入库的物料，点击右下角的箭头进行进行扫描

![MD06](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD06.png)



6.点击左下角按钮单个选中扫描，点击右下角按钮批量扫描

![MD07](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD07.png)



7.这是批量扫描页面，点击右下角按钮，就能打开摄像头进行条码扫描

![MD08](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD08.png)

8.扫描后的结果返回在此页面中，根据任务数量可以进行数量的增加，也可继续重复扫描来添加数量。扫描完毕之后选择右上角的按钮保存结果。

![MD09](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD09.png)

9.扫描结果保存在这个页面上，确认无误点击右上角的保存按钮，就完成了这个任务的出入库操作。

![MD11](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\MD11.png)



10. 点击库存汇报，查找到刚才做过的4068这张单据

![md14](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\md14.png)

11.左滑点击查看

![md13](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\md13.png)

12.点击右上角的按钮选择同步到B1当中，生成单据。

![md15](D:\iWorkSpace\GitHub\UserStory\InventoryManagement\MD\image\md15.png)

#### 5.2采购退货草稿业务场景

略。。。。。。

#### 5.3销售应收发票草稿业务场景

略。。。。。。

#### 5.4库存转储草稿业务场景





