#JMESPath

The code view of the Railroad syntax:

'Diagram(
  'Expression = ',Choice(2,
Group('@', 'current-node'),
Group('literal', 'literal'),
Group(NonTerminal('Identifier'), 'identifier'),
Group(Sequence('[',OneOrMore(NonTerminal('Expression'),','), ']'), 'multi-select-list'),
Group(Sequence('{',OneOrMore(Sequence(NonTerminal('Identifier'), ':', NonTerminal('Expression')), ','),'}'), 'multi-select-hash'),
Group(Sequence(NonTerminal('Expression'), Choice(0, '>', '>=', '<', '<=', '==', '!='), NonTerminal('Expression')), 'comparator-expression'),
Group(Sequence('!', NonTerminal('Expression')), 'not-expression'),
Group(Sequence(NonTerminal('Expression'), '||', NonTerminal('Expression')), 'or-expression'),
Group(Sequence(NonTerminal('Expression'), '&&', NonTerminal('Expression')), 'and-expression'),
Group(Sequence(NonTerminal('Expression'), '|', NonTerminal('Expression')), 'pipe-expression'),
Group(Sequence('(', NonTerminal('Expression'), ')'), 'paranthesis-expression'),

Group(  Sequence(Group(Choice(0,'avg','function-name'),'available functions'),
'(', ZeroOrMore(Group(Choice(0,NonTerminal('Expression'), Sequence('&', NonTerminal('Expression')), '@'),'Function Parameter options'), ','),')',),'function-expression'),

Group(Sequence(NonTerminal('Expression'), '[', Choice(0, '*','[]',Sequence('?', NonTerminal('Expression')), 'number', Group(Sequence(Optional('number'), ':','number'),'slice-expression')),']'), 'index-expression'),

Group(Sequence(NonTerminal('Expression'), '.', Choice(0, NonTerminal('Identifier'), Group(Sequence('[',OneOrMore(NonTerminal('Expression'),','), ']'), 'multi-select-list'), Group(Sequence('{',OneOrMore(Sequence(NonTerminal('Identifier'), ':', NonTerminal('Expression')), ','),'}'), 'multi-select-hash'), Group(  Sequence(Group('function-name','see available functions'),
'(', ZeroOrMore(Group(Choice(0,NonTerminal('Expression'), Sequence('&', NonTerminal('Expression')), '@'),'Function Parameter options'), ','),')',),'function-expression'), '*')), 'sub-expression'),

)
  )
'

As a URL: https://tabatkins.github.io/railroad-diagrams/generator.html#Diagram(%0A%20%20'Expression%20%3D%20'%2CChoice(2%2C%0AGroup('%40'%2C%20'current-node')%2C%0AGroup('literal'%2C%20'literal')%2C%0AGroup(NonTerminal('Identifier')%2C%20'identifier')%2C%0AGroup(Sequence('%5B'%2COneOrMore(NonTerminal('Expression')%2C'%2C')%2C%20'%5D')%2C%20'multi-select-list')%2C%0AGroup(Sequence('%7B'%2COneOrMore(Sequence(NonTerminal('Identifier')%2C%20'%3A'%2C%20NonTerminal('Expression'))%2C%20'%2C')%2C'%7D')%2C%20'multi-select-hash')%2C%0AGroup(Sequence(NonTerminal('Expression')%2C%20Choice(0%2C%20'%3E'%2C%20'%3E%3D'%2C%20'%3C'%2C%20'%3C%3D'%2C%20'%3D%3D'%2C%20'!%3D')%2C%20NonTerminal('Expression'))%2C%20'comparator-expression')%2C%0AGroup(Sequence('!'%2C%20NonTerminal('Expression'))%2C%20'not-expression')%2C%0AGroup(Sequence(NonTerminal('Expression')%2C%20'%7C%7C'%2C%20NonTerminal('Expression'))%2C%20'or-expression')%2C%0AGroup(Sequence(NonTerminal('Expression')%2C%20'%26%26'%2C%20NonTerminal('Expression'))%2C%20'and-expression')%2C%0AGroup(Sequence(NonTerminal('Expression')%2C%20'%7C'%2C%20NonTerminal('Expression'))%2C%20'pipe-expression')%2C%0AGroup(Sequence('('%2C%20NonTerminal('Expression')%2C%20')')%2C%20'paranthesis-expression')%2C%0A%0AGroup(%20%20Sequence(Group(Choice(0%2C'avg'%2C'function-name')%2C'available%20functions')%2C%0A'('%2C%20ZeroOrMore(Group(Choice(0%2CNonTerminal('Expression')%2C%20Sequence('%26'%2C%20NonTerminal('Expression'))%2C%20'%40')%2C'Function%20Parameter%20options')%2C%20'%2C')%2C')'%2C)%2C'function-expression')%2C%0A%0AGroup(Sequence(NonTerminal('Expression')%2C%20'%5B'%2C%20Choice(0%2C%20'*'%2C'%5B%5D'%2CSequence('%3F'%2C%20NonTerminal('Expression'))%2C%20'number'%2C%20Group(Sequence(Optional('number')%2C%20'%3A'%2C'number')%2C'slice-expression'))%2C'%5D')%2C%20'index-expression')%2C%0A%0AGroup(Sequence(NonTerminal('Expression')%2C%20'.'%2C%20Choice(0%2C%20NonTerminal('Identifier')%2C%20Group(Sequence('%5B'%2COneOrMore(NonTerminal('Expression')%2C'%2C')%2C%20'%5D')%2C%20'multi-select-list')%2C%20Group(Sequence('%7B'%2COneOrMore(Sequence(NonTerminal('Identifier')%2C%20'%3A'%2C%20NonTerminal('Expression'))%2C%20'%2C')%2C'%7D')%2C%20'multi-select-hash')%2C%20Group(%20%20Sequence(Group('function-name'%2C'see%20available%20functions')%2C%0A'('%2C%20ZeroOrMore(Group(Choice(0%2CNonTerminal('Expression')%2C%20Sequence('%26'%2C%20NonTerminal('Expression'))%2C%20'%40')%2C'Function%20Parameter%20options')%2C%20'%2C')%2C')'%2C)%2C'function-expression')%2C%20'*'))%2C%20'sub-expression')%2C%0A%0A)%0A%20%20)%0A
