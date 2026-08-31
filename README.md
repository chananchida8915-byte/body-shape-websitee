
<!DOCTYPE html>
<html lang="th">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">

    <title>เว็บไซต์วิเคราะห์รูปร่างและแนะนำการแต่งกาย</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            padding: 20px;
            font-family: Arial, "Noto Sans Thai", sans-serif;
            background: #fceef3;
        }

        .container {
            width: 90%;
            max-width: 650px;
            margin: 30px auto;
            padding: 30px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #d85b87;
            margin-top: 0;
        }

        h2 {
            color: #d85b87;
        }

        h3 {
            color: #d85b87;
        }

        p {
            line-height: 1.7;
        }

        .intro {
            text-align: center;
        }

        section {
            margin-top: 25px;
        }

        label {
            display: block;
            margin-top: 15px;
            margin-bottom: 5px;
            font-weight: bold;
        }

        input,
        select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 10px;
            font-size: 16px;
        }

        button {
            width: 100%;
            margin-top: 25px;
            padding: 14px;
            border: none;
            border-radius: 10px;
            background: #d85b87;
            color: white;
            font-size: 18px;
            cursor: pointer;
        }

        button:hover {
            background: #c74875;
        }

        /* กล่องขั้นตอน */
        .step {
            padding: 15px;
            margin: 15px 0;
            border-radius: 12px;
            border-left: 6px solid #d85b87;
            background: #fff5f8;
        }

        .step-title {
            font-weight: bold;
            color: #d85b87;
            margin-bottom: 5px;
        }

        /* ผลลัพธ์ */
        .result-box {
            display: none;
            margin-top: 30px;
            padding: 20px;
            background: #fff5f8;
            border-radius: 15px;
        }

        .result-image {
            width: 260px;
            height: 350px;
            max-width: 100%;
            object-fit: contain;
            display: none;
            margin: 20px auto;
            border-radius: 12px;
        }

        #result {
            text-align: center;
            color: #d85b87;
            font-size: 26px;
        }

        .info-box {
            background: white;
            padding: 15px;
            margin-top: 15px;
            border-radius: 10px;
            line-height: 1.8;
        }

        ul {
            line-height: 1.8;
        }

        .error {
            color: #c0392b;
            font-weight: bold;
        }
    
        /* รองรับมือถือ */
        html {
            -webkit-text-size-adjust: 100%;
        }

        body {
            min-width: 0;
            width: 100%;
            padding: 12px;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 650px;
            margin: 10px auto;
            padding: 20px 16px;
            border-radius: 16px;
        }

        h1 {
            font-size: clamp(24px, 7vw, 32px);
            line-height: 1.3;
        }

        h2 {
            font-size: clamp(19px, 5vw, 24px);
            line-height: 1.4;
        }

        h3 {
            font-size: clamp(21px, 6vw, 28px);
            line-height: 1.4;
        }

        p, li, label, select, input, button {
            font-size: 16px;
        }

        input, select, button {
            min-height: 48px;
            -webkit-appearance: none;
            appearance: none;
        }

        input, select {
            width: 100%;
        }

        button {
            touch-action: manipulation;
        }

        .result-image {
            width: 100%;
            max-width: 320px;
            height: auto;
            max-height: 430px;
            object-fit: contain;
        }

        .info-box {
            overflow-wrap: anywhere;
        }

        @media (max-width: 480px) {
            body {
                padding: 8px;
            }

            .container {
                margin: 4px auto;
                padding: 16px 12px;
            }

            section {
                margin-top: 18px;
            }

            .step {
                padding: 13px;
                margin: 12px 0;
            }

            .intro {
                font-size: 15px;
            }

            .result-image {
                max-width: 280px;
            }
        }

    </style>
</head>

<body>

    <div class="container">

        <h1>เว็บไซต์วิเคราะห์รูปร่าง</h1>

        <p class="intro">
            กรอกข้อมูลพื้นฐานและข้อมูลสัดส่วน
            เพื่อวิเคราะห์รูปร่างและรับคำแนะนำการแต่งกาย
        </p>


        <!-- ==================================
             ขั้นตอนที่ 1
        ================================== -->
        <section>

            <h2>ขั้นตอนที่ 1 กรอกข้อมูลพื้นฐาน</h2>

            <div class="step">
                <div class="step-title">
                    กรอกข้อมูลพื้นฐาน
                </div>

                <p>
                    กรุณากรอกเพศ น้ำหนัก ส่วนสูง
                    และสัดส่วนร่างกาย
                </p>
            </div>

            <label for="gender">
                เพศ
            </label>

            <select id="gender">
                <option value="">-- เลือกเพศ --</option>
                <option value="หญิง">หญิง</option>
                <option value="ชาย">ชาย</option>
            </select>


            <label for="weight">
                น้ำหนัก (กิโลกรัม)
            </label>

            <input
                type="number"
                id="weight"
                placeholder="เช่น 55"
                step="0.1"
                min="1"
            >


            <label for="height">
                ส่วนสูง (เซนติเมตร)
            </label>

            <input
                type="number"
                id="height"
                placeholder="เช่น 165"
                step="0.1"
                min="1"
            >


            <label for="bust">
                รอบอก (นิ้ว)
            </label>

            <input
                type="number"
                id="bust"
                placeholder="เช่น 34"
                step="0.1"
                min="1"
            >


            <label for="waist">
                รอบเอว (นิ้ว)
            </label>

            <input
                type="number"
                id="waist"
                placeholder="เช่น 26"
                step="0.1"
                min="1"
            >


            <label for="hip">
                รอบสะโพก (นิ้ว)
            </label>

            <input
                type="number"
                id="hip"
                placeholder="เช่น 36"
                step="0.1"
                min="1"
            >

        </section>


        <!-- ==================================
             ปุ่มวิเคราะห์
        ================================== -->

        <button onclick="analyzeBody()">
            วิเคราะห์รูปร่าง
        </button>


        <!-- ==================================
             ผลลัพธ์
        ================================== -->

        <section
            id="resultBox"
            class="result-box"
        >

            <h2>
                ผลการวิเคราะห์
            </h2>


            <!-- ขั้นตอนที่ 2 -->
            <div class="step">

                <div class="step-title">
                    1. คำนวณค่า BMI
                </div>

                <div class="info-box">

                    <strong>BMI:</strong>

                    <span id="bmi">
                        -
                    </span>

                    <br>

                    <strong>ผลการประเมิน:</strong>

                    <span id="bmiStatus">
                        -
                    </span>

                </div>

            </div>


            <!-- ขั้นตอนที่ 3 -->
            <div class="step">

                <div class="step-title">
                    2. วิเคราะห์สัดส่วนร่างกาย
                </div>

                <div class="info-box">

                    <strong>รอบอก:</strong>
                    <span id="showBust">-</span> นิ้ว

                    <br>

                    <strong>รอบเอว:</strong>
                    <span id="showWaist">-</span> นิ้ว

                    <br>

                    <strong>รอบสะโพก:</strong>
                    <span id="showHip">-</span> นิ้ว

                </div>

            </div>


            <!-- ขั้นตอนที่ 4 -->
            <div class="step">

                <div class="step-title">
                    3. จำแนกประเภทรูปร่าง
                </div>

                <h3 id="result">
                    -
                </h3>

            </div>


            <!-- รูป -->
            <img
                id="hourglassImage"
                class="result-image"
                src="imge/Kim.jpg"
                alt="รูปร่างนาฬิกาทราย"
            >

            <img
                id="pearImage"
                class="result-image"
                src="imge/Knowles.jpg"
                alt="รูปร่างลูกแพร์"
            >

            <img
                id="invertedImage"
                class="result-image"
                src="imge/Campbell.jpg"
                alt="รูปร่างสามเหลี่ยมกลับหัว"
            >

            <img
                id="appleImage"
                class="result-image"
                src="imge/Jennif.jpg"
                alt="รูปร่างแอปเปิ้ล"
            >

            <img
                id="rectangleImage"
                class="result-image"
                src="imge/Diaz.jpg"
                alt="รูปร่างทรงกระบอก"
            >


            <!-- ขั้นตอนที่ 5 -->
            <div class="step">

                <div class="step-title">
                    4. วิเคราะห์จุดเด่น-จุดด้อย
                </div>

                <div
                    id="description"
                    class="info-box"
                >
                    -
                </div>

            </div>


            <!-- ขั้นตอนที่ 6 -->
            <div class="step">

                <div class="step-title">
                    5. เลือกแนวทางการแต่งกายที่เหมาะสม
                </div>

                <div
                    id="recommendation"
                    class="info-box"
                >
                    -
                </div>

            </div>


            <!-- ขั้นตอนที่ 7 -->
            <div class="step">

                <div class="step-title">
                    6. แสดงคำแนะนำเสื้อผ้า
                </div>

                <div class="info-box">

                    <ul id="clothingList">
                    </ul>

                </div>

            </div>

        </section>

    </div>


    <script>

        /* ==================================
           ซ่อนรูปทั้งหมด
        ================================== */

        function hideAllImages() {

            document.getElementById("hourglassImage").style.display = "none";

            document.getElementById("pearImage").style.display = "none";

            document.getElementById("invertedImage").style.display = "none";

            document.getElementById("appleImage").style.display = "none";

            document.getElementById("rectangleImage").style.display = "none";

        }


        /* ==================================
           คำนวณ BMI
        ================================== */

        function calculateBMI(weight, height) {

            const heightMeter = height / 100;

            return weight / (heightMeter * heightMeter);

        }


        /* ==================================
           ประเมิน BMI
        ================================== */

        function getBMIStatus(bmi) {

            /*
                เกณฑ์ตัวอย่างสำหรับเว็บไซต์
                สามารถปรับตามเกณฑ์ที่โครงงานกำหนดได้
            */

            if (bmi < 18.5) {

                return "น้ำหนักน้อย";

            }

            else if (bmi < 23) {

                return "อยู่ในช่วงปกติ";

            }

            else if (bmi < 25) {

                return "น้ำหนักเกิน";

            }

            else if (bmi < 30) {

                return "อ้วนระดับ 1";

            }

            else {

                return "อ้วนระดับ 2";

            }

        }


        /* ==================================
           วิเคราะห์รูปร่าง
        ================================== */

        function analyzeBody() {

            const gender =
                document.getElementById("gender").value;

            const weight =
                Number(document.getElementById("weight").value);

            const height =
                Number(document.getElementById("height").value);

            const bust =
                Number(document.getElementById("bust").value);

            const waist =
                Number(document.getElementById("waist").value);

            const hip =
                Number(document.getElementById("hip").value);


            /* ตรวจสอบข้อมูล */

            if (
                gender === "" ||
                !weight ||
                !height ||
                !bust ||
                !waist ||
                !hip
            ) {

                alert(
                    "กรุณากรอกข้อมูลให้ครบทุกช่อง"
                );

                return;

            }


            /* แสดงกล่องผลลัพธ์ */

            document.getElementById(
                "resultBox"
            ).style.display = "block";


            /* ซ่อนรูป */

            hideAllImages();


            /* ==================================
               ขั้นตอนที่ 2
               คำนวณ BMI
            ================================== */

            const bmi =
                calculateBMI(weight, height);

            document.getElementById(
                "bmi"
            ).innerText = bmi.toFixed(2);

            document.getElementById(
                "bmiStatus"
            ).innerText = getBMIStatus(bmi);


            /* ==================================
               ขั้นตอนที่ 3
               วิเคราะห์สัดส่วน
            ================================== */

            document.getElementById(
                "showBust"
            ).innerText = bust;

            document.getElementById(
                "showWaist"
            ).innerText = waist;

            document.getElementById(
                "showHip"
            ).innerText = hip;


            const bustHip =
                Math.abs(bust - hip);

            const bustWaist =
                bust - waist;

            const hipWaist =
                hip - waist;


            /* ==================================
               ตัวแปรผลลัพธ์
            ================================== */

            let shape = "";

            let description = "";

            let recommendation = "";

            let clothing = [];

            let imageId = "";


            /* ==================================
               ขั้นตอนที่ 4
               จำแนกรูปร่าง
            ================================== */


            /* นาฬิกาทราย */

            if (
                bustHip <= 2 &&
                bustWaist >= 6 &&
                hipWaist >= 6
            ) {

                shape =
                    "รูปร่างนาฬิกาทราย";

                description =
                    "ไหล่และสะโพกมีความกว้างใกล้เคียงกัน แต่มีช่วงเอวที่คอดชัดเจน ถือเป็นหุ่นที่สมส่วน.สัดส่วนสวย ดูตันหากแต่งผิด ";

                recommendation =
                    "สามารถเลือกเสื้อผ้าที่ช่วยสร้างความสมดุลของสัดส่วน และเลือกแบบที่สวมใส่สบายตามความชอบ";

                clothing = [
                    "เสื้อคอวี",
                    "เสื้อเข้ารูปพอดีตัว",
                    "เดรสที่มีการกำหนดช่วงเอว",
                    "กางเกงหรือกระโปรงเอวสูง"
                ];

                imageId =
                    "hourglassImage";

            }


            /* ลูกแพร์ */

            else if (
                hip - bust >= 2 &&
                hipWaist >= 6
            ) {

                shape =
                    "รูปร่างลูกแพร์";

                description =
                    "ช่วงสะโพกมีขนาดมากกว่าช่วงอก ช่วงสะโพกและต้นขาใหญ่กว่าช่วงไหล่และหน้าอก.เอวสวย อ่อนช้อย สะโพก ต้นขาใหญ่กว่าส่วนบน ";

                recommendation =
                    "สามารถเลือกเสื้อผ้าที่ช่วยสร้างความสมดุลระหว่างช่วงบนและช่วงล่าง";

                clothing = [
                    "เสื้อคอวี",
                    "เสื้อที่มีรายละเอียดบริเวณช่วงบน",
                    "เสื้อแขนพอง",
                    "กางเกงหรือกระโปรงทรงเรียบ"
                ];

                imageId =
                    "pearImage";

            }


            /* สามเหลี่ยมกลับหัว */

            else if (
                bust - hip >= 2 &&
                bustWaist >= 6
            ) {

                shape =
                    "รูปร่างสามเหลี่ยมกลับหัว";

                description =
                    "ช่วงอกมีขนาดมากกว่าช่วงสะโพก  สะโพกค่อนข้างแคบ";

                recommendation =
                    "สามารถเลือกเสื้อผ้าที่ช่วยสร้างความสมดุลระหว่างช่วงบนและช่วงล่าง";

                clothing = [
                    "เสื้อทรงเรียบ",
                    "เสื้อคอวี",
                    "กางเกงทรงกว้าง",
                    "กระโปรงที่ช่วยเพิ่มความสมดุลช่วงล่าง"
                ];

                imageId =
                    "invertedImage";

            }


            /* แอปเปิ้ล */

            else if (
                waist >= bust - 2 &&
                waist >= hip - 2
            ) {

                shape =
                    "รูปร่างแอปเปิ้ล";

                description =
                    "รอบเอวมีขนาดใกล้เคียงกับรอบอกและรอบสะโพก ช่วงลำตัวส่วนบนหนา (ไหล่, หน้าอก, ท้อง) และใหญ่กว่าสะโพก.";

                recommendation =
                    "สามารถเลือกเสื้อผ้าทรงที่สวมใส่สบายและช่วยสร้างเส้นสายของเสื้อผ้า";

                clothing = [
                    "เสื้อทรงตรง",
                    "เสื้อคอวี",
                    "เดรสทรงตรง",
                    "กางเกงหรือกระโปรงทรงตรง"
                ];

                imageId =
                    "appleImage";

            }


            /* ทรงกระบอก */

            else {

                shape =
                    "รูปร่างทรงกระบอก";

                description =
                    "รอบอก รอบเอว และรอบสะโพกมีขนาดค่อนข้างใกล้เคียงกัน.ไหล่ เอว ไม่ค่อยมีส่วนเว้าส่วนโค้ง";

                recommendation =
                    "สามารถเลือกเสื้อผ้าหลากหลายรูปแบบตามสไตล์ที่ชอบ และเลือกแบบที่สวมใส่สบาย";

                clothing = [
                    "เสื้อเข้ารูปพอดีตัว",
                    "เดรสที่มีเข็มขัด",
                    "เสื้อคอวี",
                    "กางเกงหรือกระโปรงเอวสูง"
                ];

                imageId =
                    "rectangleImage";

            }


            /* ==================================
               แสดงผลขั้นตอนที่ 4
            ================================== */

            document.getElementById(
                "result"
            ).innerText = shape;


            /* ==================================
               ขั้นตอนที่ 5
               จุดเด่น-จุดด้อย
            ================================== */

            document.getElementById(
                "description"
            ).innerText = description;


            /* ==================================
               ขั้นตอนที่ 6
               แนวทางการแต่งกาย
            ================================== */

            document.getElementById(
                "recommendation"
            ).innerText = recommendation;


            /* ==================================
               ขั้นตอนที่ 7
               แสดงคำแนะนำเสื้อผ้า
            ================================== */

            const clothingList =
                document.getElementById(
                    "clothingList"
                );

            clothingList.innerHTML = "";


            clothing.forEach(function(item) {

                const li =
                    document.createElement("li");

                li.innerText = item;

                clothingList.appendChild(li);

            });


            /* ==================================
               แสดงรูปที่ตรงกับรูปร่าง
            ================================== */

            document.getElementById(
                imageId
            ).style.display = "block";


            /* เลื่อนไปยังผลลัพธ์ */

            document.getElementById(
                "resultBox"
            ).scrollIntoView({
                behavior: "smooth"
            });

        }

    
        // ป้องกันหน้าเว็บค้างหากรูปภาพภายนอก/ไฟล์เดิมหาไม่พบ
        document.querySelectorAll(".result-image").forEach(function(img) {
            img.addEventListener("error", function() {
                this.style.display = "none";
            });
        });

    </script>

</body>

</html>
