<h2>8.2.1 记录条件评估中的日志更改</h2>

默认情况下，每次应用程序重新启动时，都会记录一个报告，其中显示了项目中进行修改的内容。该报告显示了在进行更改（例如添加或删除Bean以及设置配置属性）时对应用程序自动配置的更改。

要禁用报告的日志记录，请设置以下属性：
```bash
spring.devtools.restart.log-condition-evaluation-delta=false
```
