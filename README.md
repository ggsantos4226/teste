# teste
teste iptv
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>IPTV Player Multiplataforma</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="manifest" href="manifest.json">
  <style>
    body {
      background-color: #111;
      color: #fff;
      font-family: sans-serif;
      text-align: center;
      padding: 20px;
    }
    video {
      width: 100%;
      max-width: 800px;
      height: auto;
      border: 2px solid #0f0;
      margin-top: 20px;
    }
    select {
      margin-top: 20px;
      padding: 10px;
      font-size: 16px;
      width: 90%;
      max-width: 400px;
    }
  </style>
</head>
<body>
  <h1>IPTV Grátis Multiplataforma</h1>

  <select id="channelSelector" onchange="changeChannel()">
    <option value="https://stream.ads.ottera.tv/live/WEATHERNETWORKWEATHERNETWORKWEATHERNETWORK/playlist.m3u8">The Weather Network</option>
    <option value="https://newsmax-lh.akamaihd.net/i/newsmax_1@123456/master.m3u8">Newsmax</option>
    <option value="https://cdn-cf-east.streamablecdn.com/live/espn.m3u8">ESPN (Exemplo)</option>
  </select>

  <video id="iptvPlayer" controls autoplay></video>

  <script>
    const player = document.getElementById("iptvPlayer");
    const selector = document.getElementById("channelSelector");
    function changeChannel() {
      player.src = selector.value;
      player.play();
    }
    window.onload = changeChannel;
  </script>
</body>
</html>
