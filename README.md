# Resume_landingpage

##**The Purpose of the LP:**

First step for searching a new job is making the Resume/CV. Good structured and details one could raise your chances to be noticed. Many web designers , developers create websites in order to promote themselves. Then came an idea of making resume as a LP to show not only my creativity , beginning knowledge of web development and also professionalism and experience. 


The development was introduced using the HTML language for the verticals using CSS cascading style sheets and JavaScript scripts.


**Structure of LP:**

*Page 1* – Main screen.
*Page 2* – Basic information about me.
*Page 3* – Education & Experience.
*Page 4* – Projects that was done by me
*Page 5* – How to get in touch. 


What  interesting tricks does it contain?

-	On the main page when page decreases , menu hides and burger menu appears.
It was done using CSS .

-	Automatic typing : was used :

animation: type 5s steps(50, end);
and
@keyframes type{
from { width: 0; }}

-	For Social Media icons was used Font Awesome library .
-	Net was made using Javascript. 
-	Buttons “Hire me”, “Download CV”:

.button_hire{
height: 40px;
width: 200px;
background-image: linear-gradient(to left,transparent,transparent 50%,black 50%,black);
background-position: 100% 0;
background-size: 200% 100%;
transition: all .25s ease-in;
display: inline-block;
font-family: 'Open Sans Condensed', sans-serif;
font-size: 25px;
font-weight: bold;
color: black;
text-align: center;
line-height: 40px;
border: 3px solid black;
}

background-size: 200% 100% hides background image

Hover makes background-image with adding background-position and transition;

.button_hire:hover{
color:white;
background-position: 0 0;
transition: all .25s ease-in;

}

-	Buttons in “Hobbies”: 

Was used grid for location buttons then created 8 buttons. To make short border lines, I decesied to make 2 squares before and after buttons: 

.item.item4::before, 
.item.item4::after {
content: '';
position: absolute;
left: 0;
bottom: 0;
width: 45px;
border-bottom: 5px solid #ddd;
height: 45px;
border-left: 5px solid #ddd;
transition: .4s;
}

.item.item4::after {
border-left: 0;
border-bottom: 0;
border-top: 5px solid #ddd;
top: 0;
border-right: 5px solid #ddd;
right: 0;
left: auto;
}

Then used Hover to make those lines black and make them slide up and down relatively: 

.item.item4:hover:before,
.item.item4:hover:after {
content: '';
position: absolute;
left: 0;
bottom: 0;
width: 60px;
border-bottom: 5px solid black;
height: 20px;
border-left: 5px solid black;
transition: .4s;
}

.item.item4:hover:after {
border-left: 0;
border-bottom: 0;
border-top: 5px solid black;
top: 0;
border-right: 5px solid black;
right: 0;
left: auto;
}

-	Triangle in skills section made with before: 

.progress .progress-bar::before {
content: "";
border-bottom: 15px solid #000;
border-left: 15px solid transparent;
border-right: 15px solid transparent;
position: absolute;
bottom: -5px;
right: -5px;
}

(Progress – container 
Progress-bar – line)

-	Work animation: 

.smoke #words:hover li {
animation: animate 2s linear forwards;
}

@keyframes animate {
0% {
transform: rotate(0deg) translateY(0px);
opacity 1;
filter: blur(1px);
}
100% {
transform: rotate(45deg) translateY(-200px);
opacity: 0;
filter: blur(20px);}
}

Used :nth-child for other letters:

.smoke #words li:nth-child(1) {
animation-delay: 0s;
}

.smoke #words li:nth-child(2) {
animation-delay: .4s;
}

.smoke #words li:nth-child(3) {
animation-delay: .8s;
}

.smoke #words li:nth-child(4) {
animation-delay: 1.2s;
}

.smoke #words li:nth-child(5) {
animation-delay: 1.6s;
}

Pictures animation: 

.gallery-wrap {
display: flex;
flex-direction: row;
width: 100%;
height: 70vh;
margin-top: 1%;
}

.item {
flex: 1;
height: 100%;
background-position: center;
background-size: cover;
background-repeat: none;
transition: flex 0.8s ease;
}

.item:hover {
flex: 7;
}

-	After “Works”, come section with sentence and circles.

Circles were made with using ::before and ::after. 

Animations:

Rotating circle {
animation: rotate 5.5s infinite;
animation-fill-mode: forwards;
animation-timing-function: linear;
}

@keyframes rotate {
0% {
transform: rotate(0);
}
100% {
transform: rotate(360deg);
}
}

shadow animation {
box-shadow: inset -1px 4px 13px 0px #778899;
animation: shadow 3.5s infinite;
animation-direction: alternate-reverse;
animation-timing-function: linear;
}

@keyframes shadow {
0% {
box-shadow: inset -1px 4px 13px 0px #778899;
}
10% {
box-shadow: inset -3px 4px 10px 0px #778899;
}
20% {
box-shadow: inset -6px 4px 7px 0px #778899;
}
30% {
box-shadow: inset -9px 4px 4px 0px #778899;
}
40% {
box-shadow: inset -12px 4px 1px 0px #778899;
}
50% {
box-shadow: inset -14px 4px -3px 0px #778899;
}
60% {
box-shadow: inset -12px 4px -6px 0px #778899;
}
70% {
box-shadow: inset -11px 4px -9px 0px #778899;
}
80% {
box-shadow: inset -9px 4px -12px 0px #778899;
}
}

sentance {
-webkit-mask-image: linear-gradient(-75deg, rgba(0,0,0,.6) 30%, #000 50%, rgba(0,0,0,.8) 70%);
-webkit-mask-size: 200%;
animation: shine 2s infinite;
}

@-webkit-keyframes shine {
from {
-webkit-mask-position: 150%;
}
to {
-webkit-mask-position: -50%;
}
