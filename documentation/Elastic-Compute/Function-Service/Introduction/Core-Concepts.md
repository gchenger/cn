# 核心概念 

## Serverless

用户使用Serverless服务，无需关心底层服务器等基础设施，只需关心业务本身，使得整体业务实现了轻量化。服务会根据业务实际需求实时弹性伸缩所需资源，而用户只需为资源的实际消耗付费。

 

## 函数即服务（FaaS）

函数即服务（FaaS） 提供了一种无状态、由事件触发、短暂、弹性伸缩的Serverless计算服务。

函数即服务由事件触发，函数仅在事件发生时由事件触发执行，并只处理本次事件，无状态运行。函数服务根据业务的实时并发量自动伸缩所需资源来应对业务的高峰低谷。

 

## 函数（Function）

函数是函数服务中的最小资源单位，每个函数包括用户自定义代码和任何依赖库。

 

## 事件（Event）

函数由事件触发并执行。触发器在触发函数时会将事件传递给Function。事件在传递时采用特定的JSON数据结构，并以event入参的方式传递给Function。

 

## 触发器（Trigger）和事件源(Event Source)

触发器是触发函数执行的方式。

事件源是一个触发函数并执行其逻辑的京东云服务。

事件源产生事件，当事件发生时，如果满足触发器定义的规则，事件源则调用触发器所对应的函数，根据事件源的特点以同步或异步的方式触发函数执行。
