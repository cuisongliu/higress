# 股票助手

API认证需要的APP Code请在阿里云API市场申请: https://market.aliyun.com/apimarket/detail/cmapi00065924

## 什么是云市场API MCP服务

阿里云云市场是生态伙伴的交易服务平台，我们致力于为合作伙伴提供覆盖上云、商业化和售卖的全链路服务，帮助客户高效获取、部署和管理优质生态产品。云市场的API服务涵盖以下几个类目：应用开发、身份验证与金融、车辆交通与物流、企业服务、短信与运营商、AI应用与OCR、生活服务。
云市场API依托Higress提供MCP服务，您只需在云市场完成订阅并获取AppCode，通过Higress MCP Server进行配置，即可无缝集成云市场API服务。

## 如何在使用云市场API MCP服务

1. 进入API详情页，订阅该API。您可以优先使用免费试用。
2. 前往云市场用户控制台，使用阿里云账号登陆后查看已订阅API服务的AppCode，并配置到Higress MCP Server的配置中。注意：在阿里云市场订阅API服务后，您将获得AppCode。对于您订阅的所有API服务，此AppCode是相同的，您只需使用这一个AppCode即可访问所有已订阅的API服务。
3. 云市场用户控制台会实时展示已订阅的预付费API服务的可用额度，如您免费试用额度已用完，您可以选择重新订阅。

# 功能简介

## 功能简介

`stock-helper` 服务器是一个专为股票、期货及外汇市场设计的多功能API服务。它提供了多种工具，包括K线图、报价、排行等，以帮助用户获取实时和历史数据，进行技术分析和决策支持。通过这些工具，用户可以轻松地访问到A股、港股、美股、全球指数、内盘和外盘期货以及外汇市场的相关信息。

## 工具简介

### A股K线
- **用途**: 提供A股不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 技术分析、交易策略制定、历史数据回测等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `ma`: 返回MA均线，可选值为：5,10,15,20,25,30。
  - `symbol`: 品种代码，例如sh688193。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### A股K线复权
- **用途**: 提供A股复权后的K线数据。
- **使用场景**: 长期投资分析、基本面分析等。
- **参数**:
  - `fuquan`: 复权状态，0不复权，1前复权，2后复权。
  - `limit`: 返回条数，默认10。
  - `symbol`: 品种代码，例如sh688193。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### A股报价
- **用途**: 提供A股的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 品种代码，以英文逗号分割，如sz000002,bj430047。

### A股排行
- **用途**: 提供A股按特定条件（如涨跌率、成交量等）排序的排行榜。
- **使用场景**: 发现热点股票、市场趋势分析等。
- **参数**:
  - `asc`: 排序顺序，0倒序（由大到小），1正序（由小到大），默认0。
  - `limit`: 每页条数，最大100条，默认10。
  - `market`: 市场代码，如沪深A股、创业板等。
  - `page`: 页码，默认1。
  - `sort`: 排序字段，如涨跌率、成交量等。

### 全球指数K线
- **用途**: 提供全球指数的不同时间周期（如日K、周K、月K等）的K线数据。
- **使用场景**: 全球市场分析、资产配置等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 指数品种代码，详见代码表。
  - `type`: K线类型，如日K、周K、月K等。

### 全球指数报价
- **用途**: 提供全球指数的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 指数品种代码，详见代码表。

### 内盘期货K线
- **用途**: 提供内盘期货不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 期货市场分析、交易策略制定等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 期货品种代码，详见代码表。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### 内盘期货合约
- **用途**: 提供内盘期货合约的相关信息。
- **使用场景**: 合约选择、风险管理等。
- **参数**:
  - `symbol`: 期货品种代码，详见代码表。

### 内盘期货报价
- **用途**: 提供内盘期货的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 期货品种代码，详见代码表。

### 外汇K线
- **用途**: 提供外汇不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 外汇市场分析、交易策略制定等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 品种代码，如FXINDEX，详见代码表。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### 外汇报价
- **用途**: 提供外汇的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 品种代码，如FXINDEX,CNYRUB，详见代码表。

### 外盘期货K线
- **用途**: 提供外盘期货不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 期货市场分析、交易策略制定等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 期货品种代码，详见代码表。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### 外盘期货合约
- **用途**: 提供外盘期货合约的相关信息。
- **使用场景**: 合约选择、风险管理等。
- **参数**:
  - `symbol`: 期货品种代码，详见代码表。

### 外盘期货报价
- **用途**: 提供外盘期货的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 期货品种代码，详见代码表。

### 港股K线
- **用途**: 提供港股不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 港股市场分析、交易策略制定等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 品种代码，如08026。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### 港股报价
- **用途**: 提供港股的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 品种代码，以英文逗号分割，如08026,02203。

### 港股排行
- **用途**: 提供港股按特定条件（如涨跌率、成交量等）排序的排行榜。
- **使用场景**: 发现热点股票、市场趋势分析等。
- **参数**:
  - `asc`: 排序顺序，0倒序（由大到小），1正序（由小到大），默认0。
  - `limit`: 每页条数，最大100条，默认10。
  - `page`: 页码，默认1。
  - `sort`: 排序字段，如涨跌率、成交量等。

### 美股K线
- **用途**: 提供美股不同时间周期（如1分钟、5分钟、日K线等）的K线数据。
- **使用场景**: 美股市场分析、交易策略制定等。
- **参数**:
  - `limit`: 返回条数，默认10。
  - `symbol`: 品种代码。
  - `type`: K线类型，如1分钟、5分钟、日K线等。

### 美股品种
- **用途**: 提供美股品种的相关信息。
- **使用场景**: 品种选择、风险管理等。
- **参数**:
  - `market`: 市场，如美交所、纽交所、纳斯达克。

### 美股报价
- **用途**: 提供美股的实时报价信息。
- **使用场景**: 实时监控、快速交易决策等。
- **参数**:
  - `symbol`: 品种代码，以英文逗号分割，如INTC,AAPL。

### 美股排行
- **用途**: 提供美股按特定条件（如涨跌率、成交量等）排序的排行榜。
- **使用场景**: 发现热点股票、市场趋势分析等。
- **参数**:
  - `asc`: 排序顺序，0倒序（由大到小），1正序（由小到大），默认0。
  - `limit`: 每页条数，最大100条，默认10。
  - `market`: 市场代码，如全部美股、科技股、中概股等。
  - `page`: 页码，默认1。
  - `sort`: 排序字段，如涨跌率、成交量等。
