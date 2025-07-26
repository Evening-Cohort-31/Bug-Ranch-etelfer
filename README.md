# Welcome to Bug Wrangler Ranch

This first self-assessment is for you to hone several Core Skills that you need as a software developer.

Taking your time now to be thorough, reflective, patient and curious will give you the foundation to be successful throughout the rest of this course and your career.

If you rush this, or think of it as a test to be "passed", then you will already be on the wrong path.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Description

Slim Jenkins offers a vacation package for people who have always wanted to join a cattle driving team across the American Midwest.

He calls it the **Kansas Slim's Cattle Adventure**.

People join a team of experienced drovers who will train them in the basics of herding cattle and driving them across hundreds of miles to their destination at Old Red's Ranch.

Unfortunately, someone gained access to the code that produces an outline of the adventure to the paying customers, so Slim has hired you to examine and fix the code.

## Learning Objectives

Here are your learning objectives for this self-assessment.

1. Able to use the debugger to step through existing code to discover root causes of bugs.
2. Drawing a sequence diagram for a project.
   > Use the [sequencediagram.org](https://sequencediagram.org/) site to generate your sequence diagram. Make sure you save your work as you go.
3. Demonstrate learning efficiency by researching concepts you haven't seen before using your peers, mentors, and the World Wide Web as resources.
4. Awareness of when you need help, and then seeking it out.

## Example Output

If you are able to fix all of the bugs, you will output similar to what is below. It will not be identical, but similar.

```sh
************************************************
**  K A N S A S   S L I M ' S   C A T T L E   **
************************************************

\|/         (__)
     '------(oo)
       ||   (__)               \|/
       ||w--||     \|/
   \|/
            \|/                     (__)
                             '------(oo)
                               ||   (__)
                               ||w--||     \|/

You will be accompanying 5 drovers as they drive 50 cattle to Old Red's Ranch for grazing

The herd is made of up the following types of cattle:
Ankole-Watusi,Brown Swiss,Brown Swiss,American Angus,Brown Swiss,
Ankina,American Angus,Ankina,Brown Swiss,Ankole-Watusi,Brown Swiss,
Brown Swiss,American Angus,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankina,Brown Swiss,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankole-Watusi,American Angus,Brown Swiss,American Angus,Ankole-Watusi,
Ankole-Watusi,American Angus,Ankina,Ankina,Ankina,Ankole-Watusi,
American Angus,Brown Swiss,American Angus,Brown Swiss,American Angus,
American Angus,Ankina,Brown Swiss,American Angus,Ankina,Brown Swiss,
American Angus,Ankole-Watusi,Ankina,American Angus,Brown Swiss

Here is the team of drovers you will be joining
        * Melvyn Hethron
        * Yancy Gresley
        * Willabella Attarge
        * Ynes Gyenes
        * Farlie Spere


Your journey will take you through the wildness of the American Midwest and across the following terrain
        * forest
        * plain
        * river
        * mountain
```

1. In the **main** module, one of the first lines of code is `const drovers = hireDrovers(cattleToDrive)`. Explain what the value of the `drovers` variable is when that line of code runs.

The drovers variable represents the array of objects that was formed when invoking the hireDrovers function using the argument of cattleToDrive. In this case because the amount of cattle to drive was 50 and the function hireDrovers essentially takes that number and divides it by five and then chooses five random objects from the database of drovers, the drovers variable is an array of five objects that are all taken from the list of drovers in the database.

2. At the bottom of the main module, you will see the following code - `for (const drover of drovers)`. Explain what the values of both the `drover` and the `drovers` variables are.

Drover is each object within the array of objects and drovers represents the entire array of objects. It's basically saying, there is a group of drovers and within it each other drovers is individually called a drover.

3. In the **journey** module, there is a `journeyMaker()` function. In that function, there is a variable named `areas` which will have the value of an object. Use your debugger to show what the value of each key is on that object. Use [Loom](https://www.loom.com) to record your session.
. 
   > (https://www.loom.com/share/5388c8bbddb044fdab679247d85bcf0c)
   > 
4. Also in the **journey** module, there is the following code:
   ```js
   for (let forestNumber = 0; forestNumber < areas.forests; forestNumber++) {
      journey.push("forest")
   }
   ```
   
  This code is a for loop where you have the key of forests that was listed under the object areas. The for loop sets a variable for the amount of forests which is listed as forestNumber and lets it start at 0. Let instead of constant allows for the value of the variable to change which is crucial when doing a for loop where when it gains more data it may add to the amount of forests. It goes on to day that if the amount of forests is less than the forests that are currently listed as the key under the object of areas, then add to the amount. This will happen each time that the for loop runs. Each time this occurs, it will push the amount of forests into the journey array that was created under the journeyMaker function. 
  
5. Explain the value of the `database` variable in the **database** module. Be as comprehensive as possible.
   
 The database variable is a collection of data that contains two main arrays, cattleTypes and drovers. These arrays contain curly brackets which each signify a seperate object that belongs to their respective array as well as keys for each object that are all followed by the value assigned to each key. The keys are the same for each object within the array, but the values differ, making them all their own objects with their own identities.
 
6. In the **drovers** module, there is a `hireDrovers()` function. You will notice the following code on that line - `(herdSize)`. What is that defining, and where does it get its value?
   
It is defining the parameter of the function of hireDrovers. When the function is invoked, herdSize will be the argument that is used to be able to get data that becomes the output of the function. In this case, when the function is invoked, the herdSize is 50, which we can get from the variable of cattleToHerd. By stating let herdSize = 0, it is not a constant and therefore can be changed based upon the varying amount of cattle that need to be herded by the drovers which makes the function more flexible and be able to be used in more that just one situation if needed.

## When You Are Done

After you have answered all the questions above, you need to push all of your code back up to Github. Follow these instructions.

1. Be in the `bug-wrangler-ranch` directory.
2. `git add --all`
3. `git commit -m "Code complete"`
4. `git push origin main`

Then go to the Learning Platform and click the **Self-assessment Complete** button.