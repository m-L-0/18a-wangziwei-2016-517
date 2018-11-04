1.tf.where不传入第二、三个参数时，返回条件为真的每个元素的索引
  比较运算中，参与比较的元素必须具有相同的dtype,否则无法比较
2.tf.group可以将一系列op、Tensor组合成为一个op，没有返回值
3.一般的多路分支选择结构使用tf.case来实现，接收一个由case项组成的list，每个case项都是由条件与执行函数组成的元组。
4.tf.while_loop中的cond和body函数的参数必须一样，body的返回值必须与参数一样，cond、body函数的输入参数如果为变量，使用了变量的初始值作为输入张量。
5.tf.equal  tf.not_equal不支持运算符重载
