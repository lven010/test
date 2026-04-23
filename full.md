# 目 录

# 引言.. 1

（一） 编写目的...  
（二） 定义...  
（三） 参考资料..

# 程序系统的结构.. 2

（一） 系统总图...  
（二） 在线业务... 2  
（三） 业务台帐... 3

# 三、 数据字典.. 3

# 四、 新建地价模块设计说明. 3

（一） 程序描述.. 3  
（二） 功能...  
（三） 输入项... 4  
（四） 输出项..   
（五） 流程逻辑.. 4  
（六） 接口...

# 五、 编辑地价业务. 9

（一） 程序描述.. 9  
（二） 功能... 9  
（三） 输入项... ..10  
（四） 输出项.. ..10  
（五） 流程逻辑.. ..11  
（六） 接口... .12

# 六、 红线上传设计说明. .14

（一） 程序描述.. .14  
（二） 功能... ..14  
（三） 输入项... .15  
（四） 输出项.. .15  
（五） 流程逻辑. .15  
（六） 接口.... ...16

# 1． 上传红线.. .16

# 七、 地价列表.. .16

（一） 程序描述.. .16  
（二） 功能... .17  
（三） 输入项... .17  
（四） 输出项.. ...18  
（五） 流程逻辑.. .18  
（六） 接口... .19

# 八、 地价数据导入模板下载. .21

（一） 程序描述. ..21  
（二） 功能.... ..21  
（三） 输入项... ...21

（四） 输出项.. ..22  
（五） 流程逻辑.. .22  
（六） 接口... ..23

# 九、 地价数据导入. .23

（一） 程序描述.. ..23  
（二） 功能... ..24  
（三） 输入项... ..24  
（四） 输出项.. ..25  
（五） 流程逻辑.. ..25  
（六） 接口... ..26

# 一、引言

# （一）编写目的

本文档为《三水区地价管理信息系统》概要设计说明书，对该系统的层次划分、模块功能、数据结构、接口、出错处理和扩展性进行设计，目的是让软件开发人员根据本文档的内容进行程序开发，使设计的产品符合用户的需求，同时为测试人员提供参考。

# （二）定义

《三水区地价管理信息系统》是整合各类国土房管资源数据的基础上，利用GIS 技术、数据库管理技术、软件开发技术等，建立专业、便捷、规范的土地综合数据管理系统，实现对国土资源核心数据的分层叠加与分析、查询与浏览、共享与交换、数据更新与历史管理，全方位服务于土地的各个业务环节，为管理决策部门提供科学的、准确的数据分析和决策支持。

# （三）参考资料

三水区地价管理信息系统软件需求规格说明书

# 二、程序系统的结构

# （一）系统总图

![](images/e515bcfe5764e8f866c890f5ec086a148cbaf585041ac458053eaefcde455f33.jpg)  
图 2-1 系统总图

# （二）在线业务

![](images/d4a71aaf7306c2ea3d64bbfb068437f55f7ff16ec4a56cad9809ef6c0de848a6.jpg)

图 2-2 在线业务

# （三）业务台帐

![](images/71be50c62b948bddac5703803ca6db3ea4617c768a39fab9f4a9d99ae08cd412.jpg)  
图 2-3 业务台帐

# 三、数据字典

参见三水区地价管理信息系统建设采购项目数据库设计说明书。

# 四、新建地价模块设计说明

# （一）程序描述

标定地价列表点击“新建”按钮 ，弹出新建地价界面。界面左侧由上而下显示台帐绑定的表单、台帐附件目录、台帐模板目录。点击左侧表单可进行表单切换，切换表单后表单中填写的数据会自动保存到数据库中，也可点击“保存”按钮手动进行保存。

# （二）功能

点击新建按钮，显示台帐新建界面。界面显示：

![](images/a296eabb643c830933c298e191b6a1fe0f8910bb37751b45abc753fc452a554a.jpg)

![](images/17acff3a379bff5762d5108c8b491274cca5e6436d17cd07bd4a1fad1e87bf36.jpg)  
图 5-2-1 新建台帐界面  
图 5-2-2 新建台帐 IPO 图

# （三）输入项

表单配置的各字段数据。

# （四）输出项

无

# （五）流程逻辑

![](images/1171ec5fb68dc8063eb8fbc6464ffd2f06b7e2872f1d1ebfd93801d951bf0fce.jpg)  
图5-2-3 新建台帐流程逻辑

# （六）接口

![](images/53aa4f7d47c0d95342a1d158c487ce3ba9c47bc70d956e39bb045996c507d34d.jpg)

![](images/3d2e69df768641c475f15bcf4b2fef951eba9b551ffe621cf313b14507cd9733.jpg)  
图 5-6-1 主界面说明

图 5-6-1 新建台帐

# 1．获取绑定按钮列表

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>buttonList: 获取绑定按钮列表</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 2．根据台帐名称获取附件树

接口类名称：LedgerFileController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getFileTree: 根据台帐名称获取附件树</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 3．根据地价信息获取模板树

接口类名称：LedgerTemplateController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getTreeInfo: 根据地 价信息获取模板树</td><td>ResultSet</td><td>String</td><td>台帐名称</td></tr></table>

# 4．获取表单树以及目录

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getFormCoreTree: 获取表单树以及目录</td><td>ResultSet</td><td>String</td><td>台帐名称</td></tr></table>

# 5．获取表单验证规则

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="2">getTaskFormValidRule:获取表单验证规则</td><td rowspan="2">ResultInfo</td><td>String</td><td>台帐名称</td></tr><tr><td>String</td><td>表单KEY</td></tr></table>

# 6．获取表单

接口类名称：FormCoreController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="2">getTaskForm: 获取表单</td><td rowspan="2">ResultSet</td><td>Integer</td><td>表单版本</td></tr><tr><td>String</td><td>表单KEY</td></tr></table>

# 7．根据业务编号查询台帐业务数据

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="3">get: 根据业务编号查询
出台帐业务数据</td><td rowspan="3">ResultInfo</td><td>String</td><td>台帐名称</td></tr><tr><td>String</td><td>表单KEY</td></tr><tr><td>String</td><td>业务编号</td></tr></table>

# 五、编辑地价业务

# （一）程序描述

点击地价列表“编辑”按钮，弹出台帐编辑界面。新建台帐时填写的表单数据、上传的附件文件也会回显到界面中。界面左侧由上而下显示台帐绑定的表单、台帐附件目录、台帐模板目录。点击左侧表单可进行表单切换，切换表单后表单中填写的数据会自动保存到数据库中，也可点击“保存”按钮手动进行保存。

# （二）功能

![](images/3e8505aa05cd57396fc209d06318e5fce6a1fc230be5b137c272ae0991d4fe4b.jpg)  
台帐编辑界面：

![](images/f009d019372a66467f21f4a425a6eaaea00f6b442fa942793b520041cfd648f1.jpg)  
图 6-2-1 台帐编辑界面

![](images/7e7e347e97b991ad5e8b338830f1e737c4a7d466dc10874750a44209f1566e2d.jpg)  
图 6-2-4 编辑台帐 IPO 图

# （三）输入项

表单配置的各字段数据。

# （四）输出项

无

# （五）流程逻辑

![](images/f2a073db879699b5c38b80be21b35bbbccd8629f28570f26bd2ba5c2217c7a15.jpg)  
图 6-5-1 编辑台帐流程逻辑

# （六）接口

![](images/658b35ca1fb100327dac80688b60c8b34a5f28d5097fe9e1fb90a13247f7aa29.jpg)  
图 6-6-1 编辑台帐

# 1．获取绑定按钮列表

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>buttonList: 获取绑定按钮列表</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 2．根据台帐名称获取附件树

接口类名称：LedgerFileController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getFileTree: 根据台帐名称获取附件树</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 3．根据地价信息获取模板树

接口类名称：LedgerTemplateController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getTreeInfo: 根据地 价信息获取模板树</td><td>ResultSet</td><td>String</td><td>台帐名称</td></tr></table>

# 4．获取表单树以及目录

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getFormCoreTree: 获取表单树以及目录</td><td>ResultSet</td><td>String</td><td>台帐名称</td></tr></table>

# 5．获取表单验证规则

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="2">getTaskFormValidRule:获取表单验证规则</td><td rowspan="2">ResultInfo</td><td>String</td><td>台帐名称</td></tr><tr><td>String</td><td>表单KEY</td></tr></table>

# 6．获取表单

接口类名称：FormCoreController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="2">getTaskForm: 获取表单</td><td rowspan="2">ResultSet</td><td>Integer</td><td>表单版本</td></tr><tr><td>String</td><td>表单KEY</td></tr></table>

# 7．根据业务编号查询台帐业务数据

接口类名称：LedgerController；

接口方法：  

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="3">get: 根据业务编号查询
出台帐业务数据</td><td rowspan="3">ResultInfo</td><td>String</td><td>台帐名称</td></tr><tr><td>String</td><td>表单KEY</td></tr><tr><td>String</td><td>业务编号</td></tr></table>

# 六、红线上传设计说明

# （一）程序描述

用于直接使用红线文件上传红线示例。

# （二）功能

打开流程示例，点击红线上传按钮，弹出上传文件选择窗口，选择红线文件上传。

![](images/686f2a555bbb4462a10c20afc855d5d661ffd5c0d4a03d7b3a97a24486db2009.jpg)

![](images/42341207202f03d28c1ef640671281b44e38d13188de09cdfa599f910ae6dd53.jpg)  
红线上传 IPO图

# （三）输入项

红线文件

# （四）输出项

无

# （五）流程逻辑

![](images/c406b7a3fca4562e66d603a0ba779c0a815a5c3fe7ee3c728d3baa302b5debd9.jpg)

红线上传流程逻辑图

# （六）接口

![](images/43e4633933a07bc2548e75104b1b89a1657d627f5078f97eaf4a041585d2c864.jpg)

# 1．上传红线

接口类名称：LedgerRedLineInstanceController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="2">uploadRedLine: 上传红线</td><td rowspan="2">ResultInfo</td><td>String</td><td>地块号</td></tr><tr><td>File</td><td>红线文件</td></tr></table>

# 七、地价列表

# （一）程序描述

地价台帐字段信息以列表形式展示，上方显示搜索条件文本框。可输入需要搜索的文字进行模糊搜索，如需更多条件搜索，可点击搜索框右侧的展示按钮，展开更多搜索条件进行数据搜索。

# （二）功能

业务台帐列表界面，界面如下：

![](images/2df4f4fdc2785172fab7958ef2d154645a3772a23b118d191bb2f72ccf1641dc.jpg)  
图 8-2-1 台帐列表界面

输入查询内容 ，系统查询出数据并加载到界面中。

![](images/d79bde87f1f718e1dee85a6610813846f55854d636c37b9d373188c78974d048.jpg)  
图 8-2-2 台帐列表搜索界面

![](images/c66b5f58f1288a1bf1dda6ab8ecb957d18b5e19d0408ab8da7a344c2eac08355.jpg)  
图 8-2-3 台帐列表 IPO 图

# （三）输入项

无

# （四）输出项

打开台帐列表后，显示列表字段数据。

# （五）流程逻辑

![](images/ad48411dba2db9f4b53e21bb72f70029fc2d0e94e29c2b9551663e12ad4e9b1e.jpg)  
图8-5-1 台帐列表流程逻辑

# （六）接口

![](images/57117c89a8ee4c8631744216b4f0035e1b487b33426fe7c3404788c2ebc0f543.jpg)  
图 8-6-1 台帐列表

# 1.获取地价显示配置

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getPageShowConfig: 获取地价显示配置</td><td>ResultSet</td><td>String</td><td>台帐名称</td></tr></table>

# 2.地价高级查询查询接口

接口类名称：LedgerSearchConfigController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>list: 地价高级查询查询接口</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 3．获取台帐列表表头

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>getTodoTitle: 获取台帐列表表头</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 4．获取业务台帐列表数据接口

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td rowspan="3">list: 获取业务台帐列表数据接口</td><td rowspan="3">ResultInfo</td><td>String</td><td>台帐名称</td></tr><tr><td>Integer</td><td>当前页数</td></tr><tr><td>Integer</td><td>每页数量</td></tr></table>

# 八、地价数据导入模板下载

# （一）程序描述

点击台帐菜单，进入到业务台帐列表界面。点击“模板下载”按钮 ，数据导入模板会自动下载到本地电脑。

# （二）功能

![](images/1fa9c0bd242a4b02c51300d51815c85885a551dfc11534bff7aafa45949cc7af.jpg)  
图 9-2-1 数据导入模板下载IPO图

# （三）输入项

无

# （四）输出项

下载数据导入模板文件。

# （五）流程逻辑

![](images/ba33fb5e40ce8c65cc0c412115016150d054dd73de842a2753858d9b71980fd5.jpg)  
图9-5-1 数据导入模板下载流程逻辑

# （六）接口

![](images/e118de645a2c7f570a90114bd50cdb1504e45e6b274e8e96539133071ee1d805.jpg)  
图 9-6-1 数据导入模板下载

# 1．导出地价数据导入模板

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>exportLedgerTemplate: 
导出地价数据导入模板</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>

# 九、地价数据导入

# （一）程序描述

先将数据导入模板下载本地，并将数据填写到模板中。点击“导入”按钮 ，选择模板文件，点击确定即完成数据导入操作。数据导入完成后列表会显示出导入的数据。

# （二）功能

台帐数据导入界面：

![](images/7d55d51296759ebfc5133e2ac4a800e52f72cd1842ee14d0724f7bc344283199.jpg)  
图 10-2-1 数据导入界面

选择模板文件界面：

![](images/f6466508b134a7fcb57f9d197fc41068f04a8cd59d639dccb00d090a2b9363be.jpg)

![](images/2f23c19df25e1cd38bbbaeb8dec8f146254f3152586705183baa2381dbe3317d.jpg)  
图10-2-2 选择模板文件界面  
图 10-2-2 数据导入 IPO 图

# （三）输入项

<table><tr><td>名称</td><td>数据的类型</td><td>有效范围</td><td>输入的方式</td></tr><tr><td>选择数据导入模板</td><td></td><td></td><td>鼠标人工选择</td></tr></table>

# （四）输出项

列表加载出导入的数据。

# （五）流程逻辑

![](images/133eb83c20432fc80851f00845f88eb88f84269a519c4950b76a4c3718cad95f.jpg)  
图 10-5-1 台帐数据导入流程逻辑

# （六）接口

![](images/5984c75bf3acf5ce5616373ed9f2f7cf9b08e23e190f1980d0757a89175daf72.jpg)  
图 10-6-1 数据导出

# 1．导出地价信息

接口类名称：LedgerController；

接口方法：

<table><tr><td>名称与描述</td><td>返回类型</td><td>参数类型</td><td>参数描述</td></tr><tr><td>export: 导出地价信息</td><td>ResultInfo</td><td>String</td><td>台帐名称</td></tr></table>