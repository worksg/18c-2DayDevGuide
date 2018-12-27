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

## 2.3 以用户HR身份连接到Oracle数据库

要执行本文档中的教程和示例，您必须以用户HR身份连接到Oracle数据库。

用户HR拥有本文档中的示例和教程使用的HR示例模式。

[Unlocking the HR Account](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-F779D716-7901-4A84-B854-67F4E03D24FB)

您必须先解锁HR帐户并重置其密码，然后才能以用户HR身份连接到Oracle数据库。

[Connecting to Oracle Database as User HR from SQL*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3EBC7F86-1D6E-4E44-9D17-B3FCB69607CB)

您可以使用SQL\*Plus以用户HR身份连接到Oracle数据库。

[Connecting to Oracle Database as User HR from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-872A147C-19D2-4782-AFA4-9987E7AE66BA)

您可以使用SQL Developer以HR用户身份连接到Oracle数据库。

### 2.3.1 解锁HR账户

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

### 2.3.2 使用SQL*Plus以用户HR身份连接到Oracle数据库

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

### 2.3.3 从SQL Developer以用户HR身份连接到Oracle数据库

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

## 2.4 使用SQL * Plus探索Oracle数据库
如果从SQL\*Plus以用户HR身份连接到Oracle数据库，则可以查看HR模式对象和EMPLOYEES表的属性。

> 说明:
> 
> 如果你没有使用SQL\*Plus以用户HR连接到Oracle数据库, 请查看"
> [Connecting to Oracle Database as User HR from SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3EBC7F86-1D6E-4E44-9D17-B3FCB69607CB)" 然后回到本节点。

[Viewing HR Schema Objects with SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-7BCD3985-F47E-4354-B711-3F05D3B82088)

<!-- With SQL\*Plus, you can view the objects that belong to the HR schema by querying the static data dictionary view **USER_OBJECTS**. -->
使用SQL\*Plus，您可以通过查询静态数据字典视图**USER_OBJECTS**来查看属于HR模式的对象。

[Viewing EMPLOYEES Table Properties and Data with SQL\*Plus](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-65EB3CC5-9383-4EF2-AE20-884F5CB24EA4)

<!-- You can a SQL\*Plus command, the SQL **SELECT**statement, and static data dictionary views to view the properties and data of the HR.EMPLOYEES table. -->
您可以使用SQL\*Plus命令，SQL **SELECT**语句和静态数据字典视图来查看HR.EMPLOYEES表的属性和数据。

### 2.4.1 使用SQL * Plus查看HR模式对象
使用SQL\*Plus，您可以通过查询静态数据字典视图**USER_OBJECTS**来查看属于HR模式的对象。

[Example 2-2](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-7BCD3985-F47E-4354-B711-3F05D3B82088__CEGDDFDD) 显示了如何查看属于HR模式的对象的名称和数据类型。

***Example 2-2 使用SQL\*Plus查看HR模式对象***
```
COLUMN OBJECT_NAME FORMAT A25
COLUMN OBJECT_TYPE FORMAT A25

SELECT OBJECT_NAME, OBJECT_TYPE FROM USER_OBJECTS
ORDER BY OBJECT_TYPE, OBJECT_NAME;
```
结果类似于:
```
OBJECT_NAME               OBJECT_TYPE
------------------------- -------------------------
COUNTRY_C_ID_PK           INDEX
DEPT_ID_PK                INDEX
DEPT_LOCATION_IX          INDEX
EMP_DEPARTMENT_IX         INDEX
EMP_EMAIL_UK              INDEX
EMP_EMP_ID_PK             INDEX
EMP_JOB_IX                INDEX
EMP_MANAGER_IX            INDEX
EMP_NAME_IX               INDEX
JHIST_DEPARTMENT_IX       INDEX
JHIST_EMPLOYEE_IX         INDEX
JHIST_EMP_ID_ST_DATE_PK   INDEX
JHIST_JOB_IX              INDEX
JOB_ID_PK                 INDEX
LOC_CITY_IX               INDEX
LOC_COUNTRY_IX            INDEX
LOC_ID_PK                 INDEX
LOC_STATE_PROVINCE_IX     INDEX
REG_ID_PK                 INDEX
ADD_JOB_HISTORY           PROCEDURE
SECURE_DML                PROCEDURE
DEPARTMENTS_SEQ           SEQUENCE
EMPLOYEES_SEQ             SEQUENCE
LOCATIONS_SEQ             SEQUENCE
COUNTRIES                 TABLE
DEPARTMENTS               TABLE
EMPLOYEES                 TABLE
JOBS                      TABLE
JOB_HISTORY               TABLE
LOCATIONS                 TABLE
REGIONS                   TABLE
SECURE_EMPLOYEES          TRIGGER
UPDATE_JOB_HISTORY        TRIGGER
EMP_DETAILS_VIEW          VIEW

34 rows selected.
```

**也可以看看:**

*[Oracle Database Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=REFRN20146)* 有关**USER_OBJECTS**的信息

"[Selecting Table Data](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-ECC91F84-8E75-42B9-B733-5CBE4D5717FD)" 有关使用查询查看表数据的信息

"[About Sample Schema HR](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/two-day-developer-intro.html#GUID-F55D4815-FCD8-4075-AEBC-BC2B57A47F9E)" 有关模式HR的简要信息

### 2.4.2 使用SQL*Plus查看EMPLOYEES表属性和数据

您可以使用SQL\*Plus命令，SQL **SELECT**语句和静态数据字典视图来查看HR.EMPLOYEES表的属性和数据。

<!-- You can use the SQL\*Plus command DESCRIBE to view the properties of the columns of the EMPLOYEES table in the HR schema and the SQL statement **SELECT** to view the data. To view other properties of the table, use static data dictionary views (for example, **USER_CONSTRAINTS**, **USER_INDEXES**, and **USER_TRIGGERS**). -->

您可以使用SQL\*Plus命令DESCRIBE来查看HR模式中EMPLOYEES表的列的属性，并使用SQL语句**SELECT**来查看数据。 要查看表的其他属性，请使用静态数据字典视图（例如，**USER_CONSTRAINTS**，**USER_INDEXES**和**USER_TRIGGERS**）。

[Example 2-3](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-65EB3CC5-9383-4EF2-AE20-884F5CB24EA4__CEGCGJGA) 显示了如何在HR模式中查看EMPLOYEES表的属性。

***Example 2-3 使用SQL\*Plus查看EMPLOYEES表属性***
```
DESCRIBE EMPLOYEES
```
结果:
```
 Name                                      Null?    Type
 ----------------------------------------- -------- -------------
 
 EMPLOYEE_ID                               NOT NULL NUMBER(6)
 FIRST_NAME                                         VARCHAR2(20)
 LAST_NAME                                 NOT NULL VARCHAR2(25)
 EMAIL                                     NOT NULL VARCHAR2(25)
 PHONE_NUMBER                                       VARCHAR2(20)
 HIRE_DATE                                 NOT NULL DATE
 JOB_ID                                    NOT NULL VARCHAR2(10)
 SALARY                                             NUMBER(8,2)
 COMMISSION_PCT                                     NUMBER(2,2)
 MANAGER_ID                                         NUMBER(6)
 DEPARTMENT_ID                                      NUMBER(4)
```
[Example 2-4](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-65EB3CC5-9383-4EF2-AE20-884F5CB24EA4__CEGBDFHB) 显示了如何在HR模式中查看EMPLOYEES表中的某些数据。

***Example 2-4 使用SQL\*Plus查看EMPLOYEES表数据***
```
COLUMN FIRST_NAME FORMAT A20
COLUMN LAST_NAME FORMAT A25
COLUMN PHONE_NUMBER FORMAT A20

SELECT LAST_NAME, FIRST_NAME, PHONE_NUMBER FROM EMPLOYEES
ORDER BY LAST_NAME;
```
结果类似于:
```
LAST_NAME                 FIRST_NAME           PHONE_NUMBER
------------------------- -------------------- --------------------
Abel                      Ellen                011.44.1644.429267
Ande                      Sundar               011.44.1346.629268
Atkinson                  Mozhe                650.124.6234
Austin                    David                590.423.4569
Baer                      Hermann              515.123.8888
Baida                     Shelli               515.127.4563
Banda                     Amit                 011.44.1346.729268
Bates                     Elizabeth            011.44.1343.529268
...
Urman                     Jose Manuel          515.124.4469
Vargas                    Peter                650.121.2004
Vishney                   Clara                011.44.1346.129268
Vollman                   Shanta               650.123.4234
Walsh                     Alana                650.507.9811
Weiss                     Matthew              650.123.1234
Whalen                    Jennifer             515.123.4444
Zlotkey                   Eleni                011.44.1344.429018
 
107 rows selected.
```
**也可以看看:**

*[SQL\*Plus User's Guide and Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQPUG040)* 有关*DESCRIBE*的信息

"[Selecting Table Data](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-ECC91F84-8E75-42B9-B733-5CBE4D5717FD)" 有关使用查询查看表数据的信息

*[Oracle Database Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=REFRN002)* 有关静态数据字典视图的信息

## 2.5 使用SQL Developer探索Oracle数据库
如果从SQL Developer以用户HR身份连接到Oracle数据库，则可以查看HR模式对象和EMPLOYEES表的属性。

[Tutorial: Viewing HR Schema Objects with SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-C5118FEB-8476-4CA2-A1D5-81ACFFCD1927)  
本教程介绍如何使用SQL Developer查看属于HR模式的对象，即如何**浏览**HR模式。

[Tutorial: Viewing EMPLOYEES Table Properties and Data with SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-D1FFB912-EDC5-4DE0-BABC-902207A2F04C)  
本教程介绍如何使用SQL Developer查看HR模式中EMPLOYEES表的属性和数据。

### 2.5.1 教程：使用SQL Developer查看HR模式对象
本教程介绍如何使用SQL Developer查看属于HR模式的对象，即如何**浏览**HR模式。

> 说明:
>
> 如果您未从SQL Developer以用户HR身份连接到Oracle数据库，请参阅 "[Connecting to Oracle Database as User HR from SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-872A147C-19D2-4782-AFA4-9987E7AE66BA)" 然后回到本教程。

**浏览HR模式:**

1. 在Connections框架中，在hr_conn图标的左侧，单击 **加号 (+)**.

    如果未连接到数据库，则会打开“连接信息”窗口。 如果已连接到数据库，则会展开hr_conn信息（请参阅步骤2中“单击确定”后面的信息）.

2. 如果“连接信息”窗口打开:

    a. 在“用户名”字段中，输入hr.

    b. 在“密码”字段中，输入用户HR的密码.

    c. 单击 **确定**.

hr_conn信息展开：加号变为减号（ - ），在hr_conn图标下，将显示模式对象类型列表 - 表，视图，索引等。 （如果单击减号，hr_conn信息将折叠：减号将成为加号，列表将消失。）

**也可以看看:**

*[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10200)* 有关SQL Developer用户界面的更多信息

"[About Sample Schema HR](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/two-day-developer-intro.html#GUID-F55D4815-FCD8-4075-AEBC-BC2B57A47F9E)" 有关模式HR的简要信息

### 2.5.2 教程：使用SQL Developer查看EMPLOYEES表属性和数据

本教程介绍如何使用SQL Developer查看HR模式中EMPLOYEES表的属性和数据。

> 说明:
> 
> 如果您没有浏览HR模式，请参阅 "[Tutorial: Viewing HR Schema Objects with SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-C5118FEB-8476-4CA2-A1D5-81ACFFCD1927)" 然后回到本教程。

**查看EMPLOYEES表的属性和数据:**

1. 在Connections视窗中，展开**Tables**.
   
    在Tables下，将显示HR模式中的表列表。

2. 选择表**EMPLOYEES**.

    在Oracle SQL Developer窗口的右侧框架的“列”窗格中，将显示该表的所有列的列表。 每列的右侧是其属性名称，数据类型等。 （要查看所有列属性，请将水平滚动条向右移动。）

3. 在右侧视窗中，单击选项卡**数据**.
   
    将出现“数据”窗格，其中显示此表中所有记录的编号列表。 （要查看更多记录，请向下移动垂直滚动条。要查看更多记录列，请将水平滚动条向右移动。）

4. 在右侧视窗中，单击选项卡**约束**.
   
    将出现“约束”窗格，其中显示了此表上所有约束的列表。 每个约束的右侧是其属性名称，类型，搜索条件等。 （要查看所有约束属性，请将水平滚动条向右移动。）

5. 单击相应的选项卡，浏览其他属性.
    
    要查看用于创建EMPLOYEES表的SQL语句，请单击**SQL**选项卡。 SQL语句显示在名为EMPLOYEES的窗格中。 要关闭此窗格，请单击名称EMPLOYEES右侧的**x**。

**也可以看看:**

*[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10200)* 有关SQL Developer用户界面的更多信息

<!-- https://tool.lu/markdown/ -->
## 2.6 选择表数据

注意：

要执行本节中的教程和示例，您必须以SQL Developer中的用户HR身份连接到Oracle数据库。 有关说明，请参阅“ [从SQL Developer连接到Oracle数据库作为用户HR](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-872A147C-19D2-4782-AFA4-9987E7AE66BA "您可以使用SQL Developer以HR用户身份连接到Oracle数据库。") ” 。

*   [关于查询](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-A6EC754C-D820-43EC-8509-DD7CF663FD03)  
    **查询**或SQL SELECT语句从一个或多个表或视图中选择数据。
*   [在SQL Developer中运行查询](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)  
    本节介绍如何使用Worksheet在SQL Developer中运行查询。
*   [教程：选择表的所有列](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-A1D0A59B-3DD6-4678-A6ED-7DDAD1B6BC6A)  
    本教程介绍如何选择EMPLOYEES表的所有列。
*   [教程：选择表的特定列](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-62692CDF-8E8B-4B91-A577-CE3D484A718E)  
    本教程介绍如何仅选择EMPLOYEES表的FIRST\_NAME，LAST\_NAME和DEPARTMENT_ID列。
*   [在新标题下显示选定的列](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-68201783-B6A2-4860-B0D0-25D8ADCDA487)  
    在显示的查询结果中，默认列标题是列名称。 要在新标题下显示列，请在列名称后面指定新标题（ **别名** ）。别名在查询期间重命名列，但不会在数据库中更改其名称。
*   [选择满足指定条件的数据](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-374D905A-3DE0-46F3-8525-A647E65DE8DF)  
    要仅选择与指定条件匹配的数据，请在SELECT语句中包含WHERE子句。
*   [对所选数据进行排序](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-584DB914-BB6D-46CF-B7D6-3EB3E94723F1)  
    显示查询结果时，记录可以按任何顺序排列，除非您使用ORDER BY子句指定其顺序。
*   [从多个表中选择数据](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-5EC90E59-F2CF-42D0-AF74-943062278E23)  
    要从多个表中选择数据，请使用称为**连接**的查询。联接中的表必须至少共享一个列名。
*   [在查询中使用运算符和函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3E045FD9-CEA9-4BF5-B4F5-33085E1BC085)  
    查询的select_list可以包括SQL表达式，它可以包括SQL运算符和SQL函数。 这些运算符和函数可以将表数据作为操作数和参数。将评估SQL表达式，并将其值显示在查询结果中。

### 2.6.1 关于查询

**查询**或SQL SELECT语句从一个或多个表或视图中选择数据。

最简单的查询形式具有以下语法：

 SELECT select_list FROM source_list

select_list指定从中选择数据的列，source_list指定具有这些列的表或视图。

嵌套在另一个SQL语句中的**查询**称为**子查询** 。

在SQL * Plus环境中，您可以在SQL>提示符后输入查询（或任何其他SQL语句）。

在SQL Developer环境中，您可以在Worksheet中输入查询（或任何其他SQL语句）。

注意：

显示查询结果时，记录可以按任何顺序排列，除非您使用ORDER BY子句指定其顺序。 有关更多信息，请参阅“ [对所选数据进行排序](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-584DB914-BB6D-46CF-B7D6-3EB3E94723F1 "显示查询结果时，记录可以按任何顺序排列，除非您使用ORDER BY子句指定其顺序。") ” 。

也可以看看：

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF007) 有关查询和子查询的更多信息
    
*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF01702) 有关SELECT语句的更多信息
    
*   [SQL*Plus User's Guide and Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQPUG008) 有关SQL * Plus命令行界面的更多信息
    
*   [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10700) 了解有关在SQL Developer中使用Worksheet的信息
    

### 2.6.2 在SQL Developer中运行查询

本节介绍如何使用Worksheet在SQL Developer中运行查询。

注意：

工作表不仅限于查询; 您可以使用它来运行任何SQL语句。

在SQL Developer中运行查询：

1.  如果SQL Developer的右框显示hr_conn窗格：
    
    1.  如果未显示Worksheet子窗格，请单击选项卡工作表 。
        
    2.  转到第[4](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651__CEGIAJHJ)步。
        
2.  单击图标SQL Worksheet 。
    
3.  如果“ 选择连接”窗口打开：
    
    1.  如果“ 连接”字段没有值`hr_conn` ，请从菜单中选择该值。
        
    2.  单击确定 。
        
    
    将出现一个窗格，其中包含标记为hr_conn的选项卡和两个子窗格，即Worksheet和Query Builder 。 在工作表中 ，您可以输入SQL语句。
    
4.  在工作表中 ，键入查询（ SELECT语句）。
    
5.  单击图标Run Statement 。
    
    查询运行。 在工作表下 ，将出现“ 查询结果”窗格，显示查询结果。
    
6.  在hr_conn选项卡下，单击图标Clear 。
    
    查询消失，您可以在工作表中输入另一个SQL语句。 运行另一个SQL语句时，其结果将显示在“ 查询结果”窗格中，替换以前运行的SQL语句的结果。
    
也可以看看：

 [Oracle SQL Developer用户指南](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG10700) ，了解有关在SQL Developer中使用Worksheet的信息

### 2.6.3 教程：选择表的所有列

本教程介绍如何选择EMPLOYEES表的所有列。

要选择EMPLOYEES表的所有列：

1.  如果存在带有选项卡hr_conn的窗格，请选择它。 否则，单击图标SQL Worksheet ，如“ [在SQL Developer中运行查询](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651 "本节介绍如何使用Worksheet在SQL Developer中运行查询。") ”中所示 。
2.  在工作表中 ，输入以下查询：
    
    SELECT * FROM EMPLOYEES;
    
3.  单击图标Run Statement 。
    
    查询运行。 在“ 工作表”下 ，将显示“ 查询结果”窗格，其中显示了EMPLOYEES表的所有列。
    

警告：

在包含存储敏感数据的列（例如密码或信用卡信息）的表上使用SELECT *时要非常小心。

也可以看看：

“ [教程：使用SQL Developer查看EMPLOYEES表属性和数据](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-D1FFB912-EDC5-4DE0-BABC-902207A2F04C "本教程介绍如何使用SQL Developer查看HR模式中EMPLOYEES表的属性和数据。") ” ，了解有关使用SQL Developer查看表数据的另一种方法的信息

### 2.6.4 教程：选择表的特定列

本教程介绍如何仅选择EMPLOYEES表的FIRST\_NAME，LAST\_NAME和DEPARTMENT_ID列。

要仅选择FIRST\_NAME，LAST\_NAME和DEPARTMENT_ID：

1.  如果存在带有选项卡hr_conn的窗格，请选择它。 否则，单击图标SQL Worksheet ，如“ [在SQL Developer中运行查询](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651 "本节介绍如何使用Worksheet在SQL Developer中运行查询。") ”中所示 。
2.  如果“ 工作表”窗格包含查询，请单击“ 清除 ”图标清除查询。
3.  在工作表中 ，输入以下查询：
    
    SELECT FIRST_NAME, LAST_NAME, DEPARTMENT_ID FROM EMPLOYEES;
    
4.  单击图标Run Statement 。
    
    查询运行。 在工作表下 ，将出现“ 查询结果”窗格，显示查询结果 ，类似于：
    ```
    FIRST_NAME           LAST_NAME                 DEPARTMENT_ID
    -------------------- ------------------------- -------------
    Donald               OConnell                             50
    Douglas              Grant                                50
    Jennifer             Whalen                               10
    Michael              Hartstein                            20
    Pat                  Fay                                  20
    Susan                Mavris                               40
    Hermann              Baer                                 70
    Shelley              Higgins                             110
    William              Gietz                               110
    Steven               King                                 90
    Neena                Kochhar                              90
     
    FIRST_NAME           LAST_NAME                 DEPARTMENT_ID
    -------------------- ------------------------- -------------
    Lex                  De Haan                              90
    ...
    Kevin                Feeney                               50
     
    107 rows selected.
    ```

### 2.6.5 在新标题下显示所选列

在显示的查询结果中，默认列标题是列名称。 要在新标题下显示列，请在列名称后面指定新标题（ **别名** ）。 别名在查询期间重命名列，但不会在数据库中更改其名称。

 [示例2-5](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-68201783-B6A2-4860-B0D0-25D8ADCDA487__CEGJADAB)中的查询选择与“ [教程：选择表的特定列](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-62692CDF-8E8B-4B91-A577-CE3D484A718E "本教程介绍如何仅选择EMPLOYEES表的FIRST_NAME，LAST_NAME和DEPARTMENT_ID列。") ”中的查询相同的列，但它也为它们指定了别名。 由于别名未用双引号括起来，因此它们以大写字母显示。

如果将列别名括在双引号中，则保留大小写，并且别名可以包含空格，如[示例2-6](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-68201783-B6A2-4860-B0D0-25D8ADCDA487__CEGBBEGD)所示。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF01702) 有关 SELECT语句的更多信息，包括列别名（ c_alias）

示例2-5 在新标题下显示所选列
```
SELECT FIRST_NAME First, LAST_NAME last, DEPARTMENT_ID DepT
FROM EMPLOYEES;
```
结果类似于：
```
FIRST                LAST                            DEPT
-------------------- ------------------------- ----------
Donald               OConnell                          50
Douglas              Grant                             50
Jennifer             Whalen                            10
Michael              Hartstein                         20
Pat                  Fay                               20
Susan                Mavris                            40
Hermann              Baer                              70
Shelley              Higgins                          110
William              Gietz                            110
Steven               King                              90
Neena                Kochhar                           90
 
FIRST                LAST                            DEPT
-------------------- ------------------------- ----------
Lex                  De Haan                           90
...
Kevin                Feeney                            50
 
107 rows selected.
```
示例2-6 在列别名中保留大小写和包含空格
```
SELECT FIRST_NAME "Given Name", LAST_NAME "Family Name"
FROM EMPLOYEES;
```
结果类似于：
```
Given Name           Family Name
-------------------- -------------------------
Donald               OConnell
Douglas              Grant
Jennifer             Whalen
Michael              Hartstein
Pat                  Fay
Susan                Mavris
Hermann              Baer
Shelley              Higgins
William              Gietz
Steven               King
Neena                Kochhar
 
Given Name           Family Name
-------------------- -------------------------
Lex                  De Haan
...
Kevin                Feeney
 
107 rows selected.
```
### 2.6.6 选择满足特定条件的数据

要仅选择与指定条件匹配的数据，请在SELECT语句中包含WHERE子句。

WHERE子句中的条件可以是任何SQL条件（有关SQL条件的信息，请参阅[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF005)）。

[示例2-7](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-374D905A-3DE0-46F3-8525-A647E65DE8DF__CEGGJDHI)中的查询仅为部门90中的员工选择数据。

要仅为部门100,110和120中的员工选择数据，请使用此WHERE子句：
```
WHERE DEPARTMENT_ID IN (100, 110, 120);
```
[示例2-8](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-374D905A-3DE0-46F3-8525-A647E65DE8DF__CEGBCCIE)中的查询仅为姓氏以“Ma”开头的员工选择数据。

要仅为姓氏包含“ma”的员工选择数据，请使用此WHERE子句：
```
WHERE LAST_NAME LIKE '%ma%';
```

[示例2-9](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-374D905A-3DE0-46F3-8525-A647E65DE8DF__CEGGGHGF)中的查询测试两个条件 \- 工资是否至少为11000，以及佣金百分比是否为空。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF01702) 有关 SELECT语句的更多信息，包括 WHERE子句
    
*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF005) 有关SQL条件的详细信息
    

示例2-7 从一个部门选择数据
```
SELECT FIRST_NAME, LAST_NAME, DEPARTMENT_ID
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 90;
```
结果类似于：
```
FIRST_NAME           LAST_NAME                 DEPARTMENT_ID
-------------------- ------------------------- -------------
Steven               King                                 90
Neena                Kochhar                              90
Lex                  De Haan                              90

3 rows selected.
```
示例2-8 选择以相同子字符串开头的姓氏的数据
```
SELECT FIRST_NAME, LAST_NAME
FROM EMPLOYEES
WHERE LAST_NAME LIKE 'Ma%';
```
结果类似于：
```
FIRST_NAME           LAST_NAME
-------------------- -------------------------
Jason                Mallin
Steven               Markle
James                Marlow
Mattea               Marvins
Randall              Matos
Susan                Mavris
 
6 rows selected.
```
示例2-9 选择满足两个条件的数据
```
SELECT FIRST_NAME, LAST_NAME, SALARY, COMMISSION_PCT "%"
FROM EMPLOYEES
WHERE (SALARY >= 11000) AND (COMMISSION_PCT IS NOT NULL);
```
结果类似于：
```
FIRST_NAME           LAST_NAME                     SALARY          %
-------------------- ------------------------- ---------- ----------
John                 Russell                        14000         .4
Karen                Partners                       13500         .3
Alberto              Errazuriz                      12000         .3
Gerald               Cambrault                      11000         .3
Lisa                 Ozer                           11500        .25
Ellen                Abel                           11000         .3
 
6 rows selected.
```
### 2.6.7 对所选数据进行排序

显示查询结果时，记录可以按任何顺序排列，除非您使用ORDER BY子句指定其顺序。

[示例2-10](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-584DB914-BB6D-46CF-B7D6-3EB3E94723F1__CEGCEDFB)中的查询结果按`LAST_NAME`升序（默认值）排序。

或者，在SQL Developer中，可以省略ORDER BY子句并双击要排序的列的名称。

排序标准不必包含在选择列表中，如[例2-11](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-584DB914-BB6D-46CF-B7D6-3EB3E94723F1__CEGEGADJ)所示。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF01702) 有关 SELECT语句的更多信息，包括 ORDER BY子句

示例2-10 按LAST_NAME对所选数据进行排序
```
SELECT FIRST_NAME, LAST_NAME, HIRE_DATE
FROM EMPLOYEES
ORDER BY LAST_NAME;
```
结果:
```
FIRST_NAME           LAST_NAME                 HIRE_DATE
-------------------- ------------------------- ---------
Ellen                Abel                      11-MAY-04
Sundar               Ande                      24-MAR-08
Mozhe                Atkinson                  30-OCT-05
David                Austin                    25-JUN-05
Hermann              Baer                      07-JUN-02
Shelli               Baida                     24-DEC-05
Amit                 Banda                     21-APR-08
Elizabeth            Bates                     24-MAR-07
...
FIRST_NAME           LAST_NAME                 HIRE_DATE
-------------------- ------------------------- ---------
Jose Manuel          Urman                     07-MAR-06
Peter                Vargas                    09-JUL-06
Clara                Vishney                   11-NOV-05
Shanta               Vollman                   10-OCT-05
Alana                Walsh                     24-APR-06
Matthew              Weiss                     18-JUL-04
Jennifer             Whalen                    17-SEP-03
Eleni                Zlotkey                   29-JAN-08

107 rows selected
```
示例2-11 按未选择的列对选定数据进行排序
```
SELECT FIRST_NAME, HIRE_DATE
FROM EMPLOYEES
ORDER BY LAST_NAME;
```
结果:
```
FIRST_NAME           HIRE_DATE
-------------------- ---------
Ellen                11-MAY-04
Sundar               24-MAR-08
Mozhe                30-OCT-05
David                25-JUN-05
Hermann              07-JUN-02
Shelli               24-DEC-05
Amit                 21-APR-08
Elizabeth            24-MAR-07
...
FIRST_NAME           HIRE_DATE
-------------------- ---------
Jose Manuel          07-MAR-06
Peter                09-JUL-06
Clara                11-NOV-05
Shanta               10-OCT-05
Alana                24-APR-06
Matthew              18-JUL-04
Jennifer             17-SEP-03
Eleni                29-JAN-08
 
107 rows selected.
```
### 2.6.8 从多个表中选择数据

要从多个表中选择数据，请使用称为**连接**的查询。联接中的表必须至少共享一个列名。

假设您要选择每位员工的FIRST\_NAME，LAST\_NAME和DEPARTMENT_NAME。FIRST\_NAME和LAST\_NAME位于EMPLOYEES表格中，DEPARTMENT_NAME位于DEPARTMENTS表格中。两个表都有DEPARTMENT_ID。您可以使用[示例2-12](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-5EC90E59-F2CF-42D0-AF74-943062278E23__CEGBJFFJ)中的查询。

对于仅出现在连接的一个表中的列名，表名限定符是可选的，但对于出现在两个表中的列名称都是必需的。以下查询等效于[示例2-12](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-5EC90E59-F2CF-42D0-AF74-943062278E23__CEGBJFFJ)中的查询：
```
SELECT FIRST_NAME "First",
LAST_NAME "Last",
DEPARTMENT_NAME "Dept. Name"
FROM EMPLOYEES, DEPARTMENTS
WHERE EMPLOYEES.DEPARTMENT_ID = DEPARTMENTS.DEPARTMENT_ID
ORDER BY DEPARTMENT_NAME, LAST_NAME;
```
要使使用限定列名的查询更具可读性，请使用表别名，如以下示例所示：
```
SELECT FIRST_NAME "First",
LAST_NAME "Last",
DEPARTMENT_NAME "Dept. Name"
FROM EMPLOYEES e, DEPARTMENTS d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID
ORDER BY d.DEPARTMENT_NAME, e.LAST_NAME;
```
虽然您在FROM子句中创建了别名，但您可以在查询的前面使用它们，如下例所示：
```
SELECT e.FIRST_NAME "First",
e.LAST_NAME "Last",
d.DEPARTMENT_NAME "Dept. Name"
FROM EMPLOYEES e, DEPARTMENTS d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID
ORDER BY d.DEPARTMENT_NAME, e.LAST_NAME;
```
**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF30046) 有关联接的详细信息

示例2-12 从两个表中选择数据（连接两个表）
```
SELECT EMPLOYEES.FIRST_NAME "First",
EMPLOYEES.LAST_NAME "Last",
DEPARTMENTS.DEPARTMENT_NAME "Dept. Name"
FROM EMPLOYEES, DEPARTMENTS
WHERE EMPLOYEES.DEPARTMENT_ID = DEPARTMENTS.DEPARTMENT_ID
ORDER BY DEPARTMENTS.DEPARTMENT_NAME, EMPLOYEES.LAST_NAME;
```
结果:
```
First                Last                      Dept. Name                       
-------------------- ------------------------- ------------------------------   
William              Gietz                     Accounting                       
Shelley              Higgins                   Accounting                       
Jennifer             Whalen                    Administration                   
Lex                  De Haan                   Executive                        
Steven               King                      Executive                        
Neena                Kochhar                   Executive                        
John                 Chen                      Finance                          
...
Jose Manuel          Urman                     Finance                          
Susan                Mavris                    Human Resources                  
David                Austin                    IT                               
...
Valli                Pataballa                 IT                               
Pat                  Fay                       Marketing                        
Michael              Hartstein                 Marketing                        
Hermann              Baer                      Public Relations                 
Shelli               Baida                     Purchasing                       
...
Sigal                Tobias                    Purchasing                       
Ellen                Abel                      Sales                            
...
Eleni                Zlotkey                   Sales                            
Mozhe                Atkinson                  Shipping                         
...
Matthew              Weiss                     Shipping                         
 
106 rows selected.
```
### 2.6.9 在查询中使用运算符和函数

查询的select_list可以包括SQL表达式，它可以包括SQL运算符和SQL函数。这些运算符和函数可以将表数据作为操作数和参数。将评估SQL表达式，并将其值显示在查询结果中。

*   [在查询中使用算术运算符](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-75E0CFD9-3B69-45C4-A3D4-B4ED7FBA61AD)  
    基本算术运算符 \- \+（加法）， \- （减法），\*（乘法）和/（除法） \- 对列值进行操作。
*   [在查询中使用数字函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3DED1F6D-719B-41AB-9682-C43E95410E13)  
    数字函数接受数字输入并返回数值。每个数字函数为每个计算的行返回一个值。
*   [在查询中使用连接运算符](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-552A3DC5-AFB3-48F1-BED9-90D3650A5CE9)  
    连接运算符（`||`）将两个字符串组合成一个字符串，方法是将第二个字符串附加到第一个字符串。例如，`'a'||'b'='ab'`。您可以使用此运算符组合查询结果的同一列中的两列或表达式的信息。
*   [在查询中使用字符函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-1A5EC7DB-7501-4CC8-B550-516798B1F533)  
    字符函数接受字符输入。大多数返回字符值，但有些返回数值。每个字符函数为每个计算的行返回一个值。
*   [在查询中使用日期时间函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3243357D-48EC-4275-B770-20DA1E5469FD)  
    日期时间函数在DATE，时间戳和间隔值上运行。每个日期时间函数为每个计算的行返回一个值。
*   [在查询中使用转换函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-9E724355-6B45-46DC-A15B-59EBAC38E701)  
    转换函数将一种数据类型转换为另一种数据。
*   [在查询中使用聚合函数](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B8DF101D-1613-42F2-ABF5-AE67E00E3C2B)  
    聚合函数采用一组行并返回单个结果行。行组可以是整个表或视图。
*   [在查询中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-703425FD-82B2-400F-AA87-C48604CE89FF)  
    使用与NULL相关的函数与NULL相关的函数有助于处理NULL值。
*   [在查询中使用CASE表达式](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B7BACC62-95F0-42D9-BA26-882FE5268A0F)  
    一个CASE表达式可让您使用IF ... THEN ... ELSE逻辑在SQL语句中不调用子程序。有两种CASE表达式，简单和搜索。
*   [使用解码功能中查询](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-5DFAEBA9-C1E7-4AC5-942C-0DEC6C2A1EB1)  
    该DECODE函数的表达式进行比较，以几个搜索值。只要表达式的值与搜索值匹配，DECODE就会返回与该搜索值关联的结果。如果DECODE找不到匹配项，则返回默认值（如果指定）或NULL（如果未指定默认值）。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF003) 有关SQL运算符的详细信息
    
*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF006) 有关SQL函数的更多信息
    

#### 2.6.9.1 在查询中使用算术运算符

基本算术运算符 \- \+（加法）， \- （减法），\*（乘法）和/（除法） \- 对列值进行操作。

[示例2-13](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-75E0CFD9-3B69-45C4-A3D4-B4ED7FBA61AD__CEGJDCII)中的查询按照SALARY的降序显示部门90中每个员工的LAST_NAME，SALARY（月工资）和年薪。

示例2-13在查询中使用算术表达式
```
SELECT LAST_NAME,
SALARY "Monthly Pay",
SALARY * 12 "Annual Pay"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 90
ORDER BY SALARY DESC;
```
结果:
```
LAST_NAME                 Monthly Pay Annual Pay
------------------------- ----------- ----------
King                            24000     288000
De Haan                         17000     204000
Kochhar                         17000     204000
```
#### 2.6.9.2 在查询中使用数字函数

数字函数接受数字输入并返回数值。每个数字函数为每个计算的行返回一个值。

SQL [数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=DSQLRF20031)中列出并描述了SQL支持的数字函数。

[示例2-14](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3DED1F6D-719B-41AB-9682-C43E95410E13__CEGIACAA)中的查询使用数字函数`ROUND`显示部门100中每个员工的每日工资，四舍五入到最接近的分数。

[示例2-15](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3DED1F6D-719B-41AB-9682-C43E95410E13__CEGDGGAB)中的查询使用数字函数`TRUNC`显示部门100中每个员工的每日工资，截断为最接近的美元。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20031) 有关SQL数字函数的详细信息

示例2-14 舍入数字数据
```
SELECT LAST_NAME,
ROUND (((SALARY * 12)/365), 2) "Daily Pay"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY LAST_NAME;
```
结果:
```
LAST_NAME                  Daily Pay
------------------------- ----------
Chen                          269.59
Faviet                        295.89
Greenberg                     394.52
Popp                          226.85
Sciarra                       253.15
Urman                         256.44
 
6 rows selected.
```
示例2-15 截断数字数据
```
SELECT LAST_NAME,
TRUNC ((SALARY * 12)/365) "Daily Pay"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY LAST_NAME;
```
结果:
```
LAST_NAME                  Daily Pay
------------------------- ----------
Chen                             269
Faviet                           295
Greenberg                        394
Popp                             226
Sciarra                          253
Urman                            256
 
6 rows selected.
```
#### 2.6.9.3 在查询中使用连接运算符

连接运算符（`||`）通过将第二个字符串附加到第一个字符串，将两个字符串组合成一个字符串。例如，`'a'||'b'='ab'`。您可以使用此运算符组合查询结果的同一列中的两列或表达式的信息。

[示例2-16](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-552A3DC5-AFB3-48F1-BED9-90D3650A5CE9__CEGIHCBE)中的查询连接了每个所选员工的名字，空格和姓氏。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF51158) for more information about the concatenation operator

示例2-16 连接字符数据
```
SELECT FIRST_NAME || ' ' || LAST_NAME "Name"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY LAST_NAME;
```
结果:
```
Name
---------------------------------------------
John Chen
Daniel Faviet
Nancy Greenberg
Luis Popp
Ismael Sciarra
Jose Manuel Urman
 
6 rows selected.
```
#### 2.6.9.4 在查询中使用字符函数

字符函数接受字符输入。大多数返回字符值，但有些返回数值。每个字符函数为每个计算的行返回一个值。

SQL [数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20032)中列出并描述了SQL支持的字符函数。

功能UPPER，INITCAP和LOWER显示用大写，初始资本和小写，其分别字符的参数。

[示例2-17](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-1A5EC7DB-7501-4CC8-B550-516798B1F533__CEGGAAFJ)中的查询以大写形式显示LAST\_NAME，FIRST\_NAME的第一个字符为大写，其他所有字符均为小写，EMAIL为小写。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20032) 有关SQL字符函数的详细信息

示例2-17 更改字符数据的大小写
```
SELECT UPPER(LAST_NAME) "Last",
INITCAP(FIRST_NAME) "First",
LOWER(EMAIL) "E-Mail"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY EMAIL;
```
结果:
```
Last                      First                E-Mail
------------------------- -------------------- -------------------------
FAVIET                    Daniel               dfaviet
SCIARRA                   Ismael               isciarra
CHEN                      John                 jchen
URMAN                     Jose Manuel          jmurman
POPP                      Luis                 lpopp
GREENBERG                 Nancy                ngreenbe
 
6 rows selected.
```
#### 2.6.9.5 在查询中使用日期时间函数

日期时间功能在日期，时间戳和间隔值上运行。每个日期时间函数为每个计算的行返回一个值。

SQL [数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20033)中列出并描述了SQL支持的日期时间函数。

对于每个DATE和时间戳值，Oracle数据库存储以下信息：

*   Year
    
*   Month
    
*   Date
    
*   Hour
    
*   Minute
    
*   Second
    
    对于每个时间戳值，Oracle数据库还存储第二个小数部分，您可以指定其精度。要同时存储时区，请使用数据类型TIMESTAMP WITH TIME ZONE或TIMESTAMP WITH LOCAL TIME ZONE。
    
有关DATE数据类型的更多信息，请参见[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00202)。

有关TIMESTAMP数据类型的更多信息，请参见[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00203)。

有关其他时间戳数据类型和间隔数据类型的信息，请参阅[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00200)。

[示例2-18](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3243357D-48EC-4275-B770-20DA1E5469FD__CEGBCDFJ)中的查询使用EXTRACT和SYSDATE函数来显示部门100中每个员工的工作年限。的SYSDATE函数返回系统时钟作为当前的日期DATE值。有关SYSDATE函数的更多信息，请参见[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF06124)。有关EXTRACT函数的信息，请参见[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00639)。

[示例2-19](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-3243357D-48EC-4275-B770-20DA1E5469FD__CEGEHDBB)中的查询使用SYSTIMESTAMP函数显示当前系统日期和时间。该SYSTIMESTAMP函数返回一个TIMESTAMP值。有关SYSTIMESTAMP函数的信息，请参见[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF06125)。

查询的FROM子句中的表DUAL是Oracle数据库与数据字典一起自动创建的单行表。如果要使用SELECT语句计算常量表达式，请从DUAL中选择。因为DUAL只有一行，所以常量只返回一次。有关从DUAL中选择的更多信息，请参阅[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20036)。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20033) 有关SQL datetime函数的详细信息

示例2-18 显示日期之间的年数
```
SELECT LAST_NAME,
(EXTRACT(YEAR FROM SYSDATE) - EXTRACT(YEAR FROM HIRE_DATE)) "Years Employed"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY "Years Employed";
```
结果:
```
LAST_NAME                 Years Employed
------------------------- --------------
Popp                                   5
Urman                                  6
Chen                                   7
Sciarra                                7
Greenberg                             10
Faviet                                10
 
6 rows selected.
```
示例2-19 显示系统日期和时间
```
SELECT EXTRACT(HOUR FROM SYSTIMESTAMP) || ':' ||
EXTRACT(MINUTE FROM SYSTIMESTAMP) || ':' ||
ROUND(EXTRACT(SECOND FROM SYSTIMESTAMP), 0) || ', ' ||
EXTRACT(MONTH FROM SYSTIMESTAMP) || '/' ||
EXTRACT(DAY FROM SYSTIMESTAMP) || '/' ||
EXTRACT(YEAR FROM SYSTIMESTAMP) "System Time and Date"
FROM DUAL;
```
结果取决于当前的SYSTIMESTAMP值，但具有以下格式：
```
System Time and Date
------------------------------------------------------------------
18:17:53, 12/27/2012
```
#### 2.6.9.6 在查询中使用转换函数

转换函数将一种数据类型转换为另一种。

SQL [数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20034)中列出并描述了SQL支持的转换函数。

[示例2-20](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-9E724355-6B45-46DC-A15B-59EBAC38E701__CEGCBBCI)中的查询使用TO_CHAR函数将HIRE_DATE值（类型为DATE）转换为具有该格式的字符值`FMMonth DD YYYY`。`FM`从月份名称中删除前导空格和尾随空格。`FMMonth DD YYYY`是**日期时间格式模型**的示例。有关日期时间格式模型的信息，请参阅[Oracle数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00212)。

[示例2-21](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-9E724355-6B45-46DC-A15B-59EBAC38E701__CEGIJDDJ)中的查询使用TO_NUMBER函数将POSTAL_CODE值（类型为VARCHAR2）转换为NUMBER类型的值，并将其用于计算。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20034) 有关SQL转换函数的详细信息
    
*   "[About the NLS_DATE_FORMAT Parameter](working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45 "此参数指定与TO_CHAR和TO_DATE函数一起使用的默认日期格式。")"
    

示例2-20 使用格式模板将日期转换为字符
```
SELECT LAST_NAME,
HIRE_DATE,
TO_CHAR(HIRE_DATE, 'FMMonth DD YYYY') "Date Started"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY LAST_NAME;
```
结果:
```
LAST_NAME                 HIRE_DATE Date Started
------------------------- --------- -----------------
Chen                      28-SEP-05 September 28 2005
Faviet                    16-AUG-02 August 16 2002
Greenberg                 17-AUG-02 August 17 2002
Popp                      07-DEC-07 December 7 2007
Sciarra                   30-SEP-05 September 30 2005
Urman                     07-MAR-06 March 7 2006
 
6 rows selected.
```
示例2-21 将字符转换为数字
```
SELECT CITY,
POSTAL_CODE "Old Code",
TO_NUMBER(POSTAL_CODE) + 1 "New Code"
FROM LOCATIONS
WHERE COUNTRY_ID = 'US'
ORDER BY POSTAL_CODE;
```
结果:
```
CITY                           Old Code       New Code
------------------------------ ------------ ----------
Southlake                      26192             26193
South Brunswick                50090             50091
Seattle                        98199             98200
South San Francisco            99236             99237
 
4 rows selected.
```
#### 2.6.9.7 在查询中使用聚合函数

聚合函数采用一组行并返回单个结果行。行组可以是整个表或视图。

SQL [数据库SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20035)中列出并描述了SQL支持的聚合函数。

与GROUP BY子句一起使用时，聚合函数特别强大，该子句将查询结果按一个或多个列分组，每个组的结果。

[示例2-22](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B8DF101D-1613-42F2-ABF5-AE67E00E3C2B__CEGGIDDF)中的查询使用COUNT函数和GROUP BY子句来显示向每个经理报告的人数。通配符*表示整个记录。

[示例2-22](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B8DF101D-1613-42F2-ABF5-AE67E00E3C2B__CEGGIDDF)显示一名员工未向经理报告。以下查询选择该员工的名字，姓氏和职位：
```
COLUMN FIRST_NAME FORMAT A10;
COLUMN LAST_NAME FORMAT A10;
COLUMN JOB_TITLE FORMAT A10;
```
```
SELECT e.FIRST_NAME,
e.LAST_NAME,
j.JOB_TITLE
FROM EMPLOYEES e, JOBS j
WHERE e.JOB_ID = j.JOB_ID
AND MANAGER_ID IS NULL;
```
结果:
```
FIRST_NAME LAST_NAME  JOB_TITLE
---------- ---------- ----------
Steven     King       President
```
要使查询仅返回聚合值满足指定条件的行，请在查询的HAVING子句中使用聚合函数。

[示例2-23](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B8DF101D-1613-42F2-ABF5-AE67E00E3C2B__CEGGAIJC)中的查询显示了每个部门每年花在工资上的金额，但仅适用于金额超过1,000,000美元的部门。

[示例2-24](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B8DF101D-1613-42F2-ABF5-AE67E00E3C2B__CEGFJGCC)中的查询使用多个聚合函数来显示每个JOB_ID的工资统计信息。

**也可以看看:**

[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20035) 有关SQL聚合函数的详细信息

示例2-22 计算每个组中的行数
```
SELECT MANAGER_ID "Manager",
COUNT(*) "Number of Reports"
FROM EMPLOYEES
GROUP BY MANAGER_ID
ORDER BY MANAGER_ID;
```
结果:
```
   Manager Number of Reports
---------- -----------------
       100                14
       101                 5
       102                 1
       103                 4
       108                 5
       114                 5
       120                 8
       121                 8
       122                 8
       123                 8
       124                 8
       145                 6
       146                 6
       147                 6
       148                 6
       149                 6
       201                 1
       205                 1
                           1
 
19 rows selected.
```
示例2-23 将聚合函数限制为满足条件的行
```
SELECT DEPARTMENT_ID "Department",
SUM(SALARY*12) "All Salaries"
FROM EMPLOYEES
HAVING SUM(SALARY * 12) >= 1000000
GROUP BY DEPARTMENT_ID;
```
结果:
```
Department All Salaries
---------- ------------
        50      1876800
        80      3654000
```
示例2-24 使用统计信息的聚合函数
```
SELECT JOB_ID,
COUNT(*) "#",
MIN(SALARY) "Minimum",
ROUND(AVG(SALARY), 0) "Average",
MEDIAN(SALARY) "Median",
MAX(SALARY) "Maximum",
ROUND(STDDEV(SALARY)) "Std Dev"
FROM EMPLOYEES
GROUP BY JOB_ID
ORDER BY JOB_ID;
```
结果:
```
JOB_ID              #    Minimum    Average     Median    Maximum    Std Dev
---------- ---------- ---------- ---------- ---------- ---------- ----------
AC_ACCOUNT          1       8300       8300       8300       8300          0
AC_MGR              1      12008      12008      12008      12008          0
AD_ASST             1       4400       4400       4400       4400          0
AD_PRES             1      24000      24000      24000      24000          0
AD_VP               2      17000      17000      17000      17000          0
FI_ACCOUNT          5       6900       7920       7800       9000        766
FI_MGR              1      12008      12008      12008      12008          0
HR_REP              1       6500       6500       6500       6500          0
IT_PROG             5       4200       5760       4800       9000       1926
MK_MAN              1      13000      13000      13000      13000          0
MK_REP              1       6000       6000       6000       6000          0
PR_REP              1      10000      10000      10000      10000          0
PU_CLERK            5       2500       2780       2800       3100        239
PU_MAN              1      11000      11000      11000      11000          0
SA_MAN              5      10500      12200      12000      14000       1525
SA_REP             30       6100       8350       8200      11500       1524
SH_CLERK           20       2500       3215       3100       4200        548
ST_CLERK           20       2100       2785       2700       3600        453
ST_MAN              5       5800       7280       7900       8200       1066
 
19 rows selected.
```
#### 2.6.9.8 在查询中使用NULL相关函数

与NULL相关的函数有助于处理NULL值。

的NULL该SQL支持-相关功能中列出并描述[Oracle数据库的SQL语言参考](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF30049)。

[示例2-25中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-703425FD-82B2-400F-AA87-C48604CE89FF__CEGDHHHG)的查询返回姓氏以“B”开头的员工的姓氏和佣金。如果员工没有收到任何佣金（即，如果COMMISSION_PCT为NULL），则NVL函数将“不适用”替换为NULL。

[示例2-26中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-703425FD-82B2-400F-AA87-C48604CE89FF__CEGCECIA)的查询使用NVL2函数返回姓氏以“B”开头的员工的姓氏，工资和收入：如果COMMISSION_PCT不为NULL，则收入为工资加佣金; 如果COMMISSION_PCT为NULL，则收入仅为工资。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00684) 有关 NVL功能的更多信息
    
*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00685) 有关 NVL2功能的更多信息
    

示例2-25 将字符串替换为NULL值
```
SELECT LAST_NAME,
NVL(TO_CHAR(COMMISSION_PCT), 'Not Applicable') "COMMISSION"
FROM EMPLOYEES
WHERE LAST_NAME LIKE 'B%'
ORDER BY LAST_NAME; 
```
结果:
```
LAST_NAME                 COMMISSION
------------------------- ----------------------------------------
Baer                      Not Applicable
Baida                     Not Applicable
Banda                     .1
Bates                     .15
Bell                      Not Applicable
Bernstein                 .25
Bissot                    Not Applicable
Bloom                     .2
Bull                      Not Applicable
 
9 rows selected.
```
示例2-26 为NULL和非NULL值指定不同的表达式
```
SELECT LAST_NAME, SALARY,
NVL2(COMMISSION_PCT, SALARY + (SALARY * COMMISSION_PCT), SALARY) INCOME
FROM EMPLOYEES WHERE LAST_NAME LIKE 'B%'
ORDER BY LAST_NAME;
```
结果:
```
LAST_NAME                     SALARY     INCOME
------------------------- ---------- ----------
Baer                           10000      10000
Baida                           2900       2900
Banda                           6200       6820
Bates                           7300       8395
Bell                            4000       4000
Bernstein                       9500      11875
Bissot                          3300       3300
Bloom                          10000      12000
Bull                            4100       4100
 
9 rows selected.
```
#### 2.6.9.9 在查询中使用CASE表达式

CASE表达式允许您在SQL语句中使用IF ... THEN ... ELSE逻辑而无需调用子程序。 有两种CASE表达式，简单和搜索。

[示例2-27中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B7BACC62-95F0-42D9-BA26-882FE5268A0F__CEGEFFIE)的查询使用简单的CASE表达式来显示每个国家/地区代码的国家/地区名称。

[示例2-28中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B7BACC62-95F0-42D9-BA26-882FE5268A0F__CEGEBIAF)的查询使用搜索的CASE表达式，根据与服务长度关联的日期范围显示建议的工资增长（15％，10％，5％或0％）。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF20037) 有关 CASE表达式的更多信息
    
*   [Oracle Database PL/SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=LNPLS278) 有关 CASE表达式的更多信息
    
*   "[Using the DECODE Function in Queries](connecting-exploring-database.html#GUID-5DFAEBA9-C1E7-4AC5-942C-0DEC6C2A1EB1 "DECODE函数将表达式与多个搜索值进行比较。 只要表达式的值与搜索值匹配，DECODE就会返回与该搜索值关联的结果。 如果DECODE找不到匹配项，则返回默认值（如果指定）或NULL（如果未指定默认值）。")"
    
*   "[Using the CASE Statement](stored-subprograms-packages.html#GUID-985AF0C3-948B-4EE7-95D6-B814A35CD8F2 "CASE语句从一系列条件中选择，并执行相应的语句。")"
    

示例2-27 在查询中使用简单CASE表达式
```
SELECT UNIQUE COUNTRY_ID ID,
       CASE COUNTRY_ID
         WHEN 'AU' THEN 'Australia'
         WHEN 'BR' THEN 'Brazil'
         WHEN 'CA' THEN 'Canada'
         WHEN 'CH' THEN 'Switzerland'
         WHEN 'CN' THEN 'China'
         WHEN 'DE' THEN 'Germany'
         WHEN 'IN' THEN 'India'
         WHEN 'IT' THEN 'Italy'
         WHEN 'JP' THEN 'Japan'
         WHEN 'MX' THEN 'Mexico'
         WHEN 'NL' THEN 'Netherlands'
         WHEN 'SG' THEN 'Singapore'
         WHEN 'UK' THEN 'United Kingdom'
         WHEN 'US' THEN 'United States'
       ELSE 'Unknown'
       END COUNTRY
FROM LOCATIONS
ORDER BY COUNTRY_ID;
```
结果:
```
ID COUNTRY
-- --------------
AU Australia
BR Brazil
CA Canada
CH Switzerland
CN China
DE Germany
IN India
IT Italy
JP Japan
MX Mexico
NL Netherlands
SG Singapore
UK United Kingdom
US United States
 
14 rows selected.
```
示例2-28 在查询中使用搜索的CASE表达式
```
SELECT LAST_NAME "Name",
HIRE_DATE "Started",
SALARY "Salary",
CASE
  WHEN HIRE_DATE < TO_DATE('01-Jan-03', 'dd-mon-yy')
    THEN TRUNC(SALARY*1.15, 0)
  WHEN HIRE_DATE >= TO_DATE('01-Jan-03', 'dd-mon-yy') AND
       HIRE_DATE < TO_DATE('01-Jan-06', 'dd-mon-yy')
    THEN TRUNC(SALARY*1.10, 0)
  WHEN HIRE_DATE >= TO_DATE('01-Jan-06', 'dd-mon-yy') AND
       HIRE_DATE < TO_DATE('01-Jan-07', 'dd-mon-yy')
    THEN TRUNC(SALARY*1.05, 0)
  ELSE SALARY
END "Proposed Salary"
FROM EMPLOYEES
WHERE DEPARTMENT_ID = 100
ORDER BY HIRE_DATE;
```
结果:
```
Name                      Started       Salary Proposed Salary
------------------------- --------- ---------- ---------------
Faviet                    16-AUG-02       9000           10350
Greenberg                 17-AUG-02      12008           13809
Chen                      28-SEP-05       8200            9020
Sciarra                   30-SEP-05       7700            8470
Urman                     07-MAR-06       7800            8190
Popp                      07-DEC-07       6900            6900

6 rows selected.
```
#### 2.6.9.10 在查询中使用DECODE函数

该DECODE函数的表达式进行比较，以几个搜索值。只要表达式的值与搜索值匹配，DECODE就会返回与该搜索值关联的结果。如果DECODE找不到匹配项，则返回默认值（如果指定）或NULL（如果未指定默认值）。

[示例2-29中](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-5DFAEBA9-C1E7-4AC5-942C-0DEC6C2A1EB1__CEGCACGA)的查询使用DECODE函数显示三个不同作业的建议工资增长。表达式为JOB_ID; 搜索值为“PU\_CLERK”，“SH\_CLERK”和“ST_CLERK”; 默认为SALARY。

注意：

DECODE函数的参数可以是任何SQL数字或字符类型。在比较之前，Oracle会自动将表达式和每个搜索值转换为第一个搜索值的数据类型。Oracle会自动将返回值转换为与第一个结果相同的数据类型。如果第一个结果具有数据类型CHAR或第一个结果为NULL，则Oracle将返回值转换为数据类型VARCHAR2。

**也可以看看:**

*   [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00631) 有关 DECODE函数的信息
    
*   "[Using CASE Expressions in Queries](connecting-exploring-database.html#GUID-B7BACC62-95F0-42D9-BA26-882FE5268A0F "CASE表达式允许您在SQL语句中使用IF ... THEN ... ELSE逻辑而无需调用子程序。 有两种CASE表达式，简单和搜索。")"
    

示例2-29 在查询中使用DECODE函数
```
SELECT LAST_NAME, JOB_ID, SALARY,
DECODE(JOB_ID,
 'PU_CLERK', SALARY * 1.10,
 'SH_CLERK', SALARY * 1.15,
 'ST_CLERK', SALARY * 1.20,
 SALARY) "Proposed Salary"
FROM EMPLOYEES
WHERE JOB_ID LIKE '%_CLERK'
AND LAST_NAME < 'E'
ORDER BY LAST_NAME;
```
结果:
```
LAST_NAME                 JOB_ID         SALARY Proposed Salary
------------------------- ---------- ---------- ---------------
Atkinson                  ST_CLERK         2800            3360
Baida                     PU_CLERK         2900            3190
Bell                      SH_CLERK         4000            4600
Bissot                    ST_CLERK         3300            3960
Bull                      SH_CLERK         4100            4715
Cabrio                    SH_CLERK         3000            3450
Chung                     SH_CLERK         3800            4370
Colmenares                PU_CLERK         2500            2750
Davies                    ST_CLERK         3100            3720
Dellinger                 SH_CLERK         3400            3910
Dilly                     SH_CLERK         3600            4140
 
11 rows selected.
```