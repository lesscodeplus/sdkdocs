## 2.3. Type System in NoCodeXpress Engine

NoCodeXpress engine has a dynamic type system with the following data types. Some blocks return various data types, while some function block are restricted to accept only a particular data type.


1. Number : INT, LONG, SHORT, FLOAT, DOUBLE
2. Boolean
3. String
4. Object
5. Array
6. DateTime
7. Expression


Expression data type is used to perform arithmetic and logical operations. In blocks such as 'If' expession data type is required as a parameter as its conditionbundleRenderer.renderToStream
Expressions can include variables enclosed by two curley brackets '{{ }}'

Examples of logical expressions

{{x}} > 1
{{x}} >= 1
{{x}} = 1
{{x}} = 'supun'
{{x}} is null
{{x}} is not null
{{x}} = 1 AND {{y}} = 2
{{x}} = 1 OR {{z}} = 2

Logical expressions are typically used in 'If' blocks 


Examples of arithmetic expressions;

{{x}} + 1
2 - 1
{{x}} * {{y}}
10 / 5

Arithmetic expressions are typically used in the 'Expression' block
