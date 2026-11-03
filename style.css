<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GPMSCTECH NEW BASE TECHNOLOGY</title>
<style>
body{margin:0;background:#071b38;color:white;font-family:Arial,sans-serif}
header{text-align:center;padding:25px 12px;background:#0b2850}
.faith{color:#e8c66a;font-weight:bold}
h1,h2{color:#e8c66a}
main{max-width:850px;margin:auto;padding:15px}
section{background:#102e55;padding:20px;margin:15px 0;border-radius:12px}
input,select,button{box-sizing:border-box;width:100%;padding:12px;margin:7px 0;border-radius:7px}
input,select{background:#071b38;color:white;border:1px solid #607b9d}
button{background:#e8c66a;color:#071b38;border:0;font-weight:bold}
.status{background:#071b38;padding:12px;border-radius:7px;white-space:pre-wrap}
.gold{color:#e8c66a}.small{font-size:13px;color:#c4d1e2}
.timer{font-size:35px;color:#e8c66a;font-weight:bold}
a{color:#e8c66a}
.hidden{display:none}
</style>
</head>
<body>

<header>
<p class="faith">Praise And Glory To God The Father Almighty, Jesus Christ God Almighty, And The Holy Spirit God Almighty, Amen.</p>
<h1>GPMSCTECH NEW BASE TECHNOLOGY</h1>
<p>@speed_awr360°</p>
<p>Global Positive Mind Set Center Technology</p>
</header>

<main>

<section>
<h2>Official 24-Hour Trial</h2>
<div id="trialStatus" class="status">Loading...</div>
<div id="timer" class="timer">--:--:--</div>
<p class="small">The official trial begins when the administrator activates the launch schedule. The website remains visible after the trial ends.</p>
</section>

<section>
<h2>Customer Registration / Login</h2>

<label>Full Name</label>
<input id="fullName" placeholder="Enter your full name">

<label>Email</label>
<input id="email" type="email" placeholder="Enter your email">

<label>Password</label>
<input id="password" type="password" placeholder="At least 6 characters">

<button id="registerBtn">CREATE ACCOUNT</button>
<button id="loginBtn">SIGN IN</button>
<button id="logoutBtn" class="hidden">SIGN OUT</button>

<div id="accountStatus" class="status">Not signed in.</div>
</section>

<section>
<h2>Subscription and Payment</h2>
<p>Monthly price: <b class="gold">TZS 20,000</b></p>

<label>Select Subscription Duration</label>
<select id="months">
<option value="1">1 Month - TZS 20,000</option>
<option value="2">2 Months - TZS 40,000</option>
<option value="3">3 Months - TZS 60,000</option>
<option value="4">4 Months - TZS 80,000</option>
<option value="5">5 Months - TZS 100,000</option>
<option value="6">6 Months - TZS 120,000</option>
<option value="7">7 Months - TZS 140,000</option>
<option value="8">8 Months - TZS 160,000</option>
<option value="9">9 Months - TZS 180,000</option>
<option value="10">10 Months - TZS 200,000</option>
<option value="11">11 Months - TZS 220,000</option>
<option value="12">12 Months - TZS 240,000</option>
</select>

<div class="status">
Bank: CRDB BANK PLC
Lipa Namba: 10055686
Recipient: Garaji Joseph Masambu
</div>

<label>CRDB Transaction Reference</label>
<input id="transactionReference" placeholder="Enter payment reference">

<button id="paymentBtn">SUBMIT PAYMENT FOR VERIFICATION</button>

<p class="small">Payment is manually checked by the administrator through CRDB. Submission does not mean payment has been approved.</p>
</section>

<section>
<h2>Security QR Verification</h2>
<label>Private QR / Access Code</label>
<input id="qrCode" placeholder="Enter your private access code">
<button id="qrBtn">SUBMIT QR FOR VERIFICATION</button>
<p class="small">The code is hashed before submission. The administrator must verify it before granting access.</p>
</section>

<section>
<h2>My Service Access</h2>
<div id="accessStatus" class="status">Sign in to check your access.</div>
</section>

<section>
<h2>Contact GPMSCTECH</h2>
<p>Email: georgemasambu64@gmail.com</p>
<p>Email: gmasambu238@gmail.com</p>
<p>Phone / WhatsApp: +255717314652</p>
<p>Phone / WhatsApp: +255744769060</p>
<p>Owner: Garaji Joseph Masambu</p>
</section>

<div id="message" class="status">System ready.</div>

</main>

<script type="module">

import {initializeApp}
from "https://www.gstatic.com/firebasejs/13.1.0/firebase-app.js";

import {
getAuth,
createUserWithEmailAndPassword,
signInWithEmailAndPassword,
signOut,
onAuthStateChanged,
updateProfile
}
from "https://www.gstatic.com/firebasejs/13.1.0/firebase-auth.js";

import {
getFirestore,
doc,
getDoc,
setDoc,
collection,
addDoc,
serverTimestamp
}
from "https://www.gstatic.com/firebasejs/13.1.0/firebase-firestore.js";

const firebaseConfig = {
apiKey: "AIzaSyBYmWzzWfvHkuRgHpQhvDzj6m0o8oRzHrw",
authDomain: "gpmsctech-18abb.firebaseapp.com",
projectId: "gpmsctech-18abb",
storageBucket: "gpmsctech-18abb.firebasestorage.app",
messagingSenderId: "554624850081",
appId: "1:554624850081:web:6cc5cbe084f83548ed78e0",
measurementId: "G-Q00NCG4CBR"
};

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);
const db = getFirestore(app);

const $ = id => document.getElementById(id);

let currentUser = null;
let launchData = null;

function notify(text){
$("message").textContent = text;
}

async function createUserProfile(user,name=""){
const ref=doc(db,"users",user.uid);
const snap=await getDoc(ref);

if(!snap.exists()){
await setDoc(ref,{
email:user.email || "",
displayName:name || user.displayName || "",
accountStatus:"pending",
createdAt:serverTimestamp()
});
}
}

async function sha256(value){
const result=await crypto.subtle.digest(
"SHA-256",
new TextEncoder().encode(value)
);
return [...new Uint8Array(result)]
.map(b=>b.toString(16).padStart(2,"0"))
.join("");
}

// Registration
$("registerBtn").onclick=async()=>{
try{
const name=$("fullName").value.trim();
const email=$("email").value.trim();
const password=$("password").value;

if(!name || !email || password.length<6){
throw Error("Enter your name, email and password of at least 6 characters.");
}

const result=await createUserWithEmailAndPassword(auth,email,password);
await updateProfile(result.user,{displayName:name});
await createUserProfile(result.user,name);

notify("Account successfully created.");
await refreshAccount(result.user);

}catch(error){
notify(error.message);
}
};

// Login
$("loginBtn").onclick=async()=>{
try{
const result=await signInWithEmailAndPassword(
auth,
$("email").value.trim(),
$("password").value
);

await createUserProfile(result.user);
await refreshAccount(result.user);
notify("Successfully signed in.");

}catch(error){
notify(error.message);
}
};

// Logout
$("logoutBtn").onclick=async()=>{
await signOut(auth);
notify("You have signed out.");
};

// Payment request
$("paymentBtn").onclick=async()=>{
try{
if(!currentUser) throw Error("Please sign in first.");

const months=Number($("months").value);
const reference=$("transactionReference").value.trim();

if(reference.length<5) throw Error("Enter a valid transaction reference.");

await addDoc(collection(db,"payments"),{
uid:currentUser.uid,
email:currentUser.email || "",
months:months,
amount:months*20000,
currency:"TZS",
paymentMethod:"CRDB_LIPA_NAMBA",
lipaNamba:"10055686",
transactionReference:reference,
status:"pending",
createdAt:serverTimestamp()
});

$("transactionReference").value="";
notify("Payment request received. Waiting for CRDB verification.");

}catch(error){
notify(error.message);
}
};

// QR request
$("qrBtn").onclick=async()=>{
try{
if(!currentUser) throw Error("Please sign in first.");

const code=$("qrCode").value.trim();
if(code.length<12) throw Error("Enter your private access code.");

const qrHash=await sha256(code);

await addDoc(collection(db,"qrRequests"),{
uid:currentUser.uid,
qrHash:qrHash,
status:"pending",
createdAt:serverTimestamp()
});

$("qrCode").value="";
notify("QR request submitted for administrator verification.");

}catch(error){
notify(error.message);
}
};

// Trial countdown
function updateTimer(){
if(!launchData ||
launchData.status!=="active" ||
!launchData.trialEndsAt){

$("trialStatus").textContent="Official trial has not started.";
$("timer").textContent="--:--:--";
return;
}

const end=launchData.trialEndsAt.toDate().getTime();
const remaining=Math.max(0,end-Date.now());

if(remaining===0){
$("trialStatus").textContent="The 24-hour trial has ended.";
$("timer").textContent="00:00:00";
return;
}

const h=Math.floor(remaining/3600000);
const m=Math.floor((remaining%3600000)/60000);
const s=Math.floor((remaining%60000)/1000);

$("trialStatus").textContent="Official trial is active.";
$("timer").textContent=
[h,m,s].map(x=>String(x).padStart(2,"0")).join(":");
}

async function loadLaunch(){
try{
const snap=await getDoc(doc(db,"system","launch"));
launchData=snap.exists()?snap.data():null;
updateTimer();
setInterval(updateTimer,1000);
}catch(error){
$("trialStatus").textContent="Unable to load launch schedule.";
}
}

// Account and access
async function refreshAccount(user){
if(!user){
$("accountStatus").textContent="Not signed in.";
$("accessStatus").textContent="Sign in to check access.";
return;
}

const snap=await getDoc(doc(db,"users",user.uid));

if(!snap.exists()){
$("accountStatus").textContent="Profile not found.";
return;
}

const data=snap.data();

const expiry=data.subscriptionExpiresAt?.toDate
?data.subscriptionExpiresAt.toDate():null;

const trialActive=launchData?.status==="active" &&
launchData.trialEndsAt?.toDate &&
Date.now()<launchData.trialEndsAt.toDate().getTime();

const paidActive=expiry &&
expiry.getTime()>Date.now() &&
data.qrVerified===true &&
data.accountStatus==="active";

$("accountStatus").textContent=
"Email: "+user.email+
"\nAccount: "+(data.accountStatus||"pending")+
"\nQR: "+(data.qrVerified===true?"Verified":"Pending")+
"\nExpiry: "+(expiry?expiry.toLocaleString():"Not approved");

$("accessStatus").textContent=
trialActive?"Official trial is active.":
paidActive?"Your subscription is marked active.":
"Paid access is pending administrator approval.";
}

onAuthStateChanged(auth,async user=>{
currentUser=user;
$("logoutBtn").classList.toggle("hidden",!user);

if(user){
try{
await refreshAccount(user);
}catch(error){
notify(error.message);
}
}else{
await refreshAccount(null);
}
});

await loadLaunch();

</script>
</body>
</html>
