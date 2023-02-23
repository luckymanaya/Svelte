<!--CSS Styling-->
<style>
    h1{
        background-color: pink;
        color: rgb(241, 40, 151);
        text-decoration-color: rgb(241, 40, 151);
        font-size: 30px;
        font-style: bold;
        font-weight: normal;
        text-align: center;
    }

    button
    {
        background-color: pink;
        border-radius: 100px;
    }
</style>

<!--JavaScript-->
<script>
    let count = 0;
    let first_name = "Lucky";

    function IncrementCount()
    {
        count++;
    }
    function Reset()
    {
        count = 0;
    }
</script>

<!--HTML Structure-->
<title>Lucky's Website</title>
<div>
    <h1><small>Hello</small> <i>{first_name}</i>!</h1>
</div>

<button on:click = {IncrementCount}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>
    
</p>
<button on:click = {Reset} style = "background-color: red">
    Reset
</button>
