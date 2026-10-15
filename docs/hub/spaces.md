<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>B2B Cold Email Sender</title>
    <style>
        body { font-family: Tahoma, Arial, sans-serif; background-color: #0f172a; color: #f8fafc; padding: 20px; margin: 0; }
        .container { max-width: 600px; margin: 0 auto; background: #1e293b; padding: 25px; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.5); }
        h2 { text-align: center; color: #38bdf8; margin-top: 0; }
        label { display: block; margin-top: 15px; font-weight: bold; color: #94a3b8; }
        input, textarea, select { width: 100%; padding: 12px; margin-top: 5px; border-radius: 8px; border: 1px solid #334155; background-color: #0f172a; color: #fff; box-sizing: border-box; font-size: 14px; }
        button { width: 100%; padding: 14px; background-color: #2563eb; color: white; border: none; border-radius: 8px; margin-top: 20px; font-size: 16px; font-weight: bold; cursor: pointer; transition: background 0.3s; }
        button:hover { background-color: #1d4ed8; }
        .status { margin-top: 15px; padding: 12px; border-radius: 8px; display: none; text-align: center; font-weight: bold; }
        .success { background-color: #065f46; color: #34d399; }
        .error { background-color: #991b1b; color: #fca5a5; }
    </style>
</head>
<body>
    <div class="container">
        <h2>🚀 B2B Email Sender Engine</h2>
        <form id="emailForm">
            <label>مضيف SMTP (Host):</label>
            <input type="text" id="smtpHost" placeholder="e.g. smtp.gmail.com or mail.domain.com" required>

            <label>المنفذ (Port):</label>
            <input type="number" id="smtpPort" value="587" required>

            <label>اسم المستخدم / البريد (Username):</label>
            <input type="email" id="smtpUser" placeholder="your-email@domain.com" required>

            <label>كلمة المرور / App Password:</label>
            <input type="password" id="smtpPass" placeholder="******" required>

            <hr style="border: 0.5px solid #334155; margin-top: 20px;">

            <label>إيميل المستلم (Recipient):</label>
            <input type="email" id="toEmail" placeholder="client@company.com" required>

            <label>عنوان الرسالة (Subject):</label>
            <input type="text" id="subject" placeholder="B2B Business Proposal" required>

            <label>محتوى الرسالة (Body):</label>
            <textarea id="body" rows="6" placeholder="اكتب نص الرسالة هنا..." required></textarea>

            <button type="submit" id="sendBtn">إرسال الرسالة الآن 📤</button>
        </form>
        <div id="statusBox" class="status"></div>
    </div>

    <script>
        document.getElementById('emailForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const statusBox = document.getElementById('statusBox');
            statusBox.style.display = 'block';
            statusBox.className = 'status success';
            statusBox.innerText = 'تم تسجيل بيانات الإرسال بنجاح وجاري تجهيز عملية التمرير...';
        });
    </script>
</body>
</html>
