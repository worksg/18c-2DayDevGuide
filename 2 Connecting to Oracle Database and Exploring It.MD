# 2 连接Oracle数据库和探索它
你可以只通过SQL\*Plus或SQL Developer这样的客户端程序来连接Oracle数据库. 当连接上数据库后，你可以查看数据对象、查看数据库表的属性和数据、和使用查询功能从Oracle数据库的数据表中取回数据

在你通过客户端程序来连接Oracle数据库后，你可以进入客户端程序和执行命令。更多详细信息，可参考客户端程序相关的文档

[Connecting to Oracle Database from SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F386B7FE-7FDD-4C49-B809-63A46D339473) 

SQL\*Plus 是一个可以连接Oracle数据库的客户端程序。 这个主题展示了如何启动SQL\*Plus并连接Oracle数据库

[Connecting to Oracle Database from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-4EF62A6C-8CDA-470A-901E-C24D2A9A5245)

SQL Developer 是一个可以连接Oracle数据库的客户端程序。 

[Connecting to Oracle Database as User HR](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-E010ADBC-E264-4E5E-8F04-7F3D02CF95C8)

完成这个文档中的教程和例子，你必须以账户HR来连接Oracle数据库。

[Exploring Oracle Database with SQL*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-E1407FE1-B4A9-4402-A576-E98716F943DC)

如果你使用SQL\*Plus程序以账户HR来连接Oracle数据库，你可以查看HR数据对象和数据表EMPLOYEES的属性

[Exploring Oracle Database with SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B38A7C64-DCE5-4A33-9DAD-27DB1E212EFD)

如果你使用SQL Developer程序以账户HR来连接Oracle数据库，你可以查看HR数据对象和数据表EMPLOYEES的属性

[Selecting Table Data](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-ECC91F84-8E75-42B9-B733-5CBE4D5717FD)

<!-- ## 2.1 Connecting to Oracle Database from SQL*Plus -->

## 2.1 使用SQL\*Plus连接Oracle数据库

<!-- SQL\*Plus is a client program from which you can access Oracle Database. This topic shows how to start SQL\*Plus and connect to Oracle Database. -->

SQL\*Plus是一个可以用来连接Oracle数据库的客户端程序。这个主题展示了如何使用SQL\*Plus来连接Oracle数据库

<!-- Note:
For steps 3 and 4 of the following procedure, you need a user name and password. -->

> 说明：
> 
> 对于以下过程的步骤3和4，你需要用户名和密码。

<!-- To connect to Oracle Database from SQL\*Plus: -->

从SQL\*Plus连接Oracle数据库

<!-- 1. If you are on a Windows system, display a Windows command prompt. -->

1. 如果您在Windows系统上，则显示Windows命令提示符。

<!-- 2. At the command prompt, type sqlplus and then press the key Enter. -->

2. 在命令提示符下，键入*sqlplus*，然后按**回车键**。

<!-- 3. At the user name prompt, type your user name and then press the key Enter. -->

3. 在用户名提示符下，键入用户名，然后按**回车键**。

<!-- 4. At the password prompt, type your password and then press the key Enter. -->

4. 在密码提示符下，键入密码，然后按**回车键**。

> 说明：
>
> 为了安全考虑，你的密码不会显示在屏幕上

<!-- The system connects you to an Oracle Database instance. -->

该系统将您连接到一个Oracle数据库实例。

<!-- You are in the SQL\*Plus environment. At the SQL> prompt, you can enter and run SQL*Plus commands, SQL statements, PL/SQL statements, and operating system commands. -->

您在SQL\*Plus环境中。在SQL>提示符下，您可以输入和运行SQL\*Plus命令、SQL语句、PL/SQL语句和操作系统命令。

<!-- To exit SQL\*Plus, type exit and press the key Enter. -->

若要退出SQL\*Plus，请键入*exit*并按**回车键**。

<!-- Note:
Exiting SQL\*Plus ends the SQL\*Plus session, but does not shut down the Oracle Database instance. -->

> 说明：
> 
> 退出SQL\*Plus会结束SQL\*Plus会话，但不会关闭Oracle数据库实例。

<!-- Example 2-1 starts SQL\*Plus, connects to Oracle Database, runs a SQL SELECT statement, and exits SQL\*Plus. User input is bold. -->

[Example 2-1](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F386B7FE-7FDD-4C49-B809-63A46D339473__CEGHFHIG) 运行SQL\*Plus，连接Oracle数据库，运行一个SQL SELECT语句，并退出SQL*Plus。用户输入是**粗体**的。

> 译者注: code块内无法显示加粗效果，所以被两个星号夹住的字体标记为加粗的字体，即用户输入

**Example 2-1 使用SQL\*Plus连接Oracle数据库**
```bash
> sqlplus
SQL*Plus: Release 12.1.0.1.0 Production on Thu Dec 27 07:43:41 2012
 
Copyright (c) 1982, 2012, Oracle.  All rights reserved.
 
Enter user-name: **你的用户名**
Enter password: **你的密码**
 
Connected to:
Oracle Database 12c Enterprise Edition Release - 12.1.0.1.0 64bit Production
 
SQL> **select count(*) from employees;**
 
  COUNT(*)
----------
       107
 
SQL> **exit**
 
Disconnected from Oracle Database 12c Enterprise Edition Release - 12.1.0.1.0 64bit Production
> 
```
**也可以看看:**
- "[Connecting to Oracle Database as User HR from SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3EBC7F86-1D6E-4E44-9D17-B3FCB69607CB)"
- "[About SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/two-day-developer-intro.html#GUID-C5ABE48D-C8D7-4BB7-AD66-406719AF6BFD)" 有关SQL\*Plus的简单介绍
- [SQL\*Plus User's Guide and Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQPUG002) 有关启动SQL\*Plus和连接Oracle数据库的更多详细信息


<!-- ## 2.2 Connecting to Oracle Database from SQL Developer -->
## 2.2 从SQL Developer连接Oracle数据库
<!-- SQL Developer is a client program with which you can access Oracle Database. -->
SQL Developer是一个可以连接Oracle数据库的客户端程序

<!-- You are encouraged to use the currently available release of SQL Developer, which you can download from: -->
建议您使用当前可用的SQL Developer版本，您可以从以下链接下载：

http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/

<!-- This section assumes that SQL Developer is installed on your system, and shows how to start it and connect to Oracle Database. If SQL Developer is not installed on your system, then see [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10100) for installation instructions. -->

本节假定您的系统上安装了SQL Developer，并说明了如何启动它并连接到Oracle数据库。如果SQL Developer没有装在你的系统上，查看[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10100)的安装说明

<!-- > Note:
> 
> For the following procedure:
> 
> - If you're using a SQL Developer kit that does not include the JDK, then the first time you start SQL Developer on your system, you must provide the path to the Java Development Kit.
> 
> - When prompted, you need to enter a user name and password. -->

> 说明:
> 
> 对于以下过程:
> 
> - 如果您使用的是不包含JDK的SQL Developer工具包，那么第一次在系统上启动SQL Developer时，必须提供Java Development Kit的路径。
> 
> - 出现提示时，您需要输入用户名和密码。


<!-- **To connect to Oracle Database from SQL Developer:** -->
**从SQL Developer连接到Oracle数据库:**

<!-- 1. Start SQL Developer.
   
    For instructions, see [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10100).

    If this is the first time you have started SQL Developer on your system, you are prompted to enter the path to the Java Development Kit (JDK) installation (for example, *C:\Program Files\Java\jdk1.8.0_65*). Either type the path after the prompt or browse to it, and then press the key **Enter**. -->

1. 启动SQL Developer。
   
    进一步说明可查看 [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10100).

    如果这是您第一次在系统上启动SQL Developer，系统会提示您输入Java Development Kit（JDK）安装的路径（例如，*C:\Program Files\Java\jdk1.8.0_65*）。 在提示后键入路径或浏览到该路径，然后按**回车键**。

<!-- 2. In the Connections frame, click the icon **New Connection**. -->
2. 在连接视窗中, 点击图标 **新的连接**.

<!-- 3. In the New/Select Database Connection window:

    a. Type the appropriate values in the fields Connection Name, Username, and Password.

    &emsp;For security, the password characters that you type appear as asterisks.

    &emsp;Near the Password field is the check box Save Password. By default, it is deselected. Oracle recommends accepting the default.

    b. If the Oracle pane is not showing, click the tab **Oracle**.

    c. In the Oracle pane, accept the default values.

    &emsp;(The default values are: Connection Type, Basic; Role, default, Hostname, localhost; Port, 1521; SID option, selected; SID field, xe.)

    d. Click the button **Test**.

    &emsp;The connection is tested. If the connection succeeds, the Status indicator changes from blank to Success.

    e. If the test succeeded, click the button **Connect**.

    &emsp;The New/Select Database Connection window closes. The Connections frame shows the connection whose name you entered in the Connection Name field in step 3. -->

3. 在“新建/选择数据库连接”窗口中：

    a. 在“连接名称”，“用户名”和“密码”字段中键入适当的值。

    &emsp;为安全起见，您键入的密码字符显示为星号。

    &emsp;在密码区域附近是保存密码的选择框。默认情况下未勾选。 Oracle建议使用默认值。

    b. 如果未显示Oracle窗格，请单击选项卡**Oracle**。

    c. 在Oracle窗格中，接受默认值。

    &emsp;（默认值为：连接类型，基本;角色，默认，主机名，localhost;端口，1521; SID选项，勾选; SID字段，xe。）

    d. 单击按钮**测试**。

    &emsp;连接将会进行测试。如果连接成功，则状态指示器将从空白更改为成功。

    e. 如果测试成功了，请单击按钮**连接**。

    &emsp;“新建/选择数据库连接”窗口会关闭。 连接视窗中会显示您在步骤3的连接名称字段中输入的连接名称。

<!-- You are in the SQL Developer environment. -->
当前你正处于SQL Developer环境。

<!-- To exit SQL Developer, select **Exit** from the File menu. -->
若要退出SQL Developer，请在文件菜单中选择**退出**。

<!-- > Note:
> 
> Exiting SQL Developer ends the SQL Developer session, but does not shut down the Oracle Database instance. The next time you start SQL Developer, the connection you created using the preceding procedure still exists. SQL Developer prompts you for the password that you supplied in step 3 (unless you selected the check box Save Password). -->

> 说明:
> 
> 退出SQL Developer会结束SQL Developer会话，但不会关闭Oracle数据库实例。 下次启动SQL Developer时，使用上述过程创建的连接仍然存在。 SQL Developer会提示您输入在步骤3中提供的密码（除非您勾选了“保存密码”选框）。

**也可以看看:**

- "[Connecting to Oracle Database as User HR from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-872A147C-19D2-4782-AFA4-9987E7AE66BA)"

<!-- - "[About SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/two-day-developer-intro.html#GUID-C00AD6B2-394E-4FD9-A0E4-E0A227662354)" for a brief description of SQL Developer -->

- "[About SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/two-day-developer-intro.html#GUID-C00AD6B2-394E-4FD9-A0E4-E0A227662354)" 关于SQL Developer的简单介绍

<!-- - [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10400) for more information about using SQL Developer to create connections to Oracle Database -->

- [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10400) 有关使用SQL Developer创建Oracle数据库连接的更多信息

# 2.3 以用户HR身份连接到Oracle数据库

要执行本文档中的教程和示例，您必须以用户HR身份连接到Oracle数据库。

用户HR拥有本文档中的示例和教程使用的HR示例模式。

[Unlocking the HR Account](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F779D716-7901-4A84-B854-67F4E03D24FB)

您必须先解锁HR帐户并重置其密码，然后才能以用户HR身份连接到Oracle数据库。

[Connecting to Oracle Database as User HR from SQL*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3EBC7F86-1D6E-4E44-9D17-B3FCB69607CB)

您可以使用SQL\*Plus以用户HR身份连接到Oracle数据库。

[Connecting to Oracle Database as User HR from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-872A147C-19D2-4782-AFA4-9987E7AE66BA)

您可以使用SQL Developer以HR用户身份连接到Oracle数据库。

## 2.3.1 解锁HR账户

您必须先解锁HR帐户并重置其密码，然后才能以用户HR身份连接到Oracle数据库。

默认情况下，安装HR模式时，HR帐户将被锁定，其密码已过期。

> 说明:
> 
> 对于以下过程，您需要具有**ALTER USER**系统特权的用户的名称和密码。


**解锁HR帐户并重置密码:**

1. 使用SQL\*Plus，以具有**ALTER USER**系统特权的用户身份连接到Oracle数据库。
2. 在*SQL>*提示符下，解锁HR帐户并重置其密码:

    > 注意:
    > 
    > 选择安全密码。 有关安全密码的准则，可以查看 [Oracle Database Security Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=DBSEG10005).

        ALTER USER HR ACCOUNT UNLOCK IDENTIFIED BY password;

    系统响应:

        User altered.

    HR帐户已解锁，密码为*password*.

现在，您可以使用密码*password*以用户HR身份连接到Oracle数据库

**也可以看看:**

- [Oracle Database 2 Day + Security Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=TDPSG20030) 有关Oracle数据库提供的预定义用户帐户的信息，包括HR
- [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10710) 有关在SQL Developer中访问SQL\*Plus的信息

## 2.3.2 使用SQL*Plus以用户HR身份连接到Oracle数据库

您可以使用SQL\*Plus以用户HR身份连接到Oracle数据库。

> 说明:
> 
> 如果HR账户被锁定, 可以查看 "[Unlocking the HR Account](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F779D716-7901-4A84-B854-67F4E03D24FB)" and then return to this section.

**从SQL\*Plus以用户HR身份连接到Oracle数据库:**

> 说明:
> 
> 此任务中，您需要HR帐户的密码.

1. 如果已连接到Oracle数据库，请关闭当前连接。
2. 按照说明 "[Connecting to Oracle Database from SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F386B7FE-7FDD-4C49-B809-63A46D339473)" 进行操作, 在第[3]((https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F386B7FE-7FDD-4C49-B809-63A46D339473__CEGBCAGC))步输入用户名 *HR* 在步骤[4]((https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F386B7FE-7FDD-4C49-B809-63A46D339473__CEGDAHFF))输入HR帐户的密码.

    您现在以用户HR连接到Oracle数据库。

**也可以看看:**

*[SQL*Plus User's Guide and Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQPUG008)* 有关使用SQL\*Plus创建HR连接的示例

## 2.3.3 从SQL Developer以用户HR身份连接到Oracle数据库

您可以使用SQL Developer以HR用户身份连接到Oracle数据库。

> 说明:
> 
> 如果HR帐户已锁定，请参阅“解锁HR帐户”，然后返回此部分。

**从SQL Developer以用户HR身份连接到Oracle数据库:**

> 说明:
> 
> 在此任务中，您需要HR帐户的密码。

按照说明 "[Connecting to Oracle Database from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-4EF62A6C-8CDA-470A-901E-C24D2A9A5245)", 在步骤[3]((https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-4EF62A6C-8CDA-470A-901E-C24D2A9A5245__CEGGJCBH))中输入以下值:

- 对于连接名称，输入 *hr_conn*.

    (您可以输入其他名称，但本文档中的教程假定您将连接命名为hr_conn。)

- 对于用户名称, 输入 *HR*.
- 对用户密码, 输入HR账户的密码.

您现在以用户HR连接到Oracle数据库。