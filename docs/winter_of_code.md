# Winter of Code

## About The Program

Winter of Code is a program aimed to increase participation for the Google Summer of Code program among students in colleges and universities.
Winter of Code is here to light up your winter spirits with the wide world of open source development. This initiative aims to prepare you for the grand Google Summer of Code. Join us for a month-long programming project with an open-source organization.

As a part of the Winter of Code, students are paired with mentors. This initiative aims at developing your skills in real-world software development in a wide range of specializations. In turn, the participating organisation gets to know your potential and also gives you the correct exposure that you need i your formative years. Above all, we hope you get encouraged into the world of open source and develop more code for the benefit of all.

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

### Winter Of Code

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


### [Config Parser RS](https://github.com/mexili/configparser-rs)
This crate provides the Ini struct which implements a basic configuration language which provides a structure similar to whatÕs found in Windows' ini files. You can use this to write Rust programs which can be customized by end users easily.

This is a simple configuration parsing utility with no dependencies built on Rust. It is inspired by Python's configparser.

