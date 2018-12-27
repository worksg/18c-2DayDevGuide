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

<!-- ## 7.4 Changing NLS Parameter Values -->
## 7.4 改变NLS参数值
<!-- You can change the value of one or more NLS parameters in any of these ways. -->
您可以通过以下任何方式更改一个或多个NLS参数的值。

<!-- - Change the values for all SQL Developer connections, current and future. -->
- 更改所有SQL Developer连接的值，当前的连接和以后的连接。

<!-- - On the client, change the settings of the corresponding NLS environment variables. -->
- 在客户端上，更改相应NLS环境变量的设置。

    仅在客户端上，NLS环境变量的新值将覆盖相应NLS参数的值。

    您可以使用环境变量为客户端指定与区域设置相关的行为。 例如，在Linux系统上，下面的语句将 **NLS_SORT** 环境变量的值设置为FRENCH，从而覆盖 **NLS_SORT** 参数的值：

        % setenv NLS_SORT FRENCH

    > 说明:
    > 
    > 环境变量可能有平台依赖。

<!-- - Change the values only for the current session, using an **ALTER SESSION** statement with this syntax:
    ```
    ALTER SESSION SET parameter_name=parameter_value
      [ parameter_name=parameter_value ]... ;
    ```

    Only in the current session, the new values override those set in all of the preceding ways.

    You can use the **ALTER SESSION** to test your application with the settings for different locales. -->

- 仅使用具有以下语法的 **ALTER SESSION** 语句更改当前会话的值:
    ```
    ALTER SESSION SET parameter_name=parameter_value
      [ parameter_name=parameter_value ]... ;
    ```

    仅在当前会话中，新值将覆盖此前所有方式中设置的值。

    您可以在不同语言环境下使用 **ALTER SESSION** 设置语言和测试您的应用程序。

<!-- - Change the values only for the current SQL function invocation.

    Only for the current SQL function invocation, the new values override those set in all of the preceding ways.

    [Changing NLS Parameter Values for All SQL Developer Connections](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F46B4DC0-00F6-4B58-9BF8-9F1791B8E8B5)

    You can change the values of NLS parameters for all SQL Developer connections, current and future.

    [Changing NLS Parameter Values for the Current SQL Function Invocation](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A23AFF23-CAF3-4ABB-999A-ED4BA5F48C94)

    SQL functions whose behavior depends on the values of NLS parameters are called **locale-dependent**. Some locale-dependent SQL functions have optional NLS parameters. -->

- 仅为当前SQL函数调用更改值.

    仅对于当前的SQL函数调用，新值将覆盖此前所有方式中设置的值。

    [Changing NLS Parameter Values for All SQL Developer Connections](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F46B4DC0-00F6-4B58-9BF8-9F1791B8E8B5)

    更改所有SQL Developer连接的值，当前的连接和以后的连接。

    [Changing NLS Parameter Values for the Current SQL Function Invocation](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A23AFF23-CAF3-4ABB-999A-ED4BA5F48C94)

    SQL函数行为依赖NLS参数值的SQL函数称为**语言环境相关**。 一些与语言环境相关的SQL函数拥有可选的NLS参数

**也可以看看:**

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* 有关**ALTER SESSION**语句的更多信息

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG188)* 有关设置NLS参数值的更多信息

### 7.4.1 更改所有SQL Developer连接的NLS参数值

你可以更改所有SQL Developer连接的值，当前的连接和以后的连接。

<!-- **To change National Language Support Parameter values:** -->
**更改国家语言支持参数值:**

1. 从SQL Developer菜单工具中，选择 **首选项**。
2. 在“首选项”窗口的左侧框架中，展开 **数据库**。
3. 在数据库首选项列表中，点击 **NLS**.
   
    将显示NLS参数列表及其当前值。 菜单是值字段。

4. From the menu to the right of each parameter whose value you want to change, select the desired value.
5. 从菜单右侧的参数列表中寻找想要更改的参数，再选择所需的参数值。
6. 点击 **OK**.

    NLS参数现在具有您指定的值。 如果需要验证这些值，可以查看"[Viewing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-24B37C78-7D48-4103-9CF1-04852BA8D30F)"。

> 说明:
> 
> 如果NLS参数值未反映您的更改，请点击图标**运行报告**.

**也可以看看:**

*[Oracle SQL Developer User's Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=RPTUG11100)* 有关SQL Developer首选项的更多信息

### 7.4.2 更改当前SQL函数调用的NLS参数值

SQL函数行为依赖NLS参数值的SQL函数称为**语言环境相关**。 一些与语言环境相关的SQL函数拥有可选的NLS参数

具有可选NLS参数的语言环境相关函数是:

- TO_CHAR
- TO_DATE
- TO_NUMBER
- NLS_UPPER
- NLS_LOWER
- NLS_INITCAP
- NLSSORT

在上述所有功能中，您可以指定这些NLS参数:

- NLS_DATE_LANGUAGE
- NLS_DATE_LANGUAGE
- NLS_NUMERIC_CHARACTERS
- NLS_CURRENCY
- NLS_ISO_CURRENCY
- NLS_DUAL_CURRENCY
- NLS_CALENDAR
- NLS_SORT

在NLSSORT函数中，您还可以指定这些NLS参数:

- NLS_LANGUAGE
- NLS_TERRITORY
- NLS_DATE_FORMAT

要在函数中指定NLS参数，请使用此语法:

    'parameter=value' ['parameter=value']...

假设您在评估此查询时希望**NLS_DATE_LANGUAGE**为AMERICAN：
<!-- Suppose that you want **NLS_DATE_LANGUAGE** to be AMERICAN when this query is evaluated: -->

    SELECT last_name FROM employees WHERE hire_date > '01-JAN-1999';

在运行查询之前，您可以将**NLS_DATE_LANGUAGE**设置为AMERICAN:

    ALTER SESSION SET NLS_DATE_LANGUAGE=American;
    SELECT last_name FROM employees WHERE hire_date > '01-JAN-1999';

或者，您可以使用语言环境相关的SQL函数**TO_DATE**及其可选的**NLS_DATE_LANGUAGE**参数，在查询中将**NLS_DATE_LANGUAGE**设置为AMERICAN
<!-- Alternatively, you can set **NLS_DATE_LANGUAGE** to AMERICAN inside the query, using the locale-dependent SQL function **TO_DATE** with its optional **NLS_DATE_LANGUAGE** parameter: -->

    SELECT last_name FROM employees
    WHERE hire_date > TO_DATE('01-JAN-1999', 'DD-MON-YYYY',
                            'NLS_DATE_LANGUAGE=AMERICAN');

**提示:**

在SQL函数中使用NLS参数的会话默认值通常会带来更好的性能。 因此，仅在不能使用默认NLS参数值的SQL语句中，才在语言环境相关的SQL函数中指定可选的NLS参数。

**也可以看看:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG009)* 有关语言环境相关的SQL函数及可选的NLS参数的更多信息

## 7.5 关于单独的NLS参数
许多单独的NLS参数都是可以使用的。

[About Locale and the NLS_LANG Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-49D71D37-9D14-461A-A900-37C4A2DDFA58)  
**语言环境**是一个系统或应用程序运行的语言和文化环境。 为Oracle数据库软件指定区域设置的最简单方法是设置**NLS_LANG**参数。

[About the NLS_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F2D1BEC5-5CFA-4681-A912-5DB5BA8E0A45)  
此参数指定数据库的默认语言。

[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)  
此参数指定日期格式，时间戳格式，小数和组分隔符，本地货币符号，ISO货币符号和双币种符号的默认约定。

[About the NLS_DATE_FORMAT Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45)  
此参数指定与**TO_CHAR**和**TO_DATE**函数一起使用的默认日期格式。

[About the NLS_DATE_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-DE7C4871-61FB-4202-9873-366E1C402577)  
此参数指定由以下各项生成的日期和月份的名称和缩写语言：SQL函数**TO_CHAR**和**TO_DATE**，默认日期格式（由**NLS_DATE_FORMAT**设置）和符号 AM，PM，AD和BC的默认语言等价物。

[About NLS_TIMESTAMP_FORMAT and NLS_TIMESTAMP_TZ_FORMAT Parameters](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-1D9AD0B5-CC59-45E3-BFC5-56A26F59740D)  
<!-- This parameter specifies the default date format for the **TIMESTAMP** audiotape and **TIMESTAMP WITH LOCAL TIME ZONE** audiotape **TIMESTAMP WITH LOCAL TIME ZONE** audiotape. -->
此参数指定**TIMESTAMP**和**TIMESTAMP WITH LOCAL TIME ZONE**，**TIMESTAMP WITH LOCAL TIME ZONE**的默认日期格式。

[About the NLS_CALENDAR Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A49E60C9-0904-4346-8CB8-6AC25091A10F)  
此参数指定数据库的日历系统。

[About the NLS_NUMERIC_CHARACTERS Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-519B6162-11D8-43A6-9F58-AB9B8B5D2E20)  
此参数指定十进制字符（用于分隔数字的整数和小数部分）和组分隔符（例如，它将整数组分隔为数千和数百万）。 组分隔符是数字格式元素**G**返回的字符。

[About the NLS_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-12AA1194-6F42-4350-8223-4A23E6437AAC)  
此参数指定本地货币符号（由数字格式元素**L**返回的字符串）。

[About the NLS_ISO_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-996B8BC8-1455-411A-990F-F2EDCB506489)  
此参数指定ISO货币符号（数字格式元素**C**返回的字符串）。

[About the NLS_DUAL_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-0C31F9C0-7FA7-4010-B916-0093691B3649)  
此参数指定双币种符号（引入以支持欧元过渡期间的欧元货币符号）。

[]](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5CE0611F-F2F9-4A29-8CA6-6CF49B89F096)  
此参数指定具有**ORDER BY**子句的查询的语言排序顺序（整理顺序）。

[About the NLS_COMP Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5476FAD6-81BD-477F-BB7A-91146674261E)  
此参数指定SQL操作的字符比较行为。

[About the NLS_LENGTH_SEMANTICS Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-7E2C2E2F-04B7-4AA1-9887-4A569F54B3CD)  
此参数指定字符数据类型**CHAR**，**VARCHAR2**和**LONG**的列的长度语义; 也就是说，这些列是以字节还是以字符指定的。 （仅适用于在设置参数后声明的列。）

**也可以看看:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG003)* 有关设置全球化支持环境的更多信息

"[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.1 关于Locale和NLS_LANG参数
**区域**设置是系统或应用程序运行的语言和文化环境。 为Oracle数据库软件指定区域设置的最简单方法是设置**NLS_LANG**参数。

**NLS_LANG**参数为服务器会话（例如，SQL语句处理）和客户端应用程序（例如，Oracle数据库工具中的显示格式）设置参数**NLS_LANGUAGE**和**NLS_TERRITORY**的默认值。 **NLS_LANG**参数还设置客户端应用程序用于输入或显示的数据的字符集。

在数据库安装期间设置**NLS_LANG**的默认值。 您可以使用**ALTER SESSION**语句更改NLS参数的值，包括**NLS_LANG**为您的会话设置的值。 但是，只有客户端可以更改客户端环境中的NLS设置。

**也可以看看:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG189)* 有关使用NLS_LANG参数指定语言环境的详细信息

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG014)* 有关Oracle数据库支持的语言，区域，字符集和其他区域设置数据的信息

"[About the NLS_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F2D1BEC5-5CFA-4681-A912-5DB5BA8E0A45)"

"[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)"

"[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.2 关于NLS_LANGUAGE参数
此参数指定数据库的默认语言。

**指定**：数据库的默认语言。 默认约定：

- 服务器消息的语言
- SQL函数**TO_CHAR**和**TO_DATE**中指定的名称和日期和月份缩写的语言
- AM，PM，AD和BC的默认语言等效符号
- 指定**ORDER BY**子句时字符数据的默认排序顺序
- 写作方向
- 肯定和否定响应字符串（例如，YES和NO）

**可接受的变量**: Oracle支持的任何语言名称。 有关列表，请参阅 *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG014)*.

**默认变量**: 由**NLS_LANG**设置，描述于 "[About Locale and the NLS_LANG Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-49D71D37-9D14-461A-A900-37C4A2DDFA58)".

**设置默认值:**

- **NLS_DATE_LANGUAGE**, 描述于 "[About the NLS_DATE_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-49D71D37-9D14-461A-A900-37C4A2DDFA58)".

- **NLS_SORT**, 描述于 "[About the NLS_SORT Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5CE0611F-F2F9-4A29-8CA6-6CF49B89F096)".

Example 7-1 显示如何设置**NLS_LANGUAGE**到意大利语和德语并影响服务器消息和月份缩写。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-1 NLS_LANGUAGE影响服务器消息和月份缩写***

1. 请注意**NLS_LANGUAGE**的当前值.

2. 如果步骤1中的值不是意大利语，请更改它:
```
ALTER SESSION SET NLS_LANGUAGE=ITALIAN;
```

3. 查询不存在的表:
```
SELECT * FROM nonexistent_table;
```
结果:
```
SELECT * FROM nonexistent_table
              *
ERROR at line 1:
ORA-00942: tabella o vista inesistente
```

4. 运行此查询:
```
SELECT LAST_NAME, HIRE_DATE
FROM EMPLOYEES
WHERE EMPLOYEE_ID IN (111, 112, 113);
```
结果:
```
LAST_NAME                 HIRE_DATE
------------------------- ---------
Sciarra                   30-SET-97
Urman                     07-MAR-98
Popp                      07-DIC-99
 
3 rows selected.
```

5. Change the value of NLS_LANGUAGE to GERMAN:
```
ALTER SESSION SET NLS_LANGUAGE=GERMAN;
```

6. 重复步骤3中的查询.

结果:
```
SELECT * FROM nonexistent_table
              *
ERROR at line 1:
ORA-00942: Tabelle oder View nicht vorhanden
```
7. 重复步骤4中的查询.

结果：
```
LAST_NAME                 HIRE_DATE
------------------------- ---------
Sciarra                   30-SEP-97
Urman                     07-MRZ-98
Popp                      07-DEZ-99
 
3 rows selected.
```
8. 将NLS_LANGUAGE设置为它在步骤1中具有的值。

**也可以看看:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG199)* 有关NLS_LANGUAGE参数的详细信息

"[About Language Support](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-900E2652-5198-4EFA-A2E8-C51FC37A7809)"

"[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.3 关于NLS_TERRITORY参数
此参数指定日期格式，时间戳格式，小数和组分隔符，本地货币符号，ISO货币符号和双币种符号的默认约定。

**指定**：默认约定：

- Date format

- Time stamp format

- Decimal character and group separator

- Local currency symbol

- ISO currency symbol

- Dual currency symbol

**可接受的变量**: Oracle支持的任何地域名称。 有关列表，请参阅[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG014).

**Default Value**: 由NLS_LANG设置，描述于 "[About Locale and the NLS_LANG Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-49D71D37-9D14-461A-A900-37C4A2DDFA58)".

**设置默认值**:

- **NLS_DATE_FORMAT**, ，描述于 "[About the NLS_DATE_FORMAT Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45)".

- **NLS_TIMESTAMP_FORMAT** 和 **NLS_TIMESTAMP_TZ_FORMAT**, 描述于 "[About NLS_TIMESTAMP_FORMAT and NLS_TIMESTAMP_TZ_FORMAT Parameters](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-1D9AD0B5-CC59-45E3-BFC5-56A26F59740D)".

- **NLS_NUMERIC_CHARACTERS**, 描述于 "[About the NLS_NUMERIC_CHARACTERS Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-1D9AD0B5-CC59-45E3-BFC5-56A26F59740D)".

- **NLS_CURRENCY**, 描述于 "[About the NLS_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-12AA1194-6F42-4350-8223-4A23E6437AAC)".

- **NLS_ISO_CURRENCY**, 描述于 "[About the NLS_ISO_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-996B8BC8-1455-411A-990F-F2EDCB506489)".

- **NLS_DUAL_CURRENCY**, 描述于 "[About the NLS_DUAL_CURRENCY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-0C31F9C0-7FA7-4010-B916-0093691B3649)".

[Example 7-2](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5__CACGGBHH) 显示如何将**NLS_TERRITORY**设置为日语和英语并影响货币符号。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-2 NLS_TERRITORY影响货币符号***

1. 请注意**NLS_TERRITORY**的当前值。

2. 如果步骤1中的值不是日语，请更改它:
```
ALTER SESSION SET NLS_TERRITORY=JAPAN;
```
3. 运行此查询:
```
SELECT TO_CHAR(SALARY,'L99G999D99') SALARY
FROM EMPLOYEES
WHERE EMPLOYEE_ID IN (100, 101, 102);
```
结果:
```
SALARY
--------------------
          ©24,000.00
          ©17,000.00
          ©17,000.00
 
3 rows selected.
```
4. 将NLS_TERRITORY的值更改为英语:
```
ALTER SESSION SET NLS_TERRITORY=AMERICA;
```
5. 重复步骤3中的查询.

结果:
```
SALARY
--------------------
          $24,000.00
          $17,000.00
          $17,000.00
 
3 rows selected.
```
6. 将NLS_TERRITORY设置为它在步骤1中具有的值。

**也可以看看:**

*[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG200)* 有关**NLS_TERRITORY**参数的更多信息

"[About Territory Support](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-C3063ABA-DBEB-4F4F-BF09-2188E7245B9D)"

"[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.4 关于NLS_DATE_FORMAT参数
此参数指定与**TO_CHAR**和**TO_DATE**函数一起使用的默认日期格式。

**指定**：与**TO_CHAR**和**TO_DATE**函数一起使用的默认日期格式（在“[Using Conversion Functions in Queries](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-9E724355-6B45-46DC-A15B-59EBAC38E701)”中引入）。

**可接受的变量**: 任何有效的日期时间格式模型。 例如：
```
NLS_DATE_FORMAT='MM/DD/YYYY'
```
有关日期时间格式模型的信息，请参阅 [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00212).

**默认值**: 由**NLS_TERRITORY**设置，描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

默认日期格式可能与给定区域中使用的约定不对应。 要以本地化格式获取日期，您可以使用“DS”（短日期）和“DL”（长日期）格式。

[Example 7-3](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45__CACJHAJI) 显示如何将**NLS_TERRITORY**设置为英语和法语并影响默认，短期和长日期格式。

[Example 7-4](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45__CACDIGCI) 更改**NLS_DATE_FORMAT**的值，覆盖**NLS_TERRITORY**设置的默认值。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-3 NLS_TERRITORY影响日期格式***

1. 请注意NLS_TERRITORY的当前值。

2. 如果步骤1中的值不是英语，请更改它:
```
ALTER SESSION SET NLS_TERRITORY=AMERICA;
```
3. 运行此查询:
```
SELECT hire_date "Default",
       TO_CHAR(hire_date,'DS') "Short",
       TO_CHAR(hire_date,'DL') "Long"
FROM employees
WHERE employee_id IN (111, 112, 113);
```
结果:
```
Default    Short      Long
--------- ---------- -----------------------------
30-SEP-05 9/30/2005  Friday, September 30, 2005
07-MAR-98 3/7/2006   Tuesday, March 07, 2006
07-DEC-99 12/7/2007  Friday, December 07, 2007
 
3 rows selected.
```
4. 将**NLS_TERRITORY**的值更改为法语：
```
ALTER SESSION SET NLS_TERRITORY=FRANCE;
```
5. 重复步骤3中的查询。

结果:
```
Default  Short      Long
-------- ---------- ---------------------------
30/09/05 30/09/2005 friday 30 september 2005
07/03/06 07/03/2006 tuesday 7 march 2006
07/12/07 07/12/2007 friday 7 december 2007
 
3 rows selected.
```
（要以法语获取日期和月份的名称，必须在运行查询之前将**NLS_LANGUAGE**或**NLS_DATE_LANGUAGE**设置为FRENCH。）

6. 将**NLS_TERRITORY**设置为它在步骤1中的值。

***Example 7-4 NLS_DATE_FORMAT覆盖NLS_TERRITORY***

1. 请注意**NLS_TERRITORY**和**NLS_DATE_FORMAT**的当前值。

2. 如果步骤1中**NLS_TERRITORY**的值不是英语，请更改它：
```
ALTER SESSION SET NLS_TERRITORY=AMERICA;
```

3. 如果步骤1中**NLS_DATE_FORMAT**的值不是'Day Month ddth'，请更改它：
```
ALTER SESSION SET NLS_DATE_FORMAT='Day Month ddth';
```
4. 运行此查询（从上一个示例，步骤3）：
```
SELECT hire_date "Default",
       TO_CHAR(hire_date,'DS') "Short",
       TO_CHAR(hire_date,'DL') "Long"
FROM employees
WHERE employee_id IN (111, 112, 113);
```
结果:
```
Default                  Short      Long
------------------------ ---------- -----------------------------
Friday    September 30th 9/30/2005  Tuesday, September 30, 2005
Tuesday   March     07th 3/7/2006   Saturday, March 07, 2006
Friday    December  07th 12/7/2007  Tuesday, December 07, 2007

3 rows selected.
```
5. 将**NLS_TERRITORY**和**NLS_DATE_FORMAT**设置为它们在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG204)* 有关**NLS_DATE_FORMAT**参数的详细信息

- [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF06128) 有关**TO_CHAR**函数的更多信息

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF06132)* 有关**TO_DATE**函数的更多信息

- "[About Date and Time Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-3274A5DD-B8B7-463B-9672-BDF51D69A35D)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.5 关于NLS_DATE_LANGUAGE参数
此参数指定由以下项生成的日期和月份的名称和缩写语言：SQL函数**TO_CHAR**和**TO_DATE**，默认日期格式（由**NLS_DATE_FORMAT**设置），以及默认语言等效项AM，PM，AD和符号的符号 公元前。

**指定**：由以下各项生成的名称和日期和月份缩写的语言：

- SQL函数**TO_CHAR**和**TO_DATE**（在“[Using Conversion Functions in Queries](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-9E724355-6B45-46DC-A15B-59EBAC38E701)”中介绍）

- 默认日期格式（由**NLS_DATE_FORMAT**设置，在“[About the NLS_DATE_FORMAT Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-79B81BEE-38A2-4AC9-95AA-652F0A852C45)”中描述）

- AM，PM，AD和BC的默认语言等效符号

**可接受的变量**: Oracle支持的AM，PM，AD和BCAny语言名称的默认语言等效符号。 有关列表，请参阅[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG014).

**默认值**: 由**NLS_LANGUAGE**设置，描述于 "[About the NLS_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F2D1BEC5-5CFA-4681-A912-5DB5BA8E0A45)".

[Example 7-5](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-DE7C4871-61FB-4202-9873-366E1C402577__CACFGIFI) 显示如何将**NLS_DATE_LANGUAGE**设置为法语和瑞典语并影响显示的系统日期。


要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-5 NLS_DATE_LANGUAGE影响显示的SYSDATE***

1. 请注意**NLS_DATE_LANGUAGE**的当前值。

2. 如果步骤1中**NLS_DATE_LANGUAGE**的值不是FRENCH，请更改它：
```
ALTER SESSION SET NLS_DATE_LANGUAGE=FRENCH;
```
3. 执行此查询:
```
SELECT TO_CHAR(SYSDATE, 'Day:Dd Month yyyy') "System Date"
FROM DUAL;
```
结果:
```
System Date
--------------------------
Vendredi:28 December   2012
```
4. 将**NLS_DATE_LANGUAGE**的值更改为SWEDISH：
```
ALTER SESSION SET NLS_DATE_LANGUAGE=SWEDISH;
```
5. 重复步骤3中的查询。

结果:
```
System Date
-------------------------
Fredag :28 December   2012
```
6. 将**NLS_DATE_LANGUAGE**设置为它在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_DATE_LANGUAGE**参数的详细信息

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* 有关**TO_CHAR**函数的更多信息

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* 有关**TO_DATE**函数的更多信息

- "[About Date and Time Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-3274A5DD-B8B7-463B-9672-BDF51D69A35D)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.6 关于NLS_TIMESTAMP_FORMAT和NLS_TIMESTAMP_TZ_FORMAT参数
<!-- This parameter specifies the default date format for the TIMESTAMP audiotape and TIMESTAMP WITH LOCAL TIME ZONEaudiotapeTIMESTAMP WITH LOCAL TIME ZONEaudiotape. -->
此参数指定时间戳的默认日期格式和带本地时区的时间戳

**指定:** 默认日期格式:

- **TIMESTAMP** audiotape

- **TIMESTAMP WITH LOCAL TIME ZONE** audiotape

**可接受的变量:** 任何有效的日期时间格式模型。 例如：
```
NLS_TIMESTAMP_FORMAT='YYYY-MM-DD HH:MI:SS.FF'
NLS_TIMESTAMP_TZ_FORMAT='YYYY-MM-DD HH:MI:SS.FF TZH:TZM'
```
有关日期时间格式模型的信息，请参阅 *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)*.

**默认值:** 由**NLS_TERRITORY**设置, 描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_TIMESTAMP_FORMAT**参数的详细信息

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_TIMESTAMP_TZ_FORMAT**参数的详细信息

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关日期/时间数据类型和时区支持的信息

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* 有关**TIMESTAMP** audiotape的更多信息

- *[Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00901)* 有关**TIMESTAMP WITH LOCAL TIME ZONE**数据类型的更多信息

- "[About Date and Time Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-3274A5DD-B8B7-463B-9672-BDF51D69A35D)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.7 关于NLS_CALENDAR参数
此参数指定数据库的日历系统。

**指定：** 数据库的日历系统。

**可接受的变量:** Oracle支持的任何日历系统。 有关列表，请参阅 *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)*.

**默认值:** Gregorian

[Example 7-6](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A49E60C9-0904-4346-8CB8-6AC25091A10F__CACICBFC) 显示如何将**NLS_CALENDAR**设置为“English Hijrah”和Gregorian会影响显示的系统日期。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-6 NLS_CALENDAR会影响显示的SYSDATE***

1. 请注意**NLS_CALENDAR**的当前值。

2. 如果步骤1中**NLS_CALENDAR**的值不是“English Hijrah”，请更改它：
```
ALTER SESSION SET NLS_CALENDAR='English Hijrah';
```
3. 执行此查询：
```
SELECT SYSDATE FROM DUAL;
```
结果：
```
SYSDATE
-------------------------
17 Safar             1434
```
4. Change the value of NLS_CALENDAR to 'Gregorian':
```
ALTER SESSION SET NLS_CALENDAR='Gregorian';
```
5. 执行此查询：
```
SELECT SYSDATE FROM DUAL;
```
结果：
```
SYSDATE
---------
31-DEC-12
```
6. 将**NLS_CALENDAR**设置为它在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_CALENDAR**参数的详细信息

- "[About Calendar Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-BDDCBBAC-1CE7-4893-82CB-6A55960901C8)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.8 关于NLS_NUMERIC_CHARACTERS参数
此参数指定十进制字符（用于分隔数字的整数和小数部分）和组分隔符（例如，它将整数组分隔为数千和数百万）。 组分隔符是数字格式元素**G**返回的字符。

**指定：** 十进制字符（用于分隔数字的整数和小数部分）和组分隔符（例如，将整数组分隔为数千和数百万）。 组分隔符是数字格式元素**G**返回的字符。

**可接受的变量:** 任何两个不同的单字节字符，除了：

- A numeric character

- Plus (+)

- Minus (-)

- Less than (<)

- Greater than (>)

**默认值:** 由**NLS_TERRITORY**设置, 描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

在SQL语句中，您可以将数字表示为：

- 数字文字

数字文字不包含在引号中，始终使用句点（.）作为小数字符，并且从不包含组分隔符。

- 文本文字

文本文字用单引号括起来。 根据当前的NLS设置，如果需要，它会隐式或显式转换为数字。

[Example 7-7](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-519B6162-11D8-43A6-9F58-AB9B8B5D2E20__CACGDCBJ) 显示两个不同的**NLS_NUMERIC_CHARACTERS**设置如何影响同一查询的显示结果。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-7 NLS_NUMERIC_CHARACTERS影响十进制字符和组分隔符***

1. 请注意**NLS_NUMERIC_CHARACTERS**的当前值。

2. 如果步骤1中的**NLS_NUMERIC_CHARACTERS**的值不是“，”。 （十进制字符是逗号，组分隔符是句点），更改它：
```
ALTER SESSION SET NLS_NUMERIC_CHARACTERS=",.";
```
3. 执行此查询：
```
SELECT TO_CHAR(4000, '9G999D99') "Number" FROM DUAL;
```
结果：
```
Number
---------
 4.000,00
```
4. 将NLS_NUMERIC_CHARACTERS的值更改为“，”。 （十进制字符是句点，组分隔符是逗号）：
```
ALTER SESSION SET NLS_NUMERIC_CHARACTERS=".,";
```
5. 执行此查询：
```
SELECT TO_CHAR(4000, '9G999D99') "Number" FROM DUAL;
```
结果：
```
Number
---------
 4,000.00
```
6. 将**NLS_NUMERIC_CHARACTERS**设置为它在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_NUMERIC_CHARACTERS**参数的详细信息

- "[About Numeric and Monetary Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-647E3E45-DD62-4C80-8BBE-1EF0B7FD5C6B)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.9 关于NLS_CURRENCY参数
此参数指定本地货币符号（由数字格式元素**L**返回的字符串）。

**指定：** 本地货币符号（数字格式元素**L**返回的字符串）。

**可接受的变量:** 任何有效的货币符号字符串

**默认值:** 由**NLS_TERRITORY**设置, 描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

[Example 7-8](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-12AA1194-6F42-4350-8223-4A23E6437AAC__CACDCHCB) 更改**NLS_CURRENCY**的值，覆盖**NLS_TERRITORY**设置的默认值。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-8 NLS_CURRENCY覆盖NLS_TERRITORY***

1. 请注意**NLS_TERRITORY**和**NLS_CURRENCY**的当前值。

2. 如果步骤1中NLS_TERRITORY的值不是AMERICA，请更改它：
```
ALTER SESSION SET NLS_TERRITORY=AMERICA;
```
3. 执行此查询：
```
SELECT TO_CHAR(salary, 'L099G999D99') "Salary"
FROM EMPLOYEES
WHERE salary > 13000;
```
结果：
```
Salary
---------------------
          $024,000.00
          $017,000.00
          $017,000.00
          $014,000.00
          $013,500.00
```
4. 将**NLS_CURRENCY**的值更改为“©”：
```
ALTER SESSION SET NLS_CURRENCY='©';
```
5. 执行此查询：
```
SELECT TO_CHAR(salary, 'L099G999D99') "Salary"
FROM EMPLOYEES
WHERE salary > 13000;
```
结果：
```
Salary
---------------------
          ©024,000.00
          ©017,000.00
          ©017,000.00
          ©014,000.00
          ©013,500.00
```
6. 将**NLS_TERRITORY**和**NLS_CURRENCY**设置为它们在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_CURRENCY**参数的详细信息

- "[About Numeric and Monetary Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-647E3E45-DD62-4C80-8BBE-1EF0B7FD5C6B)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.10 关于NLS_ISO_CURRENCY参数
此参数指定ISO货币符号（数字格式元素**C**返回的字符串）。

**指定：** ISO货币符号（数字格式元素**C**返回的字符串）。

**可接受的变量:** 任何有效的货币符号字符串

**默认值:** 由**NLS_TERRITORY**设置， 描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

本地货币符号可能不明确，但ISO货币符号是唯一的。

[Example 7-9](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-996B8BC8-1455-411A-990F-F2EDCB506489__CACFIICD) 显示澳大利亚和美国地区具有相同的本地货币符号，但具有不同的ISO货币符号。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-9 NLS_ISO_CURRENCY***

1. 请注意**NLS_TERRITORY**和**NLS_ISO_CURRENCY**的当前值。

2. 如果步骤1中**NLS_TERRITORY**的值不是AUSTRALIA，请更改它：
```
ALTER SESSION SET NLS_TERRITORY=AUSTRALIA;
```
3. 执行此查询：
```
SELECT TO_CHAR(salary, 'L099G999D99') "Local",
        TO_CHAR(salary, 'C099G999D99') "ISO"
FROM EMPLOYEES
WHERE salary > 15000;
```
结果：
```
Local                 ISO
--------------------- ------------------
          $024,000.00      AUD024,000.00
          $017,000.00      AUD017,000.00
          $017,000.00      AUD017,000.00
```
4. 将NLS_TERRITORY的值更改为AMERICA：
```
ALTER SESSION SET NLS_TERRITORY=AMERICA;
```
5. 执行此查询：
```
SELECT TO_CHAR(salary, 'L099G999D99') "Local",
        TO_CHAR(salary, 'C099G999D99') "ISO"
FROM EMPLOYEES
WHERE salary > 15000;
```
结果：
```
Local                 ISO
--------------------- ------------------
          $024,000.00      USD024,000.00
          $017,000.00      USD017,000.00
          $017,000.00      USD017,000.00
```
6. 将**NLS_TERRITORY**和**NLS_ISO_CURRENCY**设置为它们在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* for more information about the NLS_ISO_CURRENCY parameter

- "[About Numeric and Monetary Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-647E3E45-DD62-4C80-8BBE-1EF0B7FD5C6B)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.11 有关NLS_ISO_CURRENCY参数的详细信息
此参数指定双币种符号（引入以支持欧元过渡期间的欧元货币符号）。

**指定：** 双币种符号（在欧元过渡期间引入以支持欧元货币符号）。

**可接受的变量:** 任何有效的货币符号字符串

**默认值:** 由NLS_TERRITORY设置， 描述于 "[About the NLS_TERRITORY Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-074AB158-FF85-4DE5-BD1C-2141B0990CE5)".

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关NLS_DUAL_CURRENCY参数的详细信息

- "[About Numeric and Monetary Formats](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-647E3E45-DD62-4C80-8BBE-1EF0B7FD5C6B)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.12 关于NLS_SORT参数
此参数指定具有ORDER BY子句的查询的语言排序顺序（整理顺序）。

**指定：** 具有ORDER BY子句的查询的语言排序顺序（整理顺序）。

**可接受的变量:**

- BINARY

排序顺序基于数据库字符集或国家字符集的二进制顺序，具体取决于数据类型。

- Oracle支持的任何语言排序名称

排序顺序基于指定语言排序名称的顺序。 语言排序名称通常与语言名称相同，但并非总是如此。 有关支持的语言排序名称列表，请参阅 *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)*.

**默认值:** 由NLS_LANGUAGE设置， 描述于 "[About the NLS_LANGUAGE Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-F2D1BEC5-5CFA-4681-A912-5DB5BA8E0A45) ".

[Example 7-10](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5CE0611F-F2F9-4A29-8CA6-6CF49B89F096__CACGJDGF) 显示两个不同的**NLS_SORT**设置如何影响同一查询的显示结果。 设置为BINARY和繁体西班牙语（SPANISH_M）。 传统西班牙语将ch，ll和ñ分别视为跟随c，l和n的字母。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

**不区分大小写排序**

Oracle数据库中的操作对案例和字符的重音敏感。 要执行不区分大小写的排序，请将_CI附加到**NLS_SORT**参数的值（例如，BINARY_CI或GERMAN_CI）。 要执行既不区分大小写又不区分重音的排序，请将_AI附加到**NLS_SORT**参数的值（例如，BINARY_AI或FRENCH_M_AI）。

***Example 7-10 NLS_SORT会影响语言排序顺序***

1. 为西班牙语单词创建表格：
```
CREATE TABLE temp (name VARCHAR2(15));
```
2. 使用一些西班牙语单词填充表格：
```
INSERT INTO temp (name) VALUES ('laguna');
INSERT INTO temp (name) VALUES ('llama');
INSERT INTO temp (name) VALUES ('loco');
```
3. 注意**NLS_SORT**的当前值。

4. 如果步骤3中的**NLS_SORT**值不是BINARY，请更改它：
```
ALTER SESSION SET NLS_SORT=BINARY;
```
5. 执行此查询：
```
SELECT * FROM temp ORDER BY name;
```
结果：
```
NAME
---------------
laguna
llama
loco
```
6. 将**NLS_SORT**的值更改为SPANISH_M（繁体西班牙语）：
```
ALTER SESSION SET NLS_SORT=SPANISH_M;
```
7. 重复步骤5中的查询。

结果：
```
NAME
---------------
laguna
loco
llama
```
Drop the table:
```
DROP TABLE temp;
```
8. 将**NLS_SORT**设置为它在步骤3中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_SORT**参数的详细信息

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关不区分大小写排序

- "[About Linguistic Sorting and String Searching](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A868EDA2-426F-4B69-8F02-E4439404242E)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.13 关于NLS_COMP参数
此参数指定SQL操作的字符比较行为。

**指定：** SQL操作的字符比较行为。

**可接受的变量:**

- BINARY

SQL比较字符的二进制代码。 如果具有更高的二进制代码，则一个字符大于另一个字符。

- LINGUISTIC

SQL根据NLS_SORT参数的值执行语言比较， 描述于 "[About the NLS_SORT Parameter](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5CE0611F-F2F9-4A29-8CA6-6CF49B89F096)".

- ANSI

提供此值仅用于向后兼容。

**默认值:** BINARY

[Example 7-11](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-5476FAD6-81BD-477F-BB7A-91146674261E__CACDBFEI) 显示查询的结果可能取决于**NLS_COMP**设置。

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-11 NLS_COMP影响SQL字符比较***

1. 请注意**NLS_SORT**和**NLS_COMP**的当前值。

2. 如果步骤1中的**NLS_SORT**和**NLS_COMP**的值分别不是SPANISH_M（繁体西班牙语）和BINARY，请更改它们：
```
ALTER SESSION SET NLS_SORT=SPANISH_M NLS_COMP=BINARY;
```
3. 执行此查询：
```
SELECT LAST_NAME FROM EMPLOYEES
WHERE LAST_NAME LIKE 'C%';
```
结果：
```
LAST_NAME                 
------------------------- 
Cabrio                    
Cambrault                 
Cambrault                 
Chen                      
Chung                     
Colmenares                
 
6 rows selected
```
4. 将**NLS_COMP**的值更改为LINGUISTIC：
```
ALTER SESSION SET NLS_COMP=LINGUISTIC;
```
5. 重复步骤3中的查询。

结果：
```
LAST_NAME                 
------------------------- 
Cabrio                    
Cambrault                 
Cambrault                 
Colmenares                
 
4 rows selected
```
这一次，Chen和Chung没有被退回，因为传统的西班牙语将ch视为跟随c的单个字符。

6. 将**NLS_SORT**和**NLS_COMP**设置为它们在步骤1中具有的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_COMP**参数的更多信息

- "[About Linguistic Sorting and String Searching](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A868EDA2-426F-4B69-8F02-E4439404242E)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

### 7.5.14 关于NLS_LENGTH_SEMANTICS参数
此参数指定字符数据类型CHAR，VARCHAR2和LONG的列的长度语义; 也就是说，这些列是以字节还是以字符指定的。 （仅适用于在设置参数后声明的列。）

**指定：** 字符数据类型CHAR，VARCHAR2和LONG的列的长度语义; 也就是说，这些列是以字节还是以字符指定的。 （仅适用于在设置参数后声明的列。）

**可接受的变量:**

- BYTE

新的CHAR，VARCHAR2和LONG列以字节为单位指定。

- CHAR

新的CHAR，VARCHAR2和LONG列以字符指定。

**默认值:** BYTE

要在SQL Developer中尝试此示例，请在工作表中输入语句和查询。 有关工作表的信息，请参阅“[Running Queries in SQL Developer](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/connecting-exploring-database.html#GUID-B16A89C8-5FFA-4254-96CB-0BCE9CF39651)”。 这里显示的结果来自SQL\*Plus; 它们的格式在SQL Developer中略有不同。

***Example 7-12 NLS_LENGTH_SEMANTICS影响VARCHAR2列的存储***

1. 请注意**NLS_LENGTH_SEMANTICS**的当前值。

2. 如果步骤1中**NLS_LENGTH_SEMANTICS**的值不是BYTE，请更改它：
```
ALTER SESSION SET NLS_LENGTH_SEMANTICS=BYTE;
```
3. 创建一个包含VARCHAR2列的表：
```
CREATE TABLE SEMANTICS_BYTE(SOME_DATA VARCHAR2(20));
```
4. 单击“**连接**”选项卡。

5. 在Connections框架中，展开**hr_conn**。

6. 在架构对象类型列表中，展开“**表**”。

7. 在表格列表中，选择**SEMANTICS_BYTE**。

 在“连接”框的右侧，“列”窗格显示对于列名称SOME_DATA，数据类型为VARCHAR2（20 BYTE）。

8. 将**NLS_LENGTH_SEMANTICS**的值更改为CHAR：
```
ALTER SESSION SET NLS_LENGTH_SEMANTICS=CHAR;
```
9. 使用**VARCHAR2**列创建另一个表：
```
CREATE TABLE SEMANTICS_CHAR(SOME_DATA VARCHAR2(20));
```
10.  在“连接”框中，单击**刷新图标**。

表格列表现在包括SEMANTICS_CHAR。

11. 选择**SEMANTICS_CHAR**.

“列”窗格显示对于列名称SOME_DATA，数据类型为VARCHAR2（20 CHAR）。

12.  再次选择**SEMANTICS_BYTE**。

“列”窗格显示对于列名称SOME_DATA，数据类型仍为VARCHAR2（20 BYTE）。

13. 将**NLS_LENGTH_SEMANTICS**的值设置为它在步骤1中的值。

**也可以看看:**

- *[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG205)* 有关**NLS_LENGTH_SEMANTICS**参数的详细信息

- "[About Length Semantics](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-9A180244-F6CA-4E10-9087-3CD8030EF956)"

- "[Changing NLS Parameter Values](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-A7206047-9B84-4448-9828-8F0FA9725793)"

## 7.6 在全球化应用程序中使用Unicode
您可以插入和检索Unicode数据。 数据在数据库和客户端程序之间透明转换，确保客户端程序独立于数据库字符集和国家字符集。

[Representing Unicode String Literals in SQL and PL/SQL](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-D472628F-DC15-4E12-9475-84C2EAEEF593)

在SQL或PL / SQL中有三种表示Unicode字符串文字的方法。

[Avoiding Data Loss During Character-Set Conversion](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-AB7D2EBA-2380-4046-B514-831308A2AECF)

作为SQL或PL / SQL语句的一部分，文字（带或不带前缀**N**）编码在与语句其余部分相同的字符集中。 在客户端，语句在客户端字符集中编码，该字符集由**NLS_LANG**参数确定。 在服务器端，语句以数据库字符集编码。

**也可以看看:**

- [Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG0073) 有关使用Unicode的SQL和PL / SQL编程的更多信息

- [Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG007) 有关使用Unicode编程的一般信息

### 7.6.1 在SQL和PL / SQL中表示Unicode字符串文字
在SQL或PL / SQL中有三种表示Unicode字符串文字的方法。

在SQL或PL / SQL中表示Unicode字符串文字的三种方法是：

- **N**'string'

**示例**: N'résumé'.

**限制**: 请参阅 "[Avoiding Data Loss During Character-Set Conversion](https://docs.oracle.com/en/database/oracle/oracle-database/18/tdddg/working-in-global-environment.html#GUID-AB7D2EBA-2380-4046-B514-831308A2AECF)".

- **NCHR**(number)

SQL函数**NCHR**返回二进制等效项是国家字符集中的数字的字符。 返回的字符具有数据类型**NVARCHAR2**。

**示例**: NCHR（36）代表默认国家字符集AL16UTF16中的$。

**限制**: NCHR值（可编号）的可移植性仅限于使用相同国家字符集的应用程序。

- **UNISTR**('string')

SQL函数**UNISTR**将字符串转换为国家字符集。

对于可移植性和数据保留，Oracle建议字符串仅包含ASCII字符和Unicode编码值。 Unicode编码值的格式为\xxxx，其中xxxx是UCS-2编码格式的字符代码值的十六进制值。
**示例**：UNISTR（'G \ 0061ry'）代表'Gary'

ASCII字符将转换为数据库字符集，然后转换为国家字符集。 Unicode编码值直接转换为国家字符集。

**也可以看看:**
- [Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG343) 有关Unicode字符串文字的更多信息

- [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00670) 有关**NCHR**功能的更多信息

- [Oracle Database SQL Language Reference](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=SQLRF00670) 有关**UNISTR**功能的更多信息

### 7.6.2 在字符集转换期间避免数据丢失

作为SQL或PL / SQL语句的一部分，文字（带或不带前缀**N**）编码在与语句其余部分相同的字符集中。 在客户端，语句在客户端字符集中编码，该字符集由**NLS_LANG**参数确定。 在服务器端，语句以数据库字符集编码。

当SQL或PL / SQL语句从客户端传输到数据库时，其字符集会相应地转换。 如果数据库字符集不包含客户端在文本文字中使用的所有字符，则此转换中的数据将丢失。 **NCHAR**字符串文字比**CHAR**文本文字更容易受到攻击，因为它们被设计为独立于数据库字符集。

为避免在转换为不兼容的数据库字符集时丢失数据，可以激活**NCHAR**文字替换功能。 有关更多信息，请参阅“[Oracle Database Globalization Support Guide](https://www.oracle.com/pls/topic/lookup?ctx=en/database/oracle/oracle-database/18/tdddg&id=NLSPG344)”。