# Journal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Our Little Journal ♡</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@400;500;600&display=swap');

*{
    box-sizing:border-box;
}

body{
    margin:0;
    background:#f8f2e9;
    color:#493a30;
    font-family:"DM Sans",sans-serif;
}

button,
input,
textarea,
select{
    font-family:inherit;
}

button{
    cursor:pointer;
}

.hidden{
    display:none!important;
}

/* =========================
   LOGIN
========================= */

.login-screen{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;

    background:
    radial-gradient(circle at 20% 20%,#ead6d1,transparent 30%),
    radial-gradient(circle at 80% 80%,#e9ddc9,transparent 30%),
    #f8f2e9;
}

.login-box{
    width:430px;
    max-width:100%;
    background:#fffdf8;
    border:1px solid #dfd0bd;
    padding:40px;
    border-radius:18px;
    box-shadow:0 25px 70px rgba(70,50,35,.13);
    text-align:center;
}

.login-heart{
    font-size:50px;
    color:#a67575;
}

.login-box h1{
    font-family:"Cormorant Garamond",serif;
    font-size:48px;
    margin:0;
    font-weight:600;
}

.subtitle{
    color:#948274;
    font-size:12px;
    line-height:1.8;
    margin:8px 0 25px;
}

.input-group{
    text-align:left;
    margin:14px 0;
}

.input-group label{
    display:block;
    font-size:11px;
    font-weight:bold;
    margin-bottom:7px;
}

.input-group input,
.input-group textarea,
.input-group select{
    width:100%;
    padding:13px;
    border:1px solid #dfd0bd;
    background:#fffefa;
    border-radius:9px;
    outline:none;
    color:#493a30;
}

.input-group input:focus,
.input-group textarea:focus{
    border-color:#a67575;
}

.primary{
    width:100%;
    padding:13px;
    border:0;
    border-radius:9px;
    background:#634a39;
    color:white;
    font-weight:bold;
    margin-top:10px;
}

.primary:hover{
    background:#49372b;
}

.switch{
    margin-top:18px;
    font-size:12px;
    color:#948274;
}

.switch button{
    border:0;
    background:none;
    color:#a67575;
    font-weight:bold;
}

.error{
    min-height:18px;
    color:#a04d4d;
    font-size:12px;
}

/* =========================
   MAIN LAYOUT
========================= */

.app{
    min-height:100vh;
}

.layout{
    min-height:100vh;
    display:grid;
    grid-template-columns:245px 1fr;
}

/* =========================
   SIDEBAR
========================= */

.sidebar{
    background:#49382d;
    color:#f9eee2;
    padding:28px 17px;
    display:flex;
    flex-direction:column;
}

.logo{
    text-align:center;
    margin-bottom:30px;
}

.logo span{
    font-size:30px;
}

.logo h2{
    font-family:"Cormorant Garamond",serif;
    font-size:29px;
    font-weight:500;
    margin:3px 0;
}

.logo small{
    color:#c9b6a3;
    font-size:8px;
    letter-spacing:2px;
}

.nav{
    width:100%;
    padding:12px 13px;
    margin:3px 0;
    border:0;
    border-radius:8px;
    background:none;
    color:#d9cabb;
    text-align:left;
    font-size:12px;
}

.nav:hover,
.nav.active{
    background:#654d3d;
    color:white;
}

.logout{
    margin-top:auto;
}

/* =========================
   CONTENT
========================= */

.content{
    padding:35px clamp(18px,5vw,65px);
}

.topbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:25px;
}

.topbar small{
    color:#9a8879;
    font-size:9px;
    letter-spacing:2px;
    font-weight:bold;
}

.topbar h1{
    font-family:"Cormorant Garamond",serif;
    font-size:43px;
    margin:2px 0 0;
    font-weight:500;
}

.new-btn{
    width:auto;
    padding:12px 18px;
}

/* =========================
   WELCOME
========================= */

.welcome{
    background:
    linear-gradient(135deg,#ead8d4,#f1e5d2);
    border:1px solid #dfd0bd;
    border-radius:15px;
    padding:35px;
}

.welcome small{
    color:#a67575;
    font-weight:bold;
    letter-spacing:2px;
    font-size:9px;
}

.welcome h2{
    font-family:"Cormorant Garamond",serif;
    font-size:38px;
    margin:8px 0;
}

.welcome p{
    max-width:650px;
    color:#76675b;
    font-size:13px;
    line-height:1.8;
}

.outline{
    padding:11px 16px;
    border:1px solid #cdb8a2;
    background:#fffdf8;
    border-radius:8px;
    color:#634a39;
    font-weight:bold;
}

/* =========================
   STATS
========================= */

.stats{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:12px;
    margin:15px 0 30px;
}

.stat{
    background:#fffdf8;
    border:1px solid #dfd0bd;
    border-radius:11px;
    padding:18px;
}

.stat small{
    color:#968474;
    font-size:10px;
}

.stat h3{
    font-family:"Cormorant Garamond",serif;
    font-size:30px;
    margin:5px 0 0;
}

/* =========================
   JOURNAL
========================= */

.section-title{
    font-family:"Cormorant Garamond",serif;
    font-size:31px;
    margin:20px 0 12px;
}

.entries{
    display:grid;
    gap:12px;
}

.entry{
    background:#fffdf8;
    border:1px solid #dfd0bd;
    border-radius:11px;
    padding:17px;
    display:flex;
    gap:14px;
    transition:.2s;
    cursor:pointer;
}

.entry:hover{
    transform:translateY(-2px);
    box-shadow:0 12px 25px rgba(70,50,35,.08);
}

.entry-icon{
    width:43px;
    height:43px;
    flex-shrink:0;
    border-radius:50%;
    background:#ead7d4;
    display:grid;
    place-items:center;
}

.entry h3{
    font-family:"Cormorant Garamond",serif;
    font-size:21px;
    margin:0 0 5px;
}

.meta{
    color:#978577;
    font-size:10px;
}

.preview{
    color:#77695d;
    font-size:11px;
    margin-top:7px;
    white-space:nowrap;
    overflow:hidden;
    text-overflow:ellipsis;
}

/* =========================
   PAPER
========================= */

.paper{
    max-width:850px;
    background:#fffdf8;
    border:1px solid #dfd0bd;
    border-radius:14px;
    padding:clamp(20px,5vw,45px);
    box-shadow:0 10px 30px rgba(70,50,35,.05);
}

.paper h2{
    font-family:"Cormorant Garamond",serif;
    font-size:37px;
    margin:0 0 20px;
}

.paper textarea{
    width:100%;
    min-height:330px;
    resize:vertical;
    border:1px solid #dfd0bd;
    border-radius:8px;
    padding:18px;
    line-height:2;
    outline:none;

    background:
    repeating-linear-gradient(
        to bottom,
        #fffdf8 0px,
        #fffdf8 31px,
        #eadfd1 32px
    );
}

.form-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:12px;
}

.actions{
    display:flex;
    justify-content:flex-end;
    gap:8px;
    margin-top:15px;
}

/* =========================
   SHARING
========================= */

.share-box{
    margin-top:20px;
    padding:20px;
    background:#f5ebe4;
    border:1px solid #dfd0bd;
    border-radius:10px;
}

.share-box h3{
    font-family:"Cormorant Garamond",serif;
    font-size:23px;
    margin:0 0 5px;
}

.share-box p{
    color:#8f7f70;
    font-size:11px;
    line-height:1.7;
}

.share-status{
    margin-top:10px;
    color:#a67575;
    font-size:11px;
    font-weight:bold;
}

/* =========================
   OUR SPACE
========================= */

.couple-card{
    max-width:650px;
    background:#fffdf8;
    border:1px solid #dfd0bd;
    border-radius:14px;
    padding:30px;
}

.couple-card h2{
    font-family:"Cormorant Garamond",serif;
    font-size:37px;
    margin:5px 0;
}

.code{
    background:#f0e4d3;
    padding:17px;
    border-radius:9px;
    text-align:center;
    font-family:monospace;
    font-size:22px;
    letter-spacing:3px;
    margin:12px 0;
}

.status{
    margin-top:15px;
    color:#a67575;
    font-size:12px;
    font-weight:bold;
}

/* =========================
   SEARCH
========================= */

.search{
    width:100%;
    padding:13px;
    border:1px solid #dfd0bd;
    border-radius:9px;
    outline:none;
    background:#fffdf8;
    margin-bottom:15px;
}

/* =========================
   MODAL
========================= */

dialog{
    width:min(92%,700px);
    border:1px solid #dfd0bd;
    border-radius:15px;
    padding:30px;
    background:#fffdf8;
    color:#493a30;
    box-shadow:0 30px 90px rgba(30,20,15,.3);
}

dialog::backdrop{
    background:rgba(50,35,25,.7);
}

.close{
    float:right;
    border:0;
    background:none;
    font-size:27px;
    color:#958375;
}

#modalTitle{
    font-family:"Cormorant Garamond",serif;
    font-size:37px;
}

#modalContent{
    border-top:1px solid #dfd0bd;
    padding-top:20px;
    line-height:2;
    white-space:pre-wrap;
    overflow-wrap:anywhere;
}

.permission{
    margin:18px 0;
    padding:14px;
    border-radius:8px;
    background:#f5ebe4;
    font-size:11px;
}

/* =========================
   MOBILE
========================= */

@media(max-width:800px){

    .layout{
        display:block;
    }

    .sidebar{
        position:sticky;
        top:0;
        z-index:20;
        padding:12px;
    }

    .logo{
        margin-bottom:8px;
    }

    .logo h2{
        font-size:23px;
    }

    .nav{
        display:inline-block;
        width:auto;
        padding:9px 10px;
    }

    .logout{
        margin-top:5px;
    }

    .content{
        padding:22px 14px;
    }

    .topbar h1{
        font-size:32px;
    }

    .stats{
        grid-template-columns:1fr;
    }

    .form-grid{
        grid-template-columns:1fr;
    }

    .welcome{
        padding:23px;
    }

    .welcome h2{
        font-size:31px;
    }

}

</style>
</head>

<body>


<!-- ==================================================
     LOGIN
================================================== -->

<div id="loginScreen" class="login-screen">

    <div class="login-box">

        <div class="login-heart">
            ♡
        </div>

        <h1>
            Our Little Journal
        </h1>

        <p class="subtitle">
            A private little place for
            <br>
            your stories, memories and feelings.
            <br><br>
            <b>Just the two of you.</b>
        </p>


        <div id="nameGroup" class="input-group hidden">

            <label>
                Your Name
            </label>

            <input
                id="name"
                placeholder="Your name"
            >

        </div>


        <div class="input-group">

            <label>
                Email
            </label>

            <input
                id="email"
                type="email"
                placeholder="your@email.com"
            >

        </div>


        <div class="input-group">

            <label>
                Password
            </label>

            <input
                id="password"
                type="password"
                placeholder="At least 6 characters"
            >

        </div>


        <div id="authError" class="error"></div>


        <button
            id="authButton"
            class="primary"
        >
            Log In
        </button>


        <div class="switch">

            <span id="switchText">
                Don't have an account?
            </span>

            <button id="switchButton">
                Create Account
            </button>

        </div>

    </div>

</div>


<!-- ==================================================
     APP
================================================== -->

<div id="app" class="app hidden">

<div class="layout">


<!-- SIDEBAR -->

<aside class="sidebar">

    <div class="logo">

        <span>♡</span>

        <h2>
            Our Little Journal
        </h2>

        <small>
            YOUR LITTLE SPACE
        </small>

    </div>


    <button
        class="nav active"
        data-page="home"
    >
        🏠 Home
    </button>


    <button
        class="nav"
        data-page="write"
    >
        ✎ Write
    </button>


    <button
        class="nav"
        data-page="private"
    >
        🔒 My Pages
    </button>


    <button
        class="nav"
        data-page="shared"
    >
        ♡ Shared Pages
    </button>


    <button
        class="nav"
        data-page="couple"
    >
        💌 Our Space
    </button>


    <button
        class="nav"
        data-page="settings"
    >
        ⚙ Settings
    </button>


    <button
        id="logoutButton"
        class="nav logout"
    >
        ⇥ Log Out
    </button>

</aside>


<!-- CONTENT -->

<main class="content">


<div class="topbar">

    <div>

        <small id="today"></small>

        <h1 id="pageTitle">
            Welcome back ♡
        </h1>

    </div>


    <button
        id="topNewButton"
        class="primary new-btn"
    >
        + New Page
    </button>

</div>


<!-- ==================================================
     HOME
================================================== -->

<section id="homePage">

    <div class="welcome">

        <small>
            YOUR LITTLE CORNER
        </small>

        <h2>
            Welcome to your little story. ♡
        </h2>

        <p>
            Write the things you want to remember.
            Your thoughts, your feelings, your memories,
            or even the random little things that made
            your day special.
        </p>

        <button
            class="outline"
            id="writeNow"
        >
            Write a Page ♡
        </button>

    </div>


    <div class="stats">

        <div class="stat">

            <small>
                My private pages
            </small>

            <h3 id="privateCount">
                0
            </h3>

        </div>


        <div class="stat">

            <small>
                Pages I shared
            </small>

            <h3 id="mySharedCount">
                0
            </h3>

        </div>


        <div class="stat">

            <small>
                Pages shared with me
            </small>

            <h3 id="receivedCount">
                0
            </h3>

        </div>

    </div>


    <h2 class="section-title">
        Recent Pages
    </h2>

    <div
        id="recentEntries"
        class="entries"
    ></div>

</section>


<!-- ==================================================
     WRITE
================================================== -->

<section
    id="writePage"
    class="hidden"
>

<div class="paper">

    <small
        style="
        color:#a67575;
        letter-spacing:2px;
        font-weight:bold;
        font-size:9px;
        "
    >
        NEW PAGE
    </small>

    <h2>
        Write your heart out.
    </h2>


    <form id="journalForm">

        <input
            type="hidden"
            id="editingId"
        >


        <div class="input-group">

            <label>
                Title
            </label>

            <input
                id="entryTitle"
                required
                maxlength="100"
                placeholder="What should you call this memory?"
            >

        </div>


        <div class="form-grid">

            <div class="input-group">

                <label>
                    Date
                </label>

                <input
                    id="entryDate"
                    type="date"
                    required
                >

            </div>


            <div class="input-group">

                <label>
                    Mood
                </label>

                <select id="entryMood">

                    <option>Happy ☀️</option>
                    <option>Love 💗</option>
                    <option>Calm 🌿</option>
                    <option>Grateful ♡</option>
                    <option>Sad ☁️</option>
                    <option>Tired ☾</option>
                    <option>Angry 🔥</option>
                    <option>Hopeful ✧</option>

                </select>

            </div>

        </div>


        <div class="input-group">

            <label>
                Dear Journal...
            </label>

            <textarea
                id="entryContent"
                required
                placeholder="Write whatever you want..."
            ></textarea>

        </div>


        <!-- PERMISSION -->

        <div class="share-box">

            <h3>
                Who can see this page?
            </h3>

            <p>
                Every page is private when you create it.
                If you want your partner to read it,
                give permission below.
            </p>


            <label>

                <input
                    id="sharePermission"
                    type="checkbox"
                >

                ♡ Allow my partner to read this page

            </label>


            <div
                id="shareStatus"
                class="share-status"
            >
                🔒 Only me
            </div>

        </div>


        <div class="actions">

            <button
                type="button"
                id="cancelWrite"
                class="outline"
            >
                Cancel
            </button>


            <button
                type="submit"
                class="primary"
                style="width:auto;"
            >
                Save Page ♡
            </button>

        </div>

    </form>

</div>

</section>


<!-- ==================================================
     PRIVATE
================================================== -->

<section
    id="privatePage"
    class="hidden"
>

<h2 class="section-title">
    My Pages 🔒
</h2>

<p style="font-size:12px;color:#968474;">
    Pages here are yours. Your partner cannot see
    the private ones.
</p>


<input
    id="privateSearch"
    class="search"
    placeholder="Search your pages..."
>


<div
    id="privateEntries"
    class="entries"
></div>

</section>


<!-- ==================================================
     SHARED
================================================== -->

<section
    id="sharedPage"
    class="hidden"
>

<h2 class="section-title">
    Shared Pages ♡
</h2>

<p style="font-size:12px;color:#968474;">
    These are pages that were given permission
    to be seen by the other person.
</p>


<input
    id="sharedSearch"
    class="search"
    placeholder="Search shared pages..."
>


<div
    id="sharedEntries"
    class="entries"
></div>

</section>


<!-- ==================================================
     COUPLE
================================================== -->

<section
    id="couplePage"
    class="hidden"
>

<div class="couple-card">

    <small
        style="
        color:#a67575;
        letter-spacing:2px;
        font-size:9px;
        font-weight:bold;
        "
    >
        JUST THE TWO OF YOU
    </small>

    <h2>
        Our Space 💌
    </h2>

    <p
        style="
        color:#8f7f70;
        font-size:12px;
        line-height:1.8;
        "
    >
        Connect your accounts first.
        Once connected, either of you can choose
        which pages you want to share.
    </p>


    <label
        style="
        font-size:11px;
        font-weight:bold;
        "
    >
        Your Couple Code
    </label>


    <div
        id="myCode"
        class="code"
    >
        ------
    </div>


    <button
        id="copyCode"
        class="outline"
    >
        Copy My Code
    </button>


    <hr
        style="
        border:0;
        border-top:1px solid #dfd0bd;
        margin:25px 0;
        "
    >


    <div class="input-group">

        <label>
            Enter your partner's Couple Code
        </label>

        <input
            id="partnerCode"
            placeholder="Example: A7K9P2QX"
        >

    </div>


    <button
        id="connectButton"
        class="primary"
    >
        Connect Us ♡
    </button>


    <div
        id="coupleStatus"
        class="status"
    ></div>

</div>

</section>


<!-- ==================================================
     SETTINGS
================================================== -->

<section
    id="settingsPage"
    class="hidden"
>

<div class="paper">

    <h2>
        Settings
    </h2>

    <p
        id="accountEmail"
        style="
        color:#968474;
        font-size:12px;
        "
    ></p>


    <hr
        style="
        border:0;
        border-top:1px solid #dfd0bd;
        margin:20px 0;
        "
    >


    <h3>
        🔒 Privacy
    </h3>

    <p
        style="
        color:#8f7f70;
        font-size:12px;
        line-height:1.8;
        "
    >
        Your journal pages are private by default.
        Your partner can only read a page after you
        explicitly give permission to that page.
    </p>

</div>

</section>


</main>

</div>

</div>


<!-- ==================================================
     ENTRY MODAL
================================================== -->

<dialog id="entryModal">

<button
    id="closeModal"
    class="close"
>
    ×
</button>

<div
    id="modalDate"
    style="
    color:#a67575;
    font-size:9px;
    letter-spacing:2px;
    font-weight:bold;
    "
></div>

<h2 id="modalTitle"></h2>

<div id="modalMood"></div>

<div
    id="modalPermission"
    class="permission"
></div>

<div id="modalContent"></div>


<div
    id="modalActions"
    class="actions"
>

    <button
        id="editButton"
        class="outline"
    >
        Edit
    </button>

    <button
        id="permissionButton"
        class="outline"
    >
        Change Permission
    </button>

    <button
        id="deleteButton"
        class="outline"
        style="
        color:#a04d4d;
        border-color:#e3c5c5;
        "
    >
        Delete
    </button>

</div>

</dialog>


<!-- ==================================================
     FIREBASE
================================================== -->

<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-app-compat.js"></script>

<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-auth-compat.js"></script>

<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore-compat.js"></script>


<script>

/*
========================================================
FIREBASE CONFIG

PALITAN MO ITO NG CONFIG MULA SA FIREBASE.
========================================================
*/

const firebaseConfig = {

    apiKey:
        "PASTE_YOUR_API_KEY",

    authDomain:
        "PASTE_YOUR_PROJECT.firebaseapp.com",

    projectId:
        "PASTE_YOUR_PROJECT_ID",

    storageBucket:
        "PASTE_YOUR_PROJECT.appspot.com",

    messagingSenderId:
        "PASTE_YOUR_SENDER_ID",

    appId:
        "PASTE_YOUR_APP_ID"

};


firebase.initializeApp(firebaseConfig);

const auth = firebase.auth();

const db = firebase.firestore();


/* ======================================================
   VARIABLES
====================================================== */

let user = null;

let userData = null;

let entries = [];

let selectedEntry = null;

let registerMode = false;


/* ======================================================
   HELPERS
====================================================== */

function $(id){
    return document.getElementById(id);
}


function today(){

    const d = new Date();

    return d.getFullYear()
        + "-"
        + String(d.getMonth()+1).padStart(2,"0")
        + "-"
        + String(d.getDate()).padStart(2,"0");

}


function prettyDate(date){

    if(!date) return "";

    return new Date(date + "T12:00:00")
        .toLocaleDateString(
            undefined,
            {
                year:"numeric",
                month:"long",
                day:"numeric"
            }
        );

}


function escapeHTML(text=""){

    return String(text).replace(
        /[&<>"']/g,
        char => ({
            "&":"&amp;",
            "<":"&lt;",
            ">":"&gt;",
            '"':"&quot;",
            "'":"&#039;"
        })[char]
    );

}


/* ======================================================
   LOGIN / REGISTER SWITCH
====================================================== */

$("switchButton").onclick = function(){

    registerMode = !registerMode;

    $("nameGroup")
        .classList
        .toggle(
            "hidden",
            !registerMode
        );

    $("authButton").textContent =
        registerMode
        ? "Create Account"
        : "Log In";

    $("switchText").textContent =
        registerMode
        ? "Already have an account?"
        : "Don't have an account?";

    $("switchButton").textContent =
        registerMode
        ? "Log In"
        : "Create Account";

    $("authError").textContent = "";

};


/* ======================================================
   LOGIN
====================================================== */

$("authButton").onclick = async function(){

    const email =
        $("email").value.trim();

    const password =
        $("password").value;

    $("authError").textContent = "";


    if(!email || !password){

        $("authError").textContent =
            "Please enter your email and password.";

        return;

    }


    try{

        if(registerMode){

            const name =
                $("name").value.trim();


            if(!name){

                $("authError").textContent =
                    "Please enter your name.";

                return;

            }


            const result =
                await auth
                    .createUserWithEmailAndPassword(
                        email,
                        password
                    );


            await result.user.updateProfile({
                displayName:name
            });


            await createProfile(
                result.user,
                name
            );


        }else{

            await auth
                .signInWithEmailAndPassword(
                    email,
                    password
                );

        }

    }catch(error){

        console.error(error);

        $("authError").textContent =
            getAuthError(error);

    }

};


function getAuthError(error){

    if(error.code ===
        "auth/email-already-in-use")
        return "Email is already registered.";

    if(error.code ===
        "auth/invalid-email")
        return "Invalid email.";

    if(
        error.code === "auth/wrong-password" ||
        error.code === "auth/invalid-credential"
    )
        return "Wrong email or password.";

    if(error.code ===
        "auth/user-not-found")
        return "Account not found.";

    if(error.code ===
        "auth/weak-password")
        return "Password must be at least 6 characters.";

    return "Something went wrong.";

}


/* ======================================================
   COUPLE CODE
====================================================== */

function makeCode(){

    const chars =
        "ABCDEFGHJKLMNPQRSTUVWXYZ23456789";

    let code = "";

    for(let i=0;i<8;i++){

        code += chars[
            Math.floor(
                Math.random()*chars.length
            )
        ];

    }

    return code;

}


/* ======================================================
   CREATE PROFILE
====================================================== */

async function createProfile(firebaseUser,name){

    let code = makeCode();

    let exists = true;


    while(exists){

        const snapshot =
            await db
                .collection("users")
                .where(
                    "coupleCode",
                    "==",
                    code
                )
                .limit(1)
                .get();


        exists = !snapshot.empty;


        if(exists)
            code = makeCode();

    }


    await db
        .collection("users")
        .doc(firebaseUser.uid)
        .set({

            name:name,

            email:firebaseUser.email,

            coupleCode:code,

            partnerUid:null,

            createdAt:
                firebase.firestore.FieldValue
                    .serverTimestamp()

        });

}


/* ======================================================
   AUTH STATE
====================================================== */

auth.onAuthStateChanged(
    async firebaseUser => {

        if(!firebaseUser){

            user = null;

            $("loginScreen")
                .classList
                .remove("hidden");

            $("app")
                .classList
                .add("hidden");

            return;

        }


        user = firebaseUser;


        await loadUser();


        $("loginScreen")
            .classList
            .add("hidden");

        $("app")
            .classList
            .remove("hidden");


        $("accountEmail").textContent =
            user.email;


        $("myCode").textContent =
            userData.coupleCode;


        startApp();

    }
);


/* ======================================================
   LOAD USER
====================================================== */

async function loadUser(){

    let doc =
        await db
            .collection("users")
            .doc(user.uid)
            .get();


    if(!doc.exists){

        await createProfile(
            user,
            user.displayName || "User"
        );

        doc =
            await db
                .collection("users")
                .doc(user.uid)
                .get();

    }


    userData =
        doc.data();

}


/* ======================================================
   START APP
====================================================== */

function startApp(){

    $("today").textContent =
        new Date()
            .toLocaleDateString(
                undefined,
                {
                    weekday:"long",
                    month:"long",
                    day:"numeric"
                }
            )
            .toUpperCase();


    $("entryDate").value =
        today();


    loadEntries();

    showPage("home");

}


/* ======================================================
   NAVIGATION
====================================================== */

const pages = [
    "home",
    "write",
    "private",
    "shared",
    "couple",
    "settings"
];


function showPage(page){

    pages.forEach(name => {

        $(name+"Page")
            .classList
            .toggle(
                "hidden",
                name !== page
            );

    });


    document
        .querySelectorAll(".nav")
        .forEach(button => {

            button.classList.toggle(
                "active",
                button.dataset.page === page
            );

        });


    const titles = {

        home:"Welcome back ♡",

        write:"Write your heart out.",

        private:"My Private Pages",

        shared:"Shared With Us ♡",

        couple:"Our Space 💌",

        settings:"Settings"

    };


    $("pageTitle").textContent =
        titles[page];


    if(page === "home")
        renderHome();

    if(page === "private")
        renderPrivate();

    if(page === "shared")
        renderShared();

}


document
    .querySelectorAll(".nav")
    .forEach(button => {

        if(!button.dataset.page)
            return;

        button.onclick = () => {

            if(
                button.dataset.page ===
                "write"
            )
                newPage();

            showPage(
                button.dataset.page
            );

        };

    });


$("topNewButton").onclick = () => {

    newPage();

    showPage("write");

};


$("writeNow").onclick = () => {

    newPage();

    showPage("write");

};


$("cancelWrite").onclick = () => {

    newPage();

    showPage("home");

};


/* ======================================================
   LOAD ENTRIES
====================================================== */

async function loadEntries(){

    if(!user)
        return;


    const ownSnapshot =
        await db
            .collection("entries")
            .where(
                "ownerUid",
                "==",
                user.uid
            )
            .get();


    const sharedSnapshot =
        await db
            .collection("entries")
            .where(
                "sharedWith",
                "array-contains",
                user.uid
            )
            .get();


    const map = new Map();


    ownSnapshot.docs.forEach(doc => {

        map.set(
            doc.id,
            {
                id:doc.id,
                ...doc.data()
            }
        );

    });


    sharedSnapshot.docs.forEach(doc => {

        map.set(
            doc.id,
            {
                id:doc.id,
                ...doc.data()
            }
        );

    });


    entries =
        [...map.values()];

    renderHome();

    renderPrivate();

    renderShared();

}


/* ======================================================
   NEW PAGE
====================================================== */

function newPage(){

    $("journalForm").reset();

    $("editingId").value = "";

    $("entryDate").value =
        today();

    $("sharePermission").checked =
        false;

    $("shareStatus").textContent =
        "🔒 Only me";

}


/* ======================================================
   SHARE CHECKBOX
====================================================== */

$("sharePermission").onchange = function(){

    if(this.checked){

        if(!userData.partnerUid){

            this.checked = false;

            alert(
                "Connect with your partner first."
            );

            return;

        }


        $("shareStatus").textContent =
            "♡ Your partner can read this page.";

    }else{

        $("shareStatus").textContent =
            "🔒 Only me";

    }

};


/* ======================================================
   SAVE ENTRY
====================================================== */

$("journalForm").onsubmit =
async function(event){

    event.preventDefault();


    const editingId =
        $("editingId").value;


    const shared =
        $("sharePermission").checked;


    const data = {

        ownerUid:user.uid,

        ownerName:
            user.displayName || "User",

        title:
            $("entryTitle").value.trim(),

        date:
            $("entryDate").value,

        mood:
            $("entryMood").value,

        content:
            $("entryContent").value.trim(),

        sharedWith:
            shared && userData.partnerUid
            ? [userData.partnerUid]
            : [],

        updatedAt:
            firebase.firestore.FieldValue
                .serverTimestamp()

    };


    try{

        if(editingId){

            await db
                .collection("entries")
                .doc(editingId)
                .update(data);

        }else{

            data.createdAt =
                firebase.firestore.FieldValue
                    .serverTimestamp();


            await db
                .collection("entries")
                .add(data);

        }


        alert(
            "Saved successfully. ♡"
        );


        newPage();

        await loadEntries();

        showPage("home");


    }catch(error){

        console.error(error);

        alert(
            "Could not save the page."
        );

    }

};


/* ======================================================
   ENTRY CARD
====================================================== */

function makeEntryCard(entry){

    const icon =
        entry.mood
        ? entry.mood.split(" ")[1] || "♡"
        : "♡";


    const isMine =
        entry.ownerUid === user.uid;


    return `

        <div
            class="entry"
            data-entry="${entry.id}"
        >

            <div class="entry-icon">
                ${icon}
            </div>

            <div style="min-width:0;flex:1;">

                <h3>
                    ${escapeHTML(entry.title)}
                </h3>

                <div class="meta">

                    ${prettyDate(entry.date)}

                    ·

                    ${escapeHTML(entry.mood)}

                    ·

                    ${
                        isMine
                        ? (
                            entry.sharedWith &&
                            entry.sharedWith.length
                            ? "♡ Shared"
                            : "🔒 Private"
                          )
                        : "♡ Shared with you"
                    }

                </div>

                <div class="preview">
                    ${escapeHTML(entry.content)}
                </div>

            </div>

        </div>

    `;

}


/* ======================================================
   HOME
====================================================== */

function renderHome(){

    if(!user)
        return;


    const mine =
        entries.filter(
            e => e.ownerUid === user.uid
        );


    const privatePages =
        mine.filter(
            e =>
                !e.sharedWith ||
                !e.sharedWith.length
        );


    const myShared =
        mine.filter(
            e =>
                e.sharedWith &&
                e.sharedWith.length
        );


    const received =
        entries.filter(
            e =>
                e.ownerUid !== user.uid &&
                e.sharedWith &&
                e.sharedWith.includes(user.uid)
        );


    $("privateCount").textContent =
        privatePages.length;


    $("mySharedCount").textContent =
        myShared.length;


    $("receivedCount").textContent =
        received.length;


    const recent =
        [...entries]
            .sort(
                (a,b) =>
                    String(b.date)
                        .localeCompare(
                            String(a.date)
                        )
            )
            .slice(0,5);


    $("recentEntries").innerHTML =
        recent.length
        ? recent.map(makeEntryCard).join("")
        :
        `
        <div class="paper">
            <p style="color:#968474;font-size:12px;">
                Nothing here yet. Write your first page. ♡
            </p>
        </div>
        `;

}


/* ======================================================
   PRIVATE
====================================================== */

function renderPrivate(search=""){

    if(!user)
        return;


    const q =
        search.toLowerCase();


    const list =
        entries.filter(
            entry =>

                entry.ownerUid === user.uid &&

                (
                    !entry.sharedWith ||
                    !entry.sharedWith.length
                ) &&

                (
                    entry.title +
                    " " +
                    entry.content +
                    " " +
                    entry.mood
                )
                .toLowerCase()
                .includes(q)

        );


    $("privateEntries").innerHTML =
        list.length
        ? list.map(makeEntryCard).join("")
        :
        `
        <div class="paper">
            <p style="color:#968474;font-size:12px;">
                No private pages yet.
            </p>
        </div>
        `;

}


/* ======================================================
   SHARED
====================================================== */

function renderShared(search=""){

    if(!user)
        return;


    const q =
        search.toLowerCase();


    const list =
        entries.filter(
            entry =>

                entry.sharedWith &&
                entry.sharedWith.includes(
                    user.uid
                ) &&

                (
                    entry.title +
                    " " +
                    entry.content +
                    " " +
                    entry.mood
                )
                .toLowerCase()
                .includes(q)

        );


    $("sharedEntries").innerHTML =
        list.length
        ? list.map(makeEntryCard).join("")
        :
        `
        <div class="paper">
            <p style="color:#968474;font-size:12px;">
                No shared pages yet.
            </p>
        </div>
        `;

}


/* ======================================================
   SEARCH
====================================================== */

$("privateSearch").oninput =
e => renderPrivate(e.target.value);


$("sharedSearch").oninput =
e => renderShared(e.target.value);


/* ======================================================
   OPEN ENTRY
====================================================== */

document.addEventListener(
    "click",
    event => {

        const card =
            event.target.closest(
                "[data-entry]"
            );


        if(!card)
            return;


        const entry =
            entries.find(
                e =>
                    e.id ===
                    card.dataset.entry
            );


        if(!entry)
            return;


        selectedEntry = entry;


        const mine =
            entry.ownerUid === user.uid;


        $("modalDate").textContent =
            prettyDate(entry.date);


        $("modalTitle").textContent =
            entry.title;


        $("modalMood").textContent =
            entry.mood;


        $("modalContent").textContent =
            entry.content;


        if(mine){

            $("modalPermission").textContent =
                entry.sharedWith &&
                entry.sharedWith.length
                ? "♡ Shared with your partner."
                : "🔒 Private. Your partner cannot see this page.";

            $("editButton")
                .classList
                .remove("hidden");

            $("permissionButton")
                .classList
                .remove("hidden");

            $("deleteButton")
                .classList
                .remove("hidden");

        }else{

            $("modalPermission").textContent =
                "♡ Your partner gave you permission to read this page.";

            $("editButton")
                .classList
                .add("hidden");

            $("permissionButton")
                .classList
                .add("hidden");

            $("deleteButton")
                .classList
                .add("hidden");

        }


        $("entryModal").showModal();

    }
);


/* ======================================================
   EDIT
====================================================== */

$("editButton").onclick =
function(){

    if(!selectedEntry)
        return;


    $("entryModal").close();


    $("editingId").value =
        selectedEntry.id;


    $("entryTitle").value =
        selectedEntry.title;


    $("entryDate").value =
        selectedEntry.date;


    $("entryMood").value =
        selectedEntry.mood;


    $("entryContent").value =
        selectedEntry.content;


    const shared =
        selectedEntry.sharedWith &&
        selectedEntry.sharedWith.length;


    $("sharePermission").checked =
        shared;


    $("shareStatus").textContent =
        shared
        ? "♡ Your partner can read this page."
        : "🔒 Only me";


    showPage("write");

};


/* ======================================================
   DELETE
====================================================== */

$("deleteButton").onclick =
async function(){

    if(!selectedEntry)
        return;


    if(
        !confirm(
            "Delete this page permanently?"
        )
    )
        return;


    try{

        await db
            .collection("entries")
            .doc(selectedEntry.id)
            .delete();


        $("entryModal").close();

        await loadEntries();

    }catch(error){

        console.error(error);

        alert(
            "Could not delete this page."
        );

    }

};


/* ======================================================
   CHANGE PERMISSION
====================================================== */

$("permissionButton").onclick =
async function(){

    if(!selectedEntry)
        return;


    if(!userData.partnerUid){

        alert(
            "Connect your partner first."
        );

        return;

    }


    const currentlyShared =
        selectedEntry.sharedWith &&
        selectedEntry.sharedWith.length;


    try{

        await db
            .collection("entries")
            .doc(selectedEntry.id)
            .update({

                sharedWith:
                    currentlyShared
                    ? []
                    : [userData.partnerUid]

            });


        $("entryModal").close();

        await loadEntries();


    }catch(error){

        console.error(error);

        alert(
            "Could not change permission."
        );

    }

};


/* ======================================================
   CLOSE MODAL
====================================================== */

$("closeModal").onclick =
function(){

    $("entryModal").close();

};


/* ======================================================
   COPY COUPLE CODE
====================================================== */

$("copyCode").onclick =
async function(){

    try{

        await navigator.clipboard.writeText(
            userData.coupleCode
        );

        alert(
            "Your couple code was copied. ♡"
        );

    }catch{

        alert(
            "Please copy the code manually."
        );

    }

};


/* ======================================================
   CONNECT PARTNER
====================================================== */

$("connectButton").onclick =
async function(){

    const code =
        $("partnerCode")
            .value
            .trim()
            .toUpperCase();


    if(!code){

        $("coupleStatus").textContent =
            "Enter your partner's code.";

        return;

    }


    if(
        code === userData.coupleCode
    ){

        $("coupleStatus").textContent =
            "That's your own code.";

        return;

    }


    try{

        const snapshot =
            await db
                .collection("users")
                .where(
                    "coupleCode",
                    "==",
                    code
                )
                .limit(1)
                .get();


        if(snapshot.empty){

            $("coupleStatus").textContent =
                "Couple code not found.";

            return;

        }


        const partner =
            snapshot.docs[0];


        await db
            .collection("users")
            .doc(user.uid)
            .update({

                partnerUid:
                    partner.id

            });


        await db
            .collection("users")
            .doc(partner.id)
            .update({

                partnerUid:
                    user.uid

            });


        userData.partnerUid =
            partner.id;


        $("coupleStatus").textContent =
            "♡ You are now connected!";


    }catch(error){

        console.error(error);

        $("coupleStatus").textContent =
            "Could not connect.";

    }

};


/* ======================================================
   LOGOUT
====================================================== */

$("logoutButton").onclick =
async function(){

    await auth.signOut();

};

</script>

</body>
</html>
