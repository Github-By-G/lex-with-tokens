# lex-by-

##print tokens for input strings 


%{
  #include<stdio.h>  
%}
letter [A-Z, a-z]
digit [0-9]
id {letter}({letter}{digit})*
%%
{id} {printf("ID ");}
[0-9]* {printf("NUM ");}
"if" {printf("IF ");}
"else" {printf("ELSE ");}
"while" {printf("WHILE ");}
"&lt;" {printf("RELOP ");}
"&gt;" {printf("RELOP ");}
"(" {printf("BRACKET ");}
")" {printf("BRACKET ");}
%%

int main(void)
{
yylex();
return 0;
}
int yywrap()
{
}
