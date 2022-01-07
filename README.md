# AWS Security Hub安全合规中心使用教程和效果展示



AWS的安全流程为（如下图）：Identify –> Protect –> Detect –> Respond –> Recover，Security Hub采用集成的方式自动化了整个流程。

![image-20220107111829180](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107111829180.png)

Security Hub介绍如下：



##  一、简介

Security Hub overview：

![image-20220107101215283](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107101215283.png)



工作原理：

![image-20220107111755648](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107111755648.png)



Security Hub 帮助您：

- [ ] 了解并管理您的总体AWS安全和合规态势
- [ ] 根据法规和最佳实践框架评估您的法规遵从性
- [ ] 从一个区域内的多个帐户收集和处理安全调查结果
- [ ] 通过将安全调查结果与见解进行分组和关联，确定最重要的问题并确定其优先级

入口地址 Try IT: https://console.aws.amazon.com/securityhub/

更多内容 Learn more: https://aws.amazon.com/security-hub/ 



## 二、安全合规标准

Security Hub 目前支持多种安全标准：

- **互联网安全中心 (CIS) AWS Foundations v1.2.0：**

  > AWS Security Hub 已满足 CIS 安全软件认证的要求，特此授予以下 CIS 基准的 CIS 安全软件认证：CIS Benchmark for CIS Amazon Web Services Foundations Benchmark, v1.2.0, Level 1 and Level 2

- **AWS 基础安全最佳实践 v1.0.0：**

  > AWS 基础安全最佳实践标准是一组控制措施，用于检测您部署的账户和资源何时偏离安全最佳实践。这些控制措施包括来自多个 AWS 服务的最佳实践。每个控件都属于以下类别之一，这些类别基于 NIST 网络安全框架中描述的功能。

- **支付卡行业数据安全标准 (PCI DSS) v3.2.1：**

  > Security Hub 中的支付卡行业数据安全标准 (PCI DSS) 标准包含一组 AWS 安全最佳实践控制。每个控件都适用于特定的 AWS 资源，并与一个或多个 PCI DSS 3.2.1 版要求相关。PCI DSS 要求可能与多个控制相关。每个 PCI DSS 控件的详细信息页面列出了与该控件相关的特定 PCI DSS 要求。Security Hub 中的 PCI DSS 合规性标准旨在帮助您进行持续的 PCI DSS 安全活动。这些控件无法验证您的系统是否符合 PCI DSS 标准。它们既不能取代内部工作，也不能保证您将通过 PCI DSS 评估。

有关这些安全标准的更多信息，请访问：[AWS Security Hub 中的可用安全标准](https://docs.aws.amazon.com/securityhub/latest/userguide/standards-available.html)



## 三、安全标准（3个）展开介绍：

**1、互联网安全中心 (CIS) AWS Foundations v1.2.0：**

- Center for Internet Security组织官网：https://www.cisecurity.org/benchmark/amazon_web_services/
- PDF内容细节《CIS Amavon Web Services Foundations》： https://d0.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf
- AWS文档（stepbystep）合规操作方法： https://docs.aws.amazon.com/zh_cn/securityhub/latest/userguide/securityhub-cis-controls.html
![image-20220107110312348](../../../../yiming/Library/Application%20Support/typora-user-images/image-20220107110312348.png)
- 内容分为四个部分：1 Identity and Access Management, 2 Logging, 3 Monitoring, 4 Networking
- Securty Hub自动化扫描结果：![image-20220107103127290](../../../../yiming/Library/Application%20Support/typora-user-images/image-20220107103127290.png)





**2、AWS 基础安全最佳实践 v1.0.0：**

- 标准内容细节： https://docs.aws.amazon.com/zh_cn/securityhub/latest/userguide/control-categories.html

- AWS文档（stepbystep）合规操作方法： https://docs.aws.amazon.com/zh_cn/securityhub/latest/userguide/securityhub-standards-fsbp-controls.html

  ![image-20220107110223176](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107110223176.png)

- 内容分为5个部分：Identify/Protect/Detect/Respond/Recover

- Securty Hub自动化扫描结果：


![image-20220107103225856](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107103225856.png)



**3、支付卡行业数据安全标准 (PCI DSS) v3.2.1：**

- AWS文档（stepbystep）合规操作方法： https://docs.aws.amazon.com/zh_cn/securityhub/latest/userguide/securityhub-pci-controls.html
![image-20220107110448879](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107110448879.png)

- Securty Hub自动化扫描结果：

  ![image-20220107110752975](../../../../yiming/Library/Application%20Support/typora-user-images/image-20220107110752975.png)



## 四、计费方式：

![image-20220107124436638](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107124436638.png)

![image-20220107124549801](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107124549801.png)

费用详情看这里：https://aws.amazon.com/cn/security-hub/pricing/



## 五、Security Hub使用教程和实际效果

1. 摘要
2. 集成
3. 洞察力
4. 检测结果
5. 安全标准
6. 使用总结

#### （1）摘要

Security Hub 摘要页面为您提供 AWS 账户的安全性和合规性状态概览。

操作方法：

1. 从AWS控制台点击服务在左上角

2. 在服务搜索栏中键入Security Hub。

3. 从列表中选择安全中心。

4. 单击左侧导航中的**摘要**。

   ![image-20220107125033859](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107125033859.png)

5. 观察**CIS AWS Foundations**的 Passed 和 Failed 状态。即使您在几分钟前才启用它，但已经收集了此安全标准的部分结果。

   

#### （2）集成

启用合作伙伴集成的 Security Hub 方面。Security Hub 能够集成来自 AWS 服务和第三方产品的安全发现。对于 AWS 服务，Security Hub 会自动启用集成，您可以选择禁用每个集成。对于第三方产品，Security Hub 使您能够有选择地启用集成，并提供指向与第三方产品相关的配置说明的链接。

Security Hub 仅检测并整合在您的 AWS 账户中启用 Security Hub 后生成的受支持 AWS 和合作伙伴产品集成中的那些安全发现。它不会追溯检测和整合在您启用 Security Hub 之前生成的安全结果。

1. 单击左侧导航窗格中的**集成**。

   ![image-20220107125334800](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107125334800.png)

2. 滚动可用集成列表。请注意，AWS 服务的集成会自动启用。返回顶部和**搜索**的**云托管**。

   ![image-20220107125416744](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107125416744.png)

3. 单击**接受结果**。查看集成所需的权限。

4. 单击**接受结果**。

   这将实施一项服务策略，允许合作伙伴解决方案将查找信息发送到此帐户。

   

#### （3）检测结果

Security Hub 导入调查结果 AWS 安全服务、您启用的第三方产品集成以及您构建的自定义集成。Security Hub 使用称为 AWS 安全调查格式 (ASFF) 的标准调查结果格式来使用这些调查结果，从而无需进行耗时的数据转换工作。然后，Security Hub 将跨集成产品的发现关联起来，以确定最重要的产品的优先级。有关调查结果格式的更多信息，请参阅[AWS 安全调查结果格式](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-findings-format.html)。

1. 点击**检测结果**从左侧导航窗格中。

   ![image-20220107125719526](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107125719526.png)

2. 在其默认视图中，“发现”选项卡可以包含大量信息供您使用。要缩小整个结果列表，请输入一些搜索条件。单击搜索栏的 ，选择**Severity label**过滤字段，过滤匹配类型**is**和搜索值**MEDIUM**（搜索值必须全部大写）。单击**应用**。

3. 选择任何结果的**标题**以在结果详细信息窗格中查看更多信息。

4. 在结果详细信息窗格中，单击右下角**资源**旁边的箭头。

5. 单击此调查结果**资源类型**（例如 AWSEc2Instance）右侧的 [+] 。这会将资源作为过滤器添加到搜索中。

6. 在结果详细信息窗格中，选择窗格顶部的结果 ID 以显示结果的完整 JSON。如果需要进一步投资，可以将结果 JSON 下载到文件中。



#### （4）洞察力（见解）

Security Hub Insight 是由聚合语句和可选过滤器定义的相关结果的集合。洞察力确定需要关注和干预的安全领域。Security Hub 提供了多个您无法修改或删除的托管（默认）见解。您还可以创建自定义见解来跟踪您的 AWS 环境和使用情况特有的安全问题。

1. 单击左侧导航窗格中的**见解**。

   ![image-20220107125926994](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107125926994.png)

2. 过滤洞察**严重性**。

   单击**24. 按结果计数的严重性**。

   过滤器中的**Group By: Resource Id**使其成为洞察力。选择一个**严重性标签**（例如严重）以查看基础发现。




#### （5）安全标准

Security Hub 目前支持多种安全标准：

- 互联网安全中心 (CIS) AWS Foundations v1.2.0：

- AWS 基础安全最佳实践 v1.0.0：

- 支付卡行业数据安全标准 (PCI DSS) v3.2.1：

  

有关这些安全标准的更多信息，请访问：[AWS Security Hub 中的可用安全标准](https://docs.aws.amazon.com/securityhub/latest/userguide/standards-available.html)

为了对您的环境资源运行 CIS AWS Foundations 标准的合规性检查，Security Hub 要么运行为[确保 Amazon Web Services 安全中](https://www.cisecurity.org/benchmark/amazon_web_services/)的检查规定的确切审计步骤，要么使用特定的 AWS Config 托管规则。要使用 AWS Config 托管规则，必须在您使用 Security Hub 的账户中启用 AWS Config。对于本次研讨会，配置已为您启用。

第一轮合规性检查将在启用 Security Hub 后的 2 小时内完成，然后每 12 小时运行一次。

1. 单击**安全标准**。

   ![image-20220107130139534](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107130139534.png)

   请注意，从您第一次启用 CIS 标准时起，安全分数应该已经发生了变化。如果您的分数显示为 0% 或 -，请禁用然后重新启用安全标准。

2. 单击查看 “AWS 基础安全最佳实践 v1.0.0” 的结果。

   ![image-20220107130454200](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107130454200.png)

3. 单击标题：**“安全组不应允许对高风险端口的无限制访问权限”**。这提供了针对此特定控制评估的所有资源的视图，以及每个资源与控制相关的当前状态。

   ![image-20220107130552061](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107130552061.png)

   在页面顶部单击**修复说明链接**，以在新选项卡中打开指南。 AWS Security Hub 安全标准为每项检查提供了补救说明。

6. 向下滚动，您会注意到有些资源的状态为**FAILED，**而有些资源的状态为**PASSED**。对于**失败的**资源之一，单击**调查**列中的三个点。这将显示将您带到 AWS Config 以查看此资源的配置时间表或对该资源执行评估的整体配置规则的链接。随意单击链接以探索有关资源和配置规则的更多信息。

![image-20220107130914686](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107130914686.png)

#### （6）总结

Security Hub 提供您的 AWS 账户的使用信息，帮助您了解您的每月账单估算值以及 Security Hub 的哪些组件会影响您的账单。Security Hub 为每个帐户提供 30 天的免费试用。在免费试用期间，Security Hub 提供对支出的估计，以便您可以评估免费试用后的支出。

1. 单击左侧导航中的**设置**。

2. 单击**设置**屏幕中的**使用**选项卡。

3. 屏幕左侧会显示您在计费周期内的使用情况。使用情况按摄取的结果和已运行的安全检查进行细分。使用情况摘要的底部是计费周期的总估计成本。右侧是当前的 Security Hub 定价，以便您可以查看帐户中的使用情况对估计成本的贡献。

   ![image-20220107131041100](https://raw.githubusercontent.com/liangyimingcom/storage/master/PicGo/image-20220107131041100.png)

现在您已经了解了 Security Hub 的功能。





## 六、不足之处

- Security Hub与AWS Console深度集成，这给安全合规修正操作带来了便利性，但是没有找到导出为图文并茂PDF报告的方法；
- 目前只能采用部分数据导出与截图的方式完成 “图文并茂PDF报告”。





## 七、附录和引用

1、AWS Security Hub Workshop动手实验 “集成、优先级排序和响应” http://security-hub-workshop.awssecworkshops.com/
















