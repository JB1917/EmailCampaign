<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Email Campaign Form</title>

<style>
body {
  font-family: Arial, sans-serif;
  max-width: 600px;
  margin: 40px auto;
}

.hidden {
  display: none;
}

button {
  margin-top: 20px;
  padding: 10px 16px;
  font-size: 16px;
}
</style>

<script>
function toggleSocietyInput() {

  const yes = document.getElementById("society_yes");
  const box = document.getElementById("society_box");

  if (yes.checked) {
    box.style.display = "block";
  } else {
    box.style.display = "none";
  }

}
</script>

</head>

<body>

<h2>Email Campaign Form</h2>

<form>

<label for="name">Your name:</label><br>
<input type="text" id="name" name="name"><br><br>


<p>Are you writing on behalf of a society?</p>

<label>
<input type="radio" name="society" id="society_yes" onclick="toggleSocietyInput()">
Yes
</label>

<label>
<input type="radio" name="society" id="society_no" onclick="toggleSocietyInput()">
No
</label>


<div id="society_box" class="hidden">
<br>
<label for="society_name">Which society?</label><br>
<input type="text" id="society_name" name="society_name">
</div>


<br>

<a href="https://example.com">
<button type="button">Continue</button>
</a>

</form>

</body>
</html>
