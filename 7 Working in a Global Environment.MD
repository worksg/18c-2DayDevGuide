# 7 在全球环境中工作

全球化支持特性使多语言应用程序能够在世界任何地方同时运行。应用程序可以使用用户的本地语言和语言环境首选项呈现用户界面的内容，并处理数据。

[About Globalization Support Features](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-D819C692-74BA-429A-90A1-8239A11E3979)

全球化支持特性使多语言应用程序能够在世界任何地方同时运行。应用程序可以使用用户的本地语言和语言环境首选项呈现用户界面的内容，并处理数据。

[About Initial NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-7C40C91D-FEC9-4454-B385-B4344CA16FC3)

除了SQL Developer, 区域语言支持的初始参数变量通过数据库的初始化参数进行设置

[Viewing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-24B37C78-7D48-4103-9CF1-04852BA8D30F)

为了查看区域语言支持的当前参数变量，可使用SQL Developer汇报区域语言支持的参数变量值

[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)

你可以通过下面任意方式来改变区域语言支持的一个或多个参数变量

[About Individual NLS Parameters](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-07CE833F-682C-47F8-82E9-0431C4F1C744)

许多独立的区域语言支持参数变量都可以改变

[Using Unicode in Globalized Applications](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-719B79BD-12AC-4810-B57E-B28BB3255179)

你可以插入和取回Unicode数据。 数据在数据库和客户端程序间是隐式转换的，这可以确保客户端程序独立于数据库字符集和语言字符集。

## 7.1 关于全球化支持特性

<!-- Globalization support features enable you to develop multilingual applications that can be run simultaneously from anywhere in the world. An application can render the content of the user interface, and process data, using the native language and locale preferences of the user. -->

全球化支持特性使您能够开发可以在世界任何地方同时运行的多语言应用程序。 应用程序可以使用用户的本机语言和区域设置首选项呈现用户界面的内容，并处理数据。

> 说明:
> 
<!-- > In the past, Oracle called globalization support National Language Support (NLS), but NLS is actually a subset of globalization support. NLS is the ability to choose a national language and store data using a specific character set. NLS is implemented with NLS parameters. -->
> 在过去，Oracle称全球化支持国家语言支持（NLS），但NLS实际上是全球化支持的一个子集。 NLS能够选择国家语言并使用特定字符集存储数据。 NLS使用NLS参数实现。


[About Language Support](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-900E2652-5198-4EFA-A2E8-C51FC37A7809)

<!-- Oracle Database enables you to store, process, and retrieve data in native languages. The languages that can be stored in a database are all languages written in scripts that are encoded by Oracle-supported character sets. Through the use of Unicode databases and data types, Oracle Database supports most contemporary languages. -->

Oracle数据库使您能够以本地语言存储，处理和检索数据。 可以存储在数据库中的语言都是由Oracle支持的字符集编码的脚本编写的语言。 通过使用Unicode数据库和数据类型，Oracle数据库支持大多数现代语言。

[About Territory Support](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-C3063ABA-DBEB-4F4F-BF09-2188E7245B9D)

<!-- The default local time format, date format, and numeric and monetary conventions depend on the local territory setting. -->

默认的本地时间格式，日期格式以及数字和货币惯例取决于本地区域设置。

[About Date and Time Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-3274A5DD-B8B7-463B-9672-BDF51D69A35D)

不同的国家/地区有不同的约定来显示小时，日，月和年。

[About Calendar Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-BDDCBBAC-1CE7-4893-82CB-6A55960901C8)

不同的国家/地区使用不同的日历。

[About Numeric and Monetary Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-647E3E45-DD62-4C80-8BBE-1EF0B7FD5C6B)

不同的国家有不同的数字和货币惯例。

[About Linguistic Sorting and String Searching](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A868EDA2-426F-4B69-8F02-E4439404242E)

<!-- Different languages have different sort orders (collating sequences). Also, different countries or cultures that use the same alphabets sort words differently. For example, in Danish, Æ is after Z, and Y and Ü are considered to be variants of the same letter. -->

不同的语言具有不同的排序顺序（整理顺序）。 此外，使用相同字母表的不同国家或文化对单词进行不同的排序。 例如，在丹麦语中，Æ在Z之后，Y和Ü被认为是同一个字母的变体。

[About Length Semantics](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-9A180244-F6CA-4E10-9087-3CD8030EF956)

<!-- To calculate the number of characters in a string, using byte length, you must know the number of bytes in each character in the character set. -->

要使用字节长度计算字符串中的字符数，必须知道字符集中每个字符的字节数。

[About Unicode and SQL National Character Data Types](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-46E9ADCE-897D-4C53-97C5-C005E8717AFE)

<!-- Unicode is a character encoding system that defines every character in most of the spoken languages in the world. In Unicode, every character has a unique code, regardless of the platform, program, or language. -->

Unicode是一种字符编码系统，它定义了世界上大多数口语中的每个字符。 在Unicode中，与平台，程序或语言无关，每个字符都有唯一的代码。

**也可以看看:**
- [Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG146) 有关全球化支持特性的更多信息

<!-- ## 7.2 About Initial NLS Parameter Values -->
## 7.2 关于初始化NLS参数变量
<!-- Except in SQL Developer, the initial values of NLS parameters are set by database initialization parameters. -->
除了SQL Developer, 区域语言支持的初始参数变量通过数据库的初始化参数进行设置

<!-- The DBA can set the values of initialization parameters in the initialization parameter file, and they take effect the next time the database is started. -->
DBA可以在参数初始化文件中设置初始化参数的值，它们将在下次启动数据库时生效。

<!-- In SQL Developer, the initial values of NLS parameters are as shown in [Table 7-1](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-7C40C91D-FEC9-4454-B385-B4344CA16FC3__CACBAIJA). -->

在SQL Developer中，NLS参数的初始值如[表格 7-1](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-7C40C91D-FEC9-4454-B385-B4344CA16FC3__CACBAIJA)所示。

***表格 7-1 SQL Developer中NLS参数的初始值***

|参数|	初始值|
|:--|:--|
|**NLS_CALENDAR**|GREGORIAN|
|**NLS_CHARACTERSET**|AL32UTF8|
|**NLS_COMP**|BINARY|
|**NLS_CURRENCY**|$|
|**NLS_DATE_FORMAT**|DD-MON-RR|
|**NLS_DATE_LANGUAGE**|AMERICAN|
|**NLS_DUAL_CURRENCY**|$|
|**NLS_ISO_CURRENCY**|AMERICA|
|**NLS_LANGUAGE**|AMERICAN|
|**NLS_LENGTH_SEMANTICS**|BYTE|
|**NLS_NCHAR_CHARACTERSET**|AL16UTF16|
|**NLS_NCHAR_CONV_EXCP**|FALSE|
|**NLS_NUMERIC_CHARACTERS**|.,|
|**NLS_SORT**|BINARY|
|**NLS_TERRITORY**|AMERICA|
|**NLS_TIMESTAMP_FORMAT**|DD-MON-RR HH.MI.SSXFF AM|
|**NLS_TIMESTAMP_TZ_FORMAT**|DD-MON-RR HH.MI.SSXFF AM TZR|
|**NLS_TIME_FORMAT**|HH.MI.SSXFF AM|
|**NLS_TIME_TZ_FORMAT**|HH.MI.SSXFF AM TZR|

**也可以看看:**

<!-- [Oracle Database Administrator's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=ADMIN11099) for information about initialization parameters and initialization parameter files -->
[Oracle Database Administrator's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=ADMIN11099) 有关初始化参数及参数初始化文件的更多信息

<!-- ## 7.3 Viewing NLS Parameter Values -->
## 7.3 查看NLS参数初始值
<!-- To view the current values of NLS parameters, use the SQL Developer report National Language Support Parameters. -->
要查看NLS参数的当前值，请使用SQL Developer报告国家语言支持的参数。

<!-- **To view the National Language Support Parameters report:** -->
**查看国家语言支持参数报告:**

<!-- 1. From the SQL Developer menu View, select **Reports**.
2. In the Reports pane, expand **Data Dictionary Reports**.
3. In the list of reports, expand **About Your Database**.
4. In the list of reports, select **National Language Support Parameters**.
5. In the Select Connection window, select **hr_conn**.
6. Click **OK**.

    The Select Connection window closes and the National Language Support Parameters pane appears, showing the names of the NLS parameters and their current values. -->

1. 在SQL Developer菜单视窗中，选择**报告**.
2. 在报告窗格中, 展开 **数据字典报告**.
3. 在报告列表中, 展开 **关于你的数据库**.
4. 在报告列表中, 选择 **国家语言支持参数**.
5. 在“选择连接”窗口中, 选择 **hr_conn**.
6. 点击 **OK**.

    “选择连接”窗口将会关闭，并显示“国家语言支持参数”窗格，其中显示NLS参数的名称及其当前值

**也可以看看:**

<!-- [Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG11000) for more information about SQL Developer reports -->
[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG11000) 有关SQL Developer报告的更多信息

## 7.4 Changing NLS Parameter Values
You can change the value of one or more NLS parameters in any of these ways.

- Change the values for all SQL Developer connections, current and future.

- On the client, change the settings of the corresponding NLS environment variables.

    Only on the client, the new values of the NLS environment variables override the values of the corresponding NLS parameters.

    You can use environment variables to specify locale-dependent behavior for the client. For example, on a Linux system, this statement sets the value of the **NLS_SORT** environment variable to FRENCH, overriding the value of the **NLS_SORT** parameter:

        % setenv NLS_SORT FRENCH

    > Note:
    > 
    > Environment variables might be platform-dependent.

- Change the values only for the current session, using an **ALTER SESSION** statement with this syntax:
    ```
    ALTER SESSION SET parameter_name=parameter_value
      [ parameter_name=parameter_value ]... ;
    ```

    Only in the current session, the new values override those set in all of the preceding ways.

    You can use the **ALTER SESSION** to test your application with the settings for different locales.

- Change the values only for the current SQL function invocation.

    Only for the current SQL function invocation, the new values override those set in all of the preceding ways.

    [Changing NLS Parameter Values for All SQL Developer Connections](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F46B4DC0-00F6-4B58-9BF8-9F1791B8E8B5)

    You can change the values of NLS parameters for all SQL Developer connections, current and future.

    [Changing NLS Parameter Values for the Current SQL Function Invocation](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A23AFF23-CAF3-4ABB-999A-ED4BA5F48C94)

    SQL functions whose behavior depends on the values of NLS parameters are called **locale-dependent**. Some locale-dependent SQL functions have optional NLS parameters.

**See Also:**

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* for more information about the **ALTER SESSION** statement
- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG188)* for more information about setting NLS parameters

## 7.4.1 Changing NLS Parameter Values for All SQL Developer Connections

You can change the values of NLS parameters for all SQL Developer connections, current and future.

**To change National Language Support Parameter values:**

1. From the SQL Developer menu Tools, select **Preferences**.
2. In the Preferences window, in the left frame, expand **Database**.
3. In the list of database preferences, click **NLS**.
   
    A list of NLS parameters and their current values appears. The value fields are menus.

4. From the menu to the right of each parameter whose value you want to change, select the desired value.
5. Click **OK**.

    The NLS parameters now have the values that you specified. To verify these values, see "[Viewing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-24B37C78-7D48-4103-9CF1-04852BA8D30F)".

> Note:
> 
> If the NLS parameter values do not reflect your changes, click the icon **Run Report**.

**See Also:**

*[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG11100)* for more information about SQL Developer preferences

## 7.4.2 Changing NLS Parameter Values for the Current SQL Function Invocation

SQL functions whose behavior depends on the values of NLS parameters are called **locale-dependent**. Some locale-dependent SQL functions have optional NLS parameters.

The local-dependent functions that have optional NLS parameters are:

- TO_CHAR
- TO_DATE
- TO_NUMBER
- NLS_UPPER
- NLS_LOWER
- NLS_INITCAP
- NLSSORT

In all of the preceding functions, you can specify these NLS parameters:

- NLS_DATE_LANGUAGE
- NLS_DATE_LANGUAGE
- NLS_NUMERIC_CHARACTERS
- NLS_CURRENCY
- NLS_ISO_CURRENCY
- NLS_DUAL_CURRENCY
- NLS_CALENDAR
- NLS_SORT

In the NLSSORT function, you can also specify these NLS parameters:

- NLS_LANGUAGE
- NLS_TERRITORY
- NLS_DATE_FORMAT

To specify NLS parameters in a function, use this syntax:

    'parameter=value' ['parameter=value']...

Suppose that you want **NLS_DATE_LANGUAGE** to be AMERICAN when this query is evaluated:

    SELECT last_name FROM employees WHERE hire_date > '01-JAN-1999';

You can set **NLS_DATE_LANGUAGE** to AMERICAN before running the query:

    ALTER SESSION SET NLS_DATE_LANGUAGE=American;
    SELECT last_name FROM employees WHERE hire_date > '01-JAN-1999';

Alternatively, you can set **NLS_DATE_LANGUAGE** to AMERICAN inside the query, using the locale-dependent SQL function **TO_DATE** with its optional **NLS_DATE_LANGUAGE** parameter:

    SELECT last_name FROM employees
    WHERE hire_date > TO_DATE('01-JAN-1999', 'DD-MON-YYYY',
                            'NLS_DATE_LANGUAGE=AMERICAN');

**Tip:**

Using session default values for NLS parameters in SQL functions usually results in better performance. Therefore, specify optional NLS parameters in locale-dependent SQL functions only in SQL statements that must not use the default NLS parameter values.

**See Also:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG009)* for more information about locale-dependent SQL functions with optional NLS parameters