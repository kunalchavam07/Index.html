<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>New IT Computer Arag – Result Portal</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Segoe UI',Arial,sans-serif;background:#f0f4f8;min-height:100vh}
.page{display:none;min-height:100vh}
.page.active{display:block}
.center{display:flex;align-items:center;justify-content:center;min-height:100vh;padding:1.5rem}
.topbar{background:#1a56db;color:#fff;padding:14px 20px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:10px}
.topbar-title{font-size:17px;font-weight:700}
.topbar-sub{font-size:12px;opacity:.85;margin-top:2px}
.card{background:#fff;border-radius:16px;box-shadow:0 2px 20px rgba(0,0,0,0.10);padding:2rem;width:100%;max-width:440px}
.field-label{font-size:13px;color:#555;font-weight:600;margin-bottom:5px;margin-top:14px;display:block}
input[type=text],input[type=password],input[type=number],select{width:100%;padding:10px 13px;font-size:14px;border:1.5px solid #dde1e7;border-radius:10px;background:#fafbfc;color:#1a1a1a;outline:none;transition:border .2s}
input[type=text]:focus,input[type=password]:focus,input[type=number]:focus,select:focus{border-color:#1a56db;background:#fff;box-shadow:0 0 0 3px rgba(26,86,219,.1)}
.btn-primary{width:100%;margin-top:18px;padding:12px;font-size:15px;font-weight:700;border-radius:10px;cursor:pointer;background:#1a56db;color:#fff;border:none;transition:background .2s}
.btn-primary:hover{background:#1447b7}
.btn-outline{padding:9px 18px;font-size:13px;font-weight:600;border-radius:9px;cursor:pointer;background:#fff;color:#1a56db;border:1.5px solid #1a56db;transition:all .2s}
.btn-outline:hover{background:#1a56db;color:#fff}
.btn-sm{padding:6px 14px;font-size:12px;font-weight:600;border-radius:8px;cursor:pointer;border:none;transition:all .2s}
.btn-edit{background:#e8f0fe;color:#1a56db}
.btn-edit:hover{background:#d2e3fc}
.btn-del{background:#fdecea;color:#c0392b}
.btn-del:hover{background:#fcd0cc}
.err{color:#c0392b;font-size:13px;margin-top:8px;background:#fdecea;border:1px solid #f5c2c2;border-radius:8px;padding:8px 12px;display:none}
.login-header{text-align:center;margin-bottom:1.5rem}
.login-icon{width:60px;height:60px;border-radius:50%;background:#e8f0fe;display:flex;align-items:center;justify-content:center;margin:0 auto 10px;font-size:28px}
.login-title{font-size:19px;font-weight:700;color:#1a1a1a}
.login-sub{font-size:13px;color:#666;margin-top:4px}
.admin-link{text-align:center;margin-top:14px}
.admin-link button{background:none;border:none;color:#888;font-size:12px;cursor:pointer;text-decoration:underline}
.admin-link button:hover{color:#1a56db}
.admin-wrap{max-width:900px;margin:0 auto;padding:1.5rem}
.section-card{background:#fff;border-radius:14px;box-shadow:0 2px 12px rgba(0,0,0,0.08);padding:1.5rem;margin-bottom:1.5rem}
.section-title{font-size:15px;font-weight:700;color:#1a1a1a;margin-bottom:1rem;display:flex;align-items:center;gap:8px}
.stat-row{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:1.25rem}
.stat-box{background:#f0f4f8;border-radius:10px;padding:12px;text-align:center}
.stat-box .sv{font-size:22px;font-weight:700;color:#1a56db}
.stat-box .sl{font-size:12px;color:#666;margin-top:2px}
.tab-row{display:flex;gap:4px;margin-bottom:1.25rem;background:#f0f4f8;border-radius:10px;padding:4px;flex-wrap:wrap}
.tab{padding:7px 10px;font-size:12px;font-weight:600;border:none;background:none;border-radius:8px;cursor:pointer;color:#666;transition:all .2s;white-space:nowrap}
.tab.active{background:#fff;color:#1a56db;box-shadow:0 1px 4px rgba(0,0,0,0.10)}
.students-table{width:100%;border-collapse:collapse;font-size:13px}
.students-table th{text-align:left;padding:9px 12px;background:#f0f4f8;color:#555;font-weight:700;font-size:12px;border-bottom:1.5px solid #e2e8f0}
.students-table td{padding:10px 12px;border-bottom:1px solid #f0f0f0;color:#333;vertical-align:middle}
.students-table tr:last-child td{border-bottom:none}
.students-table tr:hover td{background:#f8faff}
.course-tag{display:inline-block;padding:3px 10px;border-radius:20px;font-size:11px;font-weight:700}
.t-ms{background:#e8f0fe;color:#1447b7}
.t-tally{background:#e1f5ee;color:#0f6e56}
.t-prog{background:#eeedfe;color:#3c3489}
.t-ccc{background:#faeeda;color:#633806}
.t-dtp{background:#fbeaf0;color:#72243e}
.badge-pass{display:inline-block;padding:2px 9px;border-radius:20px;font-size:11px;font-weight:700;background:#d4edda;color:#1e7e34}
.badge-fail{display:inline-block;padding:2px 9px;border-radius:20px;font-size:11px;font-weight:700;background:#fdecea;color:#c0392b}
.no-data{text-align:center;padding:2rem;color:#aaa;font-size:14px}
.search-bar{display:flex;gap:10px;margin-bottom:1rem;align-items:center}
.search-bar input{flex:1}

/* ── COURSE PICKER ── */
.course-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:10px;margin-top:6px}
.course-card{border:2px solid #dde1e7;border-radius:12px;padding:14px 10px;cursor:pointer;text-align:center;transition:all .2s;background:#fafbfc;user-select:none}
.course-card:hover{border-color:#1a56db;background:#eef3fd}
.course-card.selected{border-color:#1a56db;background:#1a56db;color:#fff}
.course-card .c-icon{font-size:24px;margin-bottom:6px}
.course-card .c-name{font-size:12px;font-weight:700;line-height:1.3}

/* ── MARKS SIMPLE ── */
.marks-simple{background:#f0f4f8;border-radius:12px;padding:1rem;margin-top:1rem}
.marks-simple .ms-title{font-size:13px;font-weight:700;color:#1a56db;margin-bottom:10px}
.marks-row{display:grid;grid-template-columns:1fr 1fr;gap:10px}

/* ── MODAL ── */
.modal-bg{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,.45);z-index:500;display:none;align-items:flex-start;justify-content:center;padding:1.5rem;overflow-y:auto}
.modal-bg.open{display:flex}
.modal{background:#fff;border-radius:16px;padding:1.75rem;width:100%;max-width:480px;margin:auto}
.modal-title{font-size:17px;font-weight:700;margin-bottom:1.25rem;color:#1a1a1a}
.modal-footer{display:flex;gap:10px;justify-content:flex-end;margin-top:1.25rem}
.two-col{display:grid;grid-template-columns:1fr 1fr;gap:10px}

/* ── RESULT PAGE ── */
.result-wrap{max-width:540px;margin:0 auto;padding:1.5rem 1rem}
.congrats-banner{background:linear-gradient(135deg,#1a56db 0%,#7c3aed 100%);border-radius:16px;padding:2rem;text-align:center;color:#fff;margin-bottom:1.25rem}
.congrats-banner h1{font-size:22px;font-weight:700;margin-bottom:6px}
.congrats-banner p{font-size:14px;opacity:.92}
.star-row{font-size:30px;letter-spacing:4px;margin-bottom:10px}
.res-card{background:#fff;border-radius:14px;box-shadow:0 2px 12px rgba(0,0,0,0.07);padding:1.25rem 1.5rem;margin-bottom:1rem}
.res-card h3{font-size:11px;font-weight:700;color:#999;margin-bottom:12px;text-transform:uppercase;letter-spacing:.7px}
.res-row{display:flex;justify-content:space-between;align-items:center;padding:9px 0;border-bottom:1px solid #f0f0f0}
.res-row:last-child{border-bottom:none}
.res-row span:first-child{font-size:14px;color:#666}
.res-row span:last-child{font-size:14px;font-weight:700;color:#1a1a1a}
.grade-big{text-align:center;padding:12px 0}
.grade-letter{font-size:68px;font-weight:800;line-height:1}
.grade-pct{font-size:22px;color:#555;margin-top:4px;font-weight:600}
.grade-lbl{font-size:13px;color:#999;margin-top:3px}
.badge-row{display:flex;gap:8px;flex-wrap:wrap;justify-content:center;margin-top:10px}
.res-badge{font-size:12px;padding:4px 14px;border-radius:20px;font-weight:700;background:rgba(255,255,255,.25);color:#fff}
.logout-btn{width:100%;padding:11px;font-size:14px;border-radius:10px;cursor:pointer;background:#fff;color:#555;border:1.5px solid #dde1e7;margin-top:1rem;font-weight:600}
.logout-btn:hover{background:#f5f5f5}
#confetti-canvas{position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:9999}

@media(max-width:600px){
  .stat-row{grid-template-columns:1fr 1fr}
  .two-col{grid-template-columns:1fr}
  .students-table td:nth-child(4),.students-table th:nth-child(4){display:none}
}
</style>
</head>
<body>
<canvas id="confetti-canvas"></canvas>

<!-- ══════════════ LOGIN PAGE ══════════════ -->
<div id="page-login" class="page active">
  <div class="center">
    <div class="card">
      <div class="login-header">
        <div class="login-icon">🎓</div>
        <div class="login-title">New IT Computer Arag</div>
        <div class="login-sub">Student Examination Result Portal</div>
      </div>
      <label class="field-label" for="l-uid">Student ID</label>
      <input type="text" id="l-uid" placeholder="Enter your Student ID" autocomplete="off">
      <label class="field-label" for="l-pwd">Password</label>
      <input type="password" id="l-pwd" placeholder="Enter your Password">
      <div class="err" id="l-err">⚠ Invalid Student ID or Password. Please try again.</div>
      <button class="btn-primary" onclick="studentLogin()">📄 View My Result</button>
      <div class="admin-link">
        <button onclick="openAdminLogin()">🔒 Admin Login</button>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════ ADMIN LOGIN MODAL ══════════════ -->
<div class="modal-bg" id="modal-admin-login">
  <div class="modal" style="max-width:360px">
    <div class="modal-title">🔐 Admin Login</div>
    <label class="field-label">Admin Password</label>
    <input type="password" id="admin-pwd-input" placeholder="Enter admin password">
    <div class="err" id="admin-err">Wrong password. Please try again.</div>
    <div class="modal-footer">
      <button class="btn-outline" onclick="closeModal('modal-admin-login')">Cancel</button>
      <button class="btn-primary" style="width:auto;margin-top:0;padding:10px 22px" onclick="adminLogin()">Login</button>
    </div>
  </div>
</div>

<!-- ══════════════ ADD / EDIT STUDENT MODAL ══════════════ -->
<div class="modal-bg" id="modal-student">
  <div class="modal">
    <div class="modal-title" id="modal-student-title">➕ Add New Student</div>

    <div class="two-col">
      <div>
        <label class="field-label">Student Full Name</label>
        <input type="text" id="s-name" placeholder="e.g. Rahul Sharma">
      </div>
      <div>
        <label class="field-label">Student ID</label>
        <input type="text" id="s-id" placeholder="e.g. STU001">
      </div>
    </div>
    <div class="two-col">
      <div>
        <label class="field-label">Password</label>
        <input type="text" id="s-pass" placeholder="e.g. pass123">
      </div>
      <div>
        <label class="field-label">Exam Year</label>
        <input type="text" id="s-year" placeholder="e.g. 2024-25">
      </div>
    </div>

    <label class="field-label" style="margin-top:18px">Select Course <span style="color:#c0392b">*</span></label>
    <div class="course-grid" id="course-grid"></div>
    <input type="hidden" id="s-course-key">

    <!-- SIMPLE MARKS (shown after course selected) -->
    <div id="marks-box" style="display:none">
      <div class="marks-simple">
        <div class="ms-title" id="marks-course-label">📝 Microsoft Office — Enter Marks</div>
        <div class="marks-row">
          <div>
            <label class="field-label" style="margin-top:0">Marks Obtained</label>
            <input type="number" id="s-obtained" placeholder="e.g. 420" min="0">
          </div>
          <div>
            <label class="field-label" style="margin-top:0">Total Marks</label>
            <input type="number" id="s-total" placeholder="e.g. 500" min="1">
          </div>
        </div>
      </div>
    </div>

    <div class="err" id="s-err">Please fill all fields and select a course.</div>
    <div class="modal-footer">
      <button class="btn-outline" onclick="closeModal('modal-student')">Cancel</button>
      <button class="btn-primary" style="width:auto;margin-top:0;padding:10px 26px" onclick="saveStudent()">💾 Save Student</button>
    </div>
  </div>
</div>

<!-- ══════════════ ADMIN PANEL PAGE ══════════════ -->
<div id="page-admin" class="page">
  <div class="topbar">
    <div>
      <div class="topbar-title">🎓 New IT Computer Arag</div>
      <div class="topbar-sub">Admin Panel — Manage Students &amp; Results</div>
    </div>
    <div style="display:flex;gap:8px;align-items:center;flex-wrap:wrap">
      <button class="btn-outline" style="font-size:12px;padding:7px 14px" onclick="downloadSite()">⬇ Download Website</button>
      <button class="btn-outline" style="font-size:12px;padding:7px 14px;color:#c0392b;border-color:#e57373" onclick="adminLogout()">Logout</button>
    </div>
  </div>
  <div class="admin-wrap">
    <div class="stat-row" id="stat-row"></div>
    <div class="section-card">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1rem;flex-wrap:wrap;gap:10px">
        <div class="section-title" style="margin:0">👥 Students</div>
        <button class="btn-outline" onclick="openAddStudent()">➕ Add Student</button>
      </div>
      <div class="tab-row" id="course-tabs"></div>
      <div class="search-bar">
        <input type="text" id="search-input" placeholder="🔍 Search by name or ID…" oninput="renderTable()">
      </div>
      <div style="overflow-x:auto">
        <table class="students-table">
          <thead>
            <tr>
              <th>ID</th><th>Name</th><th>Course</th>
              <th>Obtained</th><th>Total</th><th>%</th>
              <th>Status</th><th>Actions</th>
            </tr>
          </thead>
          <tbody id="students-tbody"></tbody>
        </table>
        <div class="no-data" id="no-data" style="display:none">No students yet. Click "Add Student" to begin.</div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════ RESULT PAGE ══════════════ -->
<div id="page-result" class="page">
  <div class="topbar">
    <div>
      <div class="topbar-title">🎓 New IT Computer Arag</div>
      <div class="topbar-sub">Student Examination Result</div>
    </div>
    <button class="btn-outline" style="font-size:12px;padding:7px 14px;color:#fff;border-color:rgba(255,255,255,.5)" onclick="studentLogout()">Logout</button>
  </div>
  <div class="result-wrap">
    <div class="congrats-banner">
      <div class="star-row" id="r-stars"></div>
      <h1 id="r-title">Result Declared</h1>
      <p id="r-msg"></p>
      <div class="badge-row" id="r-badges"></div>
    </div>
    <div class="res-card">
      <h3>Student Information</h3>
      <div class="res-row"><span>Student Name</span><span id="r-name">-</span></div>
      <div class="res-row"><span>Student ID</span><span id="r-id">-</span></div>
      <div class="res-row"><span>Course</span><span id="r-course">-</span></div>
      <div class="res-row"><span>Exam Year</span><span id="r-year">-</span></div>
    </div>
    <div class="res-card">
      <h3>Overall Result</h3>
      <div class="grade-big">
        <div class="grade-letter" id="r-grade">A</div>
        <div class="grade-pct" id="r-pct">85%</div>
        <div class="grade-lbl">Percentage</div>
      </div>
      <div class="res-row"><span>Marks Obtained</span><span id="r-obtained">-</span></div>
      <div class="res-row"><span>Total Marks</span><span id="r-total">-</span></div>
      <div class="res-row"><span>Pass / Fail</span><span id="r-status">-</span></div>
    </div>
    <button class="logout-btn" onclick="studentLogout()">🚪 Logout</button>
  </div>
</div>

<script>
const ADMIN_PASS = "New2100";

const COURSES = {
  ms:    { name:"Microsoft Office", icon:"💻" },
  tally: { name:"Tally Prime",      icon:"📊" },
  prog:  { name:"Programming",      icon:"💾" },
  ccc:   { name:"CCC Course",       icon:"🖥️" },
  dtp:   { name:"DTP & Design",     icon:"🎨" }
};

const COURSE_TAG = { ms:"t-ms", tally:"t-tally", prog:"t-prog", ccc:"t-ccc", dtp:"t-dtp" };

let students  = JSON.parse(localStorage.getItem("nica_v2")||"[]");
let editIndex = -1;
let activeTab = "all";

function save(){ localStorage.setItem("nica_v2", JSON.stringify(students)); }

/* ── page switching ── */
function showPage(id){
  document.querySelectorAll(".page").forEach(p=>p.classList.remove("active"));
  document.getElementById(id).classList.add("active");
  window.scrollTo(0,0);
}

/* ── modal helpers ── */
function closeModal(id){ document.getElementById(id).classList.remove("open"); }
function openModal(id) { document.getElementById(id).classList.add("open"); }

/* ── admin login ── */
function openAdminLogin(){
  document.getElementById("admin-pwd-input").value="";
  document.getElementById("admin-err").style.display="none";
  openModal("modal-admin-login");
}
function adminLogin(){
  if(document.getElementById("admin-pwd-input").value===ADMIN_PASS){
    closeModal("modal-admin-login"); showPage("page-admin"); renderAdmin();
  } else {
    document.getElementById("admin-err").style.display="block";
  }
}
document.getElementById("admin-pwd-input").addEventListener("keydown",e=>{ if(e.key==="Enter") adminLogin(); });
function adminLogout(){ showPage("page-login"); }

/* ── student login ── */
function studentLogin(){
  const uid = document.getElementById("l-uid").value.trim().toUpperCase();
  const pwd = document.getElementById("l-pwd").value.trim();
  const s   = students.find(x=>x.id.toUpperCase()===uid && x.password===pwd);
  if(!s){ document.getElementById("l-err").style.display="block"; return; }
  document.getElementById("l-err").style.display="none";
  showResult(s);
}
document.getElementById("l-pwd").addEventListener("keydown",e=>{ if(e.key==="Enter") studentLogin(); });
function studentLogout(){ stopConfetti(); showPage("page-login"); document.getElementById("l-uid").value=""; document.getElementById("l-pwd").value=""; }

/* ── course grid ── */
function buildCourseGrid(){
  const g = document.getElementById("course-grid");
  g.innerHTML="";
  Object.entries(COURSES).forEach(([key,c])=>{
    const d = document.createElement("div");
    d.className="course-card"; d.dataset.key=key;
    d.innerHTML=`<div class="c-icon">${c.icon}</div><div class="c-name">${c.name}</div>`;
    d.onclick=()=>selectCourse(key);
    g.appendChild(d);
  });
}

function selectCourse(key){
  document.querySelectorAll(".course-card").forEach(c=>c.classList.remove("selected"));
  const card = document.querySelector(`.course-card[data-key="${key}"]`);
  if(card) card.classList.add("selected");
  document.getElementById("s-course-key").value = key;
  const c = COURSES[key];
  document.getElementById("marks-course-label").textContent = c.icon+" "+c.name+" — Enter Marks";
  document.getElementById("marks-box").style.display="block";
}

/* ── add / edit student ── */
function openAddStudent(){
  editIndex=-1;
  document.getElementById("modal-student-title").textContent="➕ Add New Student";
  ["s-name","s-id","s-pass","s-obtained"].forEach(id=>document.getElementById(id).value="");
  document.getElementById("s-year").value="2024-25";
  document.getElementById("s-total").value="500";
  document.getElementById("s-course-key").value="";
  document.getElementById("marks-box").style.display="none";
  document.getElementById("s-err").style.display="none";
  buildCourseGrid();
  openModal("modal-student");
}

function openEditStudent(idx){
  editIndex=idx;
  const s=students[idx];
  document.getElementById("modal-student-title").textContent="✏️ Edit Student";
  document.getElementById("s-name").value=s.name;
  document.getElementById("s-id").value=s.id;
  document.getElementById("s-pass").value=s.password;
  document.getElementById("s-year").value=s.year;
  document.getElementById("s-obtained").value=s.obtained;
  document.getElementById("s-total").value=s.total;
  document.getElementById("s-err").style.display="none";
  buildCourseGrid();
  selectCourse(s.courseKey);
  openModal("modal-student");
}

function saveStudent(){
  const name    = document.getElementById("s-name").value.trim();
  const id      = document.getElementById("s-id").value.trim().toUpperCase();
  const pass    = document.getElementById("s-pass").value.trim();
  const year    = document.getElementById("s-year").value.trim();
  const ck      = document.getElementById("s-course-key").value;
  const obtained= parseInt(document.getElementById("s-obtained").value);
  const total   = parseInt(document.getElementById("s-total").value);
  const errEl   = document.getElementById("s-err");

  if(!name||!id||!pass||!year||!ck||isNaN(obtained)||isNaN(total)||total<1){
    errEl.textContent="Please fill all fields, select a course, and enter valid marks.";
    errEl.style.display="block"; return;
  }
  if(obtained>total){
    errEl.textContent="Marks obtained cannot be more than total marks.";
    errEl.style.display="block"; return;
  }
  if(editIndex===-1 && students.find(s=>s.id===id)){
    errEl.textContent="Student ID already exists. Use a different ID.";
    errEl.style.display="block"; return;
  }

  const obj={ id, name, password:pass, year, courseKey:ck, courseName:COURSES[ck].name, obtained, total };
  if(editIndex===-1) students.push(obj); else students[editIndex]=obj;
  save(); closeModal("modal-student"); renderAdmin();
}

function deleteStudent(idx){
  if(confirm("Delete this student? This cannot be undone.")){ students.splice(idx,1); save(); renderAdmin(); }
}

/* ── admin render ── */
function renderAdmin(){
  const tot   = students.length;
  const passed= students.filter(s=>Math.round(s.obtained/s.total*100)>=45).length;
  const dist  = students.filter(s=>Math.round(s.obtained/s.total*100)>=75).length;
  const avg   = tot ? Math.round(students.reduce((a,s)=>a+s.obtained/s.total*100,0)/tot) : 0;
  document.getElementById("stat-row").innerHTML=`
    <div class="stat-box"><div class="sv">${tot}</div><div class="sl">Total Students</div></div>
    <div class="stat-box"><div class="sv" style="color:#1e7e34">${passed}</div><div class="sl">Passed</div></div>
    <div class="stat-box"><div class="sv" style="color:#1a56db">${dist}</div><div class="sl">Distinction</div></div>
    <div class="stat-box"><div class="sv" style="color:#856404">${avg}%</div><div class="sl">Avg Score</div></div>`;

  const counts={};
  students.forEach(s=>{ counts[s.courseKey]=(counts[s.courseKey]||0)+1; });
  let tabs=`<button class="tab ${activeTab==='all'?'active':''}" onclick="setTab('all')">All (${tot})</button>`;
  Object.entries(COURSES).forEach(([key,c])=>{
    const n=counts[key]||0;
    tabs+=`<button class="tab ${activeTab===key?'active':''}" onclick="setTab('${key}')">${c.icon} ${c.name} (${n})</button>`;
  });
  document.getElementById("course-tabs").innerHTML=tabs;
  renderTable();
}

function setTab(t){ activeTab=t; renderAdmin(); }

function renderTable(){
  const q=(document.getElementById("search-input").value||"").toLowerCase();
  const list=students.filter(s=>{
    const matchTab=activeTab==="all"||s.courseKey===activeTab;
    const matchQ=!q||s.name.toLowerCase().includes(q)||s.id.toLowerCase().includes(q);
    return matchTab&&matchQ;
  });
  const tbody=document.getElementById("students-tbody");
  const nd=document.getElementById("no-data");
  if(!list.length){ tbody.innerHTML=""; nd.style.display="block"; return; }
  nd.style.display="none";
  tbody.innerHTML=list.map(s=>{
    const ri=students.indexOf(s);
    const pct=Math.round(s.obtained/s.total*100);
    const pass=pct>=45;
    return `<tr>
      <td><b>${s.id}</b></td>
      <td>${s.name}</td>
      <td><span class="course-tag ${COURSE_TAG[s.courseKey]||''}">${s.courseName}</span></td>
      <td>${s.obtained}</td>
      <td>${s.total}</td>
      <td><b>${pct}%</b></td>
      <td>${pass?'<span class="badge-pass">✅ PASS</span>':'<span class="badge-fail">❌ FAIL</span>'}</td>
      <td style="display:flex;gap:6px">
        <button class="btn-sm btn-edit" onclick="openEditStudent(${ri})">✏️ Edit</button>
        <button class="btn-sm btn-del"  onclick="deleteStudent(${ri})">🗑 Del</button>
      </td>
    </tr>`;
  }).join("");
}

/* ── show result ── */
function getGrade(pct){
  if(pct>=90) return{l:"A+",c:"#7c3aed"};
  if(pct>=75) return{l:"A", c:"#1a56db"};
  if(pct>=60) return{l:"B", c:"#1d9e75"};
  if(pct>=45) return{l:"C", c:"#ba7517"};
  return{l:"F",c:"#e24b4a"};
}

function showResult(s){
  const pct =Math.round(s.obtained/s.total*100);
  const g   =getGrade(pct);
  const pass=pct>=45;

  document.getElementById("r-name").textContent   =s.name;
  document.getElementById("r-id").textContent     =s.id;
  document.getElementById("r-course").textContent =s.courseName;
  document.getElementById("r-year").textContent   =s.year;
  document.getElementById("r-grade").textContent  =g.l;
  document.getElementById("r-grade").style.color  =g.c;
  document.getElementById("r-pct").textContent    =pct+"%";
  document.getElementById("r-obtained").textContent=s.obtained+" marks";
  document.getElementById("r-total").textContent  =s.total+" marks";
  document.getElementById("r-status").innerHTML   =pass
    ?"<span style='color:#1e7e34;font-weight:700'>✅ PASS</span>"
    :"<span style='color:#c0392b;font-weight:700'>❌ FAIL</span>";

  let stars="",title="Result Declared",msg="You have completed your examination.",badges=[];
  if(pct>=90){stars="🌟🌟🌟";title="Outstanding Performance!";msg="You scored in the top grade. Keep shining!";badges=["Top Scorer","Distinction","Excellence Award"];}
  else if(pct>=75){stars="⭐⭐⭐";title="Congratulations!";msg="Excellent result! You performed very well.";badges=["First Class","Merit"];}
  else if(pct>=60){stars="⭐⭐";title="Well Done!";msg="Good performance. Keep working hard!";badges=["Second Class"];}
  else if(pass){stars="⭐";title="You Passed!";msg="Congratulations on passing your examination.";badges=["Pass"];}
  else{stars="";title="Result Declared";msg="You did not clear this exam. Don't give up — try again!";}

  document.getElementById("r-stars").textContent=stars;
  document.getElementById("r-title").textContent=title;
  document.getElementById("r-msg").textContent=msg;
  document.getElementById("r-badges").innerHTML=badges.map(b=>`<span class="res-badge">${b}</span>`).join("");

  showPage("page-result");
  if(pass) launchConfetti();
}

/* ── download site with students baked in ── */
function downloadSite(){
  const orig=document.documentElement.outerHTML;
  const updated=orig.replace(
    /let students\s*=\s*JSON\.parse\(localStorage\.getItem\("nica_v2"\)\|\|"\[\]"\);/,
    `let students = ${JSON.stringify(students,null,2)};`
  );
  const blob=new Blob([updated],{type:"text/html"});
  const a=document.createElement("a");
  a.href=URL.createObjectURL(blob);
  a.download="new-it-computer-arag.html";
  a.click();
}

/* ── confetti ── */
let confettiAnim=null;
function launchConfetti(){
  const canvas=document.getElementById("confetti-canvas");
  const ctx=canvas.getContext("2d");
  canvas.width=window.innerWidth; canvas.height=window.innerHeight;
  const colors=["#1a56db","#7c3aed","#d4537e","#1d9e75","#f59e0b","#e24b4a","#f0c040"];
  const pieces=Array.from({length:160},()=>({
    x:Math.random()*canvas.width,
    y:Math.random()*canvas.height-canvas.height,
    r:Math.random()*9+4,
    color:colors[Math.floor(Math.random()*colors.length)],
    speed:Math.random()*3+2,
    angle:Math.random()*360,
    spin:Math.random()*7-3.5,
    drift:Math.random()*2-1
  }));
  const start=Date.now();
  function draw(){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    if(Date.now()-start>7000){stopConfetti();return;}
    pieces.forEach(p=>{
      p.y+=p.speed; p.x+=p.drift; p.angle+=p.spin;
      if(p.y>canvas.height){p.y=-10;p.x=Math.random()*canvas.width;}
      ctx.save();ctx.translate(p.x,p.y);ctx.rotate(p.angle*Math.PI/180);
      ctx.fillStyle=p.color;ctx.fillRect(-p.r/2,-p.r/2,p.r,p.r);
      ctx.restore();
    });
    confettiAnim=requestAnimationFrame(draw);
  }
  draw();
}
function stopConfetti(){
  if(confettiAnim)cancelAnimationFrame(confettiAnim);
  const c=document.getElementById("confetti-canvas");
  if(c)c.getContext("2d").clearRect(0,0,c.width,c.height);
}
</script>
</body>
</html>
