
<html lang="ml">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tharbiyyathul Uloom Committee - West Chalipparambu</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        /* Home Page Styles */
        .home-page {
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
        }

        .home-container {
            text-align: center;
            max-width: 800px;
        }

        .home-logo {
            width: 150px;
            height: 150px;
            background: white;
            border-radius: 50%;
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4em;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .home-title {
            color: white;
            font-size: 3em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease-out;
        }

        .home-subtitle {
            color: rgba(255,255,255,0.9);
            font-size: 1.5em;
            margin-bottom: 40px;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .home-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .home-btn {
            display: inline-block;
            padding: 18px 45px;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.2em;
            font-weight: 600;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .home-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
        }

        .home-btn.admin-btn {
            background: #e74c3c;
            color: white;
        }

        .home-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 50px;
            animation: fadeInUp 1s ease-out 1s both;
        }

        .feature-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 25px;
            border-radius: 15px;
            color: white;
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s;
        }

        .feature-card:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-5px);
        }

        .feature-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .feature-title {
            font-size: 1.1em;
            font-weight: 600;
            margin-bottom: 5px;
        }

        /* Login Modal */
        .login-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .login-modal.active {
            display: flex;
        }

        .login-box {
            background: white;
            padding: 40px;
            border-radius: 15px;
            max-width: 400px;
            width: 90%;
            box-shadow: 0 15px 50px rgba(0,0,0,0.3);
        }

        .login-box h2 {
            color: #667eea;
            margin-bottom: 25px;
            text-align: center;
        }

        .login-box input {
            width: 100%;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1em;
            margin-bottom: 20px;
        }

        .login-box input:focus {
            outline: none;
            border-color: #667eea;
        }

        .login-buttons {
            display: flex;
            gap: 10px;
        }

        .login-buttons button {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .login-btn {
            background: #667eea;
            color: white;
        }

        .cancel-btn {
            background: #e0e0e0;
            color: #333;
        }

        /* Main App Container */
        .main-app {
            display: none;
            padding: 20px;
        }

        .main-app.active {
            display: block;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .header {
            background: white;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .header-left {
            text-align: left;
        }

        .header h1 {
            color: #667eea;
            font-size: 2em;
        }

        .header p {
            color: #666;
        }

        .header-right {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .admin-badge {
            background: #27ae60;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: 600;
        }

        .logout-btn {
            padding: 10px 20px;
            background: #e74c3c;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }

        .tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .tab-btn {
            flex: 1;
            padding: 15px;
            background: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            color: #667eea;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .tab-btn.active {
            background: #667eea;
            color: white;
        }

        .tab-content {
            display: none;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .tab-content.active {
            display: block;
        }

        .form-group { margin-bottom: 20px; }
        .form-group label { display: block; margin-bottom: 8px; font-weight: 600; }
        .form-group input, .form-group textarea {
            width: 100%; padding: 12px; border: 2px solid #ddd; border-radius: 8px;
        }

        .file-input-label {
            display: block; padding: 12px; background: #f8f9fa; border: 2px dashed #667eea;
            border-radius: 8px; text-align: center; cursor: pointer;
        }

        .photo-preview img { max-width: 150px; border-radius: 10px; margin-top: 10px; }

        .btn {
            padding: 12px 25px; background: #667eea; color: white; border: none;
            border-radius: 8px; cursor: pointer; font-weight: 600;
            margin: 2px;
        }

        .members-grid {
            display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px; margin-top: 20px;
        }

        .member-card {
            background: #f8f9fa; padding: 20px; border-radius: 12px;
            text-align: center; box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .member-photo {
            width: 80px; height: 80px; border-radius: 50%; object-fit: cover;
            margin-bottom: 10px; border: 3px solid white; box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .payment-status {
            display: inline-block; padding: 5px 12px; border-radius: 15px;
            font-size: 0.8em; font-weight: 600; margin-top: 10px;
        }

        .payment-pending { background: #fff3cd; color: #856404; }
        .payment-paid { background: #d4edda; color: #155724; }

        .stats {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px; margin-bottom: 30px;
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white; padding: 20px; border-radius: 12px; text-align: center;
        }

        .search-box {
            width: 100%; padding: 15px; border: 2px solid #ddd; border-radius: 10px; margin-bottom: 20px;
        }

        /* Modal for Detail and Edit View */
        .modal {
            display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.5); z-index: 3000; align-items: center; justify-content: center;
            overflow-y: auto; padding: 20px;
        }
        .modal.active { display: flex; }
        .modal-content { 
            background: white; padding: 30px; border-radius: 15px; 
            max-width: 500px; width: 90%; max-height: 90vh; overflow-y: auto;
        }

        @media (max-width: 768px) {
            .header { flex-direction: column; text-align: center; }
            .home-title { font-size: 1.8em; }
        }
    </style>
</head>
<body>

    <div id="home-page" class="home-page">
        <div class="home-container">
            <div class="home-logo">🕌</div>
            <h1 class="home-title">THARBIYYATHUL ULOOM COMMITTEE</h1>
            <p class="home-subtitle">West Chalipparambu</p>
            <div class="home-buttons">
                <button class="home-btn" onclick="enterApp(false)">View Members</button>
                <button class="home-btn admin-btn" onclick="showLoginModal()">🔒 Admin Login</button>
            </div>
            <div class="home-features">
                <div class="feature-card">
                    <div class="feature-icon">👥</div>
                    <div class="feature-title">Member Management</div>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💰</div>
                    <div class="feature-title">Payment Tracking</div>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📊</div>
                    <div class="feature-title">Dashboard</div>
                </div>
            </div>
        </div>
    </div>

    <div id="login-modal" class="login-modal">
        <div class="login-box">
            <h2>🔐 Admin Login</h2>
            <input type="password" id="admin-password" placeholder="Enter Password " onkeypress="if(event.key==='Enter') adminLogin()">
            <div class="login-buttons">
                <button class="login-btn" onclick="adminLogin()">Login</button>
                <button class="cancel-btn" onclick="closeLoginModal()">Cancel</button>
            </div>
        </div>
    </div>

    <div id="main-app" class="main-app">
        <div class="container">
            <div class="header">
                <div class="header-left">
                    <h1>THARBIYYATHUL ULOOM COMMITTEE</h1>
                    <p>West Chalipparambu</p>
                </div>
                <div class="header-right">
                    <span id="admin-badge" class="admin-badge" style="display: none;">👑 Admin</span>
                    <button class="logout-btn" onclick="goHome()">🏠 Home</button>
                </div>
            </div>

            <div class="tabs">
                <button class="tab-btn active" onclick="showTab('dashboard')">Dashboard</button>
                <button id="add-member-tab" class="tab-btn" onclick="showTab('add-member')" style="display: none;">Add Member</button>
                <button class="tab-btn" onclick="showTab('members')">All Members</button>
                <button id="payments-tab" class="tab-btn" onclick="showTab('payments')" style="display: none;">Payments</button>
            </div>

            <div id="dashboard" class="tab-content active">
                <div class="stats">
                    <div class="stat-card"><h3 id="total-members">0</h3><p>Total Members</p></div>
                    <div class="stat-card"><h3 id="pending-count">0</h3><p>Pending Payments</p></div>
                    <div class="stat-card"><h3 id="total-amount">₹0</h3><p>Total Due</p></div>
                </div>
            </div>

            <div id="add-member" class="tab-content">
                <form id="member-form">
                    <div class="form-group"><label>Name</label><input type="text" id="member-name" required></div>
                    <div class="form-group"><label>Phone</label><input type="tel" id="member-phone" required></div>
                    <div class="form-group">
                        <label>Photo</label>
                        <input type="file" id="member-photo" accept="image/*" style="display:none">
                        <label for="member-photo" class="file-input-label">📷 Upload Photo</label>
                        <div id="photo-preview" class="photo-preview"></div>
                    </div>
                    <div class="form-group"><label>Address</label><textarea id="member-address" required></textarea></div>
                    <div class="form-group"><label>Due Amount (₹)</label><input type="number" id="member-payment" value="0"></div>
                    <button type="submit" class="btn">Add Member</button>
                </form>
            </div>

            <div id="members" class="tab-content">
                <input type="text" class="search-box" id="search-members" placeholder="Search members..." oninput="displayMembers()">
                <div class="members-grid" id="members-list"></div>
            </div>

            <div id="payments" class="tab-content">
                <div class="members-grid" id="payments-list"></div>
            </div>
        </div>
    </div>

    <div id="member-modal" class="modal">
        <div class="modal-content">
            <h2 id="modal-title">Details</h2>
            <hr><br>
            <div id="modal-body"></div>
            <br>
            <button class="btn" onclick="closeModal('member-modal')">Close</button>
        </div>
    </div>

    <div id="edit-modal" class="modal">
        <div class="modal-content">
            <h2>✏️ Edit Member</h2>
            <hr><br>
            <form id="edit-form">
                <input type="hidden" id="edit-id">
                <div class="form-group"><label>Name</label><input type="text" id="edit-name" required></div>
                <div class="form-group"><label>Phone</label><input type="tel" id="edit-phone" required></div>
                <div class="form-group">
                    <label>Change Photo (Optional)</label>
                    <input type="file" id="edit-photo-input" accept="image/*" style="display:none">
                    <label for="edit-photo-input" class="file-input-label">📷 Update Photo</label>
                    <div id="edit-photo-preview" class="photo-preview"></div>
                </div>
                <div class="form-group"><label>Address</label><textarea id="edit-address" required></textarea></div>
                <div class="form-group"><label>Total Due Amount (₹)</label><input type="number" id="edit-totalDue"></div>
                <button type="button" class="btn" onclick="saveEdit()">Update Member</button>
                <button type="button" class="btn cancel-btn" onclick="closeModal('edit-modal')">Cancel</button>
            </form>
        </div>
    </div>

    <script>
        let members = [];
        let currentPhotoData = null;
        let editPhotoData = null;
        let isAdmin = false;
        const ADMIN_PASSWORD = '2112';

        // Initialization
        window.onload = () => {
            const stored = localStorage.getItem('committee_members');
            if (stored) members = JSON.parse(stored);
        };

        function showLoginModal() {
            document.getElementById('login-modal').classList.add('active');
        }

        function closeLoginModal() {
            document.getElementById('login-modal').classList.remove('active');
            document.getElementById('admin-password').value = '';
        }

        function adminLogin() {
            const pass = document.getElementById('admin-password').value;
            if (pass === ADMIN_PASSWORD) {
                enterApp(true);
                closeLoginModal();
            } else {
                alert('Incorrect Password!');
            }
        }

        function enterApp(admin) {
            isAdmin = admin;
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('main-app').classList.add('active');
            
            document.getElementById('admin-badge').style.display = admin ? 'block' : 'none';
            document.getElementById('add-member-tab').style.display = admin ? 'block' : 'none';
            document.getElementById('payments-tab').style.display = admin ? 'block' : 'none';
            
            updateDashboard();
            displayMembers();
            if(isAdmin) displayPayments();
        }

        function goHome() {
            document.getElementById('main-app').classList.remove('active');
            document.getElementById('home-page').style.display = 'flex';
        }

        function showTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
            document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            event.currentTarget.classList.add('active');
        }

        // Photo Upload Handling
        document.getElementById('member-photo').addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (ev) => {
                    currentPhotoData = ev.target.result;
                    document.getElementById('photo-preview').innerHTML = `<img src="${currentPhotoData}">`;
                };
                reader.readAsDataURL(file);
            }
        });

        // Edit Photo Upload Handling
        document.getElementById('edit-photo-input').addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (ev) => {
                    editPhotoData = ev.target.result;
                    document.getElementById('edit-photo-preview').innerHTML = `<img src="${editPhotoData}">`;
                };
                reader.readAsDataURL(file);
            }
        });

        // Add Member
        document.getElementById('member-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const newMember = {
                id: Date.now(),
                name: document.getElementById('member-name').value,
                phone: document.getElementById('member-phone').value,
                photo: currentPhotoData || 'https://via.placeholder.com/80',
                address: document.getElementById('member-address').value,
                totalDue: parseFloat(document.getElementById('member-payment').value) || 0,
                paid: 0
            };
            members.push(newMember);
            saveData();
            this.reset();
            document.getElementById('photo-preview').innerHTML = '';
            currentPhotoData = null;
            alert('Member Added!');
            updateDashboard();
            displayMembers();
            if(isAdmin) displayPayments();
        });

        function saveData() {
            localStorage.setItem('committee_members', JSON.stringify(members));
        }

        function updateDashboard() {
            document.getElementById('total-members').innerText = members.length;
            const pending = members.filter(m => m.totalDue > m.paid).length;
            document.getElementById('pending-count').innerText = pending;
            const totalDue = members.reduce((acc, m) => acc + (m.totalDue - m.paid), 0);
            document.getElementById('total-amount').innerText = '₹' + totalDue;
        }

        function displayMembers() {
            const search = document.getElementById('search-members').value.toLowerCase();
            const list = document.getElementById('members-list');
            list.innerHTML = '';
            
            members.filter(m => m.name.toLowerCase().includes(search)).forEach(m => {
                const status = m.paid >= m.totalDue ? 'Paid' : 'Pending';
                const statusClass = m.paid >= m.totalDue ? 'payment-paid' : 'payment-pending';
                
                list.innerHTML += `
                    <div class="member-card">
                        <img src="${m.photo}" class="member-photo">
                        <h3>${m.name}</h3>
                        <p>${m.phone}</p>
                        <span class="payment-status ${statusClass}">${status}</span>
                        <br><br>
                        <button class="btn" onclick="viewDetails(${m.id})">Details</button>
                        ${isAdmin ? `
                            <button class="btn" style="background:#f39c12" onclick="editMember(${m.id})">Edit</button>
                            <button class="btn" style="background:#e74c3c" onclick="deleteMember(${m.id})">Delete</button>
                        ` : ''}
                    </div>
                `;
            });
        }

        function displayPayments() {
            const list = document.getElementById('payments-list');
            list.innerHTML = '';
            members.forEach(m => {
                list.innerHTML += `
                    <div class="member-card">
                        <h3>${m.name}</h3>
                        <p>Total: ₹${m.totalDue} | Paid: ₹${m.paid}</p>
                        <p>Balance: ₹${m.totalDue - m.paid}</p>
                        <input type="number" id="pay-${m.id}" placeholder="Enter amount" style="width:100px; padding:5px; margin:10px 0;">
                        <button class="btn" onclick="makePayment(${m.id})">Update Paid</button>
                    </div>
                `;
            });
        }

        function makePayment(id) {
            const amt = parseFloat(document.getElementById(`pay-${id}`).value);
            if(isNaN(amt)) return;
            const idx = members.findIndex(m => m.id === id);
            members[idx].paid += amt;
            saveData();
            updateDashboard();
            displayMembers();
            displayPayments();
            alert('Payment Updated!');
        }

        function deleteMember(id) {
            if(confirm('Are you sure you want to delete this member?')) {
                members = members.filter(m => m.id !== id);
                saveData();
                updateDashboard();
                displayMembers();
                if(isAdmin) displayPayments();
            }
        }

        function editMember(id) {
            const m = members.find(member => member.id === id);
            document.getElementById('edit-id').value = m.id;
            document.getElementById('edit-name').value = m.name;
            document.getElementById('edit-phone').value = m.phone;
            document.getElementById('edit-address').value = m.address;
            document.getElementById('edit-totalDue').value = m.totalDue;
            document.getElementById('edit-photo-preview').innerHTML = `<img src="${m.photo}">`;
            editPhotoData = m.photo;
            document.getElementById('edit-modal').classList.add('active');
        }

        function saveEdit() {
            const id = parseInt(document.getElementById('edit-id').value);
            const idx = members.findIndex(m => m.id === id);
            
            members[idx].name = document.getElementById('edit-name').value;
            members[idx].phone = document.getElementById('edit-phone').value;
            members[idx].address = document.getElementById('edit-address').value;
            members[idx].totalDue = parseFloat(document.getElementById('edit-totalDue').value) || 0;
            members[idx].photo = editPhotoData;

            saveData();
            updateDashboard();
            displayMembers();
            if(isAdmin) displayPayments();
            closeModal('edit-modal');
            alert('Member Updated Successfully!');
        }

        function viewDetails(id) {
            const m = members.find(member => member.id === id);
            document.getElementById('modal-title').innerText = m.name;
            document.getElementById('modal-body').innerHTML = `
                <center><img src="${m.photo}" style="width:120px; border-radius:10px;"></center><br>
                <p><strong>Phone:</strong> ${m.phone}</p>
                <p><strong>Address:</strong> ${m.address}</p>
                <p><strong>Total Due:</strong> ₹${m.totalDue}</p>
                <p><strong>Total Paid:</strong> ₹${m.paid}</p>
                <p><strong>Balance:</strong> ₹${m.totalDue - m.paid}</p>
            `;
            document.getElementById('member-modal').classList.add('active');
        }

        function closeModal(modalId) {
            document.getElementById(modalId).classList.remove('active');
        }
    </script>
</body>
</html>
