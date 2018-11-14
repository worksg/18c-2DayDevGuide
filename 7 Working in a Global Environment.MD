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