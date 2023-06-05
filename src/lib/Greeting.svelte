<script>
  export let greeting;

  const today = new Date();
  const time = today.getHours();

  time >= 5 && time < 12
    ? (greeting = "Good Morning!")
    : time >= 12 && time < 18
    ? (greeting = "Good Afternoon!")
    : (greeting = "Good Evening!");
</script>

<h2>{greeting}</h2>
