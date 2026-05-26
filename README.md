<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MERN Developer Banner</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
    }

    body{
      background:#000;
      display:flex;
      justify-content:center;
      align-items:center;
      min-height:100vh;
      font-family: 'Share Tech Mono', monospace;
      overflow:hidden;
    }

    .banner{
      width:100%;
      max-width:1920px;
      height:750px;
      position:relative;
      overflow:hidden;
      background:#000;
    }

    /* Matrix Background */
    .matrix{
      position:absolute;
      inset:0;
      background:
        radial-gradient(circle at center, rgba(0,255,0,0.08), transparent 70%),
        repeating-linear-gradient(
          to bottom,
          rgba(0,255,0,0.12) 0px,
          rgba(0,255,0,0.12) 2px,
          transparent 2px,
          transparent 18px
        );
      opacity:0.3;
    }

    .matrix::before{
      content:"010101010101010101010101010101010101010101";
      position:absolute;
      width:100%;
      height:100%;
      color:#00ff44;
      font-size:20px;
      line-height:28px;
      letter-spacing:10px;
      opacity:0.15;
      white-space:pre-wrap;
      animation:move 15s linear infinite;
    }

    @keyframes move{
      from{
        transform:translateY(-100px);
      }
      to{
        transform:translateY(100px);
      }
    }

    /* Content */
    .content{
      position:relative;
      z-index:10;
      height:100%;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      gap:40px;
      padding:40px;
    }

    .title{
      text-align:center;
      color:#fff;
      font-size:70px;
      line-height:1.4;
      text-shadow:0 0 10px rgba(255,255,255,0.3);
    }

    .green{
      color:#00ff44;
      margin:0 15px;
      text-shadow:0 0 10px #00ff44;
    }

    /* Git Contribution */
    .github-grid{
      display:flex;
      flex-direction:column;
      gap:12px;
      margin-top:30px;
    }

    .months{
      display:flex;
      justify-content:space-between;
      color:#ddd;
      font-size:28px;
      padding:0 10px;
    }

    .grid{
      display:grid;
      grid-template-columns:repeat(52, 22px);
      gap:6px;
    }

    .box{
      width:22px;
      height:22px;
      border-radius:4px;
      background:#071018;
    }

    .level1{ background:#0e4429; }
    .level2{ background:#006d32; }
    .level3{ background:#26a641; }
    .level4{ background:#39d353; }

    /* Responsive */
    @media(max-width:1200px){

      .title{
        font-size:48px;
      }

      .grid{
        grid-template-columns:repeat(52, 14px);
      }

      .box{
        width:14px;
        height:14px;
      }

      .months{
        font-size:18px;
      }
    }

    @media(max-width:768px){

      .banner{
        height:auto;
        padding:80px 0;
      }

      .title{
        font-size:28px;
      }

      .grid{
        grid-template-columns:repeat(26, 10px);
      }

      .box{
        width:10px;
        height:10px;
      }

      .months{
        font-size:12px;
        gap:10px;
        flex-wrap:wrap;
        justify-content:center;
      }
    }

  </style>
</head>
<body>

  <div class="banner">

    <div class="matrix"></div>

    <div class="content">

      <div class="title">
        Full Stack MERN Developer
        <span class="green">|</span>
        React.js
        <span class="green">|</span>
        Node.js
        <span class="green">|</span>

        <br>

        MongoDB
        <span class="green">|</span>
        Freelancer
        <span class="green">|</span>

        Building Modern Web Applications
      </div>

      <!-- GitHub Contribution -->
      <div class="github-grid">

        <div class="months">
          <span>Jun</span>
          <span>Jul</span>
          <span>Aug</span>
          <span>Sep</span>
          <span>Oct</span>
          <span>Nov</span>
          <span>Dec</span>
          <span>Jan</span>
          <span>Feb</span>
          <span>Mar</span>
          <span>Apr</span>
          <span>May</span>
        </div>

        <div class="grid">

          <!-- Generate Boxes -->
          <!-- You can duplicate/change classes -->

          <div class="box level3"></div>
          <div class="box level2"></div>
          <div class="box"></div>
          <div class="box level1"></div>
          <div class="box level4"></div>
          <div class="box level2"></div>
          <div class="box"></div>
          <div class="box level3"></div>
          <div class="box level1"></div>
          <div class="box"></div>

          <!-- Repeat -->
          <!-- Fast Way -->
          <script>
            const grid = document.currentScript.parentElement;

            for(let i=0;i<500;i++){

              const box = document.createElement('div');

              const levels = [
                '',
                'level1',
                'level2',
                'level3',
                'level4'
              ];

              box.className = 'box ' + levels[Math.floor(Math.random()*levels.length)];

              grid.appendChild(box);
            }
          </script>

        </div>

      </div>

    </div>

  </div>

</body>
</html>
