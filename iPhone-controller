<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>iPhone Controller</title>
</head>
<body>
    <h1>Move or Rotate Your iPhone</h1>

    <script>
        // Function to send motion data to the iPad
        function sendMotionData(x, y, z) {
            // Target the iframe or window where the Spline scene is loaded
            window.opener.postMessage({ x, y, z }, '*');
        }

        // Listen for device motion events
        window.addEventListener('devicemotion', function(event) {
            const x = event.acceleration.x || 0;
            const y = event.acceleration.y || 0;
            const z = event.acceleration.z || 0;

            // Send the motion data to the iPad
            sendMotionData(x, y, z);
        });
    </script>
</body>
</html>
