# openssh-magic-change 魔改OPENSSH(试验品)


# 说明
工作需要,曾经拜读过OPENSSH的源码,并基于此改造和实现了一些功能,大部分是实验性质,测试我期望的功能

## 可以实现的功能
-   透明代理,这里指的是类似中间人性质的(MAN-IN-THE-MIDDLE)
-   SSH蜜罐
-   密码审计/操作审计等

## 值得研究的点
-   证书认证
-   ProxyCommand实现
-   OPENSSH+RBAC


##  参考资料
<br>
[OPENSSH 证书认证](https://juejin.im/post/5aa114f7518825555f0c8af5)<br><br>
[Pritunl Zero](https://zero.pritunl.com/)<br>

## discuss

- ringbuffer@126.com
