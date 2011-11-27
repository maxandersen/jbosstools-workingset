JBoss Tools Working Sets
========================

Implementation that provides automatic grouping of projects into workingsets based on regular expressions.

From original jira issue on this: https://issues.jboss.org/browse/JBIDE-4483

This adds a crude preference page which allow you to specify a list of patterns that will be used in sequence as follows:

<searchpattern>, <replacepattern>, <exclusive: true|false>

searchpattern is a regular expression used to match against the project names, (i.e. org\.jboss\.tools\.([^\.]+).* finds all projects starting with org.jboss.tools and puts the text between the next two dots into the first capture group)

replacepattern: which set the project should go into, can use capture groups. (i.e. "$1", will for org.jboss.tools.vpe.util and the pattern from above be: "vpe")

exlusive: wether or not we should stop searching for more names. i.e. useful to set to false for some overall grouping patterns, but you most likely just want it to be true.

History
=======
 
2011-11-27: Import from JBoss Tools into github (no history kept)

2009: Initial implementation