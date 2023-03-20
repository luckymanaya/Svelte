<!--HTML Structure-->
<head>
    <title>Lucky's Website</title>
</head>

<body>
<section class = "picture1"></section>

<!--Text-->
<section class = "firstPageText">
<p>Fashion is a form of <i>self-expression.</i></p>
</section>

<!--Flexbox-->
<section class = "flex-container">
    <section class = "picture2"></section>
    <section class = "picture3"></section>
</section>

<br>

<!--Second Page Button-->
<center>
<a href = '/secondPage'>
    <button class = "nextBtn">Next</button></a>
</center>

</body>

<style>
/*Pictures*/
.picture1{
    background-image: url('images/mannequins.jpg');
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 900px;
}
.picture2{
    background-image: url('images/castle.jpg');
    background-size: cover;
    background-position: center;
    width: 55%;
    height: 900px;
    margin: 20px;;

}
.picture3{
    background-image: url('images/three women.jpg');
    background-size: cover;
    background-position: center;
    width: 45%;
    height: 900px;
    margin: 20px;;
}

/*Text in First Page Styling*/
.firstPageText p{
    text-align: center;
    font-family: "Arial";
    font-size: 2.5em;
    color:white;
}
</style>