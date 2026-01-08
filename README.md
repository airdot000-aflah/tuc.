<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Admin Panel - Tharbiyyathul Uloom</title>
    
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

        /* --- Global Center Alignment --- */
        .page-section {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* --- Common Box Style --- */
        .card {
            background: #fff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 400px;
            width: 100%;
            text-align: center;
        }

        h1 { color: #0a6ccf; margin-bottom: 20px; font-size: 22px; }
        
        /* --- Login Styles --- */
        input[type="password"], input[type="text"], input[type="number"], input[type="date"] {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            outline: none;
        }

        .btn {
            background: #0a6ccf;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: 0.3s;
        }
        .btn:hover { background: #085cb3; }

        /* --- Hide Sections Initially --- */
        #home-page, #receipt-page { display: none; }

        /* --- Receipt Styles --- */
        .receipt-container { max-width: 420px; width: 100%; }
        .receipt {
            background: #fff;
            border: 2px solid #0a6ccf;
            position: relative;
            overflow: hidden;
            padding-bottom: 20px;
            text-align: left;
        }
        .watermark {
            position: absolute; top: 55%; left: 50%;
            transform: translate(-50%,-50%); opacity: 0.08;
            width: 180px; z-index: 0; pointer-events: none;
        }
        .header {
            background: #0a6ccf; color: #fff; text-align: center;
            padding: 15px 10px; position: relative; z-index: 1;
        }
        .receipt-title {
            background: #fff; color: #0a6ccf; display: inline-block;
            padding: 2px 12px; border-radius: 20px; margin-top: 8px;
            font-weight: bold; font-size: 13px;
        }
        .section { padding: 15px 20px; position: relative; z-index: 1; }
        .label { font-size: 10px; color: #555; font-weight: bold; text-transform: uppercase; }
        .receipt-input {
            border: none !important; border-bottom: 1px dotted #0a6ccf !important;
            border-radius: 0 !important; padding: 5px 0 !important; font-size: 14px;
        }
        .total-box {
            margin-top: 15px; border: 2px solid #0a6ccf; display: flex; align-items: center;
        }
        .total-label { background: #0a6ccf; color: #fff; padding: 8px; font-weight: bold; font-size: 13px; }
        .total-box input { border: none !important; padding: 8px !important; color: #0a6ccf; font-weight: bold; }
        
        .footer-receipt {
            display: flex; justify-content: space-between; align-items: flex-end;
            padding: 0 20px; position: relative; z-index: 1;
        }
        .cash-stamp {
            border: 2px solid #28a745; color: #28a745; padding: 4px 8px;
            font-weight: bold; transform: rotate(-10deg); border-radius: 5px; font-size: 11px;
        }

        .action-btns { display: flex; gap: 10px; margin-top: 20px; width: 100%; }
        .btn-share { background: #28a745; }

        /* --- Footer --- */
        .site-footer {
            text-align: center; padding: 10px; font-size: 11px; color: #aaa;
        }
    </style>
</head>
<body>

    <div id="login-page" class="page-section">
        <div class="card">
            <h1>Admin Login</h1>
            <input type="password" id="adminPass" placeholder="Enter Admin Password">
            <button class="btn" onclick="checkLogin()">Login</button>
            <p id="error" style="color: red; font-size: 12px; margin-top: 10px; display: none;">Incorrect Password!</p>
        </div>
    </div>

    <div id="home-page" class="page-section">
        <div class="card">
            <h1>Tharbiyyathul Uloom</h1>
            <p style="color: #666; margin-bottom: 25px;">Welcome Admin, you can now generate cash receipts.</p>
            <button class="btn" onclick="showReceiptForm()">Get Started</button>
        </div>
    </div>

    <div id="receipt-page" class="page-section">
        <div class="receipt-container">
            <div id="receipt" class="receipt">
                <div class="watermark">
                    <svg viewBox="0 0 24 24" fill="#0a6ccf"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path></svg>
                </div>
                <div class="header">
                    <h2 style="margin:0; font-size: 16px;">THARBIYYATHUL ULOOM COMMITTEE</h2>
                    <small style="font-size: 10px;">tharbiyyathululoomcommittee@gmail.com</small><br>
                    <div class="receipt-title">CASH RECEIPT</div>
                </div>
                <div class="section">
                    <div style="display: flex; gap: 10px;">
                        <div style="flex: 2;">
                            <div class="label">Date</div>
                            <input type="date" id="rDate" class="receipt-input">
                        </div>
                        <div style="flex: 1;">
                            <div class="label">No.</div>
                            <input type="text" placeholder="001" class="receipt-input">
                        </div>
                    </div>
                    <div style="margin-top: 10px;">
                        <div class="label">Received From</div>
                        <input type="text" placeholder="Name" class="receipt-input">
                    </div>
                    <div style="margin-top: 10px;">
                        <div class="label">Purpose</div>
                        <input type="text" placeholder="Reason" class="receipt-input">
                    </div>
                    <div class="total-box">
                        <div class="total-label">₹ AMOUNT</div>
                        <input type="number" placeholder="0.00">
                    </div>
                </div>
                <div class="footer-receipt">
                    <div style="text-align: center;">
                        <input type="text" class="receipt-input" style="width: 100px; text-align: center;">
                        <div class="label" style="margin-top: 5px;">Received By</div>
                    </div>
                    <div class="cash-stamp">PAID CASH</div>
                </div>
            </div>
            <div class="action-btns">
                <button class="btn" onclick="saveImg()">Download</button>
                <button class="btn btn-share" onclick="shareImg()">WhatsApp Share</button>
            </div>
            <button class="btn" style="margin-top: 10px; background: #666;" onclick="location.reload()">Logout</button>
        </div>
    </div>

    <div class="site-footer">
        airdot_design
    </div>

    <script>
        // പാസ്‌വേഡ് പരിശോധന
        function checkLogin() {
            const pass = document.getElementById('adminPass').value;
            if(pass === "2112") {
                document.getElementById('login-page').style.display = 'none';
                document.getElementById('home-page').style.display = 'flex';
            } else {
                document.getElementById('error').style.display = 'block';
            }
        }

        function showReceiptForm() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('receipt-page').style.display = 'flex';
            document.getElementById('rDate').valueAsDate = new Date();
        }

        function saveImg() {
            const receipt = document.getElementById('receipt');
            html2canvas(receipt, {scale: 3}).then(canvas => {
                let link = document.createElement("a");
                link.href = canvas.toDataURL();
                link.download = "Receipt.png";
                link.click();
            });
        }

        function shareImg() {
            const receipt = document.getElementById('receipt');
            html2canvas(receipt, {scale: 3}).then(canvas => {
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
