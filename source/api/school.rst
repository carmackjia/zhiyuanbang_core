院校
=======

GET /j/school/[idSchool]
----------------------------
* Required permissions: read
* ReturnValue:

  + id
  + schoolName
  + schoolCode
  + is211
  + is985
  + hasGraduateSchool 是否有研究生院
  + shortNameList (简称列表)
  + degreeLevel: 可授予的学历层次 
    
    * Valid Values:
      
      + 本科
      + 高职高专

  + runningType: 办学性质
    
    * Valid Value:

      * 大学
      * 学院
      * 高等职业技术学校
      * 高等专科学校
      * 高等学校分校
      * 独立学院
      * 短期职业大学
      * 成人高等学校
      * 教育学院
  
  + schoolType: 院校类型
    
    * Valid Value:
      
      * 综合
      * 工科
      * 农业
      * 林业
      * 医药
      * 师范
      * 语言
      * 财经
      * 政法
      * 体育
      * 艺术
      * 民族
      * 军事
  
  + schoolOrganizerType: 举办者类型
      * 公办
      * 民办
  
  + logo

      * fields

        * filename: 图片名称
        * url: 链接地址
        * size: 图片大小
        * isCurrent: 是否为当前使用？
  
  + authority

    * name: 主管部门名称
    * type:
      
      * 教育部
      * 其他中央部委
      * 地方所属

  + location

    * province: 省/自治区/直辖市
    * city: 城市
    * address: 通讯地址
    * campus：校区

        * isMain: 是否为主校区
        * address: 校区的地址
        * name: 校区的名称

  + telephone

    * fields:

        * name: 电话名称
        * number: 电话号码（区号、具体号码、分机号）
        * type: 电话类型
        * comment：电话注记

  + fax 学校传真

    * name: 电话名称
    * number: 具体号码

  + website 院校网址

    * fields:

      * name: 名称
      * type: 站点类型
      * url: 链接地址

  + weibo 学校微博

    * fields:

      * platform: 平台

        * Valid value:
          
          + 新浪微博
          + 腾讯微博

      * name: 微博名称
      * type: 微博类型
      * contactName: 简称
      * url: 微博地址
      * isMain: 是否为主要微博


  + weixin 学校微信
     
     * fields: 

      * name 名称
      * shortName: 简称
      * number: 号码

  + intro
      
      * short: tiny简介（20个字封顶）
      * baike:
         
         * type: 百科的类型
         * name: 词条的名称
         * url:  链接地址
         * content: 词条内容
         * summary: 词条汇总


GET /j/school/[idSchool]/history
----------------------------------

* fields: 

  * 创建
        
      * type: 创建
      * create_time: 创建时间 
      * create_name: 创建名称

  * 升格

      * type: 升格
      * time: 时间
      * from_name: 之前的名称
      * to_name: 新改过的名字

  * 合并组建

     * type: 合并组建
     * time: 时间
     * cooperator: 共建者列表
     * old_name: 老名称
     * new_name: 新名称 

  * 改建

     * type: 改建
     * time: 时间
     * cooperator: 共建者列表
     * old_name: 老名称
     * new_name: 新名称

  * 并入

     * type: 并入
     * time: 时间
     * mergeList:

       * fields:

        * school: xxxx 院校
        * major:  xxxx 专业列表

     * new_name: 新名称 

  * 更名

     * type: 更名
     * time: 时间
     * from_name: 老名称
     * to_name: 新名称     