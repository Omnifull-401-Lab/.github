# Contributing to Omnifull-401-Lab Repositories

欢迎向 **Omnifull-401-Lab** 组织下的仓库提交代码、硬件资料或文档！  
本文件是全组织通用的默认贡献规范；若某个具体项目仓库内另有专属 `CONTRIBUTING.md`，以该仓库为准。

---

## 1. Onboarding Handbook / 入队必读知识库

首次参与协作前，请先查阅我们的内部统一知识库 **[Omnifull-401-Lab/team-handbook](https://github.com/Omnifull-401-Lab/team-handbook)** *（私有仓库，需登录组织成员账号后访问）*：

1. [01｜GitHub Basics & Web Guide](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/onboarding/01-github-guide.md)
2. [02｜GitHub Desktop Guide](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/onboarding/02-github-desktop-guide.md)
3. [03｜Standard Workflow & Branching](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/onboarding/03-workflow-github-desktop.md)
4. [04｜Team Engineering Conventions](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/onboarding/04-team-conventions.md)
5. [05｜Troubleshooting & FAQ](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/onboarding/05-faq.md)

---

## 2. Standard Workflow (GitHub Flow) / 标准协作流程

1. **同步 `main`**：在 GitHub Desktop 切回 `main`，执行 `Fetch origin` / `Pull origin` 拉取最新进度。
2. **新建短期分支**：格式为 `<类型>/<简短英文描述>`（全小写英文、数字、`-`，无空格与中文），如 `feat/`、`fix/`、`docs/`、`hw/`、`refactor/`、`chore/`。
3. **本地提交并推送**：核对 `Changes` 无临时杂项文件后，填写清晰 `Summary`（如 `feat: ...`、`fix: ...`、`hw: ...`、`docs: ...`）执行 `Commit`，然后点击 `Publish branch` / `Push origin`。
4. **发起 Pull Request（PR）**：确认合并方向为 `base: main` ← `compare: <你的分支>`，按自动弹出的 PR 模板填好改动说明与测试截图（关联 Issue 可写 `Closes #编号`）。
5. **合并收尾**：合并后点击 `Delete branch` 删除短期分支，回到 GitHub Desktop 切回 `main` 并 `Pull origin`。

---

## 3. Review & Merge Policy / 审核与合并权限

- **普通成员的 PR**：发起后请在右侧 **`Reviewers`** 指定管理员或模块负责人（或发群提醒），**必须等待审核人检查 `Files changed` 并点击 `Approve` 后再合并**。
- **管理员的 PR**：自行复核 `Files changed` 无误且无冲突后，**无需等待他人审核即可直接合并**。

---

## 4. Hardware & Binary Files Rule / 硬件与工程文件协作规矩

修改原理图、PCB（立创 EDA / Altium / Cadence）、Keil `.uvprojx`、STM32CubeMX `.ioc`、Word/PPT 等难以按行自动合并的文件前：
1. **改前先在团队群或对应 Issue 报备占用时段**；
2. **看到队友占用时先错开**，等对方合并后 `Pull origin` 再接力；
3. **阶段性改完尽早提 PR 合并**，不要长期囤在本地。

---

## 5. Pre-PR Checklist / 提 PR 前 30 秒自查

- [ ] 当前处于短期分支，没有直接修改 `main`
- [ ] 文件与目录全路径均为纯英文无空格，无 `最终版` / `final` 类堆叠文件名
- [ ] 已复用团队通用 [`.gitignore`](https://github.com/Omnifull-401-Lab/team-handbook/blob/main/.gitignore)，未提交编译产物、`.lck` 临时文件或 >50 MB 大文件
- [ ] 已确认不含明文 Wi-Fi 密码、API Key、私钥或个人隐私数据
- [ ] 如涉及引脚、协议或硬件变更，已同步更新文档并在 PR 中附上验证说明或截图
