# 更新日志

本文档记录了项目的v1.3.7以来的重要变更。

## [1.4.5](https://github.com/Do1e/mijia-api/compare/v1.4.4...v1.4.5) - 2025-06-16
### bugfix
* 登陆过程中无法获取用户信息时，处理相关报错

## [1.4.4](https://github.com/Do1e/mijia-api/compare/v1.4.3...v1.4.4) - 2025-06-14
### new feature
* `get_device_info`支持[https://home.miot-spec.com/](https://home.miot-spec.com/)中的中文描述
### bugfix
* cli修复了执行`get_device_info`必须先登录的问题
### improvement
* 优化日志输出
* 使用`login`方法的警告修改得更加明确

## [1.4.3](https://github.com/Do1e/mijia-api/compare/v1.4.2...v1.4.3) - 2025-05-22
### bugfix
* 针对部分特殊的设备，修复了`get_device_info`的TypeError

## [1.4.2](https://github.com/Do1e/mijia-api/compare/v1.4.1...v1.4.2) - 2025-05-19
### new feature
* `get_device_info`支持缓存结果以加速

## [1.4.1](https://github.com/Do1e/mijia-api/compare/v1.4.0...v1.4.1) - 2025-05-19
### new feature
* cli支持`--run`以使用自然语言描述需求，交给小爱音箱执行

## [1.4.0](https://github.com/Do1e/mijia-api/compare/v1.3.14...v1.4.0) - 2025-05-19
### new feature
* 新增`mijiaAPI`的cli支持，运行`mijiaAPI --help`查看帮助

## [1.3.14](https://github.com/Do1e/mijia-api/compare/v1.3.13...v1.3.14) - 2025-05-18
### bugfix
* `available`属性判断错误，始终返回False

## [1.3.13](https://github.com/Do1e/mijia-api/compare/v1.3.12...v1.3.13) - 2025-05-18
### new feature
* 新增从cookie中提取有效期并保存在凭据中
### improvement
* `available`属性根据有效期判断

## [1.3.12](https://github.com/Do1e/mijia-api/compare/v1.3.11...v1.3.12) - 2025-05-16
### improvement
* 简化`mijiaLogin`的初始化参数，根据`save_path`的值自动判断是否需要保存凭据
* 重构了对象初始化和方法的注释

## [1.3.11](https://github.com/Do1e/mijia-api/compare/v1.3.10...v1.3.11) - 2025-05-16
### bugfix
* 验证保存路径并确保在保存验证数据之前确保目录存在

## [1.3.10](https://github.com/Do1e/mijia-api/compare/v1.3.9...v1.3.10) - 2025-05-16
### improvement
* 使用logging模块替代print函数

## [1.3.9](https://github.com/Do1e/mijia-api/compare/v1.3.8...v1.3.9) - 2025-05-16
### new feature
* 新增用户个人信息查询
* 新增用户凭据的可选保存
### improvement
* 支持非tty的二维码打印
* 优化二维码图片的删除逻辑

## [1.3.8](https://github.com/Do1e/mijia-api/compare/v1.3.7...v1.3.8) - 2025-05-14
### improvement
* 新增了devices里所有方法的注释
* 新增了`mijiaDevices`实例化时的断言检查
* 新增了操作失败时的错误提示抛出与错误代码的详情
* 优化了`mijiaDevices`实例化时的内部变量的赋值逻辑
* 优化了多处代码的可读性与简洁性
### bugfix
* 修复多处由于数据类型更新而引发的警告

## [1.3.7](https://github.com/Do1e/mijia-api/compare/v1.3.6...v1.3.7) - 2025-05-14
### new feature
* 新增自定义`run_action`参数，`in`等python关键字，可在前面加上下划线`_`
* `mijiaDevices`支持传入设备名称(米家中自定义的名称)进行初始化
