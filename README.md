# RecruitCleanAnalysis

### 分析结果：
 - 地图展现各地区 爬虫相关公司的 聚集度，见[country_rank.png](https://github.com/BuleAnt/RecruitCleanAnalysis/blob/master/country_rank.png) 文件
 - 展现最适宜应聘的公司图，见[plt1.png](https://github.com/BuleAnt/RecruitCleanAnalysis/blob/master/plt1.png)和[plt3.png](https://github.com/BuleAnt/RecruitCleanAnalysis/blob/master/plt3.png)文件

### 简要说明：
 对智联招聘“爬虫”关键字搜索职位数据做的一个分析，对于爬虫关键字职位搜索数据，见我的[智联招聘爬取数据爬取](https://github.com/BuleAnt/RecruitScrapy)。**

## 对智联招聘数据进行清洗和分析

**工具**：  Jupyter Notebook ,请大家自行安装


**数据集**： 文中数据集为 我的电脑上的数据集，请大家自行更改为自己的路径，[数据集地址](https://github.com/BuleAnt/RecruitScrapy/blob/master/RecruitScrapy/data/getRecruitList.csv)


**Untitled.ipynb**： 为分析文件，大家自行运行。查看

### 分析内容：
  
  - 对清洗后的数据进行了地区分组，统计出每个地区的相关公司数，并展现在地图上，见country_rank.png 文件。可以从地图上直观的看到，地区相关度职位的热度

  - 对各公司的 规模、工资、工作经验、反馈率 转换对应的权值，生成堆积条状图，见plt1.png和plt3.png文件。可以直观的看到，哪个公司最适合应聘
  
### 规模、工资、工作经验、反馈率转换权值规则， 这里是站在求职者的角度来看
   - 规模：
   
    ```
    #生成公司规模列表
    scaleList = ['20','20-99','100-499','500-999','1000-9999','10000']
    #替换权值列表
    scaleValueList = [4,8,10,12,14,18]
    ```
   
   
   - 工资：
   
    ```
    #求工资区间的中位数，并除1000 转换为单位为 K
    ```
   
   
   - 工作经验： 
   
    ```
    #生成工作经验列表
    experienceList = ['0-1','1-3','3-5','5-10']
    #替换权值列表
    scaleValueList = [8,6,4,1]
     ```
    
   - 反馈率： 
   
     ```
     #取发聩率的十位数部分，反馈率默认为 20%
     ```
    
