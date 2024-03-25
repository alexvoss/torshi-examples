# Torshi Demos

a collection of small projects that demonstrate the use of [Torshi] (in stealth 
mode at the moment) in a BDD practice. Will be extended to show rights-driven
development and caring design. More on that later.

[Torshi]: https://github.com/alexvoss/torshi

## Choice of Python

The examples use Python and [Behave]. This is because Python code is usually
quite readable, Python is already installed on many systems and even people who
usually work in other languages often know a bit of Python.

Of course, Torshi is also written in Python but that does not mean the examples
would need to be as Torshi is language-agnostic. However, from a maintenance
point of view, it does make sense to use the same language.

[Behave]: https://github.com/behave/behave

Unfortunately, the choice means that we have to use the tooling available, which
is not in an ideal state. To be able to use the `Rule` claums, we need to use
a developer version. 

Another choice that turned out to be somewhat tricky is of VSCode as the IDE.
The Cucumber plugin 

### Use of developer version

The latest published version of Behave v1.2.6 from 2018 and it does not support
some important language constructs. In particular, it lacks support for the
"Rule" clause, which is important for the Example Mapping practice. As a
result, this example uses a developer version of Behave. The hope is that a
version 1.2.7 will be released in the not too distant future.

### Use of parameters

The examples use `{}` in step definitions, which are positional step parameters
that both Cucumber and Behave support. This helps the Cucumber extension to
recognize step definitions.

Unfortunately, the alternative of using [behave-cucumber-matcher] does not
work with the developer version of Behave, which would mean not using "Rules."
Its use also does not lead to step definitions being matched by the VSCode
extension. So, positional step parameters it is for the moment.

See this the description of [Behave and the Cucumber VSCode Extension] for
more details.

[behave-cucumber-matcher]: https://github.com/kieran-ryan/behave-cucumber-matcher
[Behave and the Cucumber VSCode Extension]: https://github.com/cucumber/vscode/issues/143
