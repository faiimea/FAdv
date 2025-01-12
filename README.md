# 深度学习模型安全评估平台

本项目为上海交通大学“大学生创新实践计划”中“深度学习模型安全评估技术研究”项目的仓库，实现了对模型进行安全性评测的功能。

## 使用方式

在`EvaluationConfig.py`文件内加载模型并调整参数，随后运行`EvaluationPlatformNEW.py`执行测试。

## 结果说明

评测结果含十个指标，意义如下：

| 指标名                       | 领域       | 说明                                         |
| ---------------------------- | ---------- | -------------------------------------------- |
| CACC                         | 通用       | 原始模型正常任务准确率                       |
| ACC                          | 对抗鲁棒性 | 在固定扰动下执行对抗样本攻击后模型任务准确率 |
| NoisyACC                     | 对抗鲁棒性 | 叠加高斯噪声后模型任务准确率                 |
| BlurredACC                   | 对抗鲁棒性 | 施加高斯模糊后模型任务准确率                 |
| CompressedACC                | 对抗鲁棒性 | 图像压缩后模型任务准确率                     |
| trigger_std                  | 后门鲁棒性 | 检测到的后门触发器的异常系数                 |
| trigger_size                 | 后门鲁棒性 | 检测到的后门触发器的大小                     |
| PoisonSR                     | 投毒鲁棒性 | 投毒成功率                                   |
| After_Datapoison_Defense_ACC | 投毒鲁棒性 | 投毒防御后正常任务准确率                     |
| afterPoisonACC               | 投毒鲁棒性 | 被投毒攻击后模型正常任务准确率               |



