# E7 B-draft

在本目录执行 scripts/lab_cloud.py。按实验包根目录 docs/ 中的本轨道指南运行 build、gate，然后完成 CI。

services/ 为实现和服务测试，fixtures/ 为输入，scripts/ 为门禁和入口，.github/workflows/ 为 CI，work/ 为本次结果。

## 本组实现

- 轨道：B10 / DRAFT。
- `auto-build` 对候选 Dockerfile 做 digest、基础镜像、单阶段及原有指令完整性校验。
- 门禁执行正常、输出不符、无效候选、候选构建失败和运行超时五个真实工作流场景。
- 新增测试要求含第二条 `FROM` 的候选必须在构建前拒绝。
