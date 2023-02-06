![Black Logo - White BG](https://user-images.githubusercontent.com/872296/212477556-9dc6ce15-75c2-444d-b56e-54e5b3cff413.png)

# DataWars - Content Creator Handbook

This is the starting point for all our Lab writers and content creators. Part of our culture is to be process-driven, so our objective is that all your questions should be answered here. If there's anything missing, we'd love to hear about it so we can write it and help future creators. You can email me at any time at sbasulto@datawars.io.

**Important:** We're trying to provide a reduced version of this Handbook in Video format; please check the following [YouTube playlist](https://www.youtube.com/playlist?list=PLBzCxqQZiCDrJzIFE6VHK_vGzbt5Bq0va) (WIP).

# Table of Contents

- [DataWars Goal and Mission](#toc-goal-mission)
- [General Structure of a Project](#toc-project-structure)
- [Types of Projects](#toc-types-of-projects)
  - [Learn Projects](#toc-learn-projects)
  - [Practice Projects](#toc-practice-projects)
  - [Capstone Projects](#toc-capstone-projects)
- [Activities](#toc-activities)
  - [Multiple Choice Activity](#toc-multiple-choice-activity)
  - [Single Answer Activity](#toc-single-answer-activity)
  - [Jupyter Activity](#toc-jupyter-activity)
  - [Code Activity](#toc-code-activity)
  - [Activity Solutions](#toc-activity-solutions)
- [Writing your lab](#toc-writing-your-lab)
- [Contract and Methodology](#toc-contract-methodology)
  - [Getting Paid](#toc-getting-paid)
- [Tooling](#toc-tooling)
  - [Visual Studio Code](#toc-tooling-vscode)
  - [Docker](#toc-tooling-docker)

# <a id="toc-goal-mission"></a>DataWars Goal and Mission

DataWars mission is to advance Data Science/Analysis/Engineering training in a hands-on way. Our main goal is to provide hands-on projects so our students can acquire and practice skills in an interactive form: project-driven learning.

We want to break the traditional education paradigm in which learning and practice (application of what was learned) are separated in different phases. Instead, we want to combine both: learning and application.

A typical project of DataWars will explain a given concept and immediately provide interactive activities so students can practice and apply those concepts. This helps the student solidify the concepts and understand if they have any knowledge gaps.

The process is as follows:

```
Explain > Practice > Challenge > Explain > Practice > Challenge > ...
```

> Related: See [Activity Types](#todo) to learn what types of interactive activities you can use in your labs to test your student's understanding.


# <a id="toc-project-structure"></a>General Structure of a Project

A project is a combination of "learning content" + an interactive "lab". The learning content is just text that you provide for your students to follow along.

<img width="1200" src="https://user-images.githubusercontent.com/872296/212479847-63972e17-0aeb-42fc-885f-f074bd4470a1.png">

This learning content is a combination of rich text (images, links, formatting options like bold fonts, italics, etc) and embedded activities. The content is broken up in different pages or "sections" to simplify the consumption for the student. Read more about this in the [Content Portion of a Lab](#todo).

The interactive lab is a combination of different devices that your student employs to learn/practice/evidence the skills/concepts. It can be a Jupyter instance, a MySQL Database, a Linux server, etc.

# <a id="toc-types-of-projects"></a>Types of Projects

DataWars includes a combination of three types of projects:

* **Learn Projects**: a project that explains concept, recommended time to completion should be between 20 and 30 minutes.
* **Practice Projects**: a project to practice concepts and skills, completion time should be between 20 and 30 minutes.
* **Capstone Projects**: a more general project that helps student practice multiple topics in the same project. It should take between 40 and 60 minutes for a student to complete them.

Each fulfills a different function within the Learning Experience of our students.

## <a id="toc-learn-projects"></a>Learn Projects

The objective of this project type is to drive concepts and for the student to learn and apply them. It includes a lot more guidance while explaining the subjects.

After each new concept is introduced, we recommend to add different activities to solidify those concepts. So, for example, if we're teaching basic math we'd have the following sections.

```
- Introduction
- Additions
    - Activity: practice 2 + 2
    - Activity: practice 3 + 4
- Subtractions
    - Activity: practice 5 - 2
    - Activity: practice 9 - 1
etc...
```

An example of a Learn Project is: [Intro to Pandas Series](https://beta.datawars.io/module/82e51088-2737-4e63-b5a1-7680b3ef3c95)

## <a id="toc-practice-projects"></a>Practice Projects

As the name implies, these projects are about practicing and solidifying concepts. They contain a lot less guidance, it's all about different activities to practice the skills.

The activities' solutions will generally contain explanations referring to the learning portion.

An example of a Practice Project is: [Practicing filtering sorting with Pokemon](https://beta.datawars.io/module/e7ab30b3-6b76-4f7c-a69e-048a09dc804b)

## <a id="toc-capstone-projects"></a>Capstone Projects

Capstone projects are Practice Projects but combining multiple skills.

> This section needs expanding.

# <a id="toc-activities"></a>Activities

Activities are at the heart of DataWars. It's what allows us to measure and keep track of our students' skills. An activity is any interactive challenge/puzzle/exercise that requests the student to complete something and we can accurately verify their result.

There are different types of activities (shown below), but in general, all activities contain:

* A title: brief description of what the student is requested to do
* A description: optional, further details. This is free text (markdown), it can contain images, formatting, etc.
* The activity itself: discussed later
* A hint: optional, if you think something can aid your student without giving away the answer
* The solution: how to resolve the activity. This is a very important step in the learning process. We like to explain how things work, so solutions are usually very comprehensive.

The following subsections explain the different types of activities supported by DataWars. The first two (multiple choice and single answer) are "static" activities. The later two (jupyter and code activities) are dynamic activities that will check something on the user's running lab.

<img width="960" src="https://user-images.githubusercontent.com/872296/212626577-50fc7d89-15cd-477c-a2ba-5be1768950c2.png">

## <a id="toc-multiple-choice-activity"></a> Multiple Choice Activity
These are our least used and most basic type of activities. The answer can be just one option (where radio buttons will be rendered) or several (checkbox will be rendered).

If possible, try to avoid this type of activity as it's easy to brute-force it. Use it for very basic topics only.

## <a id="toc-single-answer-activity"></a> Single Answer Activity
This one checks for a single answer provided by the student. We render a simple text input and we check if the submitted solution is the same as the correct answer.

<img width="958" alt="image" src="https://user-images.githubusercontent.com/872296/212627898-acffb19d-eb28-479e-9a56-b1b0b688d74a.png">


## <a id="toc-jupyter-activity"></a> Jupyter Activity
This is a "code activity" that uses the student's running lab to verify a given exercise. For example, you can ask them to define a function in their notebook and you can check if that function works correctly. Or you can ask them to load some data in a pandas DataFrame named `df` and clean it.

In further sections we'll go into a lot more detail on how to write these activities. But the gist is that it works by using assertions. Following the above example, as an instructor, I'd write the following assertions to verify my students' submissions:

```python
assert `df` in globals(), "It seems like the `df` variable is not defined yet"
assert df.isna().sum() == 0, "It seems you still have null values in your DataFrame"
assert df.duplicated().sum() == 0, "It seems you still have duplicated in your DataFrame"
```

If all the assertions complete correctly, the activity passes and the result is recorded.

## <a id="toc-code-activity"></a> Code Activity

This activity type gives you full access to the student's lab instance and you can perform any check you want. You'll need to use your skills to write the correct code validations. A few examples:

### File exists

We could ask our student to read a CSV, clean it correctly (removing null values and duplicates), and save it in a given path. Then, our validation code would look like:

```python
import pandas as pd
from pathlib import Path

path = Path("data_cleaned.csv")
assert path.exists(), "Couldn't locate your file, are you sure you've saved it?"

df = pd.read_csv(path)
assert df.isna().sum() == 0, "It seems you still have null values in your DataFrame"
assert df.duplicated().sum() == 0, "It seems you still have duplicated in your DataFrame"
```

### Python function correctly defined

We could ask our students to define a module and a function, for example, the module `calculator.py` and the function `add` that takes two arguments and returns the sum of them. Validation code:

```python
try:
    import calculator
except ImportError:
    assert False, "Couldn't load your module. Please verify it's correctly named"

assert calculator.add(2, 3) == 5, "Your `add` function doesn't seem to work as expected"
```

## <a id="toc-activity-solutions"></a> Activity Solutions

Activity solutions are extremely important for us. Solutions don't just provide the correct answer, but they also show how the instructor decided to approach the problem and also communicate important conceptual topics that the student might have missed in the learning sections.

Make sure your solutions explain to the student why you made the decisions you made, what approaches you considered and what alternatives are there.

Check the following example:

<img width="905" alt="image" src="https://user-images.githubusercontent.com/872296/212656252-59338f0b-01b8-463a-bf07-1e8b37339045.png">


There are exceptions, of course. Sometimes the solution is just a one liner. But most of the time, we want to make sure we help the student reason while reading the solution, and not just give them the correct answer.

# <a id="toc-writing-your-lab"></a>Writing your lab

This section needs further expansion. For now, see the following self-explanatory templates:

* [Python + Jupyter](https://github.com/datawars-io-content/sample-lab-jupyter)
* [SQL with MySQL](https://github.com/datawars-io-content/sample-lab-mysql-sakila)
* R with RStudio *(coming soon)*
* R with Jupyter *(coming soon)*

# <a id="toc-contract-methodology"></a>Contract and Methodology

`#TODO: this section is under development`

## <a id="toc-getting-paid"></a> Getting Paid

Once you agree your contract and timelines for your projects, and in order to get paid, you'll need to submit your invoice to the email `ap@datawars.io`. In your invoice, it should include the projects you have worked on, and the individual rates for those projects + a grand total at the bottom.

Along with your invoice, you must submit instructions to get paid; including your bank account information, address, full name, etc.

# <a id="toc-tooling"></a>Tooling

Writing the labs and the activities might look a little annoying at first, given the specific syntax we require for our activities. That's why we've written a bit of a framework to simplify your job. Let's start with the editor and content writing section.

## <a id="toc-tooling-vscode"></a> Visual Studio Code

The recommended text editor is [Visual Studio Code](https://code.visualstudio.com/) (or VSCode for short). It's FREE and open source.

Please go ahead and install it if you don't have it already:

### VSCode Snippets

We're using VSCode because it lets us create some simple snippets that GREATLY simplify creating activities. You can find the snippets in this same repo: https://github.com/datawars-io-content/content-creator-handbook/blob/main/vscode_snippets.json

To configure the snippets, follow these steps:

#### Step 1: Configure User Snippets

Use the command pallete (`cmd + shift + P`) and go to "Configure User Snippets"

<img width="2160" alt="Screen Shot 2022-12-22 at 1 28 51 PM" src="https://user-images.githubusercontent.com/872296/209134972-5c506fc9-c7fa-4dda-ba91-250e7bd39628.png">

#### Step 2: Add snippets

Choose `markdown.json` from the list, and paste the snippets from above.

<img width="2160" alt="Screen Shot 2022-12-22 at 1 28 27 PM" src="https://user-images.githubusercontent.com/872296/209134953-2001a648-6432-40ee-bee5-ad3805fafe61.png">

### Using Snippets

Now, while you're writing your activities, you can just fire up the command pallete (`cmd + shift + P`) and type `insert snippet` and it should show you the correct option:

<img width="914" alt="image" src="https://user-images.githubusercontent.com/872296/212668685-ae4b7dce-08b8-4446-91e1-17492bd3cf74.png">

Then, just select the one you're looking for:

<img width="599" alt="image" src="https://user-images.githubusercontent.com/872296/212668819-4682df14-4d50-406f-a9b2-9b80a5fa3f69.png">

### Pasting images

There's a very convenient extension that let's you paste images from your Clipboard directly into VSCode and create a file: [Paste Image VSCode extension](https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image).

## <a id="toc-tooling-docker"></a> Docker

It might not be required for you, but we use Docker to run our labs. Please see install instructions on [their official page](https://www.docker.com/products/docker-desktop/).
