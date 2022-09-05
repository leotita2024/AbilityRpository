#官方文档
https://arthas.aliyun.com/doc/quick-start.html

#下载
wget -O arthas.zip https://arthas.aliyun.com/download/latest_version?mirror=aliyun

#解压
unzip -d arthas arthas.zip

#动态trace\watch\tt\monitor

1. telnet localhost 3658
2. trace demo.MathGame primeFactors --listenerId 1