
<html>
<head>

<style>
    body{
font-family: Arial;
background-image: url(ak.jpg);
 background-repeat: repeat-y ;
        background-size: 1600px 900px;
}

.container{
width:500px;
margin:80px auto;
background:transparent;
padding:20px;
border-radius:50px;
box-shadow:0 0 10px rgb(242, 255, 0);
}

h2{
text-align:center;
}

label{
display:block;
margin-top:10px;
}

input, textarea, select{
width:100%;
padding:8px;
margin-top:5px;
border:1px solid #000000;
border-radius:5px;
}

button{
margin-top:15px;
width:100%;
padding:10px;
background:#04e839;
color:white;
border:none;
border-radius:5px;
font-size:16px;
cursor:pointer;

}

button:hover{
background:#0520ea;
}

#response{
text-align:center;
margin-top:10px;
color:rgb(243, 3, 199);
}
</style>
</head>
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScfJe01FVBaB3uJUAWOp56-PTGlPjsmoMdvHW6GiefxThKWgw/viewform?embedded=true" width="640" height="486" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
<body>

<div class="container">
<h2 style="color: #f1018d;">Online Feedback Form</h2>

<form id="feedbackForm">

<label style="color: #f1018d;">Name:</label>
<input type="text" id="name" required placeholder="Enter your Name">

<label style="color: #f1018d;">Email:</label>
<input type="email" id="email" required placeholder="Enter your email">

<label style="color: #f1018d;">Rating:</label>
<select id="rating">
<option value="Excellent">Excellent</option>
<option value="Good">Good</option>
<option value="Average">Average</option>
<option value="Poor">Poor</option>
</select>

<label style="color: #f1018d;">Feedback:</label>
<textarea id="message" rows="4" required placeholder="Enter your feedback"></textarea>

<button type="submit">Submit Feedback</button>

</form>

<p id="response"></p>

</div>
<script>

document.getElementById("feedbackForm").addEventListener("submit", function(event){

event.preventDefault();

let name = document.getElementById("name").value;
let email = document.getElementById("email").value;
let rating = document.getElementById("rating").value;
let message = document.getElementById("message").value;

let feedbackData = {
name:name,
email:email,
rating:rating,
message:message
};

console.log(feedbackData);

document.getElementById("response").innerHTML = 
"Thank you for your feedback, " + name + "!";

document.getElementById("feedbackForm").reset();

});
</script>

</body>
</html>
