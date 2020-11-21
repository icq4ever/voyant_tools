---
Title: Introduction à Voyant Tools
Author: Aurélien Berra
Date: 2018-06-30
Description: "Cette introduction francophone à Voyant Tools peut être utilisée pour découvrir la plateforme d’une façon autonome ou servir de base à un atelier."
Language: French
Copyright: CC-BY
---

# Introduction à Voyant Tools ![Logo de Voyant Tools](../images/voyant-logo_0.png "Logo de Voyant Tools")

[Voyant Tools](http://voyant-tools.org/) is an environment for analyzing, reading and viewing digital texts.

The development of this platform is part of a larger project, presented in a book: Geoffrey Rockwell and Stéfan Sinclair, *Hermeneutica. Computer-Assisted Interpretation in the Humanities*, Cambridge, Massachusetts, MIT Press, 2016, of which [Hermeneuti.ca] (http://hermeneuti.ca/) is the companion site. Tools are never just tools.

The purpose of this tutorial is to help you discover Voyant Tools, or to help you use it better. Here is the route that I propose to you to understand the project of this platform, guide your gaze in its interface, help you to analyze corpora and - who knows? - make you think about the meaning and interest of these explorations:

0. Preparations
1. About Voyant Tools
2. Reading distances: a first approach
3. Let's take a tour of the digital workshop
4. Explore your corpora!
5. What next?


*This document is based in particular on a brief [tutorial available on the Hermeneuti.ca site](http://hermeneuti.ca/intro-workshop), on [previous workshops](http://docs.voyant-tools.org/category/workshops/) provided by the designers of the platform and on the [documentation under revision](https://voyant-tools.org/docs/#!/guide/tutorial).*

---

![Tools indicator default view](../images/voyant_skin.png "Tools indicator default view")


## 0. Preparations

Voyant Tools is freely accessible on its Canadian site, <https://voyant-tools.org>, or on its French mirror site <http://voyant.tools.huma-num.fr>. However, I strongly recommend that you install the server version of Voyant Tools on your machine, following these guidelines: <https://github.com/sgsinclair/VoyantServer/wiki/VoyantServer-Desktop>. This version will allow you to operate the platform locally, without the need for an Internet connection, without recourse to a cache memory and therefore respecting document rights and any confidentiality needs, and above all faster and more flexibly, thanks to the possibility of restarting the server if it is slowed down or crashed and to handle large corpora more easily.

It is simply a question of downloading and decompressing the folder «"VoyantServer \*_\*-M\*. Zip »in the folder where you put your applications (I replace the numbers with asterisks here: take the most recent version) , launch the application by double-clicking on the “VoyantServer.jar” file (your computer may ask you to [install Java](https://www.java.com/fr/download/)) and wait for your browser to open at a local address (by default, http://127.0.0.1:8888/; pressing the «Open We »button has the same effect).


If you want to explore a corpus that is familiar to you, all you need to do is have one or more files in a common format (plain text, HTML or XML, etc.), or know the URL of a page where the text is accessible without barriers. I will detail these options under the heading “Creating a corpus”.

![Voyant Tools Home Page](../images/voyant_home.png "Voyant Tools Home Page")


## 1. About Voyant Tools

> Voyant Tools is a web-based text analysis, reading and visualization environment. Developed by a small team of digital humanities scholars led by Stéfan Sinclair and Geoffrey Rockwell, Voyant Tools is designed for a very wide range of applications and users, from students to researchers and journalists to market analysts. It strives to balance user-friendliness with a range of analytic and interpretive functions. (Incipit du fichier [*Readme*](https://github.com/sgsinclair/Voyant/blob/master/README.md) de l’entrepôt GitHub contenant le code de Voyant Tools)

### Project history

Since the 1990s, * Humanities Computing * and * Digital Humanities * have strongly developed and structured in Canada (see, among a thousand examples, a retrospective text by Ian Lancashire on the website of the Canadian society for digital humanities, [CSDH/SCHN](http://csdh-schn.org/2017/05/31/csdhschn-beginnings-reflections-by-ian-lancashaire/) and the Text Analysis Portal for Research, [TAPoR](http://tapor.ca/home)).

In the 2000s, Stéfan Sinclair developed the HyperPo software as part of his doctoral research on Oulipo.

From around 2008, the platform was opened under the name Voyeur, then Voyant. In particular, it uses Flash and Java technologies.

In 2015, Voyant 2.0 was released, which included a rewrite in HTML 5, improved query filters and introduced tools based on proximity calculus and element sequences, or n-grams.

### Principles

Voyant Tools is essentially based on the principle of openness. Its code is published as *open source* and contributions of all kinds are welcome.

Manipulate, explore, search through textual corpora: interaction with data - fast, easy, even fun - is the watchword, to learn from the process and produce series of results. This bias responds to the conviction that theory and practice are intimately involved. Voyant Tools thus aims to show  «*how analytical tools* are *instantiations of interpretive methods that can be woven closely into other hermeneutical things, like text* » (*Hermeneutica*, p. 4).

### Voyant and [me](https://aurelienberra.org/) (or: why I am writing this tutorial)

I remember that Stéfan Sinclair took part in the [Day of DH](http://stefansinclair.name/rapid-analysis-dayofdh11/) at the beginning of the 2010s… I then discovered this field of research, after a thesis in ancient Greek. Voyeur / Seer seemed to embody many of the values, traditions and issues of a community.

Since 2014, I have been using Voyant Tools in my teaching, in the first semester of the master's [Classical humanities and digital humanities](https://classnum.hypotheses.org/1125), to initiate textual analysis, to equip the exercise scholarly pastiches and bring out the advantages and limitations of a generalist platform.

In 2016, I produced the French translation of the interface, following a discussion on the "[Digital Humanities](https://groupes.renater.fr/sympa/info/dh)" list.

In 2017-2018, I produced lists of [*stopwords* for Greek and Latin](https://github.com/aurelberra/stopwords), which were integrated into Voyant Tools.


### Voyant Tools and the construction of digital humanities

There is a tension between the ideal, or the temptation, of the single omnipotent tool and the slow acquisition of a computational culture that allows the use of specialized tools (encoding, transformation, textual analysis, network analysis, visualization data, etc.), their adaptation, even their creation. Voyant Tools partly resolves this tension through its modularity and scalability.

The next big step will probably be the Spyral notebooks. Beyond the integration of tools in the text, it is a question of publishing * notebooks * combining code and commentary, analysis and argumentation, by acclimating the tradition of * literate programming * to the human and social sciences (see the [poster](http://journalofdigitalhumanities.org/2-3/voyant-notebooks-literate-programming-and-programming-literacy/) programmatic of the authors, as well as the parallels of the project [Jupyter](http://jupyter.org/) and [R Markdown](https://rmarkdown.rstudio.com/)). The possibility of inserting a tool or dynamic views into a web page already goes in this direction. Voyant Tools is undoubtedly the type of project that leads us towards a more shared digital and statistical culture.

! [More or less mysterious word cloud](../images/frankenstein_cloud.png "More or less mysterious word cloud")


## 2.  Reading distances: a first approach

`Cirrus`. See the word cloud reproduced above and also available [in a separate view](https://voyant-tools.org/tool/Cirrus/?corpus=75b440214b14d5402b2d9ab1e0150d17&toolFlow=contexts). What does this cloud represent, in your opinion? Among its characteristics, which result from a quantification of the text? Do all the words seem relevant to you? Are there any words missing? - When you have thought about these questions, handle the parameters of the cloud: change the number of terms taken into account using the cursor, then modify the list of filtered stopwords (these are [*stopwords*](https://github.com/aurelberra/stopwords/blob/master/rationale.md#about-stopwords)) by accessing the options - the icon appears on hover above the panel and is identified by the tooltip, according to a principle constant of the interface.

Now look at this [same text at various scales and through the prism of other tools](https://voyant-tools.org/?corpus=75b440214b14d5402b2d9ab1e0150d17).

`Terms`/`Terms`. The fundamental table of frequencies. Did you see the hidden columns (hover over the displayed column headers and click the arrows)? Did you know the *sparklines*, which summarize in the right column the trends of the terms over the corpus, indicating the minimum, maximum and final values?

`Reader`/`Reader`. What happens if you hover over a word, if you select it? What does the frieze below the text represent? Have you tested the query functions?

`Contexts`/`Contexts`. The essential match (such as Keyword in Context, KWIC). Have you noticed the sliders, especially the one called « Context »? A menu also gives you the possibility of restricting the corpus to certain documents.

! [List of tools of Voyant Tools](../images/tools_list.png "List of tools of Voyant Tools")


## 3. Let's take a tour of the digital workshop

To observe the entire work environment more methodically, return to the Voyant home page (by clicking on the house icon in the blue banner at the top of the window) and open one of the two suggested corpora. by default under the "Open" button, the [Shakespeare corpus](http://voyant-tools.org/?corpus=shakespeare).

Voyant's default configuration combines a set of tools, or modules, that are complementary and sometimes coordinated. Note that additional panels are present when working on a collection of texts, as is the case in this series of parts.

To navigate in this environment, you need to understand some principles of how a **view** works:

* Each **tool** corresponds to a **panel**, which you can reduce or enlarge.
* For each panel, **options** are available. Hover, then click.
* Each panel can be manipulated or explored in its own way.
* Each panel can modify the content of other panels.

Before replacing one tool with another in a panel, by clicking on the window icon, take the time to look at the list of tools. It is structured into non-exclusive categories, according to reading scales and types of presentation.

Voyant Tools currently offers 24 online tools (see [documentation](http://voyant-tools.org/docs/#!/guide/tools)). Some of them are part of the foundations of corpus linguistics or computational linguistics (count, concordance, co-occurrence), some are in vogue in digital humanities (thematic modeling, or *topic modeling*), some are more experimental or artistic (which ones, in your opinion?). Other tools are in preparation (for example a mapping tool linked to a named entity recognition function).

You will soon see the different ways to create a corpus by importing text.

Test for yourself the export functions, which depend on the relevant tool. They can provide:

* a bibliographic reference including the names of the designers, the platform and the tool
* an image produced by a tool (PNG and SVG formats)
* other types of data produced by a tool (HTML, TSV and JSON formats)
* a new URL to display a tool separately, in the entire browser window
* a code fragment to integrate the panel or the view into an HTML page (as in the examples which will be given later, a capsule is created by an *iframe* tag, which calls on the Voyant Tools API; some CMS, like WordPress, are notoriously resistant to this procedure)

Note that it is sometimes useful to open several interfaces and compare corpora, for example a version without lemmatization and a lemmatized version of a text, or a text in its original language and a translation.

You will already have noticed that the help function appears in all panels, under the question mark.

Here are the essential tools that I suggest you review:

* `Résumé` /` Summary` offers a quantitative summary of the corpus.
* `Documents` recalls the structure of the corpus.
* `Syntagms` /` Phrases` detects groups of recurring words.

* `Tendances` /` Trends` highlights the distribution of the term (s) selected within the corpus, which is divided according to the documents that constitute it or into segments of equal length.
* `Correlations` /` Correlations` relates pairs of terms and mentions their statistical degree of correlation.
* `Collocations` /` Collocates` also provides a list of word pairs that often appear in the same contexts.
* `Links` /` Links` provides a view of frequently related terms. Double click on a term to access options.

* `Scatter plot` /` Scatter plot` is a graphical approach of distances between terms or between documents, according to various well-known analysis methods, including correspondence analysis and principal component analysis. I recommend that for a tool like this resize the panel or export a view to a separate window. Zoom in by selecting an area and zoom out by double-clicking. Double-click a point to remove it from the graph or make it the center of proximity calculations. Explore the side panel options, especially choosing the number of clusters (* clusters *) and the number of analysis dimensions.
* `Thèmes` /` Topics` performs thematic modeling: all the terms of the corpus are algorithmically grouped together in “bags of words” according to their co-occurrences and the reader can see the emergence of semantic sets, oddities to be explained or absurdities appearances that invite modification of parameters or more thought on the data. Try it out.


<!-- ## Pause ![Même les hiboux ont besoin de se reposer les yeux.](../images/SpottedEagleOwl2522MGSleep_white_small.png "Même les hiboux ont besoin de se reposer les yeux.") -->

! [Word cloud containing an arbitrary, but balanced selection of stop words used in the different lists offered by Voyant Tools](../images/voir_multilingual_stoplists_sample.png "Word cloud containing an arbitrary, but balanced selection of stop words used in the different lists offered by Voyant Tools")

## 4. Explore your corpora!

### Create a corpus

To load your corpora into Voyant, use the local version that you have installed on your computer (see the “Preparations” section above) or one of the following servers: <http://voyant.tools.huma-num.fr> or <https://voyant-tools.org>, which will display by default an interface in the language of your browser.

The interface language can be changed from the home page and at any time by clicking on the icon provided for this purpose (see the [documentation](http://voyant-tools.org/docs/#!/guide/languages)). Note however that the language is one of the parameters which can be controlled by a modification of the base URL: <https://voyant-tools.org/?lang=fr> displays the interface in French, while <http://voyant.tools.huma-num.fr/?lang=en> displays the interface in English.

In the same way, the URL of your corpus can serve as a bookmark, if you copy the character string which constitutes its unique identifier (try appending to the base URL `?Corpus=75b440214b14d5402b2d9ab1e0150d17` - do you recognize the text ?). The corpora created on the Voyant Tools server have a certain durability: they remain accessible as long as they are visited regularly, for example once every three weeks.

Voyant allows you to create a corpus in several ways. Unicode (UTF-8) is recommended and plain text is the most typical format, but more often than not other encodings and formats will work fine.

* You can **copy and paste** text.
* You can enter one or more **URLs** that Voyant will visit.
* You can **open** one of the corpora that are available by default, using the "Open" button.
* You can **load** a text from one or more files, in plain text or in HTML, XML, PDF, RTF, DOCX, XLSX, even DOC and XLS formats - or even ZIP, to group in a compressed file files in other formats.

If the format of your source files is a problem, consider that it is usually easy to convert them to another format ([Pandoc](http://pandoc.org/) is a public health tool, and [scripts from TEI consortium transformation](https://github.com/TEIC/Stylesheets#stylesheets) are effective). By the way, I recommend that you work in a [text editor](https://fr.wikipedia.org/wiki/%C3%89diteur_de_texte), and not only in word processing software like Libre Office or Word, which mainly target the printed presentation: [Atom](https://atom.io) is available for any operating system, for example.

A very accommodating set of tools in terms of languages ​​and formats, Voyant Tools is a platform for textual analysis and, as such, remains resolutely logo-centric and text-centric. You will not find a tool here for analyzing printed or manuscript images, for aligning text and images, or for processing audio or video streams.

### Commented examples

Here are a few examples, where I clarify certain points. The mentioned files are available in the [data](https://github.com/aurelberra/voyant_tools/tree/master/data) folder of this same warehouse (to download them, right click, CTRL-click or click two-finger, depending on your system configuration).

Before loading these corpora, take the time to explore the import options. These are advanced functions, which allow you to name your corpus, to load only part of the text (thanks to regular expressions for plain text, to XPath expressions for XML, to CSS selectors for HTML), specify the options for importing tables, impose a language or a segmentation mode and protect your corpus with a password. In this options window, the topic titles contain links to the documentation.

#### Import by URLs


* English: [the longest reputed Wikipedia page](https://en.wikipedia.org/wiki/List_of_compositions_by_Franz_Schubert)
    * This page clearly requires the "Multilingual" stop word list, doesn't it?
* Modern French: Lautréamont, [*Les Chants de Maldoror*](http://athena.unige.ch/athena/lautreamont/laut_mal.html)
    * The prevalence of body vocabulary strikes me as striking.
    * On a technical level, note that the default word splitting (tokenization, or segmentation) when importing text keeps as units elements containing an apostrophe such as « n'est ». You can change this setting before creating the corpus by choosing in the options of « Preparation /*Processing* » the segmentation by "Limits of single words / *Simple Word Boundaries* » ( « n'est » no longer appears as a word and its two components, « n » and « est », are filtered).
    * Even if  « l'homme » thus disappears to increase the number of occurrences of « homme », the fact remains that the text is not lemmatized, but divided into graphic forms: « homme » and « hommes » are separated. Depending on the languages ​​and the objectives of the analysis, the current lack of lemmatization in Voyant Tools is a more or less serious obstacle. In many cases, slightly more complex queries are sufficient: here,  « homme* »  and « homme|hommes » allow you to group together the forms « homme »  and « hommes » , just as « faire|fais|fait » groups together the forms. most frequent forms of the verb « faire ». Explore these possibilities by clicking on the question mark or by visiting the page that documents the [query modes](http://voyant-tools.org/docs/#!/guide/search). If lemmatization is essential for your research, it should be part of a preparatory phase, a pre-processing specific to the language of your corpus, before importing into Voyant Tools.
* Middle French: Rabelais, [*Pantagruel*](http://athena.unige.ch/athena/rabelais/rabelais_pantagruel.html)
    * I suggest you observe for example the distributions of the proper names Pantagruel and Panurge.
    * For most non-contemporary corpora (like Middle French here), testifying to a non-classical language state (archaic Greek) or marked by a strong spelling fluidity (non-standard editions), empty words will not be suitable for straight away. It is often possible to modify the list offered by default to eliminate the most embarrassing forms for analysis. For more specific work, it will probably be necessary to find a relevant list, which is not obvious if this is a more or less old corpus. Although all research has its own criteria of relevance in the matter, gradually defined, I advise you to make your lists public if you spend some time developing them. In the philological field, for example, I appreciate the opening of the Classical Language Toolkit ([CLTK](http://docs.cltk.org/)).

Since we are talking about URLs, I am inserting here two examples of integration into an HTML page: [example 1](https://aurelienberra.org/temp/voyant.html) and [code](https://github.com/aurelberra/aurelienberra/blob/master/static/temp/voyant.html) corresponding; [example 2](http://voyant-tools.org/docs/#!/guide/search), taken from the Voyant documentation.

#### Import TXT files

* Latin: Caesar, * La Guerre des Gaules * ([file](https://github.com/aurelberra/voyant_tools/blob/master/data/caesar_bellum_gallicum.txt))
    * The text of IHP 5 has been slightly cleaned up. Of course, select stop words from the "Latin" list. See that, for lack of lemmatization, the forms of the name of Caesar (« *caesar*, *caesarem* ») or of the words meaning « camp » and « enemies » (*« castra*, *castris* » and « *hostium* , *hostes*, *hostibus* ») are distinguished.
* Latin: Caesar, *La Guerre des Gaules*, lemmatized text ([file](https://github.com/aurelberra/voyant_tools/blob/master/data/caesar_bellum_gallicum_lem.txt))
    * Without being perfect, the lemmatization is enough here to see the difference with the previous text. To make sure, you can load the texts in two windows and export certain views or lists.


#### Import de fichiers TXT

* Latin : César, *La Guerre des Gaules* ([fichier](https://github.com/aurelberra/voyant_tools/blob/master/data/caesar_bellum_gallicum.txt))
    * Le texte du PHI 5 a été légèrement nettoyé. Sélectionnez bien sûr les mots vides de la liste « Latin ». Voyez que, faute de lemmatisation, les formes du nom de César (« *caesar*, *caesarem* ») ou des mots signifiant « camp » et « ennemis » (*« castra*, *castris* » et « *hostium*, *hostes*, *hostibus* ») sont distinguées.
* Latin : César, *La Guerre des Gaules*, texte lemmatisé ([fichier](https://github.com/aurelberra/voyant_tools/blob/master/data/caesar_bellum_gallicum_lem.txt))
    * Sans être parfaite, la lemmatisation suffit ici pour constater la différence avec le texte précédent. Pour vous en assurer, vous pouvez charger les textes dans deux fenêtres et exporter certaines vues ou listes.

#### Import of HTML or XML files, compressed in a ZIP archive

* French, Spanish and English: [* Digital Humanities Quarterly * 12.1](http://www.digitalhumanities.org/dhq/vol/12/1/), issue of the journal on Spanish-speaking and French-speaking digital humanities, in free access (CC-BY-ND license)
* As before, select the list of "Multilingual" stopwords. It is useful here to edit the list to filter out terms like « http », « *digital* » and « *humanities* ».
* Note that in the ZIP file proposed as an example ([XML files](https://github.com/aurelberra/voyant_tools/blob/master/data/dhq_12_1_xml.zip)), I excluded four XML files from the source, due to a reading error of some nodes. If the copyright and site configuration allow it, it is quite easy to collect HTML pages, for example with the command line tool [`wget`](https://programminghistorian.org/en/lessons/automated-downloading-with-wget) (you get for example these [HTML files](https://github.com/aurelberra/voyant_tools/blob/master/data/dhq_12_1_html.zip)).


### Free exploration

It's time for me to let you experiment.

## 5. What next? ! [Logo of the Tools indicator](../images/indicator-logo_0.png "Logo of Tools indicator")
## 5. Et ensuite ? ![Logo de Voyant Tools](../images/voyant-logo_0.png "Logo de Voyant Tools")

Besides the French version (on the [Voyant Tools] server (https://voyant-tools.org/?lang=fr) or on that of [Huma-Num](http://voyant.tools.huma-num.fr/?lang=fr)), versions in [other languages](http://voyant-tools.org/docs/#!/guide/languages) are being posted as colleagues translate interface. The [server version](https://github.com/sgsinclair/VoyantServer/#voyant-server) of Voyant Tools allows you to operate the platform locally. The [code](https://github.com/sgsinclair/Voyant) of the platform is published in *open source* (GPL license).

For more details, see the [Voyant Tools manual](http://voyant-tools.org/docs/#!/guide/start) (CC-BY license). An English [tutorial](https://voyant-tools.org/docs/#!/guide/tutorial) intended to serve as a basis for the organization of workshops or training is being drafted. To know who did what, according to which principles and using which technologies, the [*About*](https://voyant-tools.org/docs/#!/guide/about)page of this documentation is ideal. The [*Gallery*](https://voyant-tools.org/docs/#!/guide/gallery) provides various examples and the [Hermeneuti.ca](http://hermeneuti.ca/) site illustrates the Insertion of Voyant panels in online essays.

You can contact the designers, Geoffrey Rockwell (<geoffrey.rockwell@ualberta.ca>) and Stéfan Sinclair (<stefan.sinclair@mcgill.ca>). On Twitter, the [@VoyantTools](https://twitter.com/VoyantTools) account is an effective channel for information on changes to the platform and the uses that other users make of it.

Finally, all your comments on this tutorial, or on Voyant's French-speaking interface, are welcome: Aurélien Berra, <aurelien.berra@parisnanterre.fr> and [@aurelberra](https://twitter.com/aurelberra). Please do not hesitate to share your thoughts, remarks and questions.

I wish you fruitful readings, digital and human.

! [25 word cloud of this page](../images/voir_cloud_intro_paris.png "25 word cloud of this page")
