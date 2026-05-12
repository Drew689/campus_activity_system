# 04 配置管理文档

## 1. 配置项范围
README.md：项目整体说明、团队分工、目录结构、分支策略与协作规范
docs/01-project-charter.md：项目启动说明文档
docs/02-wbs.md：三级 WBS 分解成果文档
docs/03-schedule.md：简化进度计划文档
docs/04-config-plan.md：本配置管理方案文档
docs/05-summary-report.md：实验总结报告
docs/conflict.md：冲突处理示例文件
src/：示例代码或资源文件目录

## 2. 分支策略
- main
- dev
- feature-libai
- feature-zhangtan
- feature-hedequan

## 3. 命名约定
3.1 文档命名约定
格式：0X-功能说明.md
示例：
01-project-charter.md
02-wbs.md
03-schedule.md
04-config-plan.md
05-summary-report.md
3.2 分支命名约定
格式：feature-任务名
说明：分支名小写，使用连字符分隔，清晰对应任务
3.3 提交说明约定
格式：类型: 简要说明
类型说明：
init：初始化仓库 / 目录结构
feat：新增文档 / 功能
docs：修改说明类文档
fix：修复错误或冲突
merge：合并分支
示例：
feat: 完成三级WBS分解文档
docs: 更新进度计划责任人信息
fix: 解决conflict.md文件冲突
merge: 合并feature-config到dev

## 4. 合并规则
4.1 合并权限与责任人
feature-* → dev：由配置管理员审核后合并
dev → main：由全体成员确认所有内容完成、无错误后合并
4.2 合并时机
feature-* → dev：单个任务完成、文档确认无误后立即合并
dev → main：所有实验任务全部完成、冲突处理完毕，一次性合并
4.3 冲突处理流程
当合并时出现冲突，由涉及该文件的两位协作成员共同协商解决
冲突解决后，需在文件中保留解决痕迹
解决完成后，提交一个标记为 fix 的提交，再继续合并流程
禁止使用强制推送、强制覆盖等方式绕过冲突解决

## 5. 版本留痕
阶段性提交：每个任务完成后，必须提交一次完整记录，提交信息需清晰说明完成内容
分支历史保留：不删除已完成的 feature-* 分支，保留完整开发过程
版本标记：最终合并到 main 后，打一个版本标签 v1.0，标记为最终交付版本
关键提交记录：在总结报告中列出关键提交的哈希值与说明，便于追溯
