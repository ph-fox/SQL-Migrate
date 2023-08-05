# SQL-Migrate

SQL-Migrate 是一个 SQL 转换器，用于在 SQLite 数据库与 MySQL 数据库之间进行转换。它提供了将 SQLite 数据转换为 MySQL 数据库以及将 MySQL 数据库转换为 SQLite 文件的功能。

## 特性

- 支持将 SQLite 数据库转换为 MySQL 数据库
- 支持将 MySQL 数据库转换为 SQLite 文件
- 简单易用，只需几个简单的命令即可完成转换
- 支持处理常见的数据类型和表结构
- 保持数据的完整性和准确性

## 安装

使用以下命令从 PyPI 安装 SQL-Migrate：

```bash
pip install sql-migrate
```

## 使用说明

### 将 SQLite 数据库转换为 MySQL 数据库

要将 SQLite 数据库转换为 MySQL 数据库，请执行以下命令：

```bash
sql-migrate sqlite-to-mysql -s <SQLite数据库文件> -u <MySQL用户名> -p <MySQL密码> -d <目标MySQL数据库名> -h <MySQL主机地址>
```

- \`<SQLite数据库文件>\`: 要转换的 SQLite 数据库文件的路径。
- \`<MySQL用户名>\`: MySQL 数据库的用户名。
- \`<MySQL密码>\`: MySQL 数据库的密码。
- \`<目标MySQL数据库名>\`: 要导入数据的目标 MySQL 数据库名。
- \`<MySQL主机地址>\`: MySQL 数据库的主机地址。

### 将 MySQL 数据库转换为 SQLite 文件

要将 MySQL 数据库转换为 SQLite 文件，请执行以下命令：

\`\`\`bash
sql-migrate mysql-to-sqlite -s <MySQL数据库名> -u <MySQL用户名> -p <MySQL密码> -d <目标SQLite文件>
\`\`\`

- \`<MySQL数据库名>\`: 要转换的 MySQL 数据库名。
- \`<MySQL用户名>\`: MySQL 数据库的用户名。
- \`<MySQL密码>\`: MySQL 数据库的密码。
- \`<目标SQLite文件>\`: 转换后保存数据的目标 SQLite 文件的路径。

## 示例

将 SQLite 数据库文件 "data.db" 转换为 MySQL 数据库，用户名为 "root"，密码为 "password"，目标数据库名为 "mysql_db"，MySQL 主机地址为 "localhost"：

```bash
sql-migrate sqlite-to-mysql -s data.db -u root -p password -d mysql_db -h localhost
```

将 MySQL 数据库 "mysql_db" 转换为 SQLite 文件 "output.sqlite"，用户名为 "root"，密码为 "password"：

```bash
sql-migrate mysql-to-sqlite -s mysql_db -u root -p password -d output.sqlite
```

## 贡献

欢迎对 SQL-Migrate 提交问题报告和改进建议！您可以通过提交 Pull Request 来贡献代码。

## 许可证

SQL-Migrate 使用 MIT 许可证，详情请查阅 [LICENSE](LICENSE) 文件。

---

注意：请在使用 SQL-Migrate 之前备份您的数据，以免因操作不当导致数据丢失。作者对使用本工具造成的数据丢失不承担任何责任。
