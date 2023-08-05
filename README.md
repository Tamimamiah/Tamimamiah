<!DOCTYPE html>
<html>
<head>
  <title>Digital Clock</title>
</head>
<body>
  <h1 id="clock">Loading...</h1>

  <script>
    function updateClock() {
      const now = new Date();
      const hours = now.getHours().toString().padStart(2, '0');
      const minutes = now.getMinutes().toString().padStart(2, '0');
      const seconds = now.getSeconds().toString().padStart(2, '0');
      const timeString = `${hours}:${minutes}:${seconds}`;
      document.getElementById('clock').textContent = timeString;
    }

    setInterval(updateClock, 1000); // Update the clock every 1000ms (1 second)
    updateClock(); // Initial call to set the clock immediately
  </script>
</body>
</html>

