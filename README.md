## pegex

Pegular expressions, aka Pegex, formally "regular PEGs".
Possessive regular expressions using prefix operators.
Like regular expressions but prefix notation and possessive behaviour.
In C(++)

## Operators
<dl>
<dt> ^ </dt>		<dd> start of the input or start of any line </dd>
<dt> $ </dt>		<dd> end of the input or the end of any line </dd>
<dt> . </dt>		<dd> any character, including a newline </dd>
<dt> ? </dt>		<dd> Zero or one of the following expression </dd>
<dt> * </dt>		<dd> Zero or more of the following expression </dd>
<dt> + </dt>		<dd> One or more of the following expression </dd>
<dt> (expr) </dt>	<dd> Group subexpressions (does not imply capture) </dd>
<dt> |A|B... </dt>	<dd> Either A or B (or ...) </dd>
<dt> &A </dt>		<dd> Continue only if A succeeds </dd>
<dt> !A </dt>		<dd> Continue only if A fails </dd>
<dt> anychar </dt>	<dd> match that non-operator character </dd>
<dt> \char </dt>	<dd> match the escaped character (including any operator, \0 \b \e \f \n \r \t, and any other char) </dd>
<dt> \177 </dt>		<dd> match the specified octal character </dd>
<dt> \xXX </dt>		<dd> match the specified hexadecimal (0-9a-fA-F) </dd>
<dt> \x{1-2} </dt>	<dd> match the specified hexadecimal (0-9a-fA-F) </dd>
<dt> \u12345 </dt>	<dd> match the specified 1-5 digit Unicode character (only if compiled for Unicode support) </dd>
<dt> \u{1-5} </dt>	<dd> match the specified 1-5 digit Unicode character (only if compiled for Unicode support) </dd>
<dt> [a-z] </dt>	<dd> Normal character class (a literal hyphen may occur at start) </dd>
<dt> [^a-z] </dt>	<dd> Negated character class. Characters may include the \escapes listed above </dd>
</dl>

## NOT YET IMPLEMENTED:
<dl>
<dt> {n,m} </dt>	<dd> match from n (default 0) to m (default unlimited) repetitions of the following expression. </dd>
<dt> &lt;name%gt; </dt>	<dd> Call the callout function passing the specified name. </dd>
<dt> Captures. </dt>

## Note:
Possessive alternates and possessive repetition will never backtrack.
Once an alternate has matched, no subsequent alterative will be tried in that group.
Once a repetition has been made, it will never be unwound.
It is your responsibility to ensure these possessive operators never match unless it's final.
You should use negative assertions to control inappropriate greed.

## Example

## LICENSE

The MIT License. See the LICENSE file for details.
