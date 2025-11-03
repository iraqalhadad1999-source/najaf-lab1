عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مختبر الرقابة الدوائية</title>
    <style>
        /* أنماط CSS الأساسية */
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --doctor-color: #27ae60;
            --self-color: #e74c3c;
            --admin-color: #9b59b6;
            --lab1-color: #e67e22;
            --lab2-color: #16a085;
            --lab3-color: #8e44ad;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            direction: rtl;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* أنماط صفحة الدخول */
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
        }
        
        .login-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 400px;
        }
        
        .login-form h2 {
            text-align: center;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .form-group {
            margin-bottom: 15px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: var(--secondary-color);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #2980b9;
        }
        
        .btn-block {
            display: block;
            width: 100%;
        }
        
        /* أنماط لوحة التحكم */
        .dashboard {
            display: none;
        }
        
        .header {
            background-color: var(--primary-color);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        
        .user-info {
            display: flex;
            align-items: center;
        }
        
        .user-role {
            margin-left: 10px;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 14px;
        }
        
        .role-doctor {
            background-color: var(--doctor-color);
        }
        
        .role-self {
            background-color: var(--self-color);
        }
        
        .role-admin {
            background-color: var(--admin-color);
        }
        
        .lab-badge {
            padding: 3px 8px;
            border-radius: 15px;
            font-size: 12px;
            margin-right: 5px;
        }
        
        .lab-1 { background-color: var(--lab1-color); color: white; }
        .

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
lab-2 { background-color: var(--lab2-color); color: white; }
        .lab-3 { background-color: var(--lab3-color); color: white; }
        
        .logout-btn {
            background: none;
            border: 1px solid white;
            color: white;
            padding: 5px 15px;
            border-radius: 5px;
            margin-right: 15px;
            cursor: pointer;
        }
        
        .sidebar {
            width: 250px;
            background-color: white;
            height: calc(100vh - 70px);
            position: fixed;
            top: 70px;
            right: 0;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
            padding-top: 20px;
            overflow-y: auto;
        }
        
        .sidebar-menu {
            list-style: none;
        }
        
        .sidebar-menu li {
            margin-bottom: 5px;
        }
        
        .sidebar-menu a {
            display: block;
            padding: 12px 20px;
            color: var(--dark-color);
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .sidebar-menu a:hover, .sidebar-menu a.active {
            background-color: var(--light-color);
            border-right: 3px solid var(--secondary-color);
        }
        
        .main-content {
            margin-right: 250px;
            padding: 20px;
        }
        
        .page {
            display: none;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .page.active {
            display: block;
        }
        
        .page-header {
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .stats-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .stat-card {
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .stat-card h3 {
            font-size: 14px;
            color: #777;
            margin-bottom: 10px;
        }
        
        .stat-card .value {
            font-size: 24px;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }
        
        table, th, td {
            border: 1px solid #ddd;
        }
        
        th, td {
            padding: 12px;
            text-align: right;
        }
        
        th {
            background-color: var(--light-color);
        }
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        .form-container {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            margin-top: 20px;
        }
        
        .btn-primary {
            background-color: var(--secondary-color);
        }
        
        .btn-success {
            background-color: var(--doctor-color);
        }
        
        .btn-danger {
            background-color: var(--self-color);
        }
        
        .tabs {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid #ddd;
        }
        
        .tab {
            padding: 10px 20px;
            cursor: pointer;
            border: 1px solid transparent;
            border-bottom: none;
            border-radius: 5px 5px 0 0;
            margin-left: 5px;
        }
        
        .tab.active {
            background-color: white;
            border-color: #ddd;
            border-bottom-color: white;
            margin-bottom: -1px;
        }
        
        .tab-content {

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
display: none;
        }
        
        .tab-content.active {
            display: block;
        }
        
        .expired {
            background-color: #ffebee;
            color: #c62828;
        }
        
        .expiring-soon {
            background-color: #fff8e1;
        }
        
        .lab-stats {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .lab-stat-card {
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border-top: 4px solid;
        }
        
        .lab-1-card { border-color: var(--lab1-color); }
        .lab-2-card { border-color: var(--lab2-color); }
        .lab-3-card { border-color: var(--lab3-color); }
        
        .material-info {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
            border-right: 4px solid var(--secondary-color);
        }
        
        /* أنماط الاستجابة للشاشات المختلفة */
        @media (max-width: 768px) {
            .sidebar {
                width: 100%;
                height: auto;
                position: static;
            }
            
            .main-content {
                margin-right: 0;
            }
            
            .header-content {
                flex-direction: column;
                gap: 10px;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .tab {
                margin-left: 0;
                margin-bottom: 5px;
                border-radius: 5px;
            }
            
            .tab.active {
                margin-bottom: 5px;
            }
        }
        
        .status-pending { background-color: #fff3cd; color: #856404; }
        .status-accepted { background-color: #d1ecf1; color: #0c5460; }
        .status-rejected { background-color: #f8d7da; color: #721c24; }
    </style>
</head>
<body>
    <!-- صفحة الدخول -->
    <div class="login-container" id="loginPage">
        <div class="login-form">
            <h2>تسجيل الدخول</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="username">اسم المستخدم</label>
                    <input type="text" id="username" required>
                </div>
                <div class="form-group">
                    <label for="password">كلمة المرور</label>
                    <input type="password" id="password" required>
                </div>
                <button type="submit" class="btn btn-block">دخول</button>
            </form>
        </div>
    </div>

    <!-- لوحة التحكم -->
    <div class="dashboard" id="dashboard">
        <!-- الرأس -->
        <header class="header">
            <div class="container header-content">
                <div class="logo">مختبر الرقابة الدوائية</div>
                <div class="user-info">
                    <button class="logout-btn" id="logoutBtn">تسجيل الخروج</button>
                    <div class="user-role" id="userRoleDisplay"></div>
                    <span id="userLabDisplay"></span>
                    <span id="userNameDisplay"></span>
                </div>
            </div>
        </header>

        <!-- الشريط الجانبي -->
        <div class="sidebar">
            <ul class="sidebar-menu">
                <li><a href="#" class="nav-link active" data-page="dashboardPage">لوحة التحكم</a></li>
                <li id="usersManagementLink" style="display: none;"><a href="#" class="nav-link" data-page="usersPage">إدارة المستخدمين</a></li>
                <li id="reportsLink" style="display: none;"><a href="#" class="nav-link" data-page="reportsPage">التقارير والتحليلات</a></li>
                <li id="chemistrySectionLink" style="display: none;"><a href="#" class="nav-link" data-page="chemistryPage">قسم الكيمياء</a></li>

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
<li id="warehouseSectionLink" style="display: none;"><a href="#" class="nav-link" data-page="warehousePage">المخزن</a></li>
            </ul>
        </div>

        <!-- المحتوى الرئيسي -->
        <div class="main-content">
            <!-- صفحة لوحة التحكم -->
            <div class="page active" id="dashboardPage">
                <div class="page-header">
                    <h2>لوحة التحكم</h2>
                </div>
                
                <!-- إحصائيات المختبرات (للمدير فقط) -->
                <div id="labsStats" style="display: none;">
                    <h3>إحصائيات المختبرات</h3>
                    <div class="lab-stats">
                        <div class="lab-stat-card lab-1-card">
                            <h4>المختبر الأول</h4>
                            <div class="stats">
                                <p>المواد الكلية: <span id="lab1Total">0</span></p>
                                <p>المواد المنتهية: <span id="lab1Expired">0</span></p>
                                <p>الدكاترة المسؤولين: <span id="lab1Doctors">0</span></p>
                            </div>
                        </div>
                        <div class="lab-stat-card lab-2-card">
                            <h4>المختبر الثاني</h4>
                            <div class="stats">
                                <p>المواد الكلية: <span id="lab2Total">0</span></p>
                                <p>المواد المنتهية: <span id="lab2Expired">0</span></p>
                                <p>الدكاترة المسؤولين: <span id="lab2Doctors">0</span></p>
                            </div>
                        </div>
                        <div class="lab-stat-card lab-3-card">
                            <h4>المختبر الثالث</h4>
                            <div class="stats">
                                <p>المواد الكلية: <span id="lab3Total">0</span></p>
                                <p>المواد المنتهية: <span id="lab3Expired">0</span></p>
                                <p>الدكاترة المسؤولين: <span id="lab3Doctors">0</span></p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="stats-cards">
                    <div class="stat-card">
                        <h3>إجمالي المواد</h3>
                        <div class="value" id="totalMaterials">0</div>
                    </div>
                    <div class="stat-card">
                        <h3>المواد المنتهية الصلاحية</h3>
                        <div class="value" id="expiredMaterials">0</div>
                    </div>
                    <div class="stat-card">
                        <h3>المواد المضافة حديثاً</h3>
                        <div class="value" id="recentMaterials">0</div>
                    </div>
                    <div class="stat-card">
                        <h3>المستخدمين النشطين</h3>
                        <div class="value" id="activeUsers">0</div>
                    </div>
                </div>
                <div class="recent-activities">
                    <h3>آخر الأنشطة</h3>
                    <table>
                        <thead>
                            <tr>
                                <th>النشاط</th>
                                <th>المستخدم</th>
                                <th>التاريخ</th>
                            </tr>
                        </thead>
                        <tbody id="activitiesTable">
                            <!-- سيتم ملؤها بالبيانات -->
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- صفحة إدارة المستخدمين (للمدير فقط) -->
            <div class="page" id="usersPage">
                <div class="page-header">
                    <h2>إدارة المستخدمين</h2>
                </div>
                <div class="action-buttons">
                    <button class="btn btn-primary" id="addUserBtn">إضافة مستخدم</button>
                </div>
                <table>
                    <thead>

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
<tr>
                            <th>اسم المستخدم</th>
                            <th>الاسم الكامل</th>
                            <th>نوع المستخدم</th>
                            <th>المختبر</th>
                            <th>الحالة</th>
                            <th>الإجراءات</th>
                        </tr>
                    </thead>
                    <tbody id="usersTable">
                        <!-- سيتم ملؤها بالبيانات -->
                    </tbody>
                </table>
                
                <!-- نموذج إضافة مستخدم -->
                <div id="userFormModal" style="display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.5); z-index: 1000;">
                    <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: white; padding: 30px; border-radius: 10px; width: 90%; max-width: 500px;">
                        <h3>إضافة مستخدم جديد</h3>
                        <form id="addUserForm">
                            <div class="form-group">
                                <label for="newUsername">اسم المستخدم</label>
                                <input type="text" id="newUsername" required>
                            </div>
                            <div class="form-group">
                                <label for="newPassword">كلمة المرور</label>
                                <input type="password" id="newPassword" required>
                            </div>
                            <div class="form-group">
                                <label for="newFullName">الاسم الكامل</label>
                                <input type="text" id="newFullName" required>
                            </div>
                            <div class="form-group">
                                <label for="newUserType">نوع المستخدم</label>
                                <select id="newUserType" required>
                                    <option value="doctor">دكتور</option>
                                    <option value="self">ذاتية</option>
                                    <option value="admin">مدير النظام</option>
                                </select>
                            </div>
                            <div class="form-group" id="labSelection" style="display: none;">
                                <label for="userLab">المختبر المسؤول</label>
                                <select id="userLab">
                                    <option value="1">المختبر الأول</option>
                                    <option value="2">المختبر الثاني</option>
                                    <option value="3">المختبر الثالث</option>
                                </select>
                            </div>
                            <div class="action-buttons">
                                <button type="submit" class="btn btn-success">إضافة</button>
                                <button type="button" class="btn btn-danger" onclick="closeUserForm()">إلغاء</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>

            <!-- صفحة التقارير والتحليلات (للمدير فقط) -->
            <div class="page" id="reportsPage">
                <div class="page-header">
                    <h2>التقارير والتحليلات</h2>
                </div>
                <div class="reports-content">
                    <div class="form-group">
                        <label for="reportType">نوع التقرير</label>
                        <select id="reportType">
                            <option value="materials">تقرير المواد</option>
                            <option value="expiry">تقرير المواد المنتهية الصلاحية</option>
                            <option value="usage">تقرير استخدام المواد</option>
                            <option value="labs">تقرير المختبرات</option>
                        </select>
                    </div>
                    <div class="form-group">

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
<label for="dateRange">الفترة الزمنية</label>
                        <input type="date" id="startDate">
                        <span>إلى</span>
                        <input type="date" id="endDate">
                    </div>
                    <button class="btn btn-primary" id="generateReportBtn">إنشاء التقرير</button>
                    <div id="reportResults" style="margin-top: 20px;">
                        <!-- سيتم عرض نتائج التقرير هنا -->
                    </div>
                </div>
            </div>

            <!-- صفحة قسم الكيمياء (للدكتور فقط) -->
            <div class="page" id="chemistryPage">
                <div class="page-header">
                    <h2>قسم الكيمياء - <span id="currentLabName"></span></h2>
                </div>
                
                <!-- معلومات المادة المختارة -->
                <div id="selectedMaterialInfo" class="material-info" style="display: none;">
                    <h4>معلومات المادة المختارة</h4>
                    <p><strong>اسم المادة:</strong> <span id="infoMaterialName"></span></p>
                    <p><strong>رقم الوارد:</strong> <span id="infoSupplierNumber"></span></p>
                    <p><strong>المختبر:</strong> <span id="infoLab"></span></p>
                </div>
                
                <div class="form-container">
                    <form id="chemistryForm">
                        <div class="form-group">
                            <label for="selectedMaterial">اختر المادة للفحص</label>
                            <select id="selectedMaterial" required>
                                <option value="">اختر المادة</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="analysisMethod">طريقة التحليل</label>
                            <select id="analysisMethod" required>
                                <option value="">اختر طريقة التحليل</option>
                                <option value="USp">USp</option>
                                <option value="Bp">Bp</option>
                                <option value="company">Company</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="materialStatus">حالة المادة</label>
                            <select id="materialStatus" required>
                                <option value="pending">قيد المراجعة</option>
                                <option value="accepted">مقبولة</option>
                                <option value="rejected">مرفوضة</option>
                            </select>
                        </div>
                        <div class="action-buttons">
                            <button type="submit" class="btn btn-success">إضافة نتيجة الفحص</button>
                        </div>
                    </form>
                </div>
                
                <!-- مواد المختبر -->
                <div style="margin-top: 30px;">
                    <h3>مواد المختبر</h3>
                    <table>
                        <thead>
                            <tr>
                                <th>اسم المادة</th>
                                <th>رقم الوارد</th>
                                <th>طريقة التحليل</th>
                                <th>الحالة</th>
                                <th>تاريخ الإضافة</th>
                                <th>تمت الإضافة بواسطة</th>
                            </tr>
                        </thead>
                        <tbody id="labMaterialsTable">
                            <!-- سيتم ملؤها بالبيانات -->
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- صفحة المخزن (للذاتية فقط) -->
            <div class="page" id="warehousePage">
                <div class="page-header">

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
<h2>المخزن</h2>
                </div>
                
                <!-- تبويبات المخزن -->
                <div class="tabs">
                    <div class="tab active" data-tab="addMaterialTab">إضافة مادة جديدة</div>
                    <div class="tab" data-tab="viewMaterialsTab">عرض المواد المضافة</div>
                </div>
                
                <!-- محتوى تبويب إضافة مادة جديدة -->
                <div class="tab-content active" id="addMaterialTab">
                    <div class="form-container">
                        <form id="warehouseForm">
                            <div class="form-group">
                                <label for="warehouseMaterialName">اسم المادة</label>
                                <input type="text" id="warehouseMaterialName" required>
                            </div>
                            <div class="form-group">
                                <label for="materialType">نوع المادة</label>
                                <select id="materialType" required>
                                    <option value="standard">مادة قياسية</option>
                                    <option value="chemical">مادة كيميائية</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="materialLab">المختبر المستهدف</label>
                                <select id="materialLab" required>
                                    <option value="1">المختبر الأول</option>
                                    <option value="2">المختبر الثاني</option>
                                    <option value="3">المختبر الثالث</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="materialCategory">تصنيف المادة</label>
                                <input type="text" id="materialCategory" required>
                            </div>
                            <div class="form-group">
                                <label for="quantity">الكمية</label>
                                <input type="number" id="quantity" required>
                            </div>
                            <div class="form-group">
                                <label for="receiveDate">تاريخ الاستلام</label>
                                <input type="date" id="receiveDate" required>
                            </div>
                            <div class="form-group">
                                <label for="expiryDate">تاريخ الانتهاء</label>
                                <input type="date" id="expiryDate" required>
                            </div>
                            <div class="form-group">
                                <label for="supplierNumber">رقم الوارد</label>
                                <input type="text" id="supplierNumber" required>
                            </div>
                            <div class="form-group">
                                <label for="notes">ملاحظات</label>
                                <textarea id="notes" rows="3"></textarea>
                            </div>
                            <div class="action-buttons">
                                <button type="submit" class="btn btn-success">إضافة إلى المخزن</button>
                            </div>
                        </form>
                    </div>
                </div>
                
                <!-- محتوى تبويب عرض المواد المضافة -->
                <div class="tab-content" id="viewMaterialsTab">
                    <div class="action-buttons">
                        <button class="btn btn-primary" id="refreshMaterialsBtn">تحديث القائمة</button>
                    </div>
                    <div class="materials-summary">
                        <h3>المواد المضافة بواسطة: <span id="currentUserName"></span></h3>
                        <p>إجمالي المواد: <span id="userMaterialsCount">0</span> مادة</p>

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
</div>
                    <table>
                        <thead>
                            <tr>
                                <th>اسم المادة</th>
                                <th>النوع</th>
                                <th>المختبر المستهدف</th>
                                <th>التصنيف</th>
                                <th>الكمية</th>
                                <th>تاريخ الاستلام</th>
                                <th>تاريخ الانتهاء</th>
                                <th>رقم الوارد</th>
                                <th>الحالة</th>
                                <th>الإجراءات</th>
                            </tr>
                        </thead>
                        <tbody id="warehouseMaterialsTable">
                            <!-- سيتم ملؤها بالبيانات -->
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <script>
        // بيانات التطبيق الافتراضية
        const defaultUsers = [
            { 
                username: 'admin', 
                password: 'admin123', 
                type: 'admin', 
                name: 'مدير النظام',
                lab: null
            },
            { 
                username: 'doctor1', 
                password: 'doctor123', 
                type: 'doctor', 
                name: 'د. أحمد محمد',
                lab: '1'
            },
            { 
                username: 'doctor2', 
                password: 'doctor123', 
                type: 'doctor', 
                name: 'د. فاطمة علي',
                lab: '2'
            },
            { 
                username: 'self', 
                password: 'self123', 
                type: 'self', 
                name: 'موظف ذاتية',
                lab: null
            }
        ];

        const defaultActivities = [];
        const defaultMaterials = [];

        // بيانات التطبيق
        let currentUser = null;
        let materials = [];
        let users = [];
        let activities = [];

        // عناصر DOM
        const loginPage = document.getElementById('loginPage');
        const dashboard = document.getElementById('dashboard');
        const loginForm = document.getElementById('loginForm');
        const logoutBtn = document.getElementById('logoutBtn');
        const userRoleDisplay = document.getElementById('userRoleDisplay');
        const userNameDisplay = document.getElementById('userNameDisplay');
        const userLabDisplay = document.getElementById('userLabDisplay');
        const navLinks = document.querySelectorAll('.nav-link');
        const pages = document.querySelectorAll('.page');
        
        // عناصر الصلاحيات
        const usersManagementLink = document.getElementById('usersManagementLink');
        const reportsLink = document.getElementById('reportsLink');
        const chemistrySectionLink = document.getElementById('chemistrySectionLink');
        const warehouseSectionLink = document.getElementById('warehouseSectionLink');
        const labsStats = document.getElementById('labsStats');
        
        // عناصر المخزن
        const warehouseForm = document.getElementById('warehouseForm');
        const warehouseMaterialsTable = document.getElementById('warehouseMaterialsTable');
        const userMaterialsCount = document.getElementById('userMaterialsCount');
        const currentUserNameDisplay = document.getElementById('currentUserName');
        const refreshMaterialsBtn = document.getElementById('refreshMaterialsBtn');
        const tabs = document.querySelectorAll('.tab');
        const tabContents = document.querySelectorAll('.tab-content');

        // عناصر قسم الكيمياء
        const selectedMaterial = document.getElementById('selectedMaterial');
        const selectedMaterialInfo = document.getElementById('selectedMaterialInfo');
        const infoMaterialName = document.getElementById('infoMaterialName');
        const infoSupplierNumber = document.getElementById('infoSupplierNumber');
        const infoLab = document.

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
getElementById('infoLab');

        // دالة محسنة للتحقق من localStorage
        function getLocalStorage(key, defaultValue) {
            try {
                const item = localStorage.getItem(key);
                return item ? JSON.parse(item) : defaultValue;
            } catch (error) {
                console.error('خطأ في قراءة localStorage:', error);
                return defaultValue;
            }
        }

        // دالة محسنة لحفظ البيانات في localStorage
        function setLocalStorage(key, value) {
            try {
                localStorage.setItem(key, JSON.stringify(value));
                return true;
            } catch (error) {
                console.error('خطأ في حفظ localStorage:', error);
                return false;
            }
        }

        // أحداث تسجيل الدخول
        loginForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // التحقق من بيانات المستخدم
            const user = users.find(u => u.username === username && u.password === password);
            
            if (user) {
                currentUser = user;
                loginPage.style.display = 'none';
                dashboard.style.display = 'block';
                updateUserDisplay();
                updatePermissions();
                loadDashboardData();
                if (currentUser.type === 'self') {
                    loadUserMaterials();
                }
                if (currentUser.type === 'doctor') {
                    loadLabMaterials();
                    loadUnprocessedMaterials();
                }
                
                // تسجيل نشاط الدخول
                activities.push({
                    action: 'تسجيل دخول',
                    user: currentUser.name,
                    date: new Date().toLocaleDateString('ar-EG')
                });
                setLocalStorage('activities', activities);
                
                alert('تم تسجيل الدخول بنجاح!');
            } else {
                alert('بيانات الدخول غير صحيحة!');
            }
        });

        // تحديث عرض معلومات المستخدم
        function updateUserDisplay() {
            userNameDisplay.textContent = currentUser.name;
            userRoleDisplay.textContent = getRoleName(currentUser.type);
            userRoleDisplay.className = 'user-role role-' + currentUser.type;
            
            // عرض المختبر إذا كان دكتور
            if (currentUser.type === 'doctor' && currentUser.lab) {
                userLabDisplay.innerHTML = <span class="lab-badge lab-${currentUser.lab}">المختبر ${currentUser.lab}</span>;
            } else {
                userLabDisplay.innerHTML = '';
            }
        }

        // الحصول على اسم الدور
        function getRoleName(role) {
            switch(role) {
                case 'admin': return 'مدير النظام';
                case 'doctor': return 'دكتور';
                case 'self': return 'ذاتية';
                default: return 'مستخدم';
            }
        }

        // الحصول على اسم المختبر
        function getLabName(lab) {
            switch(lab) {
                case '1': return 'المختبر الأول';
                case '2': return 'المختبر الثاني';
                case '3': return 'المختبر الثالث';
                default: return 'غير محدد';
            }
        }

        // الحصول على اسم الحالة
        function getStatusName(status) {
            switch(status) {
                case 'pending': return 'قيد المراجعة';
                case 'accepted': return 'مقبولة';
                case 'rejected': return 'مرفوضة';
                default: return 'قيد المراجعة';
            }
        }

        // الحصول على كلاس الحالة
        function getStatusClass(status) {
            switch(status) {
                case 'pending': return 'status-pending';
                case 'accepted': return 'status-accepted';

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
case 'rejected': return 'status-rejected';
                default: return 'status-pending';
            }
        }

        // تحديث الصلاحيات بناءً على نوع المستخدم
        function updatePermissions() {
            // إخفاء جميع الروابط أولاً
            usersManagementLink.style.display = 'none';
            reportsLink.style.display = 'none';
            chemistrySectionLink.style.display = 'none';
            warehouseSectionLink.style.display = 'none';
            labsStats.style.display = 'none';
            
            // إظهار الروابط بناءً على الصلاحيات
            if (currentUser.type === 'admin') {
                usersManagementLink.style.display = 'block';
                reportsLink.style.display = 'block';
                labsStats.style.display = 'block';
                loadUsersTable();
                loadLabsStats();
            } else if (currentUser.type === 'doctor') {
                chemistrySectionLink.style.display = 'block';
                document.getElementById('currentLabName').textContent = getLabName(currentUser.lab);
            } else if (currentUser.type === 'self') {
                warehouseSectionLink.style.display = 'block';
            }
        }

        // تحميل المواد غير المعالجة للدكتور
        function loadUnprocessedMaterials() {
            selectedMaterial.innerHTML = '<option value="">اختر المادة</option>';
            
            // المواد التي لم يتم فحصها بعد في مختبر الدكتور الحالي
            const unprocessedMaterials = materials.filter(material => 
                material.lab === currentUser.lab && 
                !material.analysisMethod
            );
            
            unprocessedMaterials.forEach(material => {
                const option = document.createElement('option');
                option.value = material.id;
                option.textContent = ${material.name} - ${material.supplierNumber || 'بدون رقم وارد'};
                selectedMaterial.appendChild(option);
            });
        }

        // حدث عند اختيار مادة للفحص
        selectedMaterial.addEventListener('change', function() {
            const materialId = this.value;
            if (materialId) {
                const material = materials.find(m => m.id === materialId);
                if (material) {
                    infoMaterialName.textContent = material.name;
                    infoSupplierNumber.textContent = material.supplierNumber || 'غير محدد';
                    infoLab.textContent = getLabName(material.lab);
                    selectedMaterialInfo.style.display = 'block';
                }
            } else {
                selectedMaterialInfo.style.display = 'none';
            }
        });

        // تحميل إحصائيات المختبرات
        function loadLabsStats() {
            for (let i = 1; i <= 3; i++) {
                const labMaterials = materials.filter(m => m.lab === i.toString());
                const labDoctors = users.filter(u => u.type === 'doctor' && u.lab === i.toString());
                
                document.getElementById(`lab${i}Total`).textContent = labMaterials.length;
                document.getElementById(`lab${i}Expired`).textContent = labMaterials.filter(m => isExpired(m.expiryDate)).length;
                document.getElementById(`lab${i}Doctors`).textContent = labDoctors.length;
            }
        }

        // تحميل بيانات لوحة التحكم
        function loadDashboardData() {
            // تحديث الإحصائيات
            document.getElementById('totalMaterials').textContent = materials.length;
            document.getElementById('expiredMaterials').textContent = materials.filter(m => isExpired(m.expiryDate)).length;
            document.getElementById('recentMaterials').textContent = materials.filter(m => isRecent(m.addedDate)).length;
            document.getElementById('activeUsers').textContent = users.length;
            
            // تحديث جدول الأنشطة
            const activitiesTable = document.getElementById('activitiesTable');
            activitiesTable.innerHTML = '';

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
const recentActivities = activities.slice(-5).reverse();
            recentActivities.forEach(activity => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${activity.action}</td>
                    <td>${activity.user}</td>
                    <td>${activity.date}</td>
                `;
                activitiesTable.appendChild(row);
            });
        }

        // تحميل جدول المستخدمين (للمدير)
        function loadUsersTable() {
            const usersTable = document.getElementById('usersTable');
            usersTable.innerHTML = '';
            
            users.forEach(user => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${user.username}</td>
                    <td>${user.name}</td>
                    <td>${getRoleName(user.type)}</td>
                    <td>${user.lab ? getLabName(user.lab) : '-'}</td>
                    <td>نشط</td>
                    <td>
                        <button class="btn btn-danger btn-sm" onclick="deleteUser('${user.username}')">حذف</button>
                    </td>
                `;
                usersTable.appendChild(row);
            });
        }

        // تحميل المواد الخاصة بالمستخدم الحالي (ذاتية)
        function loadUserMaterials() {
            const userMaterials = materials.filter(material => material.addedBy === currentUser.username);
            userMaterialsCount.textContent = userMaterials.length;
            currentUserNameDisplay.textContent = currentUser.name;
            
            warehouseMaterialsTable.innerHTML = '';
            
            if (userMaterials.length === 0) {
                const row = document.createElement('tr');
                row.innerHTML = <td colspan="10" style="text-align: center;">لا توجد مواد مضافة</td>;
                warehouseMaterialsTable.appendChild(row);
                return;
            }
            
            userMaterials.forEach(material => {
                const row = document.createElement('tr');
                const statusClass = getMaterialStatusClass(material.expiryDate);
                const statusText = getStatusName(material.status);
                const statusStyle = getStatusClass(material.status);
                
                row.innerHTML = `
                    <td>${material.name}</td>
                    <td>${material.type === 'standard' ? 'قياسية' : 'كيميائية'}</td>
                    <td>${getLabName(material.lab)}</td>
                    <td>${material.category}</td>
                    <td>${material.quantity}</td>
                    <td>${material.receiveDate}</td>
                    <td class="${statusClass}">${material.expiryDate}</td>
                    <td>${material.supplierNumber || '-'}</td>
                    <td class="${statusStyle}">${statusText}</td>
                    <td>
                        <button class="btn btn-danger btn-sm" onclick="deleteMaterial('${material.id}')">حذف</button>
                    </td>
                `;
                warehouseMaterialsTable.appendChild(row);
            });
        }

        // تحميل مواد المختبر (للدكتور)
        function loadLabMaterials() {
            const labMaterials = materials.filter(material => material.lab === currentUser.lab);
            const labMaterialsTable = document.getElementById('labMaterialsTable');
            labMaterialsTable.innerHTML = '';
            
            if (labMaterials.length === 0) {
                const row = document.createElement('tr');
                row.innerHTML = <td colspan="6" style="text-align: center;">لا توجد مواد في هذا المختبر</td>;
                labMaterialsTable.appendChild(row);
                return;
            }
            
            labMaterials.forEach(material => {
                const row = document.createElement('tr');
                const statusText = getStatusName(material.status);
                const statusStyle = getStatusClass(material.status);

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
row.innerHTML = `
                    <td>${material.name}</td>
                    <td>${material.supplierNumber || '-'}</td>
                    <td>${material.analysisMethod || 'لم يتم الفحص'}</td>
                    <td class="${statusStyle}">${statusText}</td>
                    <td>${material.addedDate}</td>
                    <td>${material.addedBy || 'غير معروف'}</td>
                `;
                labMaterialsTable.appendChild(row);
            });
        }

        // الحصول على كلاس حالة المادة
        function getMaterialStatusClass(expiryDate) {
            if (isExpired(expiryDate)) {
                return 'expired';
            } else if (isExpiringSoon(expiryDate)) {
                return 'expiring-soon';
            }
            return '';
        }

        // التحقق من انتهاء صلاحية المادة
        function isExpired(expiryDate) {
            if (!expiryDate) return false;
            return new Date(expiryDate) < new Date();
        }

        // التحقق من قرب انتهاء صلاحية المادة (خلال 30 يوم)
        function isExpiringSoon(expiryDate) {
            if (!expiryDate) return false;
            const thirtyDaysFromNow = new Date();
            thirtyDaysFromNow.setDate(thirtyDaysFromNow.getDate() + 30);
            return new Date(expiryDate) <= thirtyDaysFromNow && new Date(expiryDate) > new Date();
        }

        // التحقق من إضافة المادة مؤخراً
        function isRecent(addedDate) {
            if (!addedDate) return false;
            const sevenDaysAgo = new Date();
            sevenDaysAgo.setDate(sevenDaysAgo.getDate() - 7);
            return new Date(addedDate) > sevenDaysAgo;
        }

        // إضافة مادة جديدة إلى المخزن (ذاتية)
        warehouseForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const material = {
                id: generateId(),
                name: document.getElementById('warehouseMaterialName').value,
                type: document.getElementById('materialType').value,
                lab: document.getElementById('materialLab').value,
                category: document.getElementById('materialCategory').value,
                quantity: document.getElementById('quantity').value,
                receiveDate: document.getElementById('receiveDate').value,
                expiryDate: document.getElementById('expiryDate').value,
                supplierNumber: document.getElementById('supplierNumber').value,
                notes: document.getElementById('notes').value,
                addedBy: currentUser.username,
                addedDate: new Date().toISOString().split('T')[0],
                status: 'pending'
            };
            
            materials.push(material);
            setLocalStorage('materials', materials);
            
            // تسجيل النشاط
            activities.push({
                action: إضافة مادة جديدة: ${material.name} للمختبر ${getLabName(material.lab)},
                user: currentUser.name,
                date: new Date().toLocaleDateString('ar-EG')
            });
            setLocalStorage('activities', activities);
            
            alert('تم إضافة المادة إلى المخزن بنجاح!');
            warehouseForm.reset();
            loadUserMaterials();
            loadDashboardData();
        });

        // إضافة مستخدم من قبل المدير
        document.getElementById('addUserForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const user = {
                username: document.getElementById('newUsername').value,
                password: document.getElementById('newPassword').value,
                name: document.getElementById('newFullName').value,
                type: document.getElementById('newUserType').value,
                lab: document.getElementById('newUserType').value === 'doctor' ? document.getElementById('userLab').value : null
            };
            
            users.push(user);
            setLocalStorage('users', users);
            
            // تسجيل النشاط

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
activities.push({
                action: إضافة مستخدم جديد: ${user.name},
                user: currentUser.name,
                date: new Date().toLocaleDateString('ar-EG')
            });
            setLocalStorage('activities', activities);
            
            alert('تم إضافة المستخدم بنجاح!');
            closeUserForm();
            loadUsersTable();
            loadDashboardData();
            loadLabsStats();
        });

        // إضافة نتيجة فحص في قسم الكيمياء (دكتور)
        document.getElementById('chemistryForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const materialId = document.getElementById('selectedMaterial').value;
            if (!materialId) {
                alert('الرجاء اختيار مادة للفحص');
                return;
            }
            
            const materialIndex = materials.findIndex(m => m.id === materialId);
            if (materialIndex === -1) {
                alert('المادة المختارة غير موجودة');
                return;
            }
            
            // تحديث بيانات المادة
            materials[materialIndex].analysisMethod = document.getElementById('analysisMethod').value;
            materials[materialIndex].status = document.getElementById('materialStatus').value;
            materials[materialIndex].examinedBy = currentUser.username;
            materials[materialIndex].examinedDate = new Date().toISOString().split('T')[0];
            
            setLocalStorage('materials', materials);
            
            // تسجيل النشاط
            activities.push({
                action: فحص مادة: ${materials[materialIndex].name} - ${materials[materialIndex].analysisMethod},
                user: currentUser.name,
                date: new Date().toLocaleDateString('ar-EG')
            });
            setLocalStorage('activities', activities);
            
            alert('تم إضافة نتيجة الفحص بنجاح!');
            document.getElementById('chemistryForm').reset();
            selectedMaterialInfo.style.display = 'none';
            loadLabMaterials();
            loadUnprocessedMaterials();
            loadDashboardData();
        });

        // حذف مادة
        function deleteMaterial(materialId) {
            if (confirm('هل أنت متأكد من حذف هذه المادة؟')) {
                materials = materials.filter(m => m.id !== materialId);
                setLocalStorage('materials', materials);
                
                // تسجيل النشاط
                activities.push({
                    action: حذف مادة,
                    user: currentUser.name,
                    date: new Date().toLocaleDateString('ar-EG')
                });
                setLocalStorage('activities', activities);
                
                if (currentUser.type === 'admin') {
                    loadLabsStats();
                } else if (currentUser.type === 'self') {
                    loadUserMaterials();
                } else if (currentUser.type === 'doctor') {
                    loadLabMaterials();
                    loadUnprocessedMaterials();
                }
                loadDashboardData();
                alert('تم حذف المادة بنجاح!');
            }
        }

        // حذف مستخدم
        function deleteUser(username) {
            if (username === currentUser.username) {
                alert('لا يمكن حذف المستخدم الحالي!');
                return;
            }
            
            if (confirm('هل أنت متأكد من حذف هذا المستخدم؟')) {
                users = users.filter(u => u.username !== username);
                setLocalStorage('users', users);
                
                // تسجيل النشاط
                activities.push({
                    action: حذف مستخدم,
                    user: currentUser.name,
                    date: new Date().toLocaleDateString('ar-EG')
                });
                setLocalStorage('activities', activities);
                
                loadUsersTable();
                loadDashboardData();
                loadLabsStats();

عِراق مُحَمد عيسى, [11/3/2025 11:47 PM]
alert('تم حذف المستخدم بنجاح!');
            }
        }

        // توليد معرف فريد
        function generateId() {
            return Date.now().toString(36) + Math.random().toString(36).substr(2);
        }

        // إظهار نموذج إضافة مستخدم
        document.getElementById('addUserBtn').addEventListener('click', function() {
            document.getElementById('userFormModal').style.display = 'block';
        });

        // إظهار/إخفاء اختيار المختبر عند تغيير نوع المستخدم
        document.getElementById('newUserType').addEventListener('change', function() {
            const labSelection = document.getElementById('labSelection');
            if (this.value === 'doctor') {
                labSelection.style.display = 'block';
            } else {
                labSelection.style.display = 'none';
            }
        });

        // إغلاق نموذج إضافة مستخدم
        function closeUserForm() {
            document.getElementById('userFormModal').style.display = 'none';
            document.getElementById('addUserForm').reset();
        }

        // التنقل بين الصفحات
        navLinks.forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                
                // إزالة النشاط من جميع الروابط
                navLinks.forEach(l => l.classList.remove('active'));
                
                // إضافة النشاط للرابط المحدد
                this.classList.add('active');
                
                // إخفاء جميع الصفحات
                pages.forEach(page => page.classList.remove('active'));
                
                // إظهار الصفحة المحددة
                const pageId = this.getAttribute('data-page');
                document.getElementById(pageId).classList.add('active');
                
                // تحميل البيانات حسب الصفحة
                if (pageId === 'warehousePage' && currentUser.type === 'self') {
                    loadUserMaterials();
                } else if (pageId === 'chemistryPage' && currentUser.type === 'doctor') {
                    loadLabMaterials();
                    loadUnprocessedMaterials();
                } else if (pageId === 'usersPage' && currentUser.type === 'admin') {
                    loadUsersTable();
                }
            });
        });

        // التنقل بين تبويبات المخزن
        tabs.forEach(tab => {
            tab.addEventListener('click', function() {
                const tabId = this.getAttribute('data-tab');
                
                // إزالة النشاط من جميع التبويبات
                tabs.forEach(t => t.classList.remove('active'));
                tabContents.forEach(tc => tc.classList.remove('active'));
                
                // إضافة النشاط للتبويب المحدد
                this.classList.add('active');
                document.getElementById(tabId).classList.add('active');
            });
        });

        // تحديث قائمة المواد
        refreshMaterialsBtn.addEventListener('click', function() {
            loadUserMaterials();
        });

        // تسجيل الخروج
        logoutBtn.addEventListener('click', function() {
            currentUser = null;
            dashboard.style.display = 'none';
            loginPage.style.display = 'flex';
            loginForm.reset();
        });

        // تهيئة التطبيق
        function initApp() {
            // تحميل البيانات من localStorage مع معالجة الأخطاء
            users = getLocalStorage('users', defaultUsers);
            materials = getLocalStorage('materials', defaultMaterials);
            activities = getLocalStorage('activities', defaultActivities);
            
            console.log('البيانات المحملة:', { users, materials, activities });
        }

        // تشغيل التطبيق
        initApp();
    </script>
</body>
</html>
