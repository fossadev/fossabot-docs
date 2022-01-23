--
id: jseval


# $(jseval)

Evaluates an argument and functions as a string. If the argument is an expression, eval() evaluates the expression. If the argument is one or more JS statements, eval() executes the statements. 


#### Parameters

string	-- A JS expression, variable, statement, or sequence of statements

A string representing a JS statement or sequence of statements. The expression can include variables and properties of existing objects.


#### Syntax

eval(string)


#### Example Output

eval(new String('2 + 2'));
* Returns a String object containing "2 + 2"



#### WARNING

* With eval(), malicious code can run inside your application without permission.

* With eval(), third-party code can see the scope of your application, whitch can lead to possible attacks.
