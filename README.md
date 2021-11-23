<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.2/css/all.css" integrity="sha384-vSIIfh2YWi9wW0r9iZe7RJPrKwp6bG+s9QZMoITbCckVJqGCCRhc+ccxNcdpHuYu" crossorigin="anonymous">

[<img src="https://img.shields.io/badge/Linkedin-kathesama-blue?style=for-the-badge&logo=linkedin">](https://www.linkedin.com/in/kathesama)
<br>
![IntellijIdea](https://img.shields.io/badge/Made%20for-IntellijIdea-1f425f.svg?style=for-the-badge)
![ReactJS](https://img.shields.io/badge/-ReactJS-blue?logo=react&logoColor=white&style=for-the-badge)
<br>
[![GitHub issues](https://img.shields.io/github/issues/kathesama/starting-seed-react?style=plastic)](https://github.com/kathesama/starting-seed-react/issues)
[![GitHub forks](https://img.shields.io/github/forks/kathesama/starting-seed-react?style=plastic)](https://github.com/kathesama/starting-seed-react/network)
[![GitHub stars](https://img.shields.io/github/stars/kathesama/starting-seed-react?style=plastic)](https://github.com/kathesama/starting-seed-react/stargazers)
<br>
![GitHub last commit](https://img.shields.io/github/last-commit/kathesama/starting-seed-react?color=red&style=plastic)
![GitHub version commits](https://img.shields.io/github/commits-since/kathesama/starting-seed-react/V2.0.0.svg?color=yellow&style=plastic)
![GitHub top language](https://img.shields.io/github/languages/top/kathesama/starting-seed-react?style=plastic)
<br>
![Maintaned](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=plastic)
![OWASP](https://img.shields.io/badge/OWASP%3F-yes-green.svg?style=plastic)
![CleanCode](https://img.shields.io/badge/CleanCode%3F-yes-green.svg?style=plastic)
[![GitHub license](https://img.shields.io/github/license/kathesama/starting-seed-react?style=plastic)](https://github.com/kathesama/starting-seed-react/blob/main/LICENSE)
![GitHub repo size](https://img.shields.io/github/repo-size/kathesama/starting-seed-react?style=plastic)
<br>

# Initial seed for a react project

Steps to run this project
1. Clone this repo
> git clone https://github.com/kathesama/starting-seed-react.git
2. Run husky init
> npx husky-init
3. Config Husky with lint-staged (console excecution)
> npm i -D lint-staged<br>
> npm set-script prepare "husky install"<br>
> npm run prepare<br>
> npx husky add .husky/pre-commit 'npx lint-staged'
<br>

Then go to *.git/hooks/commit-msg*, find the main function and replace it:
> const commitMsgFilePath = process.argv[2];

with:

>const commitMsgFilePath = path.resolve(process.env.PWD, process.argv[2].substring(1));

-> Esto corrige el path para el archivo COMMIT_EDITMSG.