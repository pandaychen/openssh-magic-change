##  基于输入输出文本流的命令解析算法分析

####  输出文本
输出的文本序列：
```bash
2022/02/22 17:56:06 [76 97 115 116 32 108 111 103 105 110 58 32 84 117 101 32 70 101 98 32 50 50 32 49 55 58 52 48 58 51 57 32 50 48 50 50 32 102 114 111 109 32 49 50 55 46 48 46 48 46 49 13 13 10]
2022/02/22 17:56:06 Last login: Tue Feb 22 17:40:39 2022 from 127.0.0.1

2022/02/22 17:56:06 [35 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 35 13 10 13 10 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 13 10 35 32 32 32 32 32 32 32 32 32 32 32 32 32 32 229 174 137 229 133 168 233 171 152 229 142 139 231 186 191 232 173 166 231 164 186 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 35 13 10 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 35 13 10 35 32 230 137 147 231 160 180 229 174 137 229 133 168 232 190 185 231 149 140 239 188 140 233 128 154 232 191 135 231 171 175 229 143 163 232 189 172 229 143 145 231 173 137 231 167 129 229 187 186 231 174 161 231 144 134 233 128 154 233 129 147 227 128 129 232 191 144 232 161 140 230 129 182 230 132 143 231 168 139 229 186 143 231 173 137 229 177 158 228 186 142 232 191 157 229 143 141 229 174 137 229 133 168 233 171 152 229 142 139 231 186 191 239 188 129 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 35 13 10 35 32 232 175 183 229 139 191 229 156 168 230 156 141 229 138 161 229 153 168 228 184 138 233 128 154 232 191 135 83 83 72 32 45 76 47 45 68 47 45 82 231 173 137 229 145 189 228 187 164 229 174 158 231 142 176 231 171 175 229 143 163 232 189 172 229 143 145 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 35 13 10 35 32 232 175 183 229 139 191 229 156 168 230 156 141 229 138 161 229 153 168 230 144 173 229 187 186 86 80 78 32 83 101 114 118 101 114 227 128 129 83 104 97 100 111 119 115 111 99 107 231 173 137 228 187 163 231 144 134 230 156 141 229 138 161 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 35 13 10 35 32 232 175 183 229 139 191 229 156 168 230 156 141 229 138 161 229 153 168 232 191 144 232 161 140 230 140 150 231 159 191 231 168 139 229 186 143 227 128 129 231 151 133 230 175 146 230 156 168 233 169 172 231 173 137 230 129 182 230 132 143 230 136 150 232 128 133 228 184 141 231 161 174 229 174 154 231 154 132 231 168 139 229 186 143 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 32 35 13 10 35 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 45 35 13 10]
2022/02/22 17:56:06 #----------------------------------------------------------------------------------------------#

################################################################################################
#              安全高压线警示                                                                  #
################################################################################################
# 打破安全边界，通过端口转发等私建管理通道、运行恶意程序等属于违反安全高压线！                 #
# 请勿在服务器上通过SSH -L/-D/-R等命令实现端口转发                                             #
# 请勿在服务器搭建VPN Server、Shadowsock等代理服务                                             #
# 请勿在服务器运行挖矿程序、病毒木马等恶意或者不确定的程序                                     #
#----------------------------------------------------------------------------------------------#

2022/02/22 17:56:06 [27 93 48 59 117 115 101 114 48 49 64 57 46 49 51 52 46 49 50 48 46 50 52 53 7]
2022/02/22 17:56:06 ]0;user01@9.134.120.245
2022/02/22 17:56:06 [27 91 63 49 48 51 52 104 91 117 115 101 114 48 49 64 86 77 95 49 50 48 95 50 52 53 95 99 101 110 116 111 115 32 126 93 36 32]
2022/02/22 17:56:06 [?1034h[user01@VM_120_245_centos ~]$ 
2022/02/22 17:56:09 [105]
2022/02/22 17:56:09 i
2022/02/22 17:56:09 [102]
2022/02/22 17:56:09 f
2022/02/22 17:56:10 [99]
2022/02/22 17:56:10 c
2022/02/22 17:56:10 [111]
2022/02/22 17:56:10 o
2022/02/22 17:56:11 [110 102 105 103 32]
2022/02/22 17:56:11 nfig 
2022/02/22 17:56:11 [101]
2022/02/22 17:56:11 e
2022/02/22 17:56:12 [116]
2022/02/22 17:56:12 t
2022/02/22 17:56:12 [104]
2022/02/22 17:56:12 h
2022/02/22 17:56:12 [49]
2022/02/22 17:56:12 1
2022/02/22 17:56:14 [8 8 8 8 27 91 75]
2022/02/22 17:56:14 [K
2022/02/22 17:56:17 [13 10]
2022/02/22 17:56:17 

2022/02/22 17:56:17 [100 111 99 107 101 114 48 58 32 102 108 97 103 115 61 52 48 57 57 60 85 80 44 66 82 79 65 68 67 65 83 84 44 77 85 76 84 73 67 65 83 84 62 32 32 109 116 117 32 49 53 48 48 13 10 32 32 32 32 32 32 32 32 105 110 101 116 32 49 57 50 46 49 54 56 46 49 48 46 49 32 32 110 101 116 109 97 115 107 32 50 53 53 46 50 53 53 46 50 53 53 46 48 32 32 98 114 111 97 100 99 97 115 116 32 49 57 50 46 49 54 56 46 49 48 46 50 53 53 13 10 32 32 32 32 32 32 32 32 101 116 104 101 114 32 48 50 58 52 50 58 57 98 58 98 48 58 97 97 58 100 56 32 32 116 120 113 117 101 117 101 108 101 110 32 48 32 32 40 69 116 104 101 114 110 101 116 41 13 10 32 32 32 32 32 32 32 32 82 88 32 112 97 99 107 101 116 115 32 49 49 51 50 48 48 50 57 55 52 32 32 98 121 116 101 115 32 54 48 48 48 52 52 51 50 57 49 57 32 40 53 53 46 56 32 71 105 66 41 13 10 32 32 32 32 32 32 32 32 82 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 32 111 118 101 114 114 117 110 115 32 48 32 32 102 114 97 109 101 32 48 13 10 32 32 32 32 32 32 32 32 84 88 32 112 97 99 107 101 116 115 32 52 51 48 56 51 57 50 51 48 50 32 32 98 121 116 101 115 32 54 50 48 50 53 52 53 53 56 55 51 49 57 32 40 53 46 54 32 84 105 66 41 13 10]
2022/02/22 17:56:17 docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 192.168.10.1  netmask 255.255.255.0  broadcast 192.168.10.255
        ether 02:42:9b:b0:aa:d8  txqueuelen 0  (Ethernet)
        RX packets 1132002974  bytes 60004432919 (55.8 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4308392302  bytes 6202545587319 (5.6 TiB)

2022/02/22 17:56:17 [32 32 32 32 32 32 32 32 84 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 111 118 101 114 114 117 110 115 32 48 32 32 99 97 114 114 105 101 114 32 48 32 32 99 111 108 108 105 115 105 111 110 115 32 48 13 10 13 10]
2022/02/22 17:56:17         TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


2022/02/22 17:56:17 [101 116 104 49 58 32 102 108 97 103 115 61 52 49 54 51 60 85 80 44 66 82 79 65 68 67 65 83 84 44 82 85 78 78 73 78 71 44 77 85 76 84 73 67 65 83 84 62 32 32 109 116 117 32 49 53 48 48 13 10 32 32 32 32 32 32 32 32 105 110 101 116 32 57 46 49 51 52 46 49 50 48 46 50 52 53 32 32 110 101 116 109 97 115 107 32 50 53 53 46 50 53 53 46 50 52 48 46 48 32 32 98 114 111 97 100 99 97 115 116 32 57 46 49 51 52 46 49 50 55 46 50 53 53 13 10 32 32 32 32 32 32 32 32 101 116 104 101 114 32 53 50 58 53 52 58 48 48 58 56 102 58 52 55 58 56 101 32 32 116 120 113 117 101 117 101 108 101 110 32 49 48 48 48 32 32 40 69 116 104 101 114 110 101 116 41 13 10 32 32 32 32 32 32 32 32 82 88 32 112 97 99 107 101 116 115 32 52 54 54 56 51 48 53 54 57 55 32 32 98 121 116 101 115 32 54 50 55 52 52 52 52 50 57 55 55 53 52 32 40 53 46 55 32 84 105 66 41 13 10 32 32 32 32 32 32 32 32 82 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 32 111 118 101 114 114 117 110 115 32 48 32 32 102 114 97 109 101 32 48 13 10 32 32 32 32 32 32 32 32 84 88 32 112 97 99 107 101 116 115 32 49 52 56 48 55 50 49 57 50 56 32 32 98 121 116 101 115 32 49 52 50 55 53 56 50 55 52 55 51 48 32 40 49 51 50 46 57 32 71 105 66 41]
2022/02/22 17:56:17 eth1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 9.134.120.245  netmask 255.255.240.0  broadcast 9.134.127.255
        ether 52:54:00:8f:47:8e  txqueuelen 1000  (Ethernet)
        RX packets 4668305697  bytes 6274444297754 (5.7 TiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1480721928  bytes 142758274730 (132.9 GiB)
2022/02/22 17:56:17 [13 10 32 32 32 32 32 32 32 32 84 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 111 118 101 114 114 117 110 115 32 48 32 32 99 97 114 114 105 101 114 32 48 32 32 99 111 108 108 105 115 105 111 110 115 32 48 13 10 13 10 108 111 58 32 102 108 97 103 115 61 55 51 60 85 80 44 76 79 79 80 66 65 67 75 44 82 85 78 78 73 78 71 62 32 32 109 116 117 32 54 53 53 51 54 13 10 32 32 32 32 32 32 32 32 105 110 101 116 32 49 50 55 46 48 46 48 46 49 32 32 110 101 116 109 97 115 107 32 50 53 53 46 48 46 48 46 48 13 10]
2022/02/22 17:56:17 
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0

2022/02/22 17:56:17 [32 32 32 32 32 32 32 32 108 111 111 112 32 32 116 120 113 117 101 117 101 108 101 110 32 48 32 32 40 76 111 99 97 108 32 76 111 111 112 98 97 99 107 41 13 10 32 32 32 32 32 32 32 32 82 88 32 112 97 99 107 101 116 115 32 57 55 48 57 55 50 56 52 32 32 98 121 116 101 115 32 49 49 56 54 48 51 56 52 49 57 57 32 40 49 49 46 48 32 71 105 66 41 13 10 32 32 32 32 32 32 32 32 82 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 32 111 118 101 114 114 117 110 115 32 48 32 32 102 114 97 109 101 32 48 13 10 32 32 32 32 32 32 32 32 84 88 32 112 97 99 107 101 116 115 32 57 55 48 57 55 50 56 52 32 32 98 121 116 101 115 32 49 49 56 54 48 51 56 52 49 57 57 32 40 49 49 46 48 32 71 105 66 41 13 10 32 32 32 32 32 32 32 32 84 88 32 101 114 114 111 114 115 32 48 32 32 100 114 111 112 112 101 100 32 48 32 111 118 101 114 114 117 110 115 32 48 32 32 99 97 114 114 105 101 114 32 48 32 32 99 111 108 108 105 115 105 111 110 115 32 48 13 10 13 10]
2022/02/22 17:56:17         loop  txqueuelen 0  (Local Loopback)
        RX packets 97097284  bytes 11860384199 (11.0 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 97097284  bytes 11860384199 (11.0 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


2022/02/22 17:56:17 [27 93 48 59 117 115 101 114 48 49 64 57 46 49 51 52 46 49 50 48 46 50 52 53 7 91 117 115 101 114 48 49 64 86 77 95 49 50 48 95 50 52 53 95 99 101 110 116 111 115 32 126 93 36 32]
2022/02/22 17:56:17 ]0;user01@9.134.120.245[user01@VM_120_245_centos ~]$ 
2022/02/22 17:56:19 [101]
2022/02/22 17:56:19 e
2022/02/22 17:56:19 [120]
2022/02/22 17:56:19 x
2022/02/22 17:56:19 [105]
2022/02/22 17:56:19 i
2022/02/22 17:56:19 [116]
2022/02/22 17:56:19 t
2022/02/22 17:56:20 [13 10 108 111 103 111 117 116 13 10]
2022/02/22 17:56:20 
logout

```


####  输入

输入序列：
```bash
[root@VM_120_245_centos ~]# go run sshclient.go 
Last login: Tue Feb 22 17:40:39 2022 from 127.0.0.1
[user01@VM_120_245_centos ~]$ [105 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                        i[102 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                                                                   f[99 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                    c[111 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                               o[9 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                               nfig [101 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                              e[116 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                                                                        t[104 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                          h[49 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                                    1[23 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                 [13 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]

docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 192.168.10.1  netmask 255.255.255.0  broadcast 192.168.10.255
        ether 02:42:9b:b0:aa:d8  txqueuelen 0  (Ethernet)
        RX packets 1132002974  bytes 60004432919 (55.8 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4308392302  bytes 6202545587319 (5.6 TiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

eth1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 9.134.120.245  netmask 255.255.240.0  broadcast 9.134.127.255
        ether 52:54:00:8f:47:8e  txqueuelen 1000  (Ethernet)
        RX packets 4668305697  bytes 6274444297754 (5.7 TiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1480721928  bytes 142758274730 (132.9 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        loop  txqueuelen 0  (Local Loopback)
        RX packets 97097284  bytes 11860384199 (11.0 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 97097284  bytes 11860384199 (11.0 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[user01@VM_120_245_centos ~]$ [101 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                        e[120 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                                                                   x[105 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                     i[116 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]
                                                                                                                                                t[13 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0]

logout
the connection was closed on the remote side on  22 Feb 22 17:56 CST
```

####  分析

键盘的控制键，输入和输出是不一样的，比如`CTRL+A`，输入字符对应的ascii为`[1]`，而在屏显buffer打印的结果是`[8 8 8 8 8 8 8 8 8]`；又如`CTRL+W`，输入对应的字符为`[23]`，屏显结果是：`[8 8 8 8 27 91 75]`