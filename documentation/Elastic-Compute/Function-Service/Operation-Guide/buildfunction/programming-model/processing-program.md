# 处理程序

在创建function函数时，需要指定一个事件处理程序，并指定对象 `event`、`context` 和 `callback`。遵循以下通用的语法结构：
```
   def my_handler(event, context):
   return 'hello world'
   ```
   

`event`:function从event参数中获取函数的输入事件，调用函数时传入的数据。此参数通常是Python dict类型。也可以是list、str、int、float或NoneType类型。您可以根据function定义好的格式编写代码从event参数中获取需要的信息。

 

`context`:function通过context参数向您的处理程序提供运行时信息。包括您的个人信息和其他信息。格式参考context对象

 

`callback`（可选）：处理程序返回值，通知终止运行函数并返回信息给调用方。您必须主动和调用callback函数，否则会出现超时错误。

* 如果您使用 RequestResponse 调用类型（同步调用），function会将 Python 函数调用的结果返回到调用 function函数的客户端。例如，function控制台使用 RequestResponse 调用类型，因此当您使用控制台调用函数时，控制台将显示返回的值。

  如果处理程序返回 NONE，function将返回 null。

* 如果您使用 Event 调用类型（异步调用），则丢弃该值。

例如：创建一个函数名为 my_handler 的函数，入口函数设置为index.handler。执行代码从event参数接收输入事件并返回包含数据的消息。
```
 def my_handler(event, context):
    message = 'Hello {} {}!'.format(event['first_name'], 
                                    event['last_name'])  
    return { 
        'message' : message
    }  
```
