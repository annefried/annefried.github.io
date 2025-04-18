---
title: 'Scientific Writing'
date: 2024-05-27
permalink: /posts/2020-09-01-scientific_writing
tags:
  - nlp
  - scientific writing
---


This blog post summarizes some important hints and tricks when writing a scientific paper or a thesis in the area of natural language processing (NLP) or computational linguistics (CL).
Of course, they are only recommendations and the ideal solution depends on your concrete topic.

__When you are advised by me or a team member on your thesis, please work through this page carefully. Feel free to ask any remaining questions about your specific thesis structure in one of our meetings. Please submit a draft for a chapter early (at the latest midway into your thesis time) for detailed feedback.__

Some initial hints:

* First, very importantly, __scientific writing is not like crime story writing__: you do not need to wait for your results until the end. Throughout your article or thesis, mention important points and findings early on.
This will help the reader to understand and contextualize your proposed method/dataset/findings, and if your results are cool, motivate them to keep reading.
* __Write top-down__ rather than bottom-up: each paragraph should start with a sentence that makes the reader expect what is going to be explained. Each section should start with 2-3 sentences stating what is going to be explained in the section. Each chapter ... (I think you got the idea). The Introduction should tell the reader what is happening in the article/thesis!
* __Consistency__: check your work for consistency: in spelling, in terminology, in typesetting.
* __Acronyms__: before submitting, carefully check if every acronym has been introduced (and also if it is only introduced the very first time the term is mentioned).


## Writing an Introduction for a Research Paper

* Motivation: Give a real-world motivation of a potential application of your work, or state which problem it solves. Then, give a high-level overview of the research area including several citations.
* Gap: What is the problem with existing approaches? Also, cite the 2-3 most closely related papers and state how you will overcome their limitations.
* Method: Give a brief high-level overview of the most important features of your method (or new dataset, if any).
* Contributions: A concise list of contributions (perhaps integrated with a Plan of the Paper, i.e., references to sections) should be at the end of your Introduction section. This part may be typeset as a bullet point list or as a list within the regular paragraph numbered with (1), (2), ... or (a), (b), ... or (i), (ii), ... etc. -- Pay special attention to the contributions, they are the currency in which your work is evaluated!


## Writing Tipps for Bachelor/Master thesis

The typical reader of your thesis is a peer: imagine a Bachelor/Master student who has taken the same courses as you have. The thesis should describe everything on a level so they can understand.

__Template and Length:__ Please use the template provided in [our uni-internal GitLab](https://git.rz.uni-augsburg.de/coling-a/coling-ba-ma-template).
There is no strict length limit, as the ideal length of a thesis strongly depends on your topic. Typically, a Bachelor thesis should not contain less than 30 pages (of text, excluding figures) and no more than 50 pages, while a Master thesis should contain between 40 and 60 pages. Keep in mind that writing _concisely_ is much harder than producing large amounts of text, so your grade does not depend on the number of pages you produce. In fact, if the writing is repetitive, this will be evaluated negatively!


__Structure:__

How to write the __Introduction__ for your thesis:
* Start with writing the background, method, and experiments chapters. You will very likely have to edit the Introduction chapter less this way.
* Assume that if a reader has only limited time, they will only read the Introduction. What should they know about your work? (They should know about the most important points!)
* Start with the description and motivation of the problem your work is attempting to solve: This could either be a real-world problem or another technical issue for which your method is a prerequisite. (1-2 pages)
* Give a high-level introduction to your topic area (just what is necessary to understand the next point). (1-2 pages)
* Give a high-level description of the solution you will present in the thesis (dataset, method, findings). (2-3 pages)
* Give a plan of the paper (in the form of a list): what chapters will follow and what do they contain? (3-4 sentences per chapter)
* Very important: give a list of contributions. Typically, a thesis will have 2-3 main contributions, focus on these, and explain them in about 10 sentences each. Which gap do they solve? What is novel about them? (about 1 page)


How to write the __Background__ chapter:
* Your thesis should not simply reproduce textbook-level knowledge. Only the general background that is important to your thesis should be explained.
* 1-2 sub-chapters ideally explain the most closely related specific prior work in detail. This will usually be around 5-10 papers for a Bachelor thesis, and 10-20 papers for a Master thesis.

How to write the __Dataset/Method__ chapter:
* Describe every step you took like a "recipe" (not a temporal report). Your work should be reproducible.
* For datasets, include corpus statistics, distribution of classes, etc., in the form of a table or diagrams.
* When including diagrams and preparing them with another program: make sure to embed PDFs.
* Talk to us how to write this best for your specific topic.


How to write the __Experimental Results__ chapter:
* Typically, our work is empirical, testing a hypothesis on some data. Clearly state what hypothesis you are testing in each experiment.
* Describe the setup, hyperparameter tuning, which model checkpoint or prompt you used, your datasplits, ...
* Include a few meaningful baselines for comparison: always predicting the majority class, etc.
* Report significance tests or standard variation of your results.
* Discuss each result: what does the finding mean?

How to write the __Discussion__ chapter:
* Discuss your results and findings from a bird's eye view: What do they implicate? What went wrong? What was unexpected?
* You can also integrate an __Outlook__ section here (the title becomes __Discussion and Outlook__): What would be the next steps? What could be improved?

How to write the __Conclusion__ chapter:
* This can be brief (1-2) pages, just summarize your main findings.

What does into the __Appendix__:
* long examples or prompts (short version in Figure in main text!)
* long pseudocode
* annotation guidelines
* huge tables with detailed experimental results (short version in main text!)
* ... ask if in doubt! ...


## Citation style

Please use the ACL Natbib citation format in Latex, which you can find [here](https://github.com/acl-org/acl-style-files).
Most relevant papers can be found in the [ACL Anthology](https://aclanthology.org/), please use the bibtex entries from this source.
If a paper is not in the ACL Anthology, try finding a high-quality Bibtex entry in [dlpb](https://dblp.org/) - also for ArXiv papers!
If an ArXiv paper has a follow-up version accepted for publication at a conference or journal, you should cite this peer-reviewed version.
Only if you cannot find an entry in these sources, resort to other sources for Bibtex entries (e.g., Google Scholar).
Please pay special attention to the instructions of how to integrate citations into the text. Always refer to the authors, _they_ state/propose/found something, not "the paper." This means you should write: "Friedrich et al. (2020) found that ..." (use the `\citet` command!) rather than: "In (Friedrich et al., 2020) it was found that ..." If a citation refers to a full sentence, put it _within_ the sentence, e.g., "XYZ can be achieved using really small language models (Friedrich et al., 2031)."

## Cross-References

Your readers should be able to read your thesis or papers in linear order. (As a child, I used to like the kind of crime stories where, as a reader, I could play detective by jumping to particular pages: a thesis or paper should not fall into this genre!)
Use cross-references with care. Forward references are almost always bad: as a rule of thumb, only use them if absolutely necessary (this should not be the case more than 2 times per thesis/article).
Instead, when you feel inclined to refer forwards, describe the important points in 2-3 sentences such that your reader will be able to follow the ideas you will describe next.
Backward references are okay, but only use them if absolutely necessary as well.


## Examples and abbreviations

I tend to just put commas before and after every _e.g._ and _i.e._ (following American English spelling).
For a good explanation, see [here](https://en.wiktionary.org/wiki/i.e.) and [here](https://en.wiktionary.org/wiki/e.g.).


## Typesetting

There is no unique wrong or right way for typesetting. Here are my recommendations.

* Introducing acronyms: "In this paper, we leverage Large Language Models (LLMs) to ..."
* IMPORTANT! Introduce acronyms the __first__ time you use them (in the main text, avoid acronyms in abstract if possible) and then use them _consistently_!
* _italic_: use for introducing (highly) specific terminology, e.g., "This work deals with distinguishing _discourse type_ vs. the _text type_." Use italics only the first time you mention the term.
* __bold__: use for paragraph headings when using the `\paragraph{...}` command. Sometimes, another phrase in the first sentence of a paragraph may function as a paragraph heading. Occasionally, it may make sense to boldface this phrase. Use this with care!
* Tables, figures etc. should be placed at the top of pages that do not have a chapter heading. Captions go below the table/figure, etc.
* For diagrams, if you are not familiar with [TikZ](https://tikz.net/), we recommend [draw.io](https://app.diagrams.net/) (embed your diagrams as PDF).
* Use chapters (sections, subsections, paragraphs). In your text, you can write "In this chapter, ..." or "In this section, ...", do not write "In this paragraph" or "In this subsection." Preferred: title case for chapter and section headings, you can use lower case spelling for subsections and lower.
* "quotes": In scientific text on NLP or CL, you will occasionally cite text examples. I tend to put them into quotes (no matter whether they are full sentences or just words or phrases). Use the `csquotes` package in Latex and use the `\enquote{...}` command for beautiful quotes and easy typesetting.

For longer examples, I use the following Latex environments (I do not typeset these numbered linguistic examples in parentheses).

```
% Put this in your pre-amble
\usepackage{enumitem}

\newcounter{examplecounter}
\newlength\myLeftmargin
\setlength{\myLeftmargin}{0pt}
\newenvironment{example}
{\refstepcounter{examplecounter}
	\begin{samepage}
		\begin{indentation}{0.2em}{0em} % first: indent on left side, second: indent on right side
			\setlength{\parsep}{0pt}
			\setlength{\parskip}{0pt}
			\setlength{\itemsep}{0pt}
			\begin{list}{(\arabic{examplecounter})}%
				{\global\addtolength\myLeftmargin{\parindent}%
					\global\addtolength\myLeftmargin{\parindent}
					\setlength\leftmargin{\myLeftmargin}%
				}
				\item\relax}
			{\end{list}
		\end{indentation}
	\end{samepage}
}

\newcommand{\labex}[1]{\label{ex:#1}}
\newcommand{\eref}[1]{(\ref{ex:#1})}

% inside the document:
\begin{example} \small
On Monday, NASA {\bf announced} that signs of liquid water {\bf have been found} on Mars. The Mars Reconnaissance Orbiter spacecraft {\bf found} evidence of the liquid on the Martian surface, [...].\\% in long dark spots on the Red Planet thought to be formed because of water flow. \\
(\itshape https://en.wikinews.org/wiki/NASA\_announces\_water\_on\_Mars)
%In a news conference, NASA's planetary science director, Jim Green {\bf said}, "We now know Mars was once a planet very much like Earth with warm salty seas and fresh water lakes [...] but something has happened to Mars, it lost its water."
\label{ex:report}
\end{example}

As illustrated by \eref{report}, ...

```

## Writing assistance

NLP develops writing assistance tools and spellcheckers - it would hence be nonsensical not to make use of them!
However, be aware that you need to double-check their output: is it really what you intended? Is nothing hallucinated?
If you use spellcheckers like [Grammarly](https://www.grammarly.com/grammar-check) that also help you to improve your style, you do not need to mention this.
If you make use of generative AI like ChatGPT for writing, please add a section in your appendix where you describe which sections you have composed with their help, and also reflect your experience with the writing tool (1-2 pages minimum).


## References

Here are some additional references that may be helpful.

An [overview](https://blog.apastyle.org/apastyle/2011/08/punctuating-around-quotation-marks.html) of where to put quotation marks in English.

A frequent mistake in English writing is to use non-parallel constructions in the same sentence. A good explanation can be found [here](https://www.lingualbox.com/blog/parallel-structure-a-key-to-effective-english-writing). Checking this out is highly recommended!

[This page](http://users.ece.cmu.edu/~koopman/essays/abstract.html) provides a nice summary of how to write good abstracts for your research papers.

I highly recommend [this book](https://www.worldscientific.com/worldscibooks/10.1142/q0232) on science research writing for non-native speakers of English as a must-read for PhD students in our field.

Super useful [academic phrasebank](https://www.phrasebank.manchester.ac.uk/) (thanks to Hanna Schmück for the suggestion).

## Tense, connectives, and other important writing issues

[Scientific Writing Cheat Sheet + Exercises (PDF)](http://annefried.github.io/files/Scientific_Writing_Exercises_09-22.pdf), developed for PhD students, but certainly also useful for Bachelor/Master students.

As a rule of thumb, in scientific writing in the NLP domain, use __present tense__. There are only a few exceptions: when reporting on a process that you performed only once (e.g., data collection or annotation), you can use past tense, and (mostly in the conclusion) when you talk about achievements, use present perfect (e.g., "In this thesis, we have demonstrated that ...").

Make use of the [Oxford comma](https://en.wikipedia.org/wiki/Serial_comma).

## Acknowledgment

I learned many of these scientific writing concepts and tricks from my absolutely marvelous PhD and scientific writing mentor [Alexis Palmer](https://www.colorado.edu/linguistics/alexis-palmer).