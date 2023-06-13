---
title: Delphi
attachments: [Clipboard_2023-06-07-12-25-45.png, Clipboard_2023-06-07-12-28-05.png, Clipboard_2023-06-07-12-28-16.png]
created: 2023-05-13T04:53:16.002Z
modified: 2023-06-07T13:03:37.275Z
---

# Delphi
by Waldo Joubert

[[@toc]]

[[@pagebreak]]

## Naming Scheme

In Delphi the naming rules for variable names are:

- all variable and component names must be unique
- names may not contain spaces
- names may not start with a number, but they can contain a number
- names may not contain any special characters (like exclamation marks) 
except for underscores (_).

Here are some naming conventions used for variables:

- variable names should describe the data they will contain. For example: 
variable name: Amount for a variable that will hold monetary data
- names should use CamelCase. This means the first word or letter is in 
lowercase, and each word afterwards starts with an uppercase letter, for 
example, rAmountPaid
- variable names should start with a single letter prefix describing the data 
type the variable will hold.

Components:

| Component | Name Scheme |
| :-------: | :---------: |
|   TMemo   |   memTest   |
| TEditBox  |   edtTest   |
|   TForm   |  frmTrest   |
|  TLabel   |   lblTest   |
|  TImage   |   imgTest   |
|  TButton  |   btnTest   |
| TSpinEdit |   spnTest   |

## Assignment
![](@attachment/Clipboard_2023-06-07-12-25-45.png)

[[@pagebreak]]

## Rules

### Semicolon
Every statement should end with a **semicolon** - (```;```). 

Example
```pascal
lblHelloWorld.Caption := 'Hello, Delphi!';
```

### Comments
Comments (which are ignored by Delphi) can be added to the code by starting the comment with two forward slashes (```//```).
Comments are used to explain code.

Example:
```pascal
btnChange.Width := 25; // This will change the width of the button.
```

### Begin & End
The ‘begin’ and ‘end;’ keywords are used to group multiple lines of code together.
Generally, for every begin, there must be an end.
```pascal
begin
	btnChange.Width := 25;
	btnChange.Height := 50;
end;
```

### The Final ‘end.’ 
the final end statement in a program must end with a full stop - (```.```).

Example:
```pascal
unit u_basicCalculator;
begin
	btnChange.Height := 50;
end;
end.
```

### Objects Properties
An object’s properties or methods are referenced using dot notation after the object’s name.

Example:
```pascal
lblHelloWorld.Caption := 'Hello, Delphi!';
```

### Variables
Delphi’s variables or objects are not case-sensitive, so “lblText” is the same as “LBLTEXT” or “lbltext".

Example:
```pascal
LBLHelloWorld.Caption := 'Hello, Delphi!';
```

[[@pagebreak]]

## Variables

### Syntax

| Variable | Name Scheme |   Example    |
| :------: | :---------: | :----------: |
|  String  |    sTest    |   'Hello'    |
| Integer  |    iTest    |     9000     |
| Boolean  |    bTest    | True \ False |
|   Real   |    rTest    |    420.69    |
|   Date   |    dTest    |  2023/06/06  |
|   Time   |    tTest    |    16:00     |

### Global Vars
- A variable must first be declared before it can be used in a program. However, 
where it is declared in a program, determines its scope. 
- Variables declared in an event handler are only created in the computer’s memory at the start of the event, and only exist as long as the event is being executed. 
- These variables cease to exist once the event has terminated. We call these variables local variables, because they cannot be accessed from another event – that is, they have a local scope.
- If a variable needs to be accessed from more than one event handler, it must be 
declared outside of the event handlers in the VAR section at the top of the 
program. 
- We say that these variables have global scope. For example, the 
variable iCount in the code snippet below is declared globally. This means it can 
be accessed and changed from any event handler in the program.
```pascal
...
type
 TForm1 			= class(TForm)
 btnShow 			: TButton;
 lblMessage 	: TLabel;
 edtName 			: TEdit;
 lblShoutOut 	: TLabel;
 lblOut 			: TLabel;

 procedure btnShowClick(Sender : TObject);
 private
 { Private declarations }
 public
 { Public declarations }
 end;

var
 Form1 	: TForm1;
 iCount :	Integer; //globsl variable

implementation
...
```

[[@pagebreak]]

## Components

### Properties

The table below shows a few of the most useful properties that you can use for Delphi components:

| NAME       | DESCRIPTION                                                                                          |
| ---------- | ---------------------------------------------------------------------------------------------------- |
| Name       | Sets the name of the component                                                                       |
| Caption    | Sets the text shown by several different components (including labels, buttons, textboxes and forms) |
| Text       | Sets or reads the text entered into a textbox (or TEdit) component                                   |
| Picture    | Sets or reads the picture shown by image components                                                  |
| Height     | Takes a number value that sets the height of the object                                              |
| Width      | Takes a number value that sets the width of the object                                               |
| Font.Size  | Takes a number value that sets the size of the font                                                  |
| Font.Color | Sets the colour of the text                                                                          |

[[@pagebreak]]

## Hotkeys
- ```CTRL``` + ```SPACEBAR``` = Code Pallet
- ```CTRL``` + ```SHIFT``` + ```S``` = Save All

[[@pagebreak]]

## Operators

### Math Operators:
| NAME             | SYMBOL | DESCRIPTION                                                           | EXAMPLE                                   | Note                                                                                |
| ---------------- | ------ | --------------------------------------------------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------- |
| Addition         | +      | Adds two values                                                       | iTotal := 2 + 1; // iTotal = 3            |                                                                                     |
| Subtraction      | -      | Subtracts the second value from the first                             | iTotal := 5 – 3; // iTotal = 2            |                                                                                     |
| Multiplication   | *      | Multiplies two values                                                 | iTotal := 2 * 4; // iTotal = 8            |                                                                                     |
| Real division    | /      | Divides the first value by the second.                                | rTotal := 10 / 4; // rTotal = 2.5         |                                                                                     |
| Integer division | div    | Divides the first number by the second, then discards the remainder   | iResult := 10 div 3; // iResult = 3       | This can only be used with integer values and the result is always an integer value |
| Modulus          | mod    | Divides the first number by the second, then keeps only the remainder | iRemainder := 10 mod 3; // iRemainder = 1 | This can only be used with integer values and the result is always an integer value |

### Comparison Operators

| COMPARISON | MEANING             |
| :--------: | ------------------- |
|     =      | Equals              |
|     <>     | Not equals to       |
|     <      | Smaller than        |
|     <=     | Smaller or equal to |
|     >      | Greater than        |
|     >=     | Greater of equal to |

### Logical Operator
| COMPARISON | MEANING                                              | Format                        |
| :--------: | ---------------------------------------------------- | ----------------------------- |
|    AND     | The AND operator is used to test two conditions      | (condition1) AND (condition2) |
|     OR     | The OR operator is used to test two conditions       | (condition1) OR (condition2)  |
|    NOT     | The NOT operator negates the result of the condition | NOT(condition)                |


[[@pagebreak]]

## Math Functions
- SQR
	```pascal
	rSquare := Sqr(4); // rSquare = 16
	rSquare := Sqr(1.6); //rSquare = 2.56
	```
- SQRT
	```pascal
	rRoot := Sqrt(16); // rRoot = 4.0
	rVal := Sqrt(6.4009) ; // rVal=2.53
	```
- ROUND
	```pascal
	iAns := Round(2.4); // iAns = 2
	iAns := Round(7.52); // iAns = 8
	iAns := Round(8.52); // iAns = 9;
	iAns := Round(8.5); // iAns = 8
	```
- TRUNC
	```pascal
	iTrunc := Trunc(2.999); // iTrunc = 2
	iTrunc := Trunc(2.4); // iTrunc = 2
	iTrunc := Trunc (7.5); // iTrunc = 7	
	```
- RANDOM
	```pascal
	rRan := random; //the result is any random real number in the range 0 to less than 1
	iRandom := Random(21) //the result is an Integer number in the range 0 to 20
	iRandom := Random(51)+5 //the result is an Integer number in the range 5 to 55
	```

[[@pagebreak]]

## Comments
```pascal
{Comnent 1}

// Comment 2

{
Muilti Line Comment
Line 2
}

```
Example Use Case:

```pascal
// ToDo: Combine all the Edits Text to the memo on each line
procedure TForm1.Button1Click(Sender: TObject);
Var
{Str} sLine, sName, sTel : String;
{Int} iAge : Int;

begin
	//Assign Vars
	{Strings}
	sName := edtName.Text;
	sTel 	:= edtTel.Text;
	{Ints}
	iAge := StrToInt(edtAge.Text);

	//Process Vars
	sLine := 'Name: ' + sName + sLineBreak + 'Tel: ' + sTel +slineBreak+ 'Age: ' IntToStr(iAge);
  
	//Output Vars
  memOutput.Lines.Append( 'Test' + slineBreak + 'Test 2' );

end;//EOButtonClick
```

[[@pagebreak]]

## String Manipulation

### Line Break
```sLineBreak```

When breaking a String into a next line to create paragraphs:
Code:
```delphi

memOutput.Lines.Append( 'Test' + slineBreak + 'Test 2' ); 

```
Output:
```
Test
Test 2
```

### Convert to String

| Type          | Example             | Result |
| ------------- | ------------------- | ------ |
| **IntToStr**  | IntToStr(_100_)     | 100    |
| **BoolToStr** | BoolToStr(_False_)  | 0      |
| **RealToStr** | RealToStr(_100.25_) | 100.25 |

[[@pagebreak]]

## If Satements

## If
```pascal
If <condition> THEN 
begin
	<statement1>;
 	…
	<statement4>;
end 
```

### If-then-else
```pascal
If <condition> THEN 
begin
	<statement1>;
 	…
	<statement4>;
end 
ELSE
begin
	<statement5>;
	<statement6>;
	…
end;
```

## Output

### Message Box
Best testing tool
```ShowMessage(String)```

Examples
```pascal
ShowMessage('Hello, world!')
ShowMessage(sName + ' is ' + IntToStr(iAge) + ' old')
``` 
	


