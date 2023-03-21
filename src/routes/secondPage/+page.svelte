<!--HTML coding-->
<body>
<section class = "picture4"></section>

<section class = "picture5">
    <p id = "textID"></p>
</section>

<br>
<center>
    <a href = '/'>
        <button class = "goBackBtn">Go Back</button></a>
</center>

<!--Javascript Code for Text-->
<script>
    let text = "";
    const words = ["Amazing", "Beautiful", "Stunning!"]

    for(let i of words){
        text += "<br> <br>" + i + "<br> <br>";
    }

document.getElementById("textID").innerHTML = text;

</script>

</body>

<style>
/*Pictures*/
.picture4{
    background-image: url('images/vogue.jpg');
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 990px;
    padding: 50px;
}
.picture5{
    background-image: url('images/runway.jpg');
    background-size: cover;
    background-position: center;
    width: 50%;
    height: 990px;
    border-radius: 50%;
    margin: 40px;
}
.picture5 p{
    margin-left: 140%;
    font-size: 2.75em;
}
</style>