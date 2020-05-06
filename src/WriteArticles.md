
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Final//EN">
<html>
<head>
<title>Writing Systems and Networking Articles</title>
<meta name="author" content="Henning Schulzrinne">
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<style> 
.pts:before {content: "["}
.pts:after {content: "] "}
.pts {
  color: #9900CC;
  font-weight: bold
}
 

a:link {text-decoration: none}
a:visited {text-decoration: none}
a:hover {text-decoration: underline; color:#888}

blockquote { 
  background-color: #ccffcc;
}

.notice {
  background: #fff6bf url(exclamation.png) center no-repeat;
  background-position: 15px 50%; /* x-pos y-pos */
  text-align: left;
  padding: 5px 20px 5px 45px;
  border-top: 2px solid #ffd324;
  border-bottom: 2px solid #ffd324;
}

tr:nth-child(odd)       { background-color:#eee; }
tr:nth-child(even)      { background-color:#fff; }

tr.odd {background-color: #cccccc}
tr.even {background-color: #eeeeee}
.heading {
  font-size: 110%;
  font-weight: bold; 
  background-color: #336699;
  color: white;
}
</style>
</head>
<body bgcolor=white>

<h1>Writing Technical Articles</h1>

<p>The notes below apply to technical papers in computer science and
electrical engineering, with emphasis on papers in systems and networks.

<p>Read Strunk and White, <i><a
href="http://www.bartleby.com/141/index.html">Elements of Style</a></i>.
Again.</p>

<p>Give the paper to somebody else to read. If you can, find two people:
one person familiar with the technical matter, another only generally
familiar with the area.</p>

<p>Papers can be divided roughly into two categories, namely original
research papers and survey papers. There are papers that combine the two
elements, but most publication venues either only accept one or the
other type or require the author to identify whether the paper should be
evaluated as a research contribution or a survey paper. (Most research
papers contain a "related work" section that can be considered a survey,
but it is usually brief compared to the rest of the paper and only
addresses a much narrower slice of the field.)</p>

<h2>Research Papers</h2>

<p>A good research paper has a clear statement of the problem the paper
is addressing, the proposed solution(s), and results achieved.  It
describes clearly what has been done before on the problem, and what is
new.</p>

<p>The goal of a paper is to describe novel technical results. There are
four types of technical results:
<ol>
<li>An algorithm;

<li>A system construct:  such as hardware design, software system,
protocol, etc.;
<blockquote>
One goal of the paper is to ensure that the next person who designs
a system like yours doesn't make the same mistakes and takes advantage
of some of your best solutions.  So make sure that the hard problems
(and their solutions) are discussed and the non-obvious mistakes (and
how to avoid them) are discussed. (Craig Partridge)
</blockquote>

<li>A performance evaluation: obtained through analyses, simulation or
measurements;

<li>A theory: consisting of a collection of theorems.
</ol>

A paper should focus on 
<ul>
<li>describing the results in sufficient details to establish their
validity;

<li>identifying the novel aspects of the results, i.e., what new knowledge is
reported and what makes
it non-obvious;

<li>identifying the significance of the results: what improvements and
impact do they suggest.
</ul>

<h2>Paper Structure</h2>

<ul>
<li>Typical outline of a paper is:

<ul>
<li>Abstract, typically not more than 100-150 words;

<li><a href="intro-style.html">Introduction</a> (brief!):  introduce
problem, outline solution; the statement of the problem should include a
clear statement why the problem is important (or interesting).

<li>Related Work (or before summary).  Hint:  In the case of a
conference, make sure to cite the work of the PC co-chairs and as many
other PC members as are remotely plausible, as well as from anything
relevant from the previous two proceedings.  In the case of a journal or
magazine, cite anything relevant from last 2-3 years or so volumes.

<li>Outline of the rest of the paper:  "The remainder of the paper is
organized as follows.  In Section 2, we introduce ..Section 3 describes
...  Finally, we describe future work in Section 5." [Note that Section
is capitalized.  Also, vary your expression between "section" being the
subject of the sentence, as in "Section 2 discusses ..." and "In
Section, we discuss ...".]

<li>Body of paper
<ul>
<li>problem
<li>approach, architecture
<li>results
</ul>

<p>The body should contain sufficient motivation, with at least one
example scenario, preferably two, with illustrating figures, followed by
a crisp generic problem statement model, i.e., functionality,
particularly emphasizing "new" functionality.  The paper may or may not
include formalisms. General evaluations of your algorithm or
architecture, e.g., material proving that the algorithm is O(log N), go
here, not in the evaluation section.</p>

<p><i>Architecture</i> of proposed system(s) to achieve this model
should be more generic than your own peculiar implementation.  Always
include at least one figure.</p>

<p><i>Realization</i>:  contains actual implementation details when
implementing architecture isn't totally straightforward.  Mention
briefly implementation language, platform, location, dependencies on
other packages and minimum resource usage if pertinent.</p>

<p><i>Evaluation</i>:  How does it really work in practice?  Provide
real or simulated performance metrics, end-user studies, mention
external technology adoptors, if any, etc.</p>

<li>Related work, if not covered at the beginning.</li>

<li>Summary and Future Work
<ul>
<li>often repeats the main result
</ul>
<li>Acknowledgements
<li>Bibliography
  
<li>Appendix (to be cut first if forced to):
<ul>
<li>detailed protocol descriptions
<li>proofs with more than two lines
<li>other low-level but important details
</ul>
</ul>
</ul>

<p>It is recommended that you write the approach and results sections
first, which go together.  Then problem section, if it is separate from
the introduction.  Then the conclusions, then the intro.  Write the
intro last since it glosses the conclusions in one of the last
paragraphs.  Finally, write the abstract.  Last, give your paper a
title.

<h2>Title</h2>

<ul>
<li>Avoid all but the most readily understood abbreviations.

<li>Avoid common phrases like "novel", "performance evaluation" and
"architecture", since almost every paper does a performance evaluation
of some architecture and it better be novel.  Unless somebody wants to
see 10,000 Google results, nobody searches for these types of words.

<p>Use adjectives that describe the distinctive features of your work,
e.g., reliable, scalable, high-performance, robust, low-complexity, or
low-cost.  (There are obviously exceptions, e.g., when the performance
evaluation is the core of the paper.  Even in that case, something more
specific is preferable, as in "Delay measurements of X" or "The quality
of service for FedEx deliveries".)

<li>If you need inspiration for a paper title, you can <a
href="http://www.cs.ucsd.edu/users/braghava/systems-topic-generator.html">consult</a>
the <i>Automatic Systems Research Topic or Paper Title Generator</i>.

</ul>

<h2>Authors</h2>

<li>The IEEE policies (Section 6.4.1) used to state the following about authorship:
<blockquote>
The IEEE affirms that authorship credit must be reserved for individuals
who have met each of the following conditions: 1) made a significant
intellectual contribution to the theoretical development, system or
experimental design, prototype development, and/or the analysis and
interpretation of data associated with the work contained in the
manuscript, 2) contributed to drafting the article or reviewing and/or
revising it for intellectual content, and 3) approved the final version
of the manuscript, including references.
</blockquote>

<p>This has now moved to the <a
href="http://www.ieee.org/portal/cms_docs_iportals/iportals/publications/PSPB/opsmanual.pdf">IEEE
PSPB Operations Manual</a>, Section 8.2.1.

<h2>Abstract</h2>

<ul>
<li>The abstract must <b>not</b> contain references, as it may be used
without the main article. It is acceptable, although not common, to
identify work by author, abbreviation or RFC number. (For example, "Our
algorithm is based upon the work by Smith and Wesson.")

<li>Avoid use of "in this paper" in the abstract. What other paper would
you be talking about here?

<li>Avoid general motivation in the abstract. You do not have to justify
the importance of the Internet or explain what QoS is.

<li>Highlight not just the problem, but also the principal results. Many
people read abstracts and then decide whether to bother with the rest of
the paper. 

<li>Since the abstract will be used by search engines, be sure that
terms that identify your work are found there. In particular, the name
of any protocol or system developed and the general area ("quality of
service", "protocol verification", "service creation environment")
should be contained in the abstract.

<li>Avoid equations and math. Exceptions: Your paper proposes 
<i>E = m c <sup>2</sup></i>.
</ul>

<h2>Introduction</h2>

<ul>
<li>Avoid stock and cliche phrases such as "recent advances in XYZ" or
anything alluding to the growth of the Internet.

<li>Be sure that the introduction lets the reader know what this paper
is about, not just how important your general area of research is.
Readers won't stick with you for three pages to find out what you are
talking about.

<li>The introduction must motivate your work by pinpointing the problem
you are addressing and then give an overview of your approach and/or
contributions (and perhaps even a general description of your results). 
In this way, the intro sets up my expectations for the rest of your
paper -- it provides the context, and a preview.

<li>Repeating the abstract in the introduction is a waste of space.

<li>Example bad introduction:
<small>
<blockquote>
<p>Here at the institute for computer research, me and my colleagues
have created the SUPERGP system and have applied it to several toy
problems.  We had previously fumbled with earlier versions of
SUPERGPSYSTEM for a while.  This system allows the programmer to easily
try lots of parameters, and problems, but incorporates a special
constraint system for parameter settings and LISP S-expression
parenthesis counting.

<p>The search space of GP is large and many things we are thinking about
putting into the supergpsystem will make this space much more colorful.

</blockquote>
</small>

<li>A pretty good introduction, drawn from Eric Siegel's class:

<blockquote>
<p>Many new domains for genetic programming require evolved programs to
be executed for longer amounts of time.  For example, it is beneficial
to give evolved programs direct access to low-level data arrays, as in
some approaches to signal processing \cite{teller5}, and protein segment
classification \cite{handley,koza6}.  This type of system automatically
performs more problem-specific engineering than a system that accesses
highly preprocessed data.  However, evolved programs may require more
time to execute, since they are solving a harder task.

<dl>
<dt><b>Previous or obvious approach</b>:  
<dd>(Note that you can also have a
related work section that gives more details about previous work.)) One
way to control the execution time of evolved programs is to impose an
absolute time limit.  However, this is too constraining if some test
cases require more processing time than others.  To use computation time
efficiently, evolved programs must take extra time when it is necessary
to perform well, but also spend less time whenever possible.

<dt><b>Approach/solution/contribution</b>:  
<dd>The first sentence of a
paragraph like this should say what the contribution is.  Also gloss the
results.

<p>In this chapter, we introduce a method that gives evolved programs the
incentive to strategically allocate computation time among fitness
cases.  Specifically, with an <i>aggregate computation time ceiling</i>
imposed over a series of fitness cases, evolved programs dynamically
choose when to stop processing each fitness case.  We present
experiments that show that programs evolved using this form of fitness
take less time per test case on average, with minimal damage to domain
performance.  We also discuss the implications of such a time
constraint, as well as its differences from other approaches to {\it
multiobjective problems}.  The dynamic use of resources other than
computation time, e.g.,  memory or fuel, may also result from placing an
aggregate limit over a series of fitness cases.

<p><dt><b>Overview:</b>
<dd>The following section surveys related work in both optimizing the
execution time of evolved programs and evolution over Turing-complete
representations.  Next we introduce the game Tetris as a test problem. 
This is followed by a description of the aggregate computation time
ceiling, and its application to Tetris in particular.  We then present
experimental results, discuss other current efforts with Tetris, and end
with conclusions and future work.
</dl>
</blockquote>
</ul>

<h2>Body of Paper</h2>

<p><a href="writing-bugs.html">Hints and common mistakes</a></p>

<h2>Bibliography</h2>

<ul>
<li>Avoid use of <i>et al.</i> in a bibliography unless list is very long
(five or more authors). The author subsumed into <i>et al.</i> may be
your advisor or the reviewer... Note punctuation of <i>et al.</i>.</li>

<li>If writing about networks or multimedia, use the <a
href="/~hgs/netbib">network bibliography</a>.  All entries not found
there should be sent to me. A listing of frequently-used references for <a
href="/~hgs/netbib/std.html">networks</a> is available.</li>

<li>Internet drafts must be marked "work in progress". Make sure that
they have been replaced by newer versions or RFCs. Any Internet Draft
reference older than six months should automatically be suspicious since
Internet Drafts expire after that time period.</li>

<li>Book citations include publication years, but no ISBN number.</li>

<li>It is now acceptable to <a href="urls.html">include URLs</a> to
material, but it is probably bad form to include a URL pointing to the
author's web page for papers published in IEEE and ACM publications,
given the copyright situation.  Use it for software and other
non-library material.  Avoid long URLs; it may be sufficient to point to
the general page and let the reader find the material.  General URLs are
also less likely to change.</p>

<li>Leave a space between first names and last name, i.e., "J. P. Doe",
not "J.P.Doe".</p>

<li>References such as 
<pre>
John Doe, "Some paper on something", technical report.
</pre>
are useless. Cite the source, date and other identifying information.</p>

<li>For conference papers, you MUST name the conference location, month
and the full conference name, not just some abbreviation. Page numbers
are nice, but optional. All of this information is readily available via
the IEEE or ACM digital libraries.</p>

<li>Check if Internet drafts have been published as RFCs or if there's a
newer version.</p>

<li>Having a citation</p>

<p><pre>
Jane Doe, "Some random paper", to be published, 2003.
</pre>
</p>

<p>is useless, as the paper has presumably been published by now. Google or
the ACM or IEEE digital libraries will help you find it.</p>

</ul>

<h2>Acknowledgements</h2>

<ul>
<li>Acknowledge your funding sources.  Some sources have specific
wording requirements and may prefer that the grant number is listed. 
The NSF requires text like "This work was supported by the National
Science Foundation under grant EIA NN-NNNNN."</li>

<li>Generally, anonymous reviewers don't get acknowledged, unless they
really provided an exceptional level of feedback or insight. Rather than
"We thank X for helping us with Y", you might vary this as "X helped
with Y.". </li>
</ul>

</ul>

<h2>Reporting Numerical Results and Simulations</h2>

<p>In all but extended abstracts, numerical results and simulations
should be reported in enough detail that the reader can duplicate the
results.  This should include all parameters used, indications of the
number of samples that contributed to the analysis and any initial
conditions, if relevant.</p>

<p>When presenting simulation results, provide insight into the
statistical confidence.  If at all possible, provide confidence
intervals.  If there's a "strange" behavior in the graph (e.g., a dip,
peak or change in slope), this behavior either needs to be explained or
reasons must be given why this is simply due to statistical aberration. 
In the latter case, gathering more samples is probably advised.</p>

<p>Figures should be chosen wisely. You can never lay out the whole
parameter space, so provide insight into which parameters are
significant over what range and which ones are less important. It's not
very entertaining to present lots of flat or linear lines.</p>

<p>The figure and table captions should contain enough context so that a
reader can understand the content of the figure or table without having
to refer to the text. Any labels or uncommon abbreviations need to be
explained in the figure or table caption.</p>

<p>The description of the graph should not just repeat the graphically
obvious such as "the delay rises with the load", but explain, for
example, how this increase relates to the load increase.  Is it linear? 
Does it follow some well-known other system behaviors such as standard
queueing systems?</p>

<h2>LaTeX Considerations</h2>
<ul>
<li>There's no need to enclose numbers in $$ (math mode).</li>

<li>Use <tt>\cite{a,b,c}</tt>, not <tt>\cite{a} \cite{b} \cite{c}</tt>.</li>

<li>Use the <tt>\usepackage{times}</tt> option for LaTeX2e - it comes
out much nicer on printers with different resolutions.  Plus, compared
to cmr, it probably squeezes an extra 10% of text out of your conference
allotment.</li>

<li>Non-index (or descriptive) subscripts are set in roman,
not italic. For example, 
<pre>
x_i
x_{\mathit index}
x_{\mathrm max}
x_{\mathrm f}
</pre>
<p>In the examples above, the index <i>i</i> or <i>index</i> is
substituted or instantiated by numbers, such as <i>x</i><sub>1</sub>,
<i>x</i><sub>2</sub>.</p></li>

<li>Multi-letter variable names should be surrounded by
<pre>\mathit</pre>, not $$, as otherwise the spacing will be wrong.</li>

<li>For uniformity, use the LaTeX2e graphics set, not the earlier
psfigure set:
<pre>
\usepackage{graphics}
...
\begin{figure}
\resizebox{!}{0.5\textheight}{\includegraphics{foo.eps}}
\caption{Some figure}
\label{fig:figure}
\end{figure}
</pre>
</li>
</ul>

<h2>Things to Avoid</h2>

<dl>
<dt>Too much motivational material</dt>
<dd>Three reasons are enough -- and they should be described very
briefly.</dd>

<dt>Describing the obvious parts of the result</dt>
<dd>"Obvious" is defined as any result that a graduate of our program
would suggest as a solution if you pose the problem that the result
solves.</dd>

<dt>Describing unnecessary details</dt>
<dd>A detail is unnecessary, if its omission will not harm the reader's
ability to understand the important novel aspects of the result.</dd>

<dt>Spelling errors</dt>
<dd>With the availability of spell checkers, there is no reason to have
spelling errors in a manuscript.  If you as the author didn't take the
time to spell-check your paper, why should the editor or reviewer take
the time to read it or trust that your diligence in technical matters is
any higher than your diligence in presentation?  Note, however, that
spell checkers don't catch all common errors, in particular word
duplication ("the the").  If in doubt, consult a dictionary such as the
(on line) <a href="http://www.m-w.com">Merriam Webster</a>.</dd>

<dt>Text in Arial:</dt>
<dd>Arial and other sans-serif fonts are fine for slides
and posters, but are harder to read in continuous text. Use Times Roman
or similar serif fonts. Unusual fonts are less likely to be available at
the recipient and may cause printing or display problems. Material
mainly to be read online typically use sans serif fonts.</dd>

</dl>

<h2>Guidelines for Experimental Papers</h2>

<p>"Guidelines for Experimental Papers" set forth for researchers
submitting articles to the journal, <i>Machine Learning</i>.</p>
 
<ol>
<li>Papers that introduce a new learning "setting" or type of
application should justify the relevance and importance of this setting,
for example, based on its utility in applications, its appropriateness
as a model of human or animal learning, or its importance in addressing
fundamental questions in machine learning.</li>
 
<li>Papers describing a new algorithm should be clear, precise, and
written in a way that allows the reader to compare the algorithm to
other algorithms.  For example, most learning algorithms can be viewed
as optimizing (at least approximately) some measure of performance.  A
good way to describe a new algorithm is to make this performance measure
explicit.  Another useful way of describing an algorithm is to define
the space of hypotheses that it searches when optimizing the performance
measure.</li>
 
<li>Papers introducing a new algorithm should conduct experiments
comparing it to state-of-the-art algorithms for the same or similar
problems.  Where possible, performance should also be compared against
an absolute standard of ideal performance.  Performance should also be
compared against a naive standard (e.g., random guessing, guessing the
most common class, etc.) as well.  Unusual performance criteria should
be carefully defined and justified.</li>
 
<li>All experiments must include measures of uncertainty of the
conclusions.  These typically take the form of confidence intervals,
statistical tests, or estimates of standard error.  Proper experimental
methodology should be employed.  For example, if "test sets" are used to
measure generalization performance, no information from the test set
should be available to the learning process.</li>
 
<li>Descriptions of the software and data sufficient to replicate the
experiments must be included in the paper.  Once the paper has appeared
in Machine Learning, authors are strongly urged to make the data used in
experiments available to other scientists wishing to replicate the
experiments.  An excellent way to achieve this is to deposit the data
sets at the Irvine Repository of Machine Learning Databases.  Another
good option is to add your data sets to the DELVE benchmark collection
at the University of Toronto.  For proprietary data sets, authors are
encouraged to develop synthetic data sets having the same statistical
properties.  These synthetic data sets can then be made freely
available.</li>

<li>Conclusions drawn from a series of experimental runs should be
clearly stated.  Graphical display of experimental data can be very
effective.  Supporting tables of exact numerical results from
experiments should be provided in an appendix.</li>
 
<li>Limitations of the algorithm should be described in detail. 
Interesting cases where an algorithm fails are important in clarifying
the range of applicability of an algorithm.</li>

</ol> 

<h2>Other Hints and Notes</h2>

<p>From Bill Stewart (Slashdot, May 7, 2006), edited</p>
<blockquote>
<ul>
<li>Write like a newspaper reporter, not a grad student.</li>

<li>Your objective is clear communication to the reader, not beauty or
eruditeness or narration of your discoveries and reasoning process.
Don't waste their time, or at least don't waste it up front.</li>

<li>Hit the important conclusions in the first few sentences so your reader
will read them. If you'd like to wrap up with them at the end of your
memo, that's fine too, in case anybody's still reading by then, but
conclusions come first.</li>

<li>If you're trying to express something complex, simplify your writing so
it doesn't get in the way. For something simple, 10th grade language
structures will do, but if it's really hairy stuff, back down to 8th
grade or so.</li>

<li>Think about what your audience knows and doesn't know, and what they
want and don't want. Express things in terms of what they know and want,
not what you know.</li>
</ul>
</blockquote>

<p>From MarkusQ, Slashdot, May 7, 2006</p>
<blockquote>
<ul>
<li><b>Top down design</b> Starting with an outline and working out the
details is the normal way of tackling an engineering problem.</li>

<li><b>Checking your facts</b> Engineers should be used to checking
anything that is even remotely doubtful before committing to it.  So
should writers.</li>

<li><b>Failure mode analysis</b> For each sentence ask yourself, could
it be misread?  How?  What is the best way to fix it?</li>

<li><b>Dependency analysis</b> Are the ideas presented in an order that
assures that each point can be understood on the basis of the readers
assumed knowledge and the information provided by preceding points?</li>

<li><b>Optimization</b> Are there any unnecessary parts?  Does the
structure require the reader to remember too many details at once,
before linking them?</li>

<li><b>Structured testing</b> If you read what you have written assuming
only the knowledge that the reader can be expected to have, does each
part work the way you intended?  If you read it aloud, does it sound the
way you intended?</li>

</ul>
</blockquote>

<h2>The Conference Review Process</h2>

<p>It is hard to generalize the review process for conferences, but
most reputable conferences operate according to these basic rules:</p>

<ol>
<li>The paper is submitted to the technical program chair(s).  All
current conferences require electronic submission, in PDF, occasionally
in Word.</li>

<li>The technical program chair assigns the paper to one or more
technical program committee members, hopefully experts in their field. 
The identity of this TPC member is kept secret.</li>

<li>The TPC member usually provides a review, but may also be asked to
find between one and three reviewers who are not members of the TPC. 
They may be colleagues of the reviewer at the same institution, his or
her graduate students or somebody listed in the references. The graduate
student reviews can be quite helpful, since these reviewers often
provide more detailed criticism rather than blanket dismissal. Any good
conference will strive to provide at least three reviews, however, since
conferences operate under tight deadlines and not all reviewers deliver
as promised, it is not uncommon that you receive only two reviews.</li>

<li>In some conferences, there is an on-line discussion of papers among
the reviewers for a particular paper.  Usually, a lead TPC member drives
the discussion and then recommends the paper for acceptance, rejection
or discussion at the TPC meeting.</li>

<li>The technical program chair then collects the reviews and sorts the
papers according to their average review scores.</li> 

<li>The TPC (or, rather, the subset that can make the meeting), then
meets in person or by phone conference.  Usually, the bottom third and
the top third are rejected and accepted, respectively, without (much)
further discussion.  The papers discussed are those in the middle of the
range, or where a TPC member feels strongly that the paper ended up in the
wrong bin, or where the review scores differ significantly. Papers that
only received two reviews are also often discussed, maybe with a quick
review by one of the TPC members as additional background. The rigor of
the TPC meeting depends on the size and reputation of the conference. In
some workshops and conferences, the TPC chairs may well make the final
decision themselves, without involving the whole TPC.</li>

</ol>

<h2>Other References</h2>

<ul>
<li><a href="http://infolab.stanford.edu/~widom/paper-writing.html"><i>Tips
for Writing Technical Papers</i></a>, January 2006</li>

<li><a href="http://www.grammarcheck.net/">Grammar checker</a></li>

<li><a href="http://australianhelp.com/grammar">Links to grammar and usage guides</a></li>

<li><a href="http://www.plainlanguage.gov/"><i>Plain Language: Improving
Communication from the Federal Government to the Public</i></a> contains
a number of helpful hints for writing clear prose.</li>

<li><a
href="http://research.microsoft.com/~simonpj/papers/giving-a-talk/giving-a-talk.htm">How
to give a good research talk</a> and how to give a good research talk</li>

<li><a
href="http://blizzard.cs.uwaterloo.ca/keshav/home/Papers/data/07/paper-reading.pdf"><i>How
to read a paper</i></a>, CCR, July 2007.</li>

<li><a href="http://www.phys.unsw.edu.au/~jw/thesis.html">How to Write a
PhD Thesis</a></li>

<li><a
href="http://www-net.cs.umass.edu/kurose/talks/top_10_tips_for_writing_a_paper.ppt">Top
10 tips for writing a paper</a>, by Jim Kurose</li>

<li><a
href="http://withoutbullshit.com/blog/10-top-writing-tips-psychology/"><em>10
top writing tips and the psychology behind them</em></a> ("write
shorter", "shorten your sentences", "rewrite passive voice", "eliminate
weasel words", "replace jargon with clarity", "cite numbers
effectively", "use I, we and you", "move key insights up", "cite
examples", "give use some signposts")</li>

<li><a href="http://www.bartleby.com">Bartleby</a> has dictionaries,
grammars, an encyclopedia, and <i>Columbia Guide To Standard American
English</i></li>

<li>Dictionaries and thesaurus:
<a href="http://www.thefreedictionary.com/">The Free Dictionary</a>,
<a href="http://www.webster-dictionary.org/">Webster's (1913)</a>,
<a href="https://www.vocabulary.com/dictionary/">vocabulary.com</a>,
<a href="http://www.finedictionary.com/">Fine Dictionary</a>,
<a href="http://www.freethesaurus.com/">Thesaurus - Synonyms, Antonyms,
and Related Words</a>
</li>

<li><a href="http://www.dictionarist.com/">Dictionarist</a>:
multi-lingual dictionary</li>

<li><a href="http://en.bab.la/dictionary/">bab.la</a>: an assortment of
multilingual dictionaries</li>

<li><a
href="http://www.computer.org/portal/pages/ieeecs/publications/author/style/index.html">IEEE
<i>IEEE Computer Society</i> style guide, including hints on how to
reference Internet drafts and RFCs</li>

<li><a href="http://sc.edu/toolbox/pdfs/2011_toolbox_styleguide.pdf">USC
editorial style guide</a></li>

<li><a href="http://steyer.net/resources.html">Articles on technical communication</a></li>

<li><a href="http://istpub.berkeley.edu:4201/style/">Berkeley
Information Systems and Technology Publications</a> style guide</li>

<li><a
href="http://andromeda.rutgers.edu/~jlynch/Writing/index.html">Guide to
Grammar and Style</a>, by J. Lynch</li>

<li><a
href="http://alt-usage-english.org/fast_faq.shtml">alt.usage.english</a>
FAQ, addressing common grammar questions</li>

<li><a href="http://ucsub.colorado.edu/~robertme/paperkey.htm">Key to
common comments made on your papers</a></li>

<li><a href="http://contentselect.pearsoned.com/unit10.html">Drafting
the Paper in an Academic Style</a></li>

<li><a
href="http://www-relg-studies.scu.edu/facstaff/murphy/courses/style-sheet.htm">Religious
Studies</a> style sheet</li>

<li><a
href="http://www.cisco.com/univercd/cc/td/doc/product/wrtrres/stylegd/01style.htm">Cisco</a>
style guide</li>

<li>Oded Goldreich wrote an essay entitled <a
href="http://www.wisdom.weizmann.ac.il/~oded/writing.html"> "How not to
write a paper"</a>, with recommendations on style and organization.</li>

<li><a
href="http://www.abajournal.com/magazine/article/ax_these_terms_from_your_legal_writing/">Terms
to avoid for legal writing</a>, applies in particular to amateur
lawyers</li>

<li>Don Knuth has online the TeX source of a book on <a
href="http://www-cs-faculty.Stanford.EDU/~knuth/klr.html">"Mathematical
Writing"</a> (also useful for Computer Science).</li>

<li><a
href="http://www.cs.ucr.edu/~michalis/TECHWRITING/structure.html"><i>The
structure of paper/report in Systems</i></a>, by Michalis Faloutsos,
U.C.  Riverside</li>

<li>
<a
href="http://www.amazon.com/exec/obidos/ASIN/0205191584/ref=ed_oe_p/002-4207005-4000631">The
Elements of Style</A>. William Strunk Jr. and E.B. White. Macmillan
Publishing Co., New York, 1979.  
<blockquote>
This is an <b>amazing</b> little book that
you can read in a few hours.  Your writing style will never be the same
afterwards.  This $8 book is the best investment you can ever make.
</blockquote>

<li>"A Guide to Writing as an Engineer"

<li><i>Spring into Technical Writing for Engineers and Scientists</i>

<li><a
href="http://www.writing-skills.com/resources/news/185/top-ten-writing-tips-for-scientists"><i>Top
ten writing tips for scientists, Sciencebase.com</i></a></li> - basic
overview of how to write about science</li>

<li>
<a href="http://www.amazon.com/exec/obidos/ASIN/020137921X/qid=929133980/sr=1-1/002-4207005-4000631">Bugs
in Writing</A>.  Lyn Dupre', (2nd ed.)  
<blockquote>
This is a great book that expands on Strunk&White.  It has more
examples, and was written by an author who edited numerous technical
publications, many of which were in computer science.
</blockquote>

<li>
<a
href="http://www.amazon.com/exec/obidos/ASIN/0226103897/qid=929134146/sr=1-1/002-4207005-4000631">The
Chicago Manual of Style</A>, Univ.  of Chicago Press. <a href="http://www.chicagomanualofstyle.org/">online</a> 
<blockquote>
This is the bible for American academic style.  It's long and heavy, but
has everything you ever want to know about style.  When in doubt, or if
you get conflicting stylistic advice, following The Chicago Manual of
Style is your best choice.
</blockquote>

<li>
<a
href="http://www.amazon.com/exec/obidos/ASIN/0195069544/qid=929134195/sr=1-2/002-4207005-4000631">A
Handbook for Scholars</A> by Mary Claire van Leunen; Alfred Knopf,
Publisher.  
<blockquote>
This is another useful book written for publishing
(computer) scientists.
</blockquote>

<li>The <a href="http://www.acm.org/uist/guide.html">UIST Guide for
Authors</a> is geared towards a specific conference, but the general
process and guidelines are similar to many other conferences.</li>

<li>
<a href="http://www.amstat.org/publications/jcgs/sci.pdf"><em>The
Science of Scientific Writing</em></a>, George D.  Gopen and Judith A. 
Swan, In <i>American Scientist</i>, Vol.  78, No.  6 (Nov-Dec, 1990),
pp.  550-558.</li>

<blockquote>
This is a useful article that teaches scientists how to write
single sentences and paragraphs, such as "follow a grammatical subject
as soon as possible with its verb" and "articulate the action of every
clause or sentence in its verb".
</blockquote>

<li><em><a
href="http://chronicle.com/article/Why-Academics-Writing-Stinks/148989/">Why
Academics Stink at Writing</a></em>
<blockquote>
Mostly discusses non-technical writing, but many of the points apply.
</blockquote>
</li>

<li><em>The Mayfield Handbook of Technical and Scientific Writing</em>,
Perelman, Paradis and Barrett, Mayfield, 1998.
<blockquote>
It is an extensive resource explaining how to write papers, reports,
memoranda and Ph.D.  thesis, how to make high-performance slides and
oral presentations, how to avoid common pitfalls and mistakes in
English, etc., with many examples of "good" and "bad" practices.
</blockquote>

<li>Roy Levin and David D. Redell,
<a href="http://www.usenix.org/events/samples/submit/advice.html">
An evaluation of the ninth SOSP submissions -or- How (and how not) to write
a good systems paper</a>, <em>ACM SIGOPS Operating Systems Review</em>
<b>17</b>(3):35-40 (July, 1983).</li>

<li>Alan Snyder,
<a href="http://www.acm.org/sigplan/oopsla/oopsla96/how91.html">
How to get your paper accepted at OOPSLA</A>, <em>OOPSLA '91
Proceedings</em>, pp. 359-363.</li>

<li>Mark Allman, <a href="http://www.icir.org/mallman/plea.txt">A
Referee's Plea</a>, 2001</li>

<li>Arnaud Legout, <a
href="http://cel.archives-ouvertes.fr/cel-00879035/en">The Art and
Science of Writing</a>, November 2013.<li>

<li>Ralph Johnson <em>et al</em>, <a
href="http://www.acm.org/sigplan/oopsla/oopsla96/how93.html">How to get
a paper accepted at OOPSLA</a>, <em>Panel at OOPSLA'93</em>, pp
429-436.</li>

<li>Craig Partridge, <a
href="http://www.acm.org/sigcomm/conference-misc/author-guide.html">How
to Increase the Chances Your Paper is Accepted at ACM SIGCOMML</a>.
<blockquote>
Generally useful advice that also applies to other networking
conferences.
</blockquote>

<li><a href="http://www.youtube.com/watch?v=g3dkRsTqdDA"><i>How to write
a great research paper</i></a></li>, Simon Peyton Jones

<li>
<a href="http://www.usenix.org/events/lisa99/cfp/guidelines.html">
What kinds of papers does USENIX publish?</a></li>

<li>Alan Jay Smith, <em>The Task of the Referee</em>, <em>IEEE Computer</em>
<b>23</b>(4):65-71 (April 1990).</li>

<li><a href="http://stipo.larc.nasa.gov/sp7084/index.html">Grammar,
Punctuation, and Capitalization</a>, NASA SP-7084</li>

<li><a
href="http://www.editorsoftware.com/stylewriter-software/">Stylewriter</a>
software</li>

</ul>

<h2>Talks</h2>

<ul>
<li><a
href="http://greatresearch.org/2013/10/04/presenting-a-technical-talk/"><i>Presenting
a Technical Talk</i></a> (Nick Feamster, 2013)</li>

<li><a href="WrittenCommunication.pptx"><i>Written Technical
Communication</i></a> (Klara Nahrstedt, 2010)</li>

<li><a href="OralPresentation.pptx"><i>Excellence in Oral Presentation
for Technical Speakers</i></a> (Klara Nahrstedt, 2010)</li>

<li><a href="http://www.cs.cornell.edu/cv/ShortTalk.htm">"The Short
Talk"</a> (Charles Van Loan)</li>

<li><a
href="http://cusg.eecs.berkeley.edu/~messer/Bad_talk.html">"Pointers on
giving a talk"</a> (D. Messerschmitt)</li>

<li><a
href="http://www.onr.navy.mil/onr/speak%5Ftips/Default.htm"><i>Tips for
Preparing Delivering Scientific Talks and Using Visual Aids</i></a>
(ONR)</li>

</ul>

<h2>Miscellaneous</h2>

<ul>
<li><a href="http://www.onlinephd.org/">Links to PhD resources</a></li>,
including PhD thesis writing and presentation</li>

<li><a
href="http://www.cl.cam.ac.uk/~mgk25/iso-paper.html">International
Standard Paper Sizes</a></li>
</ul>

<h2>Contributors</h2>

<p>This page contains material provided by Gail Kaiser, Craig Partridge,
Sumit Roy, Eric Siegel, Sal Stolfo, Luca Trevisan, Yechiam Yemini, Erez
Zadok and João Craveiro.</p>

<h2>Translations</h2>

<p><a href="https://www.akkuschraubercheck.de/schreiben-von-technischen-artikeln/">German
translation</a> by <a href="https://www.akkuschraubercheck.de">Daniel Gruber</a></p>

<hr>
<p>[<a href="proposal-hints.html">Hints for PhD proposal
defenses</a>] [<a href="defense-hints.html">Hints for PhD thesis
defenses</a>] &nbsp; [<a href="writing-bugs.html">Writing bugs</a>]
&nbsp;
&nbsp;

<hr>
<small>Last updated 
<script type="text/JavaScript">
document.write(document.lastModified)
</script>
by <a href="http://www.cs.columbia.edu/~hgs">Henning Schulzrinne</a>
</small>

</body>
</html>
