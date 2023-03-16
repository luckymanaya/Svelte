<!--HTML coding-->
<body>
<div class = "picture4"></div>
<div class = "picture5"></div>

<p id = "fashionTerms"></p>

<br>
<center>
    <a href = '/'>
        <button class = "goBackBtn">Go Back</button></a>
</center>

<!--Javascript Coding-->
<script>
    let text = "";
    const terms = ["Fashion", "Stuff", "Here"];

for (let i of terms) {
  text += i + "<br>";
}

document.getElementById("fashionTerms").innerHTML = text;

</script>

</body>