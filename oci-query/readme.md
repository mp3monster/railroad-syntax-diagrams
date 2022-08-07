This provides the railroad diagram for the OCI SQL syntax:
```
Diagram(
Stack(
Sequence(NonTerminal('query'),OneOrMore(Terminal('<resourcetype>'), ','), NonTerminal('resources')),
Optional(Sequence (NonTerminal('where'), Group(OneOrMore(Sequence(Terminal('<fieldname>'),Choice (0, '=', '!=', '==', '!==', '=~', '>=', '>', '<=', '<'), Terminal('value')), Choice(0,'&&', '||')),'Expression'))),
Optional (Sequence(NonTerminal('return'), Choice(0,'<fieldname>', 'allAdditionalFields'))),

Optional(Sequence(NonTerminal('sorted by'), '<fieldname>')),
Optional(Sequence(NonTerminal('matching'), Terminal('<keywords>'))),
Comment('Documentation at https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return','https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return','docs','https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return'))
)
```
  
The documentartion can be found at https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return','https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return','docs','https://docs.oracle.com/en-us/iaas/Content/Search/Concepts/querysyntax.htm#return
