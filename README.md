<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Receipt Generator - Tharbiyyathul Uloom</title>
    
    <script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>

    <style>
        * { box-sizing: border-box; }
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f2f5;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* --- Home Page Styles --- */
        #home-page {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }
        .hero-box {
            background: #fff;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 500px;
        }
        .hero-box h1 { color: #0a6ccf; margin-bottom: 10px; }
        .hero-box p { color: #666; margin-bottom: 30px; }
        
        .get-started-btn {
            background: #0a6ccf;
            color: white;
            padding: 15px 35px;
            border: none;
            border-radius: 50px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            text-transform: uppercase;
        }
        .get-started-btn:hover { background: #085cb3; transform: scale(1.05); }

        /* --- Receipt Page Styles --- */
        #receipt-page {
            display: none; /* Initially Hidden */
            padding: 20px;
            flex: 1;
        }
        .receipt-container {
            max-width: 420px;
            margin: auto;
        }
        .receipt {
            background: #fff;
            border: 2px solid #0a6ccf;
            position: relative;
            overflow: hidden;
            padding-bottom: 20px;
        }
        .watermark {
            position: absolute; top: 55%; left: 50%;
            transform: translate(-50%,-50%); opacity: 0.08;
            width: 200px; z-index: 0; pointer-events: none;
        }
        .header {
            background: #0a6ccf; color: #fff; text-align: center;
            padding: 20px 10px; position: relative; z-index: 1;
        }
        .receipt-title {
            background: #fff; color: #0a6ccf; display: inline-block;
            padding: 3px 15px; border-radius: 20px; margin-top: 10px;
            font-weight: bold; font-size: 14px;
        }
        .section { padding: 20px 25px; position: relative; z-index: 1; }
        .field { margin-bottom: 18px; }
        .label { font-size: 11px; color: #555; font-weight: bold; text-transform: uppercase; }
        input {
            width: 100%; border: none; border-bottom: 1.5px dotted #0a6ccf;
            padding: 8px 0; font-size: 15px; outline: none; background: transparent;
        }
        .total-box {
            margin-top: 20px; border: 2px solid #0a6ccf; display: flex; align-items: center;
        }
        .total-label { background: #0a6ccf; color: #fff; padding: 10px; font-weight: bold; }
        .total-box input { border: none; padding: 10px; font-weight: bold; color: #0a6ccf; }
        
        .footer-receipt {
            display: flex; justify-content: space-between; align-items: flex-end;
            padding: 0 25px; position: relative; z-index: 1;
        }
        .cash-stamp {
            border: 2px solid #28a745; color: #28a745; padding: 5px 10px;
            font-weight: bold; transform: rotate(-10deg); border-radius: 5px; font-size: 12px;
        }
        .action-btns { text-align: center; margin-top: 20px; }
        .btn {
            padding: 10px 20px; margin: 5px; border: none; border-radius: 5px;
            cursor: pointer; font-weight: bold; color: white;
        }
        .btn-save { background: #0a6ccf; }
        .btn-share { background: #28a745; }

        /* --- Common Footer --- */
        .site-footer {
            text-align: center; padding: 15px; font-size: 12px; color: #999;
        }
    </style>
</head>
<body>

    <div id="home-page">
        <div class="hero-box">
            <h1>Tharbiyyathul Uloom</h1>
            <p>Digital Receipt Management System</p>
            <button class="get-started-btn" onclick="startApp()">Get Started</button>
        </div>
    </div>

    <div id="receipt-page">
        <div class="receipt-container">
            <div id="receipt" class="receipt">
                <div class="watermark">
                    <svg viewBox="0 0 24 24" fill="#0a6ccf"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path></svg>
                </div>
                <div class="header">
                    <h2>THARBIYYATHUL ULOOM COMMITTEE</h2>
                    <small>tharbiyyathululoomcommittee@gmail.com</small>
                    <div class="receipt-title">CASH RECEIPT</div>
                </div>
                <div class="section">
                    <div style="display: flex; gap: 10px;">
                        <div class="field" style="flex: 2;">
                            <div class="label">Date</div>
                            <input type="date" id="rDate">
                        </div>
                        <div class="field" style="flex: 1;">
                            <div class="label">No.</div>
                            <input type="text" placeholder="001">
                        </div>
                    </div>
                    <div class="field">
                        <div class="label">Received From</div>
                        <input type="text" placeholder="Full Name">
                    </div>
                    <div class="field">
                        <div class="label">Purpose</div>
                        <input type="text" placeholder="Reason for payment">
                    </div>
                    <div class="total-box">
                        <div class="total-label">₹ AMOUNT</div>
                        <input type="number" placeholder="0.00">
                    </div>
                </div>
                <div class="footer-receipt">
                    <div style="text-align: center;">
                        <input type="text" style="width: 120px; text-align: center;">
                        <div class="label" style="margin-top: 5px;">Received By</div>
                    </div>
                    <div class="cash-stamp">PAID CASH</div>
                </div>
            </div>
            <div class="action-btns">
                <button class="btn btn-save" onclick="saveImg()">Download</button>
                <button class="btn btn-share" onclick="shareImg()">Share WhatsApp</button>
            </div>
        </div>
    </div>

    <div class="site-footer">
        airdot_design
    </div>

    <script>
        // പക്കേജ് തുടങ്ങാനുള്ള ഫങ്ക്ഷൻ
        function startApp() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('receipt-page').style.display = 'block';
            document.getElementById('rDate').valueAsDate = new Date();
        }

        // സേവ് ചെയ്യാനുള്ള ഫങ്ക്ഷൻ
        function saveImg() {
            const receipt = document.getElementById('receipt');
            html2canvas(receipt, {scale: 2}).then(canvas => {
                let link = document.createElement("a");
                link.href = canvas.toDataURL();
                link.download = "Receipt.png";
                link.click();
            });
        }

        // ഷെയർ ചെയ്യാനുള്ള ഫങ്ക്ഷൻ
        function shareImg() {
            const receipt = document.getElementById('receipt');
            html2canvas(receipt, {scale: 2}).then(canvas => {
                canvas.toBlob(blob => {
                    const file = new File([blob], "receipt.png", { type: "image/png" });
                    if (navigator.canShare && navigator.canShare({ files: [file] })) {
                        navigator.share({ files: [file], title: "Receipt" });
                    } else {
                        alert("Sharing not supported in this browser.");
                    }
                });
            });
        }
    </script>
</body>
</html>
