<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>ANONYMOUS - الدعوة</title>
  <script src="https://cdn.jsdelivr.net/npm/emailjs-com@2.6.4/dist/email.min.js"></script>
  <script>
    (function() {
      emailjs.init("zC7P7RAtx2c3kbry0"); // مفتاحك العام
    })();
  </script>
  <style>
    body {
      background-image: url('https://i.imgur.com/6M5134r.jpeg');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      margin: 0;
      color: #00ffcc;
      font-family: 'Courier New', monospace;
      overflow: hidden;
    }
    .overlay {
      background-color: rgba(0, 0, 0, 0.85);
      padding: 40px;
      margin: 50px auto;
      width: 90%;
      max-width: 600px;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 0 30px red;
    }
    .title {
      font-size: 28px;
      font-weight: bold;
      margin-bottom: 20px;
      color: #ff0000;
      letter-spacing: 3px;
    }
    .message {
      font-size: 20px;
      margin-bottom: 30px;
      line-height: 1.8;
    }
    button {
      background: none;
      border: 2px solid #00ffcc;
      color: #00ffcc;
      font-size: 18px;
      padding: 10px 30px;
      margin: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #00ffcc;
      color: #000;
    }
    img.logo {
      width: 130px;
      margin-bottom: 20px;
      filter: grayscale(100%);
    }
    .shake {
      animation: shake 0.6s;
    }
    @keyframes shake {
      0% { transform: translate(0px, 0px); }
      20% { transform: translate(-5px, 5px); }
      40% { transform: translate(5px, -5px); }
      60% { transform: translate(-5px, -5px); }
      80% { transform: translate(5px, 5px); }
      100% { transform: translate(0px, 0px); }
    }
  </style>
</head>
<body>
  <audio autoplay hidden>
    <source src="https://www.soundjay.com/horror/sounds/scary-sound-1.mp3" type="audio/mp3">
  </audio>

  <div class="overlay" id="box">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Anonymous_emblem.svg/2048px-Anonymous_emblem.svg.png" class="logo" alt="Anonymous Logo">
    <div class="title">ANONYMOUS - الدعوة</div>
    <div class="message">
      📡 تم اعتراض إشارتك<br><br>
      شخصيتك معروفة. موقعك تم تحديده. ذهنك تم فحصه.<br><br>
      اختيارك لم يكن صدفة... لقد تم اختيارك لتنفيذ مهمة في القطاع العسكري الأكثر سرية: <b>SDF</b>.<br><br>
      🕯️ <b>الموعد:</b> <i>قبل ضوء القمر</i><br>
      ❓ <b>المكان:</b> <i>سيُكشف بعد اتخاذ القرار</i><br><br>
      ⚠️ <b>إجابتك نهائية</b> ولا يمكن التراجع عنها.<br>
      هل تقبل الدخول؟
    </div>
    <button onclick="sendResponse('نعم - قَبِل المهمة')">نعم</button>
    <button onclick="sendResponse('لا - رفض المهمة')">لا</button>
  </div>

  <script>
    function sendResponse(answer) {
      document.querySelectorAll('button').forEach(btn => btn.disabled = true);
      document.getElementById('box').classList.add('shake');

      emailjs.send("service_jfwr617", "template_hxf08dl", {
        user_reply: answer,
        to_email: "abdallahpccc@gmail.com"
      }).then(() => {
        setTimeout(() => {
          alert("تم تسجيل ردّك... ترقّب ظهور التعليمات القادمة.");
        }, 1000);
      }, (error) => {
        alert("حدث خطأ أثناء الإرسال.");
        console.error(error);
      });
    }
  </script>
</body>
</html>
