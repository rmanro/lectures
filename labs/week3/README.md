# Assignment Overview: Lab for Class 11

## BusMall

### Backstory

You've been hired by a startup called BusMall, whose product is similar to the SkyMall catalog found in the seatback pockets on airplanes: a catalog of assorted high-markup products provided to a captive audience seeking a mental escape from the drudgery of travel. But in this case, BusMall catalogs are placed on TriMet transit system buses.

Since catalogs are expensive to print and distribute, and the products cost money to make and warehouse, and BusMall is a lean startup that needs to carefully watch its expenditures, BusMall wants to only feature the items that are the most likely to sell in its catalog. This means they need to do market analysis on proposed products to test their potential customer interest.

### Problem Domain

BusMall wants you to **build an app that surveys individuals to find out what products will sell**. 

To do this they want an app that displays potential products to a focus group participant and allows them to select which products they'd buy. They want to show three randomly selected products at a time, side-by-side-by-side, a total of twenty five times. 

They also need the app to track how often a product is selected. When the survey is done, they want to show the user how many times they selected each product.

The marketing team is interested in the total number of votes a product receives, as well as (potentially) the percentage of times a product was chosen when it was shown. For example, an item is shown as an option 10 times, but only selected 5 times. So it's percentage is 50%.

You are also responsible for the look and feel of the app, so don't forget a custom font, color palette, layout with semantic HTML, instructions for the survey takers, and so on.

### User Stories

Part of your assignment today is to write your own user stories. Be sure to consider the multiple roles involved: the marketing research team, the developer, and the focus group participant who will be using the application. Try to write 4-5 user stories for each role. DO THIS STEP FIRST in a file called `user_stories.md`. The commit logs in your repo will have a first couple of commits for the scaffolding process, but next you should have a 'user stories' commit that is in place before any code is written.

Reminder: user stories typically take the form of, "As X, I want Y, so that Z" but do not necessarily need that structure.

A wise student would take about 30-45 minutes to work on the user stories and also draft a technical plan for the project (a detailed to-do list of things to make, step by step and tested at each stage) before getting into the code. That time spent in thought and planning will make the code flow a lot faster. **Give yourself a series of little problems to solve (rather an a ginormous thing that you just wade through and poke at).**

Plan your work, and work your plan.

## Daily Goals

**Note: There's a lot of moving pieces in this assignment, and more details to attend to than it might seem at first. Build methodically, in small pieces, that you test and check regularly. ACP (add-commit-push) regularly on at least one non-master branch. Try sketching out a plan on paper and breaking down the problem conceptually before getting into the code.**

### Day 11

Do today's work on a branch called `collect-votes`.

**Setup**
* Create a new repo for this project called `bus-mall`.
* Scaffold your repo with the usual README, CSS, JS, and HTML files, plus a `img/` directory. Consider nesting your CSS and JS files in folders.
* Retrieve the assets from the `assets/` directory and place them in your image directory.
* Write your user stories as described above and place them in a file called `user_stories.md` in your repo. Utilize good Markdown style to make this document look nice.

**Feature goals**
* The feature you want to build today will start with selecting three random photos from the image directory and displaying them side-by-side-by-side in the browser window. The same image should not be shown twice in this group of three.
* In addition, you'll want the user to be able to click on those displayed images, and track those clicks for each image. You'll also want to track how many times each image is displayed, for statistical purposes.
* After an image is clicked, three new random images need to be automatically displayed. 
* After 25 selections have been made, turn off the event listeners on the images (to prevent additional voting) and display a list of the products with votes received with each list item looking like "3 votes for the Banana Slicer".
* To do this, you'll want to use the following:
    * a constructor function that creates an object associated with each product, and has (at a minimum) properties for the name of the product (to be used for display purposes), the filepath to its image, the number of times it has been shown, and the number of times it has been clicked. You'll probably find it useful to create a property that contains a text string you can use as an ID in HTML, as well.
    * a click handler to capture the user's clicks.


** Stretch goals **
* Disallow images to show if they were just shown in the prior group of three.
* At the end of the survey, show the percentages that the marketing team asked for in addition to the number of votes.
* Add a button that will start the survey over again for the next participant.
* Add some background music for the survey participants to enjoy (and make sure they can pause it if they don't want to listen).

**This is an individual assignment today, but you are free (heck, even encouraged) to collaborate with classmates if you want. Just be sure that if you do, be sure to make note of that collaboration in your README file.**

## Submitting Your Assignment

1. When your work is complete and ready for submission, open a Pull Request from `busmall-start` to `master`.
2. Submit the link to the above Pull Request to Canvas
3. Add a comment to this Canvas submission with answers to the following questions.
  - How did this go, overall?
  - What observations or questions do you have about what you've learned so far?
4. Once you've submitted your work, complete the merge of `busmall-start` to `master`