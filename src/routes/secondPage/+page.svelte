<!--HTML coding-->
<body>
<div class = "picture4"></div>

<section>
    <img src = 'images/runway.jpg'/> 
    <p id = "textID"></p>
</section>

<br>
<center>
    <a href = '/'>
        <button class = "goBackBtn">Go Back</button></a>
</center>

<script>
    let text = "";
    const words = ["Fashion", "Stuff", "Here"]

    for(let i of words){
        text += i + "<br>";
    }

    document.getElementById("textID").innerHTML = text;

</script>

</body>