1.tf.Session()和tf.InteractiveSession()两种会话的区别可以通过查看是否支持直接使用eval()进行区分
2.将图设置为默认图使用tf.Graph.as_default()，此方法会返回一个上下文管理器。如果不显示的添加一个默认图，系统会自动设置一个全局的默认图。所设置的默认图，在模块范围内定义的节点都将自动加入默认图中。
3.tf.get_default_graph()方法获取到当前环境中的图
4.多个图需要多个会话来运行，每个会话会尝试使用所有可用的资源。
  不同图、不同会话之间无法直接通信。
  最好在一个图中有多个不连贯的子图
5.Tensorflow的边有两种连接关系：数据依赖和控制依赖
6.张量的阶可以使用tf.rank()获取到
7.获取shape方法：a.shpe   a.get_shape()   tf.shape(a)    a.get_shape().as_list()
8.数据类型转化：tf.cast()   string转化为number不能使用tf.cast() 数字字符转化为数字使用tf.string_to_number()
9.tf.matmul()通常用来做矩阵乘法
  tf.transpose()转置
10.张量变形：tf.reshape()
   张量切片：tf.slice(input_,begin,size,name=None)
   张量分裂：tf.split()
11.序列常量：tf.linspace(start,stop,num,name=None)
            tf.range(start,limit=18,delta=3)
12.使用tf.get_variable()方法生成一个变量时，其name不能与已有的name重名。
13.直接使用tf.global_variables_initialize()与tf.local_variables_initializer()即可初始化全部变量
14.图构建好之后，运行图时，需要使用张量替代占位符，否则这个图无法运行。