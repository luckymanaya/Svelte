<script>
  export let greeting = "";

  const today = new Date();
  const time = today.getHours();

  if (time >= 5 && time < 12) greeting = "Good Morning!";
  else if (time >= 12 && time < 18) greeting = "Good Afternoon!";
  else greeting = "Good Evening!";
</script>

<h2>{greeting}</h2>
