1、打开security的debug log
-Djava.security.debug=all
安全的随机数
1、随机数加密
  加密算法获取
2、随机数种子
    计算机熵

    熵的获取
    配置
    使用


+ #### java.security.SecureRandom

SecureRandom的实现由两点要求
1、随机数的种子必须是不可预知的
2、随机数的输出序列必须是经过加密算法加密的
