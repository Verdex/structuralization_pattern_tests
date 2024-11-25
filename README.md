Set of test cases for structuralization patterns.

* _ - wild card
* $a - capture variable
* @a - template variable
* :a - atomic (both pattern and data)
* cons( ) - structure (both pattern and data)
* [ ] - list (both pattern and data)
* [| |] - list path pattern
* {| |} - path pattern
* ^ - next pattern
* , - separator
* .and( ) - for and patterns
* .or( ) - for or patterns

basic.tests contain tests for:
* wild cards
* capture variables
* template variables
* structure matches
* path pattern matches

For basic.tests atomics will appear in data, but not patterns.  A basic structuralization pattern doesn't need to
be able to represent an atomic pattern, but in order to test matches and captures there needs to be a representation
in data for the data being pattern matched.

Predicate, MatchWith, and Exact patterns are all difficult to specify without going into implementation language details
and pattern matching specific details.  For example, some implementations may allow only structural matching and 
disallow exact data matches.