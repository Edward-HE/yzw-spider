# 研招网数据爬虫项目

本项目 fork 自 [yzw](https://github.com/Hthing/yzw) ，是原项目功能的修改版。主要功能为 https://yz.chsi.com.cn/zsml/queryAction.do 页面的数据爬取。

## 主要修改功能为

-   所在省市、门类类别、学科类别可以选为空，实现对某一省市、某一学科所有学校的批量爬取。
-   将 excel 格式改为 csv 格式存储
    -   原本的 excel 格式不适合大量数据写入，xlwt 只能写入 .xls 格式，且一次只能写入 65535 条数据，可以使用 openpyxl 代替，但考虑后决定还是采用 csv 格式写入，以尽可能满足大量数据写入的需求

## TODO

-   [ ] MySQL 写入可能存在写锁问题，数据不能完全写入，有部分丢失
