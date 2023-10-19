parser grammar ExprParser;
options { tokenVocab=ExprLexer;}

program
    : (stat | def)*  EOF
    ;

stat
    : ID '=' expr ';'
    | expr ';'
    | DECL ID '(' idec (',' idec)* ')' ARROW ID ';'
    | RETURN expr ';'
    ;

type: ID ;
idec: ID COL type ;
def : DEF ID '(' idec (',' idec)* ')' ARROW ID '{' stat* '}' ;

expr: ID
    | INT
    | func
    | NOT expr
    | expr AND expr
    | expr OR expr
    | expr MULT expr
    | expr DIV expr
    | expr PLUS expr
    | expr SUB expr
    | expr ARROW '(' expr ')'
    | '(' expr ')'
    |
    
    ;

func :  ID '(' expr (',' expr)* ')' ;
