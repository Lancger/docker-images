常用docker容器镜像构建，kubernetes配置文件，helm模板,用于搭建基于容器的可控云计算基础设施,包括物理机裸机，虚拟机，多厂商云主机，有效规避云计算厂商锁定
kubernetes网络方案推荐使用cilium,支持vxlan,bgp以及eBPF引擎
容器内核参数已经为高并发大吞吐量低延迟场景优化，完美运行需要kubernetes版本>=v1.11和内核版本>=4.15，低版本kubernetes和内核需要删除sysctl相关配置，这样做会失去单实例高并发能力。
宿主机系统推荐使用ubuntu或者debian并且启用apparmor enforce模式，有效对抗容器逃脱。有能力的可以部署grsecurity内核进一步增强安全,全面对抗0day漏洞。
支持在kubernetes集群里面运行Linux桌面环境(暂无3D加速)

代码仓库: gitlab-ce,gogs
代码审核: gerrit
持续集成/发布: jenkins,spinnaker,gitlab-ci,drone
测试: chaos-monkey,chaoskube,k8s-testsuite,test-infra,sonobuoy,PowerfulSeal,
artifactory仓库: nexus2,nexus3,harbor,registry
helm应用商店: chartmuseum,kubeapps
分布式存储: ceph,minio
大数据集群: hadoop(hdfs+yarn),hbase,spark,flink
web服务器/容器: nginx-php,apache-php,tomcat,resin
SQL数据库: mysql,percona,mariadb,postgresql
NoSQL数据库/缓存/存储: memcache,rethinkdb,redis,ssdb,mongodb,cassandra
NewSQL数据库: TiDB,cockroachdb
时间序列数据库: influxdb,opentsdb,m3db
消息队列/流存储: rabbitmq,rocketmq,rocketmq-console-ng,kafka,kafka-manager
配置管理: zookeeper,zkui,qconf,etcd
定时任务管理: xxl-job
项目管理: jira,zentao
企业ERP: odoo
开发环境SDK: golang,golang-gvm,oracle-jdk,oracle-jdk-maven
微服务管理与持续发布: fabric8,jenkins-x,draft,knative
微服务框架/组件: istio,dubbo,dubbokeeper,kong,kong-dashboard,consul,openlambda
FAAS: fission,fnproject,funktion,kubeless,nuclio,open-lambda,openfaas,openwhisk,vmware-dispatch
日志集群: elastic-stack(elasticsearch+cerebro+kibana)
日志采集: logstash,filebeat,logtail
监控/APM: appdash,apm-server,cadvisor,heapster,kube-state-metrics,metrics-server,prometheus,pinpoint,jaeger,zipkin,skywalking,kubewatch,searchlight,
动态性能追踪: bcc-tools,systemtap,sysdig
kubernetes可视化管理工具: kubernetes-dashboard,weavescope,kubebox,kubedash,kube-ops-view,cabin
kubernetes灾难恢复: ark
开发工具: Telepresence,Keel,Apollo,Deis Workflow,Kel,
安全工具: anchore,clair,cert-manager,magic-namespace,notary,OpenSCAP,trireme,NeuVector,Deepfence,StackRox,Tenable,Cavirin,Kube-Bench,Sysdig Falco,Sysdig Secure,Kubesec.io;付费 Aquasec,flawcheck
编排转换：kompose

云原生（CloudNative）应用
分布式存储: rook-ceph,rook-minio,openebs
虚拟化: kubevirt
监控: prometheus-operator,jaeger-operator
配置管理: etcd-operator

桌面环境
ubuntu-xfce-vnc
ubuntu-icewm-vnc
centos-xfce-vnc
centos-icewm-vnc
