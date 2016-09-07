## 功能描述
PassPwned 是一个用于查询社工库的API接口，该接口基于MySQL数据库并使用PHP开发，接口包括：
* 查询社工库站点/数据量/接口调用统计；
* 查询基于关键词的站点信息；
* 查询基于关键词的数据详细信息；
接口返回采用Json格式，用于同域站点下的接口调用和访问。

## 接口设计
PassPwned 基于MySQL数据库设计，采用统一的表前缀，表类型分为站点数据表和基础表。
其中site_index、site_item、api_call为默认基础表，表说明如下：
* site_index：站点信息及表信息索引表；
* site_item: 站点数据表字段记录表；
* api_call： 接口调用统计表；
接口实现依赖于基础表的构建，否则会造成接口查询错误。

## 接口配置
config.php 为接口配置文件，其中可配置的内容包括：
* 数据库连接信息
* 表前缀信息
* 基础表表名信息

## UML类图
