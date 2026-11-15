
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FUNVERSE - Entertainment Hub</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
    scroll-behavior:smooth;
}

:root{
    --bg:#0b0b16;
    --card:#19192d;
    --text:white;
    --muted:#aaa7c1;
    --purple:#a855f7;
    --blue:#2563eb;
}

body{
    background:var(--bg);
    color:var(--text);
    transition:.3s;
}

body.light{
    --bg:#f2efff;
    --card:#ffffff;
    --text:#17132c;
    --muted:#68647a;
}

header{
    background:var(--card);
    padding:18px 7%;
    position:sticky;
    top:0;
    z-index:100;
    border-bottom:1px solid #4442;
}

.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:15px;
}

.logo{
    font-size:27px;
    font-weight:800;
}

.logo span,footer span{
    color:var(--purple);
}

.nav-links{
    display:flex;
    gap:22px;
}

.nav-links a{
    color:var(--text);
    text-decoration:none;
    font-size:14px;
}

.nav-links a:hover{
    color:var(--purple);
}

.theme-btn{
    padding:11px;
    border:none;
    border-radius:50%;
    background:#7c3aed;
    color:white;
    cursor:pointer;
}

.hero{
    min-height:480px;
    padding:90px 10%;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:30px;
    background:linear-gradient(120deg,#17102f,#10152d,#29103e);
}

.hero-content{
    max-width:650px;
}

.tagline{
    color:#c084fc;
    letter-spacing:3px;
    font-size:12px;
}

.hero h1{
    font-size:55px;
    line-height:1.2;
    margin:20px 0;
}

.hero h1 span{
    color:#c084fc;
}

.hero-text{
    color:#c3c1d3;
    line-height:1.8;
    margin-bottom:30px;
}

.main-btn{
    display:inline-block;
    padding:14px 28px;
    background:linear-gradient(90deg,#7c3aed,#2563eb);
    color:white;
    border-radius:30px;
    text-decoration:none;
    font-weight:600;
    border:none;
    cursor:pointer;
}

.main-btn:hover{
    box-shadow:0 0 25px #7c3aed;
}

.hero-icon{
    font-size:150px;
    color:#c084fc;
    filter:drop-shadow(0 0 30px #7c3aed);
}

.section{
    padding:75px 8%;
    text-align:center;
}

.section-title{
    font-size:34px;
    margin-bottom:10px;
}

.section-subtitle{
    color:var(--muted);
    margin-bottom:40px;
}

.card-container{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
}

.card{
    background:var(--card);
    padding:35px 20px;
    border:1px solid #7773;
    border-radius:18px;
    transition:.3s;
}

.card:hover{
    transform:translateY(-10px);
    border-color:var(--purple);
    box-shadow:0 10px 30px #7c3aed33;
}

.card i{
    font-size:45px;
    color:var(--purple);
    margin-bottom:20px;
}

.card h3{
    margin-bottom:12px;
}

.card p{
    color:var(--muted);
    font-size:14px;
    margin-bottom:20px;
}

.card button,.fun-box button,.quiz-box button{
    border:none;
    color:white;
    background:linear-gradient(90deg,#7c3aed,#2563eb);
    padding:12px 23px;
    border-radius:25px;
    cursor:pointer;
    font-weight:600;
    margin:5px;
}

.card button:hover,.fun-box button:hover{
    box-shadow:0 0 20px #a855f7;
}

.fun-section,.music-section{
    background:#10101e;
}

body.light .fun-section,
body.light .music-section{
    background:#e9e3ff;
}

.fun-box{
    background:var(--card);
    border:1px solid #7773;
    border-radius:20px;
    padding:35px;
    margin:25px auto;
    max-width:650px;
}

.fun-box i{
    font-size:45px;
    color:#c084fc;
    margin-bottom:15px;
}

.fun-box h3{
    margin-bottom:15px;
}

.fun-box p{
    color:var(--muted);
    margin:15px 0 25px;
    min-height:30px;
}

.quiz-box,.music-box{
    max-width:650px;
    margin:auto;
    padding:35px;
    background:var(--card);
    border:1px solid #7773;
    border-radius:20px;
}

#answers{
    display:grid;
    gap:12px;
    margin-top:25px;
}

#answers button{
    border-radius:10px;
    background:#292941;
}

#answers button:disabled{
    opacity:.8;
    cursor:not-allowed;
}

#quiz-result{
    margin:20px;
    font-weight:600;
}

#score{
    color:var(--purple);
    margin-top:15px;
}

.music-box i{
    font-size:55px;
    color:var(--purple);
}

.music-box p{
    color:var(--muted);
    margin:15px 0;
}

.music-box input{
    margin:15px;
    max-width:100%;
}

.music-box audio{
    width:100%;
    margin-top:20px;
}

.challenge{
    background:linear-gradient(120deg,#29104b,#151b3e);
}

.challenge h2{
    font-size:30px;
    margin-bottom:15px;
}

.challenge p{
    color:#ddd;
    margin-bottom:25px;
}

footer{
    background:#080810;
    text-align:center;
    padding:45px 15px;
}

footer p{
    color:#aaa7c1;
    font-size:13px;
    margin:12px;
}

.social-icons{
    margin:20px;
}

.social-icons i{
    color:#a855f7;
    font-size:23px;
    margin:0 12px;
}

.copyright{
    border-top:1px solid #333;
    padding-top:20px;
}

#game-result{
    margin-top:15px;
    color:var(--purple);
    font-weight:bold;
}

@media(max-width:750px){
    .navbar{
        flex-wrap:wrap;
    }

    .nav-links{
        width:100%;
        justify-content:center;
        flex-wrap:wrap;
        gap:12px;
    }

    .hero{
        flex-direction:column;
        text-align:center;
        padding:65px 6%;
    }

    .hero h1{
        font-size:38px;
    }

    .hero-icon{
        font-size:90px;
    }

    .card-container{
        grid-template-columns:1fr;
    }

    .section{
        padding:55px 5%;
    }
}
</style>
</head>

<body>

<!-- NAVBAR -->
<header>
<nav class="navbar">

<h2 class="logo">FUN<span>VERSE</span> ✦</h2>

<div class="nav-links">
<a href="#home">Home</a>
<a href="#games">Games</a>
<a href="#fun">Fun Zone</a>
<a href="#quiz">Quiz</a>
<a href="#music">Music</a>
</div>

<button class="theme-btn" onclick="toggleTheme()">
<i class="fas fa-moon"></i>
</button>

</nav>
</header>

<!-- HERO -->
<section class="hero" id="home">

<div class="hero-content">

<p class="tagline">WELCOME TO THE WORLD OF ENTERTAINMENT</p>

<h1>ENTER A WORLD OF <span>FUN!</span></h1>

<p class="hero-text">
Play games, enjoy jokes, test your brain,
explore amazing facts and have unlimited fun.
</p>

<a href="#games" class="main-btn">
EXPLORE NOW <i class="fas fa-arrow-right"></i>
</a>

</div>

<div class="hero-icon">
<i class="fas fa-gamepad"></i>
</div>

</section>

<!-- GAMES -->
<section class="section" id="games">

<h2 class="section-title">🎮 MINI GAMES</h2>
<p class="section-subtitle">Play games and challenge yourself!</p>

<div class="card-container">

<div class="card">
<i class="fas fa-hand-scissors"></i>
<h3>Rock Paper Scissors</h3>
<p>Challenge the computer!</p>
<button onclick="playRPS()">PLAY NOW</button>
</div>

<div class="card">
<i class="fas fa-hashtag"></i>
<h3>Tic Tac Toe</h3>
<p>Play a two-player strategy game.</p>
<button onclick="playTicTacToe()">PLAY NOW</button>
</div>

<div class="card">
<i class="fas fa-brain"></i>
<h3>Number Guess</h3>
<p>Guess the secret number from 1 to 10.</p>
<button onclick="playGuess()">PLAY NOW</button>
</div>

</div>
</section>

<!-- FUN ZONE -->
<section class="section fun-section" id="fun">

<h2 class="section-title">😂 FUN ZONE</h2>
<p class="section-subtitle">Ready to laugh and explore?</p>

<div class="fun-box">
<i class="fas fa-face-laugh-beam"></i>
<h3>Random Joke Generator</h3>
<p id="joke">Click the button to get a funny joke!</p>
<button onclick="generateJoke()">GET A JOKE</button>
</div>

<div class="fun-box">
<i class="fas fa-lightbulb"></i>
<h3>Amazing Fun Facts</h3>
<p id="fact">Discover something interesting!</p>
<button onclick="generateFact()">SHOW FACT</button>
</div>

</section>

<!-- QUIZ -->
<section class="section" id="quiz">

<h2 class="section-title">🧠 QUIZ CHALLENGE</h2>
<p class="section-subtitle">Let's test your knowledge!</p>

<div class="quiz-box">

<h3 id="question">Which planet is known as the Red Planet?</h3>

<div id="answers">

<button onclick="checkAnswer(this, false)">Earth</button>
<button onclick="checkAnswer(this, true)">Mars</button>
<button onclick="checkAnswer(this, false)">Jupiter</button>
<button onclick="checkAnswer(this, false)">Venus</button>

</div>

<p id="quiz-result"></p>

<button onclick="nextQuestion()">NEXT QUESTION</button>

<p id="score">Score: 0</p>

</div>
</section>

<!-- MUSIC -->
<section class="section music-section" id="music">

<h2 class="section-title">🎵 MUSIC ZONE</h2>
<p class="section-subtitle">Enjoy your favorite music!</p>

<div class="music-box">

<i class="fas fa-headphones"></i>

<h3>FUNVERSE MUSIC PLAYER</h3>

<p>Choose an audio file from your device.</p>

<input type="file" id="audioFile" accept="audio/*">

<audio id="audioPlayer" controls></audio>

</div>
</section>

<!-- CHALLENGE -->
<section class="section challenge">

<h2>ARE YOU READY FOR MORE FUN?</h2>

<p>Your entertainment journey starts here.</p>

<a href="#home" class="main-btn">BACK TO TOP ↑</a>

</section>

<!-- FOOTER -->
<footer>

<h2>FUN<span>VERSE</span> ✦</h2>

<p>Your Daily Dose of Fun, Games and Entertainment.</p>

<div class="social-icons">
<i class="fab fa-facebook"></i>
<i class="fab fa-instagram"></i>
<i class="fab fa-youtube"></i>
</div>

<p class="copyright">
© 2026 FUNVERSE. All Rights Reserved.
</p>

</footer>

<script>

// DARK AND LIGHT MODE
function toggleTheme(){
    document.body.classList.toggle("light");
}

// ROCK PAPER SCISSORS
function playRPS(){

    const choices=["Rock","Paper","Scissors"];

    let user=prompt("Choose Rock, Paper or Scissors:");

    if(!user) return;

    user=user.trim().toLowerCase();

    if(!["rock","paper","scissors"].includes(user)){
        alert("Enter Rock, Paper or Scissors!");
        return;
    }

    let computer=choices[Math.floor(Math.random()*3)].toLowerCase();

    if(user===computer){
        alert("Computer: "+computer+"\nIt's a Draw!");
    }

    else if(
        (user==="rock" && computer==="scissors") ||
        (user==="paper" && computer==="rock") ||
        (user==="scissors" && computer==="paper")
    ){
        alert("Computer: "+computer+"\nYOU WIN! 🎉");
    }

    else{
        alert("Computer: "+computer+"\nYOU LOSE!");
    }
}

// TIC TAC TOE
function playTicTacToe(){

    let board=["1","2","3","4","5","6","7","8","9"];
    let player="X";

    const wins=[
        [0,1,2],[3,4,5],[6,7,8],
        [0,3,6],[1,4,7],[2,5,8],
        [0,4,8],[2,4,6]
    ];

    while(true){

        let display=
        board.slice(0,3).join(" | ")+"\n"+
        board.slice(3,6).join(" | ")+"\n"+
        board.slice(6,9).join(" | ");

        let move=prompt("TIC TAC TOE\n\n"+display+
        "\n\nPlayer "+player+", choose position 1-9:");

        if(move===null) return;

        let index=Number(move)-1;

        if(!Number.isInteger(index)||index<0||index>8||
        board[index]==="X"||board[index]==="O"){
            alert("Invalid move!");
            continue;
        }

        board[index]=player;

        if(wins.some(line=>line.every(i=>board[i]===player))){
            alert(display+"\nPlayer "+player+" WINS!");
            return;
        }

        if(board.every(x=>x==="X"||x==="O")){
            alert("It's a DRAW!");
            return;
        }

        player=player==="X"?"O":"X";
    }
}

// NUMBER GUESSING GAME
function playGuess(){

    let secret=Math.floor(Math.random()*10)+1;
    let attempts=3;

    while(attempts>0){

        let guess=prompt("Guess a number between 1 and 10.\nAttempts left: "+attempts);

        if(guess===null) return;

        let number=Number(guess);

        if(!Number.isInteger(number)||number<1||number>10){
            alert("Enter a valid number from 1 to 10!");
            continue;
        }

        if(number===secret){
            alert("🎉 AMAZING! You guessed correctly!");
            return;
        }

        alert(number<secret?"Too low!":"Too high!");

        attempts--;
    }

    alert("GAME OVER! The number was "+secret);
}

// JOKES
const jokes=[
    "Why did the computer go to the doctor? Because it had a virus! 😂",
    "Why was the math book sad? It had too many problems!",
    "What do you call a sleeping dinosaur? A dino-snore!",
    "Why did the student eat his homework? Because the teacher said it was a piece of cake!",
    "What is a computer's favorite snack? Microchips!",
    "Why don't eggs tell jokes? They might crack up!"
];

function generateJoke(){
    let joke=jokes[Math.floor(Math.random()*jokes.length)];
    document.getElementById("joke").innerText=joke;
}

// FUN FACTS
const facts=[
    "Octopuses have three hearts!",
    "Honey can remain edible for thousands of years when properly stored.",
    "Bananas are berries, botanically speaking!",
    "The Moon moves away from Earth by about 3.8 cm every year.",
    "A group of flamingos is called a flamboyance!",
    "Sharks existed before trees!"
];

function generateFact(){
    let fact=facts[Math.floor(Math.random()*facts.length)];
    document.getElementById("fact").innerText=fact;
}

// QUIZ QUESTIONS
const questions=[
    {
        q:"Which planet is known as the Red Planet?",
        a:["Earth","Mars","Jupiter","Venus"],
        correct:1
    },
    {
        q:"How many days are there in a leap year?",
        a:["365","366","364","360"],
        correct:1
    },
    {
        q:"What is the largest ocean?",
        a:["Atlantic","Indian","Pacific","Arctic"],
        correct:2
    },
    {
        q:"Which animal is known as the King of the Jungle?",
        a:["Tiger","Elephant","Lion","Bear"],
        correct:2
    },
    {
        q:"How many colors are in a rainbow?",
        a:["5","6","7","8"],
        correct:2
    }
];

let currentQuestion=0;
let score=0;
let answered=false;

function loadQuestion(){

    let q=questions[currentQuestion];

    document.getElementById("question").innerText=q.q;

    let answerBox=document.getElementById("answers");

    answerBox.innerHTML="";

    q.a.forEach((answer,index)=>{

        let btn=document.createElement("button");

        btn.innerText=answer;

        btn.onclick=()=>checkAnswer(btn,index===q.correct);

        answerBox.appendChild(btn);
    });

    document.getElementById("quiz-result").innerText="";
    answered=false;

}

function checkAnswer(button,isCorrect){

    if(answered) return;

    answered=true;

    if(isCorrect){
        score++;
        document.getElementById("quiz-result").innerText="Correct Answer! 🎉";
    }

    else{
        document.getElementById("quiz-result").innerText="Wrong Answer! Try again next time.";
    }

    document.querySelectorAll("#answers button").forEach(btn=>{
        btn.disabled=true;
    });

    document.getElementById("score").innerText="Score: "+score;
}

function nextQuestion(){

    if(!answered){
        alert("Please answer the question first!");
        return;
    }

    currentQuestion++;

    if(currentQuestion>=questions.length){

        alert("Quiz Finished!\nYour Score: "+score+"/"+questions.length);

        currentQuestion=0;
        score=0;

        document.getElementById("score").innerText="Score: 0";
    }

    loadQuestion();
}

// MUSIC PLAYER
document.getElementById("audioFile").addEventListener("change",function(){

    const file=this.files[0];

    if(file){
        const player=document.getElementById("audioPlayer");

        player.src=URL.createObjectURL(file);
        player.play();
    }

});

</script>

</body>
</html>
