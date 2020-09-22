<div align="center">

## Encrypt Function


</div>

### Description

This function will return a string XORed with the key you specify, using the same function you can decrypt an encrypted string as long the key used to dencrypt it is the one that is was encrypted with.
 
### More Info
 
Text,Key

XORed String

XORed string will not display properly in an editbox or anything like that bacuase of nondisplayable charactars.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Andrew Downing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/andrew-downing.md)
**Level**          |Beginner
**User Rating**    |4.3 (13 globes from 3 users)
**Compatibility**  |Delphi 7, Delphi 6, Delphi 5, Delphi 4, Pre Delphi 4
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__7-5.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/andrew-downing-encrypt-function__7-976/archive/master.zip)





### Source Code

```
Function Encrypt(TextIn:string;Key:string):string;
Var
I,I2,Val,KeyLen: integer;
begin
KeyLen := length(Key);
I2 := 1;
 For I := 1 to length(TextIn) do Begin
 Inc(I2,1);
  If I2 > KeyLen then Begin
  I2 := 1;
  End;
 Val := (ord(TextIn[I]) XOR ord(Key[I2]));
 Result := Result + char(Val);
 End;
End;
```

