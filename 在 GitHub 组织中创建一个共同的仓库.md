# 在 GitHub 组织中创建一个共同的仓库

------

### 1. **登录并进入组织页面**

1. 使用你的 GitHub 账号登录 [GitHub](https://github.com/)。
2. 点击右上角 **头像**，选择 **Your organizations**。
3. 选择你创建的组织，例如 `gmall-team`。

------

### 2. **创建一个新仓库**

1. 在组织页面，点击右侧的 **New repository** 按钮。

2. 填写仓库信息：

   - **Repository name**：输入仓库名称，例如 `gmall-project`。

   - **Description**：填写仓库的描述信息（可选），例如 *"A collaborative project for GMALL system."*。

   - Visibility

     ：

     - **Public**：所有人都可以看到该仓库。
     - **Private**：只有组织成员可以访问。

3. **初始化仓库（可选）**：

   - 如果需要，可以选择：
     - **Add a README file**：创建一个初始的 README 文件。
     - **Add .gitignore**：选择适合的模板（例如 `Java` 或 `Node`）。
     - **Choose a license**：根据项目需求选择许可证（如 `MIT` 或 `Apache 2.0`）。

4. 点击 **Create repository** 按钮。

------

### 3. **设置团队和权限**

1. **进入仓库的 Settings**：
   - 打开新建的仓库页面，点击右上角的 **Settings**。
2. **管理权限**：
   - 在左侧菜单中，选择 **Collaborators and teams**。
   - 点击 **Add teams or people** 按钮，选择你想添加的团队或个人。
   - 为团队或个人分配权限：
     - **Read**：只能查看代码。
     - **Write**：可以提交代码。
     - **Admin**：可以管理仓库设置。

------

### 4. **通知组织成员**

创建好仓库并分配权限后，通知组织成员，他们可以克隆、开发并协作。

- 仓库地址示例：`https://github.com/gmall-team/gmall-project`

------

### 5. **成员协作方式**

组织成员可以通过以下方式协作：

1. **克隆仓库**：

   ```bash
   git clone https://github.com/gmall-team/gmall-project.git
   ```

2. **创建分支开发**：

   - 成员可以为新功能创建分支，并提交代码：

     ```bash
     git checkout -b feature-branch
     git add .
     git commit -m "Add new feature"
     git push origin feature-branch
     ```

3. **提交 Pull Request (PR)**：

   - 成员提交 Pull Request，组织内的代码审查者可以合并代码。

4. **保持同步**：

   - 定期拉取最新代码，确保代码库保持更新：

     ```bash
     git pull origin main
     ```

------

### 6. **管理仓库设置**

作为组织管理员，你可以随时对仓库进行管理：

- **添加/移除成员或团队**。

- 设置分支保护规则

  ：

  - 确保主分支（如 `main`）只能通过 Pull Request 合并。

- 启用 GitHub Actions

  ：

  - 配置自动化测试和部署。

------

### 总结

通过组织创建的仓库，能够实现多人协作开发，方便权限管理和团队协作。以上步骤完成后，组织成员可以按照分配的权限在仓库中协作。