# 通过kubectl或web-terminal插件连接CCE集群<a name="cce_01_0107"></a>

本文将以混合集群为例，介绍如何通过kubectl或web-terminal插件连接CCE集群。

## 通过web-terminal插件连接集群<a name="section6597175818153"></a>

**请安装和设置web-terminal。**

有关详细信息，请参见[web-terminal](web-terminal.md)安装和配置插件，安装完成后单击左侧导航栏的“插件管理“，在“插件实例”中，单击“web-terminal”名称进入插件详情页，单击“访问地址”后的链接即可登录。

## 通过kubectl连接集群<a name="section37321625113110"></a>

**背景信息**

若您需要从客户端计算机连接到kubernetes集群，请使用kubernetes命令行客户端[kubectl](https://kubernetes.io/docs/user-guide/kubectl/)。

**准备工作**

CCE支持“VPC网络内访问“和“互联网访问“两种方式访问集群。

-   VPC网络内访问：您需要在[ECS控制台](https://console.huaweicloud.com/ecm/?locale=zh-cn#/ecs/manager/vmList)购买一台云服务器，并确保和当前集群在同个VPC内。
-   互联网访问：您需要准备一台能连接公网的云服务器。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>通过“互联网访问”方式访问集群，集群的kube-apiserver将会暴露到互联网，存在被攻击的风险，建议对kube-apiserver所在节点的EIP配置DDoS高防服务。

**操作步骤**

1.  登录[CCE控制台](https://console.huaweicloud.com/cce2.0/?utm_source=helpcenter)，在左侧导航栏中选择“资源管理 \> 集群管理”，单击待连接集群下的“命令行工具 \>  kubectl”。

    **图 1**  单击kubectl<a name="fig118327236614"></a>  
    ![](figures/单击kubectl.png "单击kubectl")

2.  在集群详情页中的“kubectl“页签下，请参照界面中的提示信息完成集群连接。

    **图 2**  通过kubectl连接集群<a name="fig1366811551535"></a>  
    ![](figures/通过kubectl连接集群.png "通过kubectl连接集群")

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   您可以在“kubectl“页签下方便的**下载kubectl配置文件**（kubeconfig.json），CCE支持华为云账号和IAM用户分别下载该配置文件，IAM用户下载的配置文件只有30天的有效期，而华为云账号下载的配置文件会长期有效。
    >-   IAM用户下载的配置文件所拥有的Kubernetes权限与CCE控制台上IAM用户所拥有的权限一致。


## 相关操作<a name="section422912118536"></a>

连接集群后，您可以使用Kubernetes管理工作负载，具体请参见[Kubectl使用指南](Kubectl使用指南.md)。

