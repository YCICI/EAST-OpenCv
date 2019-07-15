## 函数说明
### 1、tf.Graph
* 通过tensorboard用图形化界面展示出来的流程结构
* 整合一段代码为一个整体存在于一个图中

#### 1.1 
tensorflow的运算，表示为数据流的图graph
计算节点operation，数据节点：tensor对象在不同操作间的数据节点

### 2、tf.import_graph_def

将图从graph_def导入到当前默认图中

tf.import_graph_def(
    graph_def,
    input_map=None,
    return_elements=None,
    name=None,
    op_dict=None,
    producer_op_list=None
)

#### 参数

* **graph_def:** 包含要导入到默认图中的操作的GraphDef proto。
* **input_map:** 将graph_def中的输入名称(作为字符串)映射到张量对象的字典。输入图中指定的输入张量的值将被重新映射到相应的张量值。
* **return_elements:** 在graph_def中包含操作名的字符串列表，将作为operationobject返回;和/或graph_def中的张量名称，它们将作为张量对象返回。
* **name: (可选.)** 将前缀放在graph_def中名称前面的前缀。注意，这并不适用于导入的函数名。默认为"import".
* **op_dict:**(可选.) 已弃用，请勿使用
* **producer_op_list:** (可选.) 一个OpList原型，带有(可能是剥离的)图表生产者使用的OpDefs列表。如果提供了，那么根据producer_op_list的默认值，在graph_def中无法识别的ops attrs将被删除。这将允许稍后的二进制文件生成更多的graphdef被早期的二进制文件所接受。

