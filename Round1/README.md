# Round 1 介绍
环境搭建：
      1.在虚拟机上建立三个slave子机器和一个master，master和slave之间要建立互信关系。
      2.将四台虚拟机的网络模式改成桥接模式。
      3.安装securecrt
      4.安装openssh-client与lrzsz
      5.安装Java环境。然后s在securecrt里面检查安装openssh-client与lrzsz是否安装成功。
            上传jdk，然后赋予这个权限，配置Java环境。测试Java是否配置成功。
      6.安装Hadoop。配置Hadoop的环境变量。
      7.建立互信关系。生成公钥。slave复制master的公钥。测试链接。
   （以上所有具体操作。可见详情。G：Hadoop/hadoop安装)
 
 数据处理：
  1.  对十一月份的数据进行正则表达式处理。取出IP和访问地址
      将ip放到set集合当中。然后进行去重，输出set大小就是uv访问量。
  
  
  2.将整个数据放到mapreduce进行处理。show为主键，ip为value。
  reduce端口。统计数量。进行排序。输出j前十
  
  3.将相邻俩天的数据都拿出来进行比较。找相同ip，去重进行统计。查看前一天的set的size。
