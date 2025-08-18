<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>양치 인증 앱</title>
  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #74b9ff, #0984e3);
      min-height: 100vh; display:flex; align-items:center; justify-content:center; padding:20px;
    }
    .container {
      background:#fff; border-radius:20px; box-shadow:0 20px 40px rgba(0,0,0,0.1);
      padding:30px; width:100%; max-width:420px; text-align:center;
    }
    .header { margin-bottom:30px; }
    .header h1 { color:#2d3436; font-size:28px; margin-bottom:10px; }
    .header .emoji { font-size:48px; margin-bottom:15px; display:block; }

    .form-group { margin-bottom:20px; text-align:left; }
    .form-group label { display:block; margin-bottom:8px; color:#2d3436; font-weight:600; }
    .form-group select, .form-group input {
      width:100%; padding:12px; border:2px solid #ddd; border-radius:10px; font-size:16px;
      transition:border-color .3s;
    }
    .form-group select:focus, .form-group input:focus { outline:none; border-color:#74b9ff; }

    .inline-row { display:flex; gap:10px; }
    .inline-row .form-group { flex:1; margin-bottom:0; }

    .btn {
      background:linear-gradient(135deg, #00b894, #00a085); color:#fff; border:none; padding:14px 24px;
      border-radius:25px; font-size:16px; font-weight:700; cursor:pointer; transition:all .25s;
      width:100%; margin-top:16px;
    }
    .btn:hover { transform:translateY(-2px); box-shadow:0 10px 20px rgba(0,184,148,0.3); }
    .btn:disabled { background:#ddd; cursor:not-allowed; transform:none; box-shadow:none; }
    .btn-secondary { background:#636e72; }
    .btn-pink { background:#fd79a8; }
    .btn-pink:hover { background:#e84393; }

    .camera-container { display:none; flex-direction:column; align-items:center; gap:20px; }
    .camera-placeholder {
      width:300px; height:300px; background:#f8f9fa; border:3px dashed #74b9ff;
      border-radius:15px; display:flex; align-items:center; justify-content:center;
      flex-direction:column; color:#636e72; font-size:16px; padding:16px; text-align:center;
    }

    .student-info {
      background:#f8f9fa; padding:15px; border-radius:10px; margin-bottom:10px; display:none;
      width:100%; text-align:left;
    }
    .student-info h3 { color:#2d3436; margin-bottom:5px; }
    .timestamp { color:#636e72; font-size:14px; }

    .success-message {
      display:none; background:#00b894; color:#fff; padding:16px; border-radius:12px; margin-top:10px;
      animation:fadeIn .5s ease-in;
      width:100%;
    }
    @keyframes fadeIn { from{opacity:0; transform:translateY(10px);} to{opacity:1; transform:translateY(0);} }

    .records-section { margin-top:24px; padding-top:20px; border-top:2px solid #f1f2f6; display:none; }
    .records-list {
      max-height:220px; overflow-y:auto; background:#f8f9fa; border-radius:10px; padding:10px; margin-top:10px;
    }
    .record-item {
      padding:10px; background:#fff; border-radius:8px; margin-bottom:8px; display:flex; justify-content:space-between;
      align-items:center; font-size:14px;
    }
    .badge {
      display:inline-block; padding:2px 8px; border-radius:999px; font-size:12px; font-weight:700;
      background:#ffeaa7; color:#636e72; margin-left:6px;
    }
    .badge-green { background:#55efc4; color:#006b4f; }

    .helper {
      margin-top:8px; font-size:12px; color:#2d3436; background:#eaf4ff; padding:8px 10px; border-radius:8px; text-align:left;
    }

    @media (max-width:480px){
      .container{ padding:20px; margin:10px; }
      .camera-placeholder{ width:260px; height:260px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <span class="emoji">🦷</span>
      <h1>양치 인증 앱</h1>
      <p>점심시간 양치 체크!</p>
    </div>

    <!-- 등록 폼 -->
    <div id="registration-form">
      <div class="inline-row">
        <div class="form-group">
          <label for="grade">학년 선택</label>
          <select id="grade" aria-label="학년 선택">
            <option value="">학년을 선택하세요</option>
            <option value="1">1학년</option>
            <option value="2">2학년</option>
            <option value="3">3학년</option>
            <option value="4">4학년</option>
            <option value="5">5학년</option>
            <option value="6">6학년</option>
          </select>
        </div>
        <div class="form-group">
          <label for="class">반 선택</label>
          <select id="class" aria-label="반 선택">
            <option value="">반을 선택하세요</option>
            <option value="1">1반</option>
            <option value="2">2반</option>
            <option value="3">3반</option>
            <option value="4">4반</option>
            <option value="5">5반</option>
          </select>
        </div>
      </div>

      <div class="form-group" style="margin-top:16px;">
        <label for="name">이름</label>
        <input type="text" id="name" placeholder="이름을 입력하세요" aria-label="이름 입력"/>
      </div>

      <div class="helper">
        • 등록 후 <strong>AR 필터</strong>는 새 탭으로 열립니다. 촬영 후 이 페이지로 돌아와 <em>양치 인증 완료</em>를 눌러 주세요.<br/>
        • 점심시간(기본 11:30–13:30) 외에는 경고가 표시됩니다.
      </div>

      <button class="btn" id="register-btn">등록하기</button>
    </div>

    <!-- 카메라 안내/버튼 -->
    <div class="camera-container" id="camera-section" aria-live="polite">
      <div class="student-info" id="student-info">
        <h3 id="student-display"></h3>
        <p class="timestamp" id="current-time"></p>
      </div>

      <div class="camera-placeholder">
        <div id="camera-placeholder-content">
          <div style="font-size:44px;">📸</div>
          <p style="margin-top:8px;">AR 필터 페이지는 보안 정책으로</p>
          <p>이 페이지 안에 직접 표시할 수 없어요.</p>
          <button class="btn" id="open-ar-btn" style="margin-top:12px;">AR 필터 열기</button>
          <p style="font-size:12px;margin-top:8px; line-height:1.4;">
            촬영 후 이 탭으로 돌아와 아래의 <strong>양치 인증 완료!</strong>를 눌러 기록하세요.
          </p>
        </div>
      </div>

      <button class="btn" id="complete-btn">양치 인증 완료!</button>
      <button class="btn btn-secondary" id="back-btn">돌아가기</button>

      <div class="success-message" id="success-message">
        <h3>🎉 양치 인증 완료!</h3>
        <p>건강한 치아를 위해 노력하는 당신이 멋져요!</p>
      </div>
    </div>

    <!-- 기록 섹션 -->
    <div class="records-section" id="records-section">
      <h3>오늘의 양치 기록</h3>
      <div class="records-list" id="records-list"></div>
      <button class="btn btn-pink" id="export-btn">엑셀로 내보내기</button>
    </div>
  </div>

  <script>
    // ===== 설정값(점심시간) =====
    const LUNCH_START = { hour: 11, minute: 30 };
    const LUNCH_END   = { hour: 13, minute: 30 };

    // ===== 상태 =====
    let currentStudent = null;
    let brushingRecords = JSON.parse(localStorage.getItem('brushingRecords') || '[]');

    // ===== 유틸 =====
    function isWithinLunch(now = new Date()) {
      const h = now.getHours();
      const m = now.getMinutes();
      const start = LUNCH_START.hour * 60 + LUNCH_START.minute;
      const end   = LUNCH_END.hour   * 60 + LUNCH_END.minute;
      const cur   = h * 60 + m;
      return cur >= start && cur <= end;
    }

    function saveRecords() {
      localStorage.setItem('brushingRecords', JSON.stringify(brushingRecords));
    }

    function updateCurrentTime() {
      const now = new Date();
      const timeString = now.toLocaleString('ko-KR', {
        year:'numeric', month:'2-digit', day:'2-digit', hour:'2-digit', minute:'2-digit'
      });
      const lunchFlag = isWithinLunch(now) ? '🍽️ 점심시간' : '⏰ 점심시간 외';
      document.getElementById('current-time').textContent = `${lunchFlag} - ${timeString}`;
    }

    function updateRecordsList() {
      const recordsList = document.getElementById('records-list');
      const today = new Date().toLocaleDateString('ko-KR');
      const todayRecords = brushingRecords.filter(r => r.date === today);

      if (todayRecords.length === 0) {
        recordsList.innerHTML = '<p style="text-align:center;color:#636e72;">오늘 기록이 없습니다.</p>';
        return;
      }

      recordsList.innerHTML = todayRecords.map(r => `
        <div class="record-item">
          <span>
            ${r.grade}학년 ${r.class}반 ${r.name}
            ${r.lunchWindow === 'Y'
              ? '<span class="badge badge-green">점심</span>'
              : '<span class="badge">외</span>'}
          </span>
          <span>${r.time}</span>
        </div>
      `).join('');
    }

    // ===== 동작 =====
    function registerStudent() {
      const grade = document.getElementById('grade').value.trim();
      const classNum = document.getElementById('class').value.trim();
      const name = document.getElementById('name').value.trim();

      if (!grade || !classNum || !name) {
        alert('모든 정보를 입력해주세요!');
        return;
      }

      currentStudent = { grade, class: classNum, name };

      // 폼 숨기고 카메라 섹션 표시
      document.getElementById('registration-form').style.display = 'none';
      document.getElementById('camera-section').style.display = 'flex';
      document.getElementById('student-info').style.display = 'block';

      // 학생 정보/시간 표시
      document.getElementById('student-display').textContent =
        `${currentStudent.grade}학년 ${currentStudent.class}반 ${currentStudent.name}`;
      updateCurrentTime();
    }

    function openAR() {
      // 같은 탭 이동을 원하면 window.location.href 사용
      window.open(
        'https://www.apoc.day/content/95db481c-d487-46b4-b0f1-a1aa6b484eb7',
        '_blank',
        'noopener'
      );
    }

    function takePhoto() {
      const now = new Date();
      if (!isWithinLunch(now)) {
        const proceed = confirm('지금은 점심시간이 아닙니다. 그래도 인증을 기록할까요?');
        if (!proceed) return;
      }

      const record = {
        ...currentStudent,
        timestamp: now.toISOString(),
        date: now.toLocaleDateString('ko-KR'),
        time: now.toLocaleTimeString('ko-KR'),
        lunchWindow: isWithinLunch(now) ? 'Y' : 'N'
      };

      brushingRecords.push(record);
      saveRecords();

      document.getElementById('success-message').style.display = 'block';
      document.getElementById('records-section').style.display = 'block';
      updateRecordsList();

      setTimeout(() => { goBack(); }, 3000);
    }

    function goBack() {
      // 카메라 섹션 숨기고 성공 메시지 숨김
      document.getElementById('camera-section').style.display = 'none';
      document.getElementById('success-message').style.display = 'none';

      // 폼 다시 표시 + 초기화
      document.getElementById('registration-form').style.display = 'block';
      document.getElementById('grade').value = '';
      document.getElementById('class').value = '';
      document.getElementById('name').value = '';

      currentStudent = null;
    }

    function exportToExcel() {
      if (brushingRecords.length === 0) {
        alert('내보낼 기록이 없습니다.');
        return;
      }
      let csvContent = "날짜,시간,학년,반,이름,점심시간여부\n";
      brushingRecords.forEach(r => {
        csvContent += `${r.date},${r.time},${r.grade}학년,${r.class}반,${r.name},${r.lunchWindow || ''}\n`;
      });

      const blob = new Blob(["\uFEFF" + csvContent], { type:'text/csv;charset=utf-8;' });
      const link = document.createElement('a');
      link.href = URL.createObjectURL(blob);
      // YYYY-MM-DD 형식 파일명
      link.download = `양치기록_${new Date().toISOString().slice(0,10)}.csv`;
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }

    // ===== 이벤트 바인딩 =====
    document.getElementById('register-btn').addEventListener('click', registerStudent);
    document.getElementById('open-ar-btn').addEventListener('click', openAR);
    document.getElementById('complete-btn').addEventListener('click', takePhoto);
    document.getElementById('back-btn').addEventListener('click', goBack);
    document.getElementById('export-btn').addEventListener('click', exportToExcel);

    // ===== 초기 로드 =====
    window.addEventListener('load', () => {
      if (brushingRecords.length > 0) {
        document.getElementById('records-section').style.display = 'block';
        updateRecordsList();
      }
    });
  </script>
</body>
</html>
