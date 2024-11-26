# 在 GitHub 上创建一个**多人项目**

需要经过以下步骤，从仓库创建到团队协作管理，以下是详细指导：

------

## 1. **创建一个仓库**

1. **登录 GitHub**： 使用你的 GitHub 账号登录 [GitHub](https://github.com/)。

2. **创建新仓库**： 点击右上角的 `+` 图标，选择 **New repository**。

3. 填写仓库信息

   ：

   - **Repository name**：填写仓库名称，例如 `gmall-project`。

   - **Description**：添加描述，比如 “A comprehensive e-commerce platform system for GMALL”。

   - Visibility

     ：

     - 选择 **Public**（公开） 或 **Private**（私有）。
     - 如果希望限制只有团队成员能访问，选择 **Private**。

   - 勾选 **Initialize this repository with a README**（推荐添加）。

4. **点击 Create repository**： 仓库创建完成！

------

## 2. **邀请协作者**

GitHub 提供两种方式来添加团队成员：**直接添加协作者** 或 **通过组织管理权限**。

### 直接添加协作者

1. 打开仓库页面，点击右上角的 **Settings**。
2. 左侧菜单中找到 **Collaborators and teams**。
3. 点击 **Add people**，输入协作者的 GitHub 用户名或邮箱。
4. 为协作者分配权限：
   - **Read**：只能查看代码。
   - **Triage**：可以管理 issue 和 pull request。
   - **Write**：可以推送代码和创建分支。
   - **Maintain**：管理仓库的基本设置。
   - **Admin**：完全控制仓库。
5. 点击 **Invite**，对方需要接受邀请。

------

### 使用 GitHub 组织

如果项目是团队项目，建议创建一个 **GitHub 组织**：

1. 创建组织

   ：

   - 点击右上角头像菜单，选择 **Your organizations**。
   - 点击 **New organization**，按照提示完成组织创建。

2. 创建团队

   ：

   - 在组织页面，点击 **Teams**，创建一个团队（如 `Developers`）。

3. 添加成员到团队

   ：

   - 添加团队成员到组织，并为团队分配具体仓库权限。

4. 将仓库移到组织

   ：

   - 在仓库的 **Settings -> General** 页面，选择 **Transfer ownership**，将仓库转移到组织。

------

## 3. **代码协作工作流**

多人项目通常使用 **Git 分支** 和 **Pull Request 工作流** 来协作。

### 代码协作的基本流程

1. **克隆仓库**： 每个协作者先通过 Git 将仓库克隆到本地：

   ```bash
   git clone https://github.com/your-username/gmall-project.git
   ```

2. **创建分支**： 每个人开发时建议创建独立分支：

   ```bash
   git checkout -b feature/branch-name
   ```

   例如，`feature/user-auth`、`fix/bug-101`。

3. **提交和推送**： 在分支中完成代码修改后，提交并推送：

   ```bash
   git add .
   git commit -m "Add user authentication feature"
   git push origin feature/branch-name
   ```

4. **创建 Pull Request (PR)**：

   - 在 GitHub 上点击 **Pull Requests**，然后点击 **New pull request**。
   - 对分支进行比较并创建 PR，描述更改内容。
   - 其他成员可以查看、评论和合并。

------

## 4. **管理问题和任务**

通过 GitHub 的 **Issue** 和 **Project** 功能，可以更好地管理任务和问题。

### 使用 Issue 管理问题

1. 创建 Issue

   ：

   - 打开仓库，点击 **Issues -> New Issue**。
   - 填写问题标题和描述（如 Bug 或 Feature 请求）。

2. 分配问题

   ：

   - 给特定成员分配任务。
   - 设置标签（如 `bug`、`enhancement`、`help wanted`）。

3. 跟踪进度

   ：

   - 使用评论讨论问题。
   - 在 Pull Request 中引用 Issue（如 `Fixes #101`），会自动关闭问题。

### 使用 Project 管理任务

1. 创建一个 Project

   ：

   - 在仓库中点击 **Projects**，选择 **Create a project**。
   - 使用 Kanban 模板管理任务（如待办、进行中、已完成）。

2. 添加任务到 Project

   ：

   - 将 Issue 或 Pull Request 直接添加到 Project 的看板中。

------

## 5. **设置工作流自动化（可选）**

使用 GitHub Actions 自动化流程，例如自动构建或测试。

### 配置 CI/CD

1. 启用 Actions

   ：

   - 在仓库中点击 **Actions**，选择模板（如 Node.js、Java Maven）。

2. 编写 Workflow 文件

   ： 在 

   ```
   .github/workflows
   ```

    中创建 YAML 文件定义工作流。 示例：

   ```yaml
   name: Build and Test
   
   on: [push, pull_request]
   
   jobs:
     build:
       runs-on: ubuntu-latest
   
       steps:
         - uses: actions/checkout@v2
         - name: Set up Node.js
           uses: actions/setup-node@v3
           with:
             node-version: '16'
         - run: npm install
         - run: npm test
   ```

------

## 6. **定期维护**

1. 代码审核

   ：

   - 确保每个 PR 都经过审核后再合并。
   - 制定代码贡献规范（如文件结构、注释格式）。

2. 文档更新

   ：

   - 在仓库中维护 `README.md`，清晰描述项目背景和使用方法。

3. 成员权限管理

   ：

   - 根据项目需求，及时调整成员权限。

------

