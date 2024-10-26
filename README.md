<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Página de Captura de Foto</title>
</head>
<body>
  <h1>Captura de foto</h1>
  <video id="video" autoplay playsinline></video>
  <script>
    const video = document.getElementById('video');

    navigator.mediaDevices.getUserMedia({ video: true })
      .then(stream => {
        video.srcObject = stream;
      })
      .catch(err => {
        console.error("Error al acceder a la cámara: ", err);
      });
  </script>
</body>
</html>
