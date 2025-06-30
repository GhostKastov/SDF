<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <title>ANONYMOUS - الدعوة</title>
  <script src="https://cdn.jsdelivr.net/npm/emailjs-com@2.6.4/dist/email.min.js"></script>
  <script>
    (function() {
      emailjs.init("zC7P7RAtx2c3kbry0"); // مفتاحك العام
    })();
  </script>
  <style>
    body {
      background-color: #000;
      color: #00ff00; /* لون أخضر كود التهكير */
      font-family: 'Courier New', monospace;
      padding: 40px;
      text-align: center;
      overflow: hidden;
      position: relative;
    }
    /* خطوط رمادية شفافة تتحرك للخلف لإيحاء حركة */
    .matrix {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
      font-family: monospace;
      font-size: 14px;
      line-height: 14px;
      color: #00ff00aa;
      white-space: nowrap;
      overflow: hidden;
      animation: scrollMatrix 10s linear infinite;
    }
    @keyframes scrollMatrix {
      0% { transform: translateY(100%); }
      100% { transform: translateY(-100%); }
    }

    .title {
      font-size: 26px;
      font-weight: bold;
      margin-bottom: 20px;
      color: #00ff00;
      letter-spacing: 2px;
      text-shadow: 0 0 5px #00ff00;
    }
    .message {
      font-size: 20px;
      margin-bottom: 30px;
      line-height: 1.6;
      text-shadow: 0 0 5px #00ff00;
    }
    button {
      background: none;
      border: 2px solid #00ff00;
      color: #00ff00;
      font-size: 18px;
      padding: 10px 25px;
      margin: 10px;
      cursor: pointer;
      transition: 0.3s;
      text-shadow: 0 0 5px #00ff00;
    }
    button:hover {
      background: #00ff00;
      color: #000;
    }
  </style>
</head>
<body>
  <!-- تأثير تهكير بسيط -->
  <div class="matrix">
    1010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010
    <br>
    0101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101
    <br>
    11110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111
    <br>
    00001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000
    <br>
    10101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010
    <br>
    01010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010101
    <br>
    11110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111
    <br>
    00001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000111100001111000011110000
  </div>

  <div class="title">ANONYMOUS - الدعوة</div>
  <div class="message">
    📡 تم اعتراض إشارتك...<br><br>
    لقد تم اختيارك لمهمة سرية ضمن القطاع العسكري <b>SDF</b>.<br><br>
    الموعد: <i>قبل ضوء القمر</i><br>
    المكان: <i>يُكشف بعد قبولك</i><br><br>
    إجابتك نهائية ولا يمكن تغييرها.<br>
    هل تقبل الانضمام؟
  </div>
  <button onclick="sendResponse('نعم - قبول المهمة')">نعم</button>
  <button onclick="sendResponse('لا - رفض المهمة')">لا</button>

  <script>
    function sendResponse(answer) {
      // تعطيل الأزرار لمنع تغيير الرد
      document.querySelectorAll('button').forEach(btn => btn.disabled = true);

      emailjs.send("service_jfwr617", "template_hxf08dl", {
        user_reply: answer,
        to_email: "abdallahpccc@gmail.com"
      }).then(() => {
        alert("تم تسجيل ردك بنجاح. ترقب التعليمات القادمة.");
      }, (error) => {
        alert("حدث خطأ أثناء الإرسال، حاول مرة أخرى.");
        console.error(error);
      });
    }
  </script>
</body>
</html>
