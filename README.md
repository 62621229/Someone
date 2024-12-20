<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تاريخ</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
        }
        #login-form {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            width: 300px;
            margin: auto;
        }
        input {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 95%;
            padding: 10px;
            margin: 10px 0;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .alert {
            display: none;
            background-color: #f8d7da;
            color: #721c24;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #f5c6cb;
            border-radius: 5px;
        }
        .images-page {
            text-align: center;
        }
        .images-page img {
            width: 200px;
            height: auto;
            margin: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="login-form">
            <h1>تسجيل الدخول</h1>
            <div>
                <input type="text" id="phone" placeholder="رقم الهاتف">
            </div>
            <div>
                <input type="password" id="password" placeholder="كلمة السر">
            </div>
            <button onclick="login()">تسجيل الدخول</button>
            <div class="alert" id="alert"></div>
        </div>
    </div>

    <script>
        function login() {
            const phone = document.getElementById("phone").value;
            const password = document.getElementById("password").value;
            const alertBox = document.getElementById("alert");

            if (phone === "2729" && password === "1229") {
                // تسجيل الدخول ناجح
                document.body.innerHTML = `
                    <div class="images-page">
                        <h1>مرحبًا بك</h1>
                        <img src="image1.jpg" alt="صورة 1">
                        <img src="image2.jpg" alt="صورة 2">
                        <img src="image3.jpg" alt="صورة 3">
                        <img src="image4.jpg" alt="صورة 4">
                        <img src="image5.jpg" alt="صورة 5">
                        <img src="image6.jpg" alt="صورة 6">
                        <img src="image7.jpg" alt="صورة 7">
                        <img src="image8.jpg" alt="صورة 8">
                    </div>
                `;
            } else if (phone === "0904642729" && password !== "0962621229") {
                showAlert("خطأ في تسجيل الدخول: كلمة السر غير صحيحة");
            } else if (phone !== "0904642729" && password === "0962621229") {
                showAlert("خطأ في تسجيل الدخول: رقم الهاتف غير صحيح");
            } else {
                showAlert("خطأ في تسجيل الدخول: رقم الهاتف وكلمة السر غير صحيحين");
            }
        }

        function showAlert(message) {
            const alertBox = document.getElementById("alert");
            alertBox.innerText = message;
            alertBox.style.display = "block";
        }
    </script>
</body>
</body>
