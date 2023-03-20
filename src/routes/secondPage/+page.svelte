<!--HTML coding-->
<body>
<section class = "picture4"></section>
<section class = "picture5"></section>

<br>
<center>
    <a href = '/'>
        <button class = "goBackBtn">Go Back</button></a>
</center>

<!--Javascript Code for Text-->
<script>
    let text = "";
    const words = ["Fashion", "Stuff", "Here"]

    for(let i of words){
        text += i + "<br>";
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
}
.picture5{
    background-image: url('images/runway.jpg');
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 1000px;
}
</style>