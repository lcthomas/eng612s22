---
layout: page
title: Lab 2
---
## Acknowledgments
The inspiration for this lab is from [Lab 3](https://f20idh.ryancordell.org/2020/09/22/Data-and-Metadata/){:target="_blank"} of Ryan Cordell's Intro to DH course (F20).

## Helpful References and Tools for Working with Spreadsheet Data
- Jenn Riley, NISO, [“Understanding Metadata,”](https://groups.niso.org/apps/group_public/download.php/17446/Understanding%20Metadata.pdf){:target="_blank"}, especially pgs 1-18
- [WTFcsv](https://databasic.io/en/wtfcsv/){:target="_blank"}
- [Raw Graphs](https://app.rawgraphs.io/){:target="_blank"}
- [Breve](http://hdlab.stanford.edu/breve/){:target="_blank"}\*
- [Flourish](https://flourish.studio/){:target="_bank"}
- [Tableau](https://public.tableau.com/en-us/s/){:target="_blank"}
- [XLMiner Analysis Toolkit](https://workspace.google.com/marketplace/app/xlminer_analysis_toolpak/600284989882){:target="_blank"}

## Woo Hoo, Spreadsheets
Today we are going to explore the exciting world of spreadsheets. Spreadsheets are the form in which we often encounter historical or literary data, and so for this reason it's worth taking the time to think about the format itself, the kinds of questions we can ask of tabular data, and the skills we might need to answer those questions. We'll be keeping it very simple in this lab. I've included a list above of various free programs and platforms you can use to visualize your data, and these tools can be useful and are well worth exploring. However, in this lab we are going to focus on the affordances of Google sheets to think about how you can explore historical and literary data without having to use any additional tools (apart from Google sheets itself).

## One: An introduction to tabular data
We'll start in class with a discussion of an example of relatively straightforward and already cleaned historical data: data from the 1840 US Census. You can find this spreadsheet in our class Google drive folder (in "Labs" > "Lab 2" > "1840 US Census"). We'll talk about how spreadsheets are organized, what the process of creating this spreadsheet might have looked like (see original reports [here](https://www.census.gov/library/publications/1841/dec/1840c.html){:target="_blank"}), and terms we will use in discussing them, including "csv/tsv," "metadata," and "controlled vocabulary."

We'll also look at this spreadsheet using one of the tools listed above: [view the 1840 Census on WTFcsv](https://databasic.io/en/wtfcsv/results/61d8a486da7d150900acd9e6?submit=true){:target="_blank"} and talk about wtf is happening here.

## Two: Explore the Trans-Atlantic Slave Trade Dataset
Then we'll move on to another example, one from our readings this week: the [Trans-Atlantic Slave Trade Database](https://www.slavevoyages.org/voyage/database){:target="_blank"}. We'll examine a downloaded spreadsheet of the data and discuss how we can use pivot tables to do initial explorations of large datasets.

We'll go through this together in class, but here's what you'll do:
1. Make a copy of the Trans-Atlantic Slave Trade Database spreadsheet *in your personal Google drive*. I've placed a copy of this spreadsheet in the "Labs" > "Lab 2" folder in our shared Google drive folder, but you should make a copy of this spreadsheet that lives in your personal Google drive account. To do this, click on [this link](https://docs.google.com/spreadsheets/d/1-pPVto-pi_UzLpxkDu6xnplStOyuWOrFd2EbSbW_WBo/copy){:target="_blank"} and then select "Make a copy" (you can also open up the class copy of this data and go to File > Make a copy to make your own copy; just make sure to either store your copy *outside* of our shared class Google drive or to include your name in the filename so I know it's your copy). This will create a file named "Copy of trans-atlantic-slave-trade" located in the root of your personal Google drive account. To see where this file is located, go to File > Make a copy; you'll be able to see where it's stored under "Folder" (it will likely say "My Drive", which means the home or root folder of your Google drive account). **Please change the filename to something that includes your name so I will easily be able to tell your personal copy apart from our class copy** (which lives in the "Lab 2" folder). Again, it's important that you complete the following steps using **your personal copy** of the Trans-Atlantic Slave Trade data.
2. We'll talk through the composition of this spreadsheet in class. Then, we will create a pivot table that displays the number of voyages per year using the "Year of arrival at port of disembarkation" metadata field. I'll walk us through how to do this in class, but you can also read [these instructions](https://support.google.com/a/users/answer/9308944?hl=en){:target="_blank"} (starting under "Create a pivot table manually"; choosing to insert the pivot table in a "New Sheet" will create a new tab in your spreadsheet where the pivot table will go).
3. We will talk about how to order this table by year and by number of voyages, and we'll create a line chart showing the number of voyages per year (x axis = year, y axis = number of voyages).
4. We will then create pivot tables displaying the counts for the following metadata fields:
    - Particular outcome of voyage
    - Outcome of voyage for slaves
    - African resistance

## Three: Explore Post45 HathiTrust data
Finally, we'll explore a dataset of metadata for fiction held by the [HathiTrust digital library](https://www.hathitrust.org/){:target="_blank"} from 1945 to 2000. This dataset is a subset of a dataset compiled by the [Post45 Data Collective](https://data.post45.org/our-data/){:target="_blank"} (theirs includes data through the early 2010s; I made a slightly smaller version for us to work with in class). You can find an [online version of this dataset on the Post45 Data Collective website](https://view.data.post45.org/index){:target="_blank"} (this is where I downloaded the data); this page is also where to look for metadata field descriptions (click on the question mark next to each column name).

Here's what you'll do:
1. First, as you did with the Trans-Atlantic Slave Trade spreadsheet, you should make a copy of the Post45 HathiTrust dataset in your personal Google drive. I've placed a copy of this spreadsheet in the "Labs" > "Lab 2" folder in our shared Google drive folder, but you should make a copy of this spreadsheet that lives in your personal Google drive account. To do this, click on [this link](https://docs.google.com/spreadsheets/d/127KKKy9TXEk6jkus73j6l-BKAyJR2ZtbpA75d7Qg1X0/copy){:target="_blank"} and then select "Make a copy" (you can also open up the class copy of this data and go to File > Make a copy to make your own copy; just make sure to either store your copy *outside* of our shared class Google drive or to include your name in the filename so I know it's your copy). This will create a file named "Copy of post45-hathitrust-fiction-1945-2000" located in the root of your personal Google drive account. To see where this file is located, go to File > Make a copy; you'll be able to see where it's stored under "Folder" (it will likely say "My Drive", which means the home or root folder of your Google drive account). **Please change the filename to something that includes your name so I will easily be able to tell your personal copy apart from our class copy** (which lives in the "Lab 2" folder). Again, it's important that you complete the following steps using **your personal copy** of the Post45 HathiTrust data.
2. Explore the dataset's metadata fields and their descriptions using [this page](https://view.data.post45.org/index){:target="_blank"}.
3. Create 2 pivot tables displaying summaries of 2 different metadata fields and/or answering 2 different questions about this dataset. For example, you might wonder how many works are tagged as particular genres, or how many works in the dataset were actually initially published prior to 1945 (for this one, you would need to think about the several different date columns included in this spreadsheet and what they each mean).
    - Alternatively, you may use one of the tools listed above for visualizing spreadsheet data (WTFcsv, Raw Graphs, Breve, Flourish, Tableau) to visualize the Post45 HathiTrust data in some way that provides answers to 2 different questions about this dataset. I think this is definitely the more challenging route, but if you are interested in exploring some of these data visualization platforms and tools, you may choose to do it.

## Lab Notebook Entry
Due:
- By class on Wed, Feb 9

In your lab notebook entry for this week, you should include the following things:
1. Links to your personal copies of the Trans-Atlantic Slave Trade dataset and the Post45 HathiTrust dataset or some other way for me to access them. If you include links in your post, you can set your Share settings for each file so that anyone with the link can view your files, so that anyone with a UM email address can view your files, or so that only someone who you have explicitly shared into each document can view the files (after clicking "Share," look under "Get Link" to see these options). Alternatively, you can [share me into your spreadsheet files](https://support.google.com/docs/answer/2494822?hl=en&co=GENIE.Platform%3DDesktop#zippy=%2Cshare-multiple-files%2Cchange-who-your-link-is-shared-with){:target="_blank"} explicitly using my non-aliased UM email address: <lxt308@miami.edu>. Again, please ensure your name is somewhere in the filename of each spreadsheet (can use just your first name).
2. At least one thing you observed or learned from your exploration of the Post45 HathiTrust dataset. This can be something odd or unexpected, something that confused you, something that initially confused you but that you figured out, etc.
3. A response to this prompt: Our readings this week focused on the affordances and limitations of quantification and objectivity. What do the spreadsheets we explored in this week's lab make it possible to know or to study or to question, and what do they occlude or make impossible to know or to study or to question? You may use any spreadsheet or any combination of spreadsheets we discussed in this week's lab and any reading or combination of readings from this week (week 3), but your notebook entry should include discussions of at least one specific spreadsheet in connection to at least one of our readings from this week. This discussion should be specific but it needn't be long (i.e., 2-4 paragraphs).
