<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>For My Favorite Person ❤️</title>
  <style>
    :root {
      --bg-color: #fff5f6;
      --card-bg: #ffffff;
      --accent-color: #ff6b81;
      --text-color: #2f3542;
      --subtext-color: #57606f;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 20px;
    }

    .container {
      width: 100%;
      max-width: 600px;
      background: var(--card-bg);
      border-radius: 20px;
      padding: 30px;
      box-shadow: 0 10px 30px rgba(255, 107, 129, 0.15);
      text-align: center;
      position: relative;
    }

    .page {
      display: none;
      animation: fadeIn 0.5s ease-in-out;
    }

    .page.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      color: var(--accent-color);
      margin-bottom: 15px;
      font-size: 2rem;
    }

    p {
      color: var(--subtext-color);
      font-size: 1.1rem;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .btn {
      background-color: var(--accent-color);
      color: white;
      border: none;
      padding: 12px 28px;
      border-radius: 25px;
      font-size: 1rem;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.2s ease;
      margin: 5px;
    }

    .btn:hover {
      transform: scale(1.05);
      box-shadow: 0 5px 15px rgba(255, 107, 129, 0.4);
    }

    .btn-secondary {
      background-color: #f1f2f6;
      color: var(--text-color);
    }

    .nav-dots {
      margin-top: 25px;
      display: flex;
      justify-content: center;
      gap: 8px;
    }

    .dot {
      width: 10px;
      height: 10px;
      background-color: #dfe4ea;
      border-radius: 50%;
      display: inline-block;
    }

    .dot.active {
      background-color: var(--accent-color);
      width: 20px;
      border-radius: 5px;
    }

    .coupon-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin: 15px 0;
    }

    .coupon {
      border: 2px dashed var(--accent-color);
      padding: 15px;
      border-radius: 12px;
      background-color: #fff0f3;
    }

    .forgive-btns {
      position: relative;
      min-height: 80px;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
    }

    #noBtn {
      position: absolute;
    }
  </style>
</head>
<body>

<div class="container">

  <!-- PAGE 1: Welcome -->
  <div class="page active" id="page1">
    <h1>Hey sundariii.. ❤️</h1>
    <p>I know you're sad and mad abhiii butt bacchuuu i love youhhh sooo muchh naa jaanu maafiii karodoooo naaaa,.</p>
    <p>aage ke pages dekhloo bacchuu kachhu</p>
    <button class="btn" onclick="nextPage()">Let's start 👉</button>
  </div>

  <!-- PAGE 2: The Apology -->
  <div class="page" id="page2">
    <h1>I'm Really Sorry 🥺</h1>
    <p>babyyyy jii please maafii kar dijiyee naaa gussa hoo koi na maafi mil jaani chaiyee naa.</p>
    <p>aap sab deserve karteee hooo sabbbbbbb kuchhhhhhh meri kuchuu puchu😘😘</p>
    <button class="btn btn-secondary" onclick="prevPage()">Back</button>
    <button class="btn" onclick="nextPage()">Next 👉</button>
  </div>

  <!-- PAGE 3: Favorite Memories -->
  <div class="page" id="page3">
    <h1>Remember When...? ✨</h1>
    <p>hummm dono sathh hoye kaise mast baate kartee:</p>
    <p>dur hooke bhii sath me movieess dekhre h enjoy kar rahe h<br>
       •aab gussa mat hoou maaf krooooooo💋<br>
       •bhyiii agar baat nai karogee chaat puja me sath kaise jaaige🤭🤭</p>
    <button class="btn btn-secondary" onclick="prevPage()">Back</button>
    <button class="btn" onclick="nextPage()">Next 👉</button>
  </div>

  <!-- PAGE 4: Reasons I Love You -->
  <div class="page" id="page4">
    <h1>merii bhumika bestt h har chizz mee 🌸</h1>
    <p>vaise thoo agar bolu thoo khatam hii nai hoogi aapki acchai:</p>
    <p>1 bhyii aapki smile dekh ke bass din baan jata h jab sath aate tution see.<br>
       2.bhumika jii bhohot strongg h sab chizzo se deal karti h stronglyyy.<br>
       3. orrr bhumikaaa seee sundarrrrrrrrrrrrrr koiii naii h bhyiiiii or mere liyaa na hogi.</p>
    <button class="btn btn-secondary" onclick="prevPage()">Back</button>
    <button class="btn" onclick="nextPage()">Next 👉</button>
  </div>

  <!-- PAGE 5: Mood Booster Coupons -->
  <div class="page" id="page5">
    <h1>Peace Offering Coupons 🎟️</h1>
    <p>Redeemable anytime by you, no questions asked:</p>
    <div class="coupon-grid">
      <div class="coupon"><b>1x Hug</b><br><small>jab tak aap bolo</small></div>
      <div class="coupon"><b>Favorite Snack</b><br><small>ice cream khaige tution ke bad</small></div>
      <div class="coupon"><b>Your Choice Movie</b><br><small>joo aap bolo</small></div>
      <div class="coupon"><b>1x Win Any Argument</b><br><small>devi jii aap hii jitogeee</small></div>
    </div>
    <button class="btn btn-secondary" onclick="prevPage()">Back</button>
    <button class="btn" onclick="nextPage()">Next 👉</button>
  </div>

  <!-- PAGE 6: My Promise to You -->
  <div class="page" id="page6">
    <h1>My Promise 🤙</h1>
    <p>• dekhooo hamesha sath rahuga kuch bhii hoo😘.<br>
       • hameshaa manaugaaa aapko jaan<br>
       • aapki saari daat binaaa kuch bole sunugaaa.</p>
    <button class="btn btn-secondary" onclick="prevPage()">Back</button>
    <button class="btn" onclick="nextPage()">Next 👉</button>
  </div>

  <!-- PAGE 7: The Forgiveness Question -->
  <div class="page" id="page7">
    <h1>pleasee maafii nawww 🥺</h1>
    <p>aao aapko pyare pyare hug dungaaa</p>
    <div class="forgive-btns">
      <button class="btn" onclick="nextPage()">YES! ❤️</button>
      <button class="btn btn-secondary" id="noBtn" onmouseover="dodgeNoButton()">No 😤</button>
    </div>
  </div>

  <!-- PAGE 8: Thank You / Happy Ending -->
  <div class="page" id="page8">
    <h1>yyayayayayayya bhumikaa maan gaaaiii ayyayayayayya🥰😍😍😍</h1>
    <p>aab nai kushhh huu balle baale hoo gaii ji😘😘😘</p>
    <p>jaldi aab mujhe whats aap me mess karoo<b>"I love youhhhh💋💋"</b> apkoooo pyariuu payaruuu karugaaaa!</p>
    <button class="btn" onclick="goToPage(1)">Restart 🔄</button>
  </div>

  <!-- Page Indicator Dots -->
  <div class="nav-dots" id="dotContainer"></div>

</div>

<script>
  let currentPage = 1;
  const totalPages = 8;

  function initDots() {
    const container = document.getElementById('dotContainer');
    container.innerHTML = '';
    for (let i = 1; i <= totalPages; i++) {
      const dot = document.createElement('span');
      dot.className = `dot ${i === currentPage ? 'active' : ''}`;
      container.appendChild(dot);
    }
  }

  function showPage(pageNumber) {
    document.querySelectorAll('.page').forEach(page => {
      page.classList.remove('active');
    });
    document.getElementById(`page${pageNumber}`).classList.add('active');
    currentPage = pageNumber;
    initDots();
  }

  function nextPage() {
    if (currentPage < totalPages) {
      showPage(currentPage + 1);
    }
  }

  function prevPage() {
    if (currentPage > 1) {
      showPage(currentPage - 1);
    }
  }

  function goToPage(pageNumber) {
    showPage(pageNumber);
  }

  // Playful dodge button for Page 7 "No" button
  function dodgeNoButton() {
    const btn = document.getElementById('noBtn');
    const x = Math.random() * 140 - 70;
    const y = Math.random() * 60 - 30;
    btn.style.transform = `translate(${x}px, ${y}px)`;
  }

  initDots();
</script>
</body>
</html>
