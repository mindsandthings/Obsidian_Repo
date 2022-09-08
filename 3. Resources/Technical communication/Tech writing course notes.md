Functional documentation:

Suitable for just getting started with a new product

Explains what you see in front of you

helps you find yoru way throuh the product

often used to physical products

  

If you're unsure where to start, you can start with this. 

  

Very valuable to show user what they see in front of them without any words, because then you dont' need translations

  

Better to have software that doesn't need documentation though

  

Startegy for writing function documentation:

1. start with teh first screen

2. describe pages and their intended use

3. describe what the customers see on teh screen

4. organize the content in the order it apepars ion teh user interface (UI)

  

Don't document stuff that doesnt' need documenting, e.g. clearly labeled buttons

  

Task-oriented documentation:

-- suitable for advance useage of a product

-- barely explains what you see in front of you; focuses on how to achieve a certain result

-- helps you find your way through the product or across multipel related products

-- often used for software products

-- guides you through the steps of a process

  

Strategy for writing task-oriented documetnation

1. identify tasks customers needs to perform

2. sequence them in a logica order

3. add supporting concepts and information that the customer needs to know

4. add supporting reference information that helps them later on, once they know the products better

  

PRocess:

1. research and collect information

2. begin writing all down "dump information"

3. begin to structure and organize the information "draft"

4. present to stakeholders and colelct feedback

5. reflect the feedback in teh documentation

6. prepare final delivery

7. publish

8. collect customers feedback and maintain the documentation

  

from the home screen, click the search bar

type "cal"

select te calculator 

to add two numbers: type the first number, then "+", then the second. 

hit the equals key

the number is displayed 

  

How to Include a YouTube Video Reference in GitHub Wiki

To embed a video link to a YouTube video, use the following syntax:

1.  <div align="left">
2.        <a href="https://www.youtube.com/watch?v=Z-vZuBX0Cmk">
3.          <img src="https://img.youtube.com/vi/Z-vZuBX0Cmk/0.jpg" style="width:100%;">
4.        </a>
5.  </div>

Where:

1. Link to the video

1.  https://www.youtube.com/watch?v=Z-vZuBX0Cmk

is the link to your YouTube video;

2. Link to the thumbnail of your video

It is in this part of the code:

1.  <img src="https://img.youtube.com/vi/Z-vZuBX0Cmk/0.jpg" style="width:100%;">

where

1.  Z-vZuBX0Cmk

is the last part of your video URL.

  

Or, to summarize:

<div align="left">

      <a href=" **_link to my video_** ">

         <img src="https://img.youtube.com/vi/ **_the last part of my link_** /0.jpg" style="width:100%;">

      </a>

</div>

  

Example:

https://github.com/JordanStanchev/Getting-Started-as-User-Assistance-Developer/wiki/This-is-My-First-Page-Here

  

**Style guides**

  

Talk to other roles that nee dstyle guides:

user assistance developer

UX

content editor

translator

software architect

product owner

software developer

  

Conciseness:

avoid redundancies

link to info instea dof copying text

use visual aids (diagrams, schemes, screenshots, etc)

  

use correct and consistent terminology

use correct navigation paths

use correct product or component names - note that marketing changing names is super common

you will always have to confirm that the feature you document really exists in the software - sometimes people will remove a feature a few minutes before release and then you've documented a nonexistent feature which can have legal consequences for you company

  

MUST = absolute requirement

MUST NOT - absolute prohibition

SHOULD recommended - there may be valid reasons in some circumstances to ignore this item

SHOULD NOT - not recommended

MAY - optional, you can choose

  

use active voice so the user knows THEY are supposed to do something

  

contraction s- decide depending on your styl,e

avoid huymor

do not assume users' gender

avoid jargon words and idioms

  

**Exerc8se**

  

What a calculator app does

A calculator app is used to add, subtract, multiply, and divide numbers. For example, you can use it to calculate the total cost of multiple items if you know if the cost of each item. 

  

How to sum up the price of coffee and a sandwich

1. Go to your phone's home screen.  [picture]

2. Tap the search box to open search.  [picture]

3. Type "cal" into search.

4. Open the app by tapping on the calculator app's icon in the list of apps.   [picture]

5. Tap the "AC" button to clear the app, if the app is not cleared.  [picture with circled]

6. Enter the cost of the coffee in dollars by tapping the "1" button. [picture with circled]

7. Tap the "+" key to tell it you want to add a number.[picture with circled]

8. Enter the cost of the sandwich in dollars by tappign the "2" button once. [picture with circled]

9. Tap the "=" button to get the total. [picture with circled]

You will now see the total displayed. [picture with circled]

  

  

  

COmmon information types:

concept

procedure

process

principle

fact

structure

classification

  

DITA types of concept, task, and reference. DITA is a type of XML; DITA topics are assembled into documents using DITA maps. Most types fit into these, and you don't need to know all of them, just these three. 

  

Instructions:

1. choose project ot document

2. define your target audience

3. define the deliverable you will create fo ryour target audience

4. develop the software documentation and information deliverables (that is, your user assistance fo rthe software product)

5. publish teh user assistance deliverables and collect users' feedback

  

Task:

1. summary

2. prerequisite

3. steps

only one set of steps to achieving the goal. you do not need to tell them all the other different ways of doing that; just one set of steps. 

Rule of thumb: if you find yourself trying to document more than 10 steps, it's too many. Something is probably wrong. 

Example is very important. 

  

  

Concept topic:

  

## Concept

### Summary

_In this section provide a brief summary of the conceptual information you plan to provide. This should allow the users to understand what they will find on this page._

### Detailed Overview

_In this section provide the details related to your conceptual information. This should allow the users to deep dive into understanding the concept. Use appropriate graphic or video files to explain the details._

### Example

_In this section provide an example of the conceptual information you plan to provide. A specific example often helps your users better understand a concept._

  

  

  

## 12 principles

  

1. Decide who you are writing for

Who are they? Where do they live? In what environment? Internet use etc. Employer rules about personal devices and internet access etc. What devices will they use. Age of audience. 

2. Identify the information needs

3. Decide on the style

sometimes more informal vs more formal

4. decide which deliverables to create

you may have different target audiences and targe groups

for agile: need to know order and sequence

5. decide which tool ot use to create your content

can it scale as it grows over time? or will it fail you when you ahve to deliver? (e.g. don't use word) sometimes you will wind up with multiple audiences and they will want personalized info. 

6. define the content structure

7. decide which information chanells to use

(and make sure the company will let you use them)

8. write documentation

9. use images and video when appropriate (he emphasizes video really hard)

10. publisht he first version

11. collect feedback and improve

12. repeat

maintenance and update cycles

  

## DITA

Concept: answers "wat is" questions. use to introduce background or overview info 

Task: "How do I". Remember, concept is already explaine dsomewhere else. Includes sectiosn for describing the context, prerequeisites, actual steps, expected results, example, and expected next steps for a task. 

Reference: factual material like programming language commands. bibliographies, catalogues, ingredients, structured descriptive prose. 

  

### Authoring in DITA:

based on info types

deliverables strtucture organized outside topic via maps

modularized and reusable

context-free

  

### Info architecture in DITA

different levels of content reuse: deliverable, map, topic, topic element

enables the development of linking strategy - across deliverables, between maps, between topics; automatically generated links or manually inserted lnks

filter and flag of final deliberable, based on profiling values (conditions)

construct taxonomies for purpose of constructing controlled vocabularies

  

# Graphics

##Types of graphics

###Types of graphics: process

Steps you have to do as a customer, and steps that happen in the background and you need to know what they are but you don't need to do anything. 

###Types of graphics: Architecture

###Types of graphics: infographics

more info than a single architecture or process diagram