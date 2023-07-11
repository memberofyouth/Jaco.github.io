https://dbdocs.io/mrzlive/first_project



您的 dbdocs 项目默认设置为**公开**。但是，您可以按照以下命令使用密码对其进行保护。

```bash
$ dbdocs password --set <password> --project <project name>
✔ Password is set for <project name>
```

或者

```bash
$ dbdocs password --project <project name>
? Enter password: [hidden]
? Re-enter password: [hidden]
✔ Password is set for <project name>
```

或者您可以使用带有 --password 的 build 命令来构建您的项目

```bash
$ dbdocs build <path to your dbml file>/database.dbml --password <password>
Pushing new database schema to project your_project...
✔ Password is set for 'Ecommerce'
Done. Visit: https://dbdocs.io/khanh-tran-quoc/Ecommerce
```

## 删除密码

从您的项目中删除密码以使其公开

```bash
$ dbdocs password --remove --project <project name>
⚠ Password is removed from 'Ecommerce'
```





## 安装

**前提条件：**确保在安装`NodeJS`前`NPM`已经安装在您的电脑上。

### 1.通过终端安装dbdocs

在终端中运行以下命令：

```bash
npm install -g dbdocs
```

或者，如果您正在使用`yarn`

```bash
yarn global add dbdocs
```

请注意，在某些情况下，您需要添加`sudo`到命令中，以便`npm`全局安装 dbdocs。

```bash
$ sudo npm install -g dbdocs
dbdocs install...
```


执行`dbdocs`命令检查它是否已经安装并预览一些命令。

```text
$ dbdocs
dbdocs ======

VERSION
  dbdocs/0.6.2 win32-x64 node-v12.16.1

USAGE
  $ dbdocs [COMMAND]
  
COMMANDS
  build     build docs
  help      display help for dbdocs
  login     login to dbdocs
  logout    logout
  ls        list projects
  password  set password for your project or remove password
  remove    remove docs
  token     generate or revoke your authentication token
  validate  validate docs content
```

### 2. 用 DBML 定义你的数据库

要使用 dbdocs，请使用[DBML](https://www.dbml.org/home/)（一种简单的开源 DSL 语言）定义您的数据库模式。我们建议您使用 Visual Studio Code，因为您可以安装随附的 DBML 语言支持包，但任何其他编辑器都可以正常工作。

假设我们创建一个名为*database.dbml*的文件，如下所示。

```text
Project Ecommerce {
  database_type: 'PostgreSQL'
  Note: '''
    # Ecommerce Database
    **markdown content here**
  '''
}
Table users as U {
  id int [pk, increment]
  full_name varchar
  created_at timestamp
  country_code int
  note: "table 'users' contains user information"
}
Table merchants {
  id int [pk]
  merchant_name varchar
  country_code int [note: "country of merchant"]
  admin_id int [ref: > U.id]
  created_at datetime [default: `now()`, note: "created time"]
  note: "table 'merchants' contains merchant information"
}
Table countries {
  code int [pk]
  name varchar
  continent_name varchar
}
Table order_items {
  order_id int [ref: > orders.id]
  product_id int    
  quantity int [default: 1]
  note: 'items in an order'
}
Table orders {
  id int [pk]
  user_id int [not null, unique]
  status varchar
  created_at varchar [note: 'When order created']
}
Enum products_status {
  out_of_stock
  in_stock
  running_low [note: 'less than 20']
}
Table products {
  id int [pk]
  name varchar
  merchant_id int [not null]
  price int
  status products_status
  created_at datetime [default: `now()`]
  
  Indexes {
    (merchant_id, status) [name:'product_status']
    id [unique]
  }
}
Ref: U.country_code > countries.code  
Ref: merchants.country_code > countries.code
Ref: order_items.product_id > products.id
Ref: products.merchant_id > merchants.id
```

*快速提示：您可以使用几条命令[行将 .sql 文件转换为 .dbml 。](https://www.dbml.org/cli/#convert-a-sql-file-to-dbml)*

项目`Note`中的信息支持 markdown 语法，所以可以在 markdown 中写下注释以获得更好的描述。它应该是这样的：

```text
Project first_project {
  database_type: 'PostgreSQL'
  Note: '''
    # Ecommerce Database
    **markdown content here**
  '''
}
```

您的文档将与您的项目名称相同。在此示例中，您的文档名称将为 `first_project`. 否则，将在第 5 步中要求您提供项目名称。

### 3. 登录 dbdocs

在生成 dbdocs 视图之前，您需要通过执行以下命令登录（通过电子邮件登录）

```bash
$ dbdocs login
? Choose a login method: Email
? Your email: <your email address>
✔ Request email authentication
? Please input OTP code sent to the email:
```

通过在电子邮件中正确输入 OTP 代码，您将能够访问 dbdocs。

![img](https://gitee.com/mrzlive/picture-bed/raw/master/picture/202206301408259.png)

### 4.生成dbdocs视图

在终端中打开包含您的 dbml 文件的文件夹，然后通过以下命令生成 dbdocs 视图。

```bash
$ dbdocs build <path to your dbml file>/database.dbml
Pushing new database schema to project your_project...
Done. Visit: https://dbdocs.io/khanh-tran-quoc/Ecommerce
```

### 5. 检查您的数据库文档！

最后一步为您提供了访问数据库文档的链接。在我们的示例中，请访问：[https](https://dbdocs.io/khanh-tran-quoc/Ecommerce) ://dbdocs.io/khanh-tran-quoc/Ecommerce进行查看。

## 删除您的项目

您可以通过 remove 命令简单地删除您的项目

```bash
$ dbdocs remove <project name>
✔ Removed successfully
```