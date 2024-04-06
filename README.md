# AirBnB MongoDB Analysis

A little assignment to practice importing and analyzing data within a MongoDB database.

Replace the contents of this file with a report, as described in the [instructions](./instructions.md).

<h1>
(Use this Assignment as 1 of my 2 late assignment extensions)
</h1>

## The origin of your data set - what is it and where does it come from. Include a link to the URL of the source.

## What format the original data file was in (CSV, JSON, or other).

Display some of the raw data from the original data file (the first 20 rows is enough - feel free to clip the text in fields to prevent line-wrapping). Use Markdown's ability to display tables - see the examples in the Markdown guide linked above.
Describe any problems that were present in the data and the scrubbing tasks that were necessary to prepare your data set for import - include any scrubbing done in Python, a text editor, or any other tool. Be specific with examples of the problems in the original data and the way in which those were solved. Feel free to show small snippets of relevant code - see the examples of code "syntax highlighting" in the Markdown guide linked above.

## show exactly two documents from the listings collection in any order

returns the first two documents from the listings collection as they are stored in the database

```

db.listings.find().limit(2)

```
