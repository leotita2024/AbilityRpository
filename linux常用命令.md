# 解压日志
for i in $(ls |grep  base-config-service-2022-03-20|grep  gz); do gzip -d $i ;done;

# 压缩日志
for i in $(ls |grep  base-config-service-2022-03-20|grep -v  gz); do gzip  $i ;done;

# 运维强行删除任务

3.2.5之前 curl - 







