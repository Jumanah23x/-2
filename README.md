<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بطاقة تهنئة</title>
    <style>
        @font-face {
            font-family: 'ElMessiri'; /* اسم الخط */
            src: url('ElMessiri.ttf') format('truetype'); /* مسار الخط */
        }
        body {
            font-family: 'ElMessiri', sans-serif;
            text-align: center;
            background-color: #f0f8ff; /* لون خلفية الصفحة */
            margin: 0;
            padding: 20px;
        }
        h1 {
            color: #4a90e2; /* لون عنوان الصفحة */
        }
        .card {
            width: 600px; /* عرض البطاقة */
            height: 500px; /* ارتفاع البطاقة */
            position: relative;
            background-image: url('بطاقة.jpg'); /* ضع مسار الصورة هنا */
            background-size: cover;
            background-position: center;
            margin: 0 auto;
            border: 5px solid #4a90e2; /* لون حدود البطاقة */
            border-radius: 10px; /* زوايا دائرية */
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2); /* ظل للبطاقة */
        }
        .name {
            font-size: 18px;
            font-weight: bold;
            color: #fff; /* لون الاسم */
            position: absolute;
            top: 86.2%; /* موقع الاسم */
            left: 50%;
            transform: translate(-50%, -50%);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* ظل للاسم */
        }
        input {
            margin: 20px;
            padding: 10px;
            font-size: 16px;
            font-family: 'ElMessiri', sans-serif;
            border: 2px solid #4a90e2; /* حدود الحقل */
            border-radius: 5px; /* زوايا دائرية */
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            font-family: 'ElMessiri', sans-serif;
            background-color: #4a90e2; /* لون خلفية الزر */
            color: #fff; /* لون نص الزر */
            border: none; /* إزالة الحدود */
            border-radius: 5px; /* زوايا دائرية */
            transition: background-color 0.3s; /* تأثير التغيير في الخلفية */
        }
        button:hover {
            background-color: #357ab8; /* لون خلفية الزر عند التحويم */
        }
    </style>
</head>
<body>

<h1>أضف اسمك على بطاقة التهنئة</h1>

<div class="card" id="card">
    <p class="name" id="name">اسمك هنا</p>
</div>

<input type="text" id="inputName" placeholder="اكتب اسمك">
<button onclick="updateName()">عرض الاسم</button>

<script>
    // تحديث الاسم على البطاقة
    function updateName() {
        var name = document.getElementById('inputName').value;
        document.getElementById('name').textContent = name;
    }
</script>

</body>
</html>
