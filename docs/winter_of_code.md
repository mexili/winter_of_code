# Winter of Code

## About The Program

Winter of Code is a program aimed to increase participation for the Google Summer of Code program among students in colleges and universities.
Winter of Code is here to light up your winter spirits with the wide world of open source development. This initiative aims to prepare you for the grand Google Summer of Code. Join us for a month-long programming project with an open-source organization.

As a part of the Winter of Code, students are paired with mentors. This initiative aims at developing your skills in real-world software development in a wide range of specializations. In turn, the participating organisation gets to know your potential and also gives you the correct exposure that you need in your formative years. Above all, we hope you get encouraged into the world of open source and develop more code for the benefit of all.

Let's Build Something Awesome Together !!

## How does the program works

### Students

Students who are interested can register for the Winter of Code by filling a form below. Every student is eligible to participate in winter of code. They can pick any project as per their interest and contribute to it. For every pull request, mentors will assign a score. These scores will help students climb the leaderboard. On successful completion of the program students will be rewarded with some cool schwags.

Student registration link: https://forms.gle/k2syZR2RYdBnm8w28

### Mentors

Apart from our in-house projects, we invite people who have built a project of their own and want some contributors in it to participate in winter of code. Mentors guide the students throughout their projects and review their code samples. They provide valuable feedback and suggest possible improvements to the code. They also assign a score according to the following metric:

<table>
  <tr>
    <th>Difficulty</th>
    <th>Score</th>
  </tr>
  <tr>
    <td>Easy</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Medium</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Hard</td>
    <td>100</td>
  </tr>
</table>

Mentor registration link: https://forms.gle/k2syZR2RYdBnm8w28

### Scoring System for Winter Of Code |Mentor Requirements|

Please add the following GitHub action in your repository:

1. Create a `labels.yml` file inside `.github/workflows` folder

2. Copy the following snippet in the `labels.yml` file

```
name: 'Label Actions'
on: 
  pull_request:
    types: labeled

jobs:
  add-score:
    runs-on: ubuntu-latest
    if: startsWith(github.event.label.name, 'user')
    steps:
      - run: |
          echo ${{ github.event.label.name }}
          SCORE=${{ github.event.label.name }}
          echo $SCORE
          curl --data "score=$SCORE" --request POST https://wocleaderboard-backend.herokuapp.com/updateLeaderBoard/
```

3. When accepting the PR, add the following label before merging it. `user=<username>:score=<score>`, e.g. if the user `sansyrox` has filled a relevant PR and you are allotting 100 marks to him, add the following label `user=sansyrox:score=100` to your **PR**.

### Leaderboard
Students participating will contribute to the projects and in turn receive a score for their pull requests. These scores will be summed up and will be shown on our winter of code leaderboard. We will then have prizes for our top contributors.

## Timeline

The winter of code program will run from Feb 1 2021 to Feb 28 2021

## Projects

### [SKRIBBL](https://github.com/mexili/skribbl)
Skribbl T-Shirts online via free hand drawing on canvas or adding a text. You can also view the skribbl history that highlights the selected skribbl. You can share your T-Shirt on various social media platforms with your friends.

### [INCOGLY](https://github.com/mexili/incogly)
Incog.ly is a peer to peer video conferencing app which keeps your identity anonymous. With the feel by avatarifying the remote side into a character with the power of emotions and expressions.

### [CSSIFY](https://github.com/mexili/cssify)
CSSify provides a solution to all these problems, by offering a rock solid base which is customisable in all it's aspects. Common tasks such as defining layouts, brand colors, spacing utilities, breakpoints, typography, etc can now be completed with a few clicks with a live preview- enormously boosting your creative speed.


### [Awesome Portfolio Websites](https://github.com/smaranjitghose/awesome-portfolio-websites)
An open-source project aimed at providing free and beautiful templates to everyone for building their portfolio websites and showcase their work to the world. We take care of the SEO and Design so that others can work on their projects without worrying about a place to showcase.

Tech Stack:
- HTML, CSS, Bootstrap, JavaScript (The defacto toolkit of any web dev)
- React
- Tailwind ( For building neat custom CSS components)
- SVG Animations (If you wish to take the challenge)


### [DocLense](https://github.com/smaranjitghose/DocLense)
An open-source document scanner. It is an application which can be used to scan and save the documents via your phone. Upcoming features to scan a business card and also edge detection.

A simple flutter based application that requires basic to intermediate level of coding for it.

### [Config Parser RS](https://github.com/mexili/configparser-rs)
This crate provides the Ini struct which implements a basic configuration language which provides a structure similar to whatÕs found in Windows' ini files. You can use this to write Rust programs which can be customized by end users easily.

This is a simple configuration parsing utility with no dependencies built on Rust. It is inspired by Python's configparser.

### [JagratiWebApp](https://github.com/garg3133/JagratiWebApp)
Jagrati is an initiative by the students of IIITDM Jabalpur to provide education to poor and under-privileged children of nearby villages at our institute.

This project is a little initiative from my side to help volunteers manage the classes and other day-to-day operations at Jagrati in a better way and make it easier for them to keep track of students, classwork-homework given to them, their attendances and other things and focus more on teaching than these side activities.

### [BlogSite](https://github.com/ALPHAVIO/BlogSite)
'Blog' and 'blogging' are now loosely used for content creation and sharing on social media, especially when the content is long-form and one creates and shares content on regular basis.

This is a dynamically updating Blog posting website developed primarily using Node Js with EJS template engine and Mongoose as ODM(Object Data Modeling library). Blogs are stored using Mongo DB.


### [UniAuth](https://github.com/uniauth)
UniAuth is written to allow anyone create a fully-private and secure identity provider within seconds. It implements an OAuth authentication flow. The backend is written in `NodeJS` using `TypeScript` and the frontend utilized `tailwind css`.

Don't worry if you are not into web development, UniAuth needs client libraries in numerous languages (like Java, Kotlin, Python, PHP to name a few), implementations for different frameworks and documentations to help fellow developers to get started.     

### [Aiden](https://github.com/mexili/aiden)
Aiden is a web app utilising tensorflow.js, browser-based Machine Learning library, to enable accessible physiotherapy for the Visually Impaired and other people as well - talking through exercises by responding to users' postures in real-time.

Aiden makes it easier for users to not only complete but to improve their techniques independently.

### [AllNotes](https://github.com/harshcasper/allNotes)

This Web Application powered by MERN Stack (`MongoDB`, `NodeJS`, `ReactJS`, `Express`) will be making use of intuitive User-Interface and User-Experience to allow Students to come onto a One-Stop Portal and share Resources and Notes related to their Syllabus and Subjects which can benefit the Society as a whole. 

This Social Application would allow Students to connect over their love of Subjects and helping out of the Community in an effective way, benefitting a lot of Students in the longer run.

### [Rotten Scripts](https://github.com/harshcasper/rotten-scripts)

Rotten Scripts contains amazing and awesome scripts written in Python, JavaScript, Bash, Powershell, and more.

Consider this repository as your personal space to find or add any new script that can make life easier for us and the Open Source community too, as a Developer, and find a utility of coding to burst out of boredom. 
