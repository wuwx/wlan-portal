大致的思路如下：
1. 用户全部终结到linux上，由linux做dns/dhcp/转发（可以NAT，也可以不NAT，我们有足够的公网IP，不打算NAT)
2. 利用ipset 做用户IP和mac的检查，符合的直接通过，不符合的利用NFQUEUE重定向到登录页面
3. 重定向程序redir_url是CERNET2014投的文章
4. 为了简化用户使用，用mac作为重要识别号，用户第一次登陆时记录mac和手机号，以后一段时间就能直接用


