<style>
/* ═══════════════════════════════════════════
   Minecraft Window Panel System
   각 섹션 = 독립된 MC GUI 창
═══════════════════════════════════════════ */

.mc-win {
  background: rgba(12,10,8,0.82);
  border: 2px solid #505050;
  box-shadow:
    inset 2px 2px 0 #707070,
    inset -2px -2px 0 #1c1c1c,
    0 8px 24px rgba(0,0,0,0.6);
  margin: 3rem 0;
}

.mc-win-bar {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 7px 14px;
  background: rgba(65,65,65,0.98);
  border-bottom: 2px solid #252525;
  box-shadow: 0 2px 0 #707070;
}
.mc-win-bar.red    { background: rgba(75,14,14,0.98); border-bottom-color:#400606; }
.mc-win-bar.blue   { background: rgba(10,36,85,0.98); border-bottom-color:#051848; }
.mc-win-bar.green  { background: rgba(10,65,20,0.98); border-bottom-color:#053210; }
.mc-win-bar.gold   { background: rgba(85,62,6,0.98);  border-bottom-color:#4a3402; }
.mc-win-bar.teal   { background: rgba(6,58,70,0.98);  border-bottom-color:#022e38; }
.mc-win-bar.purple { background: rgba(50,14,85,0.98); border-bottom-color:#280640; }

.mc-win-icon { font-size: 1rem; line-height: 1; }

.mc-win-title {
  color: #fff;
  font-family: 'Courier New', monospace;
  font-size: 0.76rem;
  font-weight: bold;
  letter-spacing: 2px;
  text-transform: uppercase;
  text-shadow: 2px 2px 0 rgba(0,0,0,0.95);
}

.mc-win-body {
  padding: 1.6rem 1.8rem;
}

/* ── 주제 한줄요약 ── */
.mc-summary {
  color: #f0f0e0;
  font-size: 1.08rem;
  line-height: 1.75;
  margin: 0;
  text-shadow: 1px 1px 0 rgba(0,0,0,0.7);
  border-left: 4px solid #f97316;
  padding-left: 1rem;
}

/* ── 문제 / 사용자 텍스트 ── */
.mc-text {
  color: rgba(238,235,220,0.90);
  font-size: 0.93rem;
  line-height: 1.70;
  margin: 0;
}

/* ── 핵심 기능 — 아이템 슬롯 그리드 ── */
.mc-slots {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(195px,1fr));
  gap: 10px;
}
.mc-slot {
  background: rgba(0,0,0,0.50);
  border: 2px solid #3c3c3c;
  box-shadow: inset 1px 1px 0 #5c5c5c, inset -1px -1px 0 #161616;
  padding: 1rem;
  display: flex;
  gap: 0.75rem;
  align-items: flex-start;
}
.mc-slot-num {
  color: #f0c040;
  font-family: 'Courier New', monospace;
  font-weight: bold;
  font-size: 1.15rem;
  flex-shrink: 0;
  min-width: 1.3rem;
  text-shadow: 2px 2px 0 rgba(0,0,0,0.8);
}
.mc-slot-text {
  color: rgba(235,232,218,0.88);
  font-size: 0.86rem;
  line-height: 1.55;
}
.mc-slot-text strong { color: #fff; font-weight: bold; }

/* ── 동작 흐름 — Advancements ── */
.mc-adv-wrap {
  background: #1a1610;
  border: 3px solid #5e4e14;
  box-shadow: inset 0 0 40px rgba(0,0,0,0.75);
  padding: 1rem 1.4rem 1.5rem;
  overflow-x: auto;
}
.mc-adv-header {
  color: #e8e4d0;
  font-family: 'Courier New', monospace;
  font-size: 0.78rem;
  font-weight: bold;
  letter-spacing: 3px;
  text-transform: uppercase;
  border-bottom: 1px solid #3a3018;
  padding-bottom: 0.5rem;
  margin-bottom: 1.1rem;
}
.mc-chain {
  display: flex;
  align-items: center;
  min-width: max-content;
}
.mc-node {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6px;
  position: relative;
}
.mc-box {
  width: 54px;
  height: 54px;
  background: #121008;
  border: 2px solid #c8a42a;
  box-shadow: 0 0 0 1px #5a4008, inset 0 0 10px rgba(0,0,0,0.85);
  border-radius: 2px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  cursor: default;
  transition: border-color 0.15s, box-shadow 0.15s;
}
.mc-node:hover .mc-box {
  border-color: #ffe566;
  box-shadow: 0 0 14px rgba(200,164,42,0.65), 0 0 0 1px #5a4008, inset 0 0 8px rgba(0,0,0,0.65);
}
.mc-lbl {
  color: #7a6a50;
  font-family: 'Courier New', monospace;
  font-size: 0.60rem;
  text-align: center;
  white-space: nowrap;
  max-width: 62px;
  line-height: 1.3;
  transition: color 0.15s;
}
.mc-node:hover .mc-lbl { color: #c8a870; }
.mc-line {
  width: 34px;
  height: 3px;
  background: linear-gradient(90deg, #4a3808, #c8a42a 50%, #4a3808);
  box-shadow: 0 1px 0 #080600;
  flex-shrink: 0;
}
.mc-tip {
  visibility: hidden;
  opacity: 0;
  position: absolute;
  bottom: calc(100% + 10px);
  left: 50%;
  transform: translateX(-50%);
  background: #0c0800;
  border: 1px solid #c8a42a;
  padding: 6px 11px;
  z-index: 30;
  white-space: nowrap;
  pointer-events: none;
  box-shadow: 2px 2px 0 #000;
  transition: opacity 0.12s;
  min-width: 110px;
}
.mc-node:hover .mc-tip { visibility: visible; opacity: 1; }
.mc-tip::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 5px solid transparent;
  border-top-color: #c8a42a;
}
.mc-tip-t { color: #ffe566; font-size: 0.76rem; font-family: 'Courier New', monospace; font-weight: bold; display: block; }
.mc-tip-d { color: #7ec8ff; font-size: 0.68rem; font-family: 'Courier New', monospace; display: block; margin-top: 2px; }

/* ── 기술 스택 — 인챈트 태그 그리드 ── */
.mc-tech-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(188px,1fr));
  gap: 8px;
}
.mc-tech {
  background: rgba(0,0,0,0.48);
  border: 1px solid #3a3a3a;
  box-shadow: inset 1px 1px 0 #4a4a4a, inset -1px -1px 0 #141414;
  padding: 0.65rem 0.95rem;
}
.mc-tech-k {
  display: block;
  color: #0ea5e9;
  font-family: 'Courier New', monospace;
  font-size: 0.64rem;
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 1.2px;
  margin-bottom: 4px;
}
.mc-tech-v {
  color: rgba(220,218,205,0.82);
  font-size: 0.82rem;
  line-height: 1.45;
}

/* ── 데이터 출처 ── */
.mc-data {
  list-style: none;
  padding: 0;
  margin: 0;
}
.mc-data li {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  padding: 0.55rem 0;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  color: rgba(230,228,215,0.85);
  font-size: 0.9rem;
  line-height: 1.55;
}
.mc-data li:last-child { border-bottom: none; }
.mc-data-dot { color: #f0c040; flex-shrink: 0; font-family: 'Courier New', monospace; }
.mc-data li.warn { color: #f0c040; }

/* ── 완료 조건 — Achievement 토스트 ── */
.mc-toast {
  background: rgba(0,0,0,0.50);
  border: 2px solid #c8a42a;
  box-shadow: inset 1px 1px 0 rgba(200,164,42,0.25), inset -1px -1px 0 rgba(0,0,0,0.4);
  padding: 1.1rem 1.3rem;
  display: flex;
  gap: 1.1rem;
  align-items: center;
}
.mc-toast-icon { font-size: 2.2rem; flex-shrink: 0; }
.mc-toast-inner { flex: 1; }
.mc-toast-tag {
  display: block;
  color: #f0c040;
  font-family: 'Courier New', monospace;
  font-size: 0.62rem;
  font-weight: bold;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 5px;
}
.mc-toast-text {
  color: #f0f0e0;
  font-size: 0.9rem;
  line-height: 1.6;
  margin: 0;
}
.mc-toast-text strong { color: #fff; }

/* ── 적격성 체크리스트 ── */
.mc-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.mc-list li {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  padding: 0.55rem 0.5rem;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  color: rgba(225,222,210,0.88);
  font-size: 0.9rem;
  line-height: 1.5;
}
.mc-list li:last-child { border-bottom: none; }
.mc-yes {
  color: #10b981;
  font-family: 'Courier New', monospace;
  font-weight: bold;
  flex-shrink: 0;
}
</style>

# 마인크래프트 스킨 변환기

---

<div class="mc-win">
  <div class="mc-win-bar">
    <span class="mc-win-icon">🎯</span>
    <span class="mc-win-title">주제 한줄요약</span>
  </div>
  <div class="mc-win-body">
    <p class="mc-summary">AI로 전신 사진을 나만의 마인크래프트 스킨으로 — 사진 업로드 한 번으로 피부톤·헤어·의상이 반영된 64×64 스킨을 자동 생성, 4방향 미리보기·PNG 다운로드 제공</p>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar red">
    <span class="mc-win-icon">⚠️</span>
    <span class="mc-win-title">주요 문제</span>
  </div>
  <div class="mc-win-body">
    <p class="mc-text">마인크래프트는 전 세계적으로 가장 많이 플레이되는 게임 중 하나로, 스킨은 핵심적인 자기표현 수단이다. 그러나 64×64 UV 맵이라는 기술적 진입 장벽 때문에 일반 사용자가 직접 제작하기 어렵고, 사진 한 장으로 자신만의 스킨을 빠르게 얻을 수 있는 수단이 없다.</p>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar blue">
    <span class="mc-win-icon">👤</span>
    <span class="mc-win-title">타깃 사용자</span>
  </div>
  <div class="mc-win-body">
    <p class="mc-text">마인크래프트를 플레이하거나 관심 있는 일반 사용자 — 자신만의 스킨을 원하지만 픽셀 아트 편집 경험이 없는 사람</p>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar green">
    <span class="mc-win-icon">⚙️</span>
    <span class="mc-win-title">핵심 기능</span>
  </div>
  <div class="mc-win-body">
    <div class="mc-slots">
      <div class="mc-slot">
        <span class="mc-slot-num">①</span>
        <span class="mc-slot-text">전신 사진 업로드 → <strong>Gemini 2.5 Flash</strong>가 피부톤·헤어·의상 색상을 <strong>JSON</strong>으로 추출</span>
      </div>
      <div class="mc-slot">
        <span class="mc-slot-num">②</span>
        <span class="mc-slot-text">추출 특징으로 레퍼런스 베이스 선택 → <strong>HSV 재채색 + 명암 템플릿</strong>(numpy / Pillow)으로 64×64 합성</span>
      </div>
      <div class="mc-slot">
        <span class="mc-slot-num">③</span>
        <span class="mc-slot-text">앞·오른쪽·뒤·왼쪽 <strong>4방향 2D 캐러셀</strong> 미리보기 + PNG 다운로드</span>
      </div>
    </div>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar gold">
    <span class="mc-win-icon">🗺️</span>
    <span class="mc-win-title">동작 흐름</span>
  </div>
  <div class="mc-win-body" style="padding:0;">
    <div class="mc-adv-wrap">
      <div class="mc-adv-header">SkinForge — Advancements</div>
      <div class="mc-chain">

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">사진 업로드</span><span class="mc-tip-d">전신 사진을 올려 주세요</span></div>
          <div class="mc-box">📸</div>
          <div class="mc-lbl">사진<br>업로드</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">Gemini 2.5 Flash</span><span class="mc-tip-d">Vision으로 이미지 분석</span></div>
          <div class="mc-box">🤖</div>
          <div class="mc-lbl">Gemini<br>Vision</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">특징 JSON 추출</span><span class="mc-tip-d">피부·헤어·의상 데이터</span></div>
          <div class="mc-box">📋</div>
          <div class="mc-lbl">특징<br>JSON</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">베이스 스킨 선택</span><span class="mc-tip-d">가장 유사한 레퍼런스</span></div>
          <div class="mc-box">🎯</div>
          <div class="mc-lbl">베이스<br>선택</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">HSV 재채색 합성</span><span class="mc-tip-d">numpy / Pillow 픽셀 처리</span></div>
          <div class="mc-box">🎨</div>
          <div class="mc-lbl">HSV<br>합성</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">64×64 PNG 생성</span><span class="mc-tip-d">마인크래프트 스킨 완성</span></div>
          <div class="mc-box">🧱</div>
          <div class="mc-lbl">64×64<br>PNG</div>
        </div>
        <div class="mc-line"></div>

        <div class="mc-node">
          <div class="mc-tip"><span class="mc-tip-t">미리보기 · 다운로드</span><span class="mc-tip-d">앞·뒤·좌·우 + PNG 저장</span></div>
          <div class="mc-box">👁️</div>
          <div class="mc-lbl">미리보기<br>다운로드</div>
        </div>

      </div>
    </div>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar teal">
    <span class="mc-win-icon">🛠️</span>
    <span class="mc-win-title">기술 스택</span>
  </div>
  <div class="mc-win-body">
    <div class="mc-tech-grid">
      <div class="mc-tech">
        <span class="mc-tech-k">UI</span>
        <span class="mc-tech-v">Gradio 5.x · gr.Blocks · 커스텀 다크 테마</span>
      </div>
      <div class="mc-tech">
        <span class="mc-tech-k">AI 분석</span>
        <span class="mc-tech-v">Gemini 2.5 Flash · google-genai SDK · Vision → JSON</span>
      </div>
      <div class="mc-tech">
        <span class="mc-tech-k">스킨 합성</span>
        <span class="mc-tech-v">Python · numpy (HSV 재채색) · Pillow (UV 맵 픽셀)</span>
      </div>
      <div class="mc-tech">
        <span class="mc-tech-k">미리보기</span>
        <span class="mc-tech-v">Pillow 2D 캐러셀 · base64 data URI 임베드</span>
      </div>
      <div class="mc-tech">
        <span class="mc-tech-k">인프라</span>
        <span class="mc-tech-v">OCI E2.1.Micro · Docker · docker-compose · nginx</span>
      </div>
      <div class="mc-tech">
        <span class="mc-tech-k">CI/CD</span>
        <span class="mc-tech-v">GitHub Actions · push → 자동 배포</span>
      </div>
    </div>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar purple">
    <span class="mc-win-icon">📦</span>
    <span class="mc-win-title">데이터 출처</span>
  </div>
  <div class="mc-win-body">
    <ul class="mc-data">
      <li><span class="mc-data-dot">▸</span> 레퍼런스 베이스 스킨 및 명암 템플릿 — <strong>본인 직접 제작</strong></li>
      <li><span class="mc-data-dot">▸</span> 인물 사진 — 사용자가 직접 업로드 (서버에 영구 저장하지 않음)</li>
      <li class="warn"><span class="mc-data-dot">⚠</span> 업로드 사진은 Gemini API 호출 후 메모리에서 즉시 해제</li>
    </ul>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar green">
    <span class="mc-win-icon">✅</span>
    <span class="mc-win-title">완료 조건</span>
  </div>
  <div class="mc-win-body">
    <div class="mc-toast">
      <div class="mc-toast-icon">🏆</div>
      <div class="mc-toast-inner">
        <span class="mc-toast-tag">Achievement Unlocked</span>
        <p class="mc-toast-text">인물 전신 사진을 업로드하고 버튼을 누르면 <strong>30초 이내</strong>에 피부톤·헤어·의상 특징이 반영된 <strong>64×64 마인크래프트 스킨 PNG</strong>가 생성되고, 4방향 미리보기와 다운로드 버튼이 활성화된다.</p>
      </div>
    </div>
  </div>
</div>

<div class="mc-win">
  <div class="mc-win-bar">
    <span class="mc-win-icon">🔍</span>
    <span class="mc-win-title">적격성 자가진단</span>
  </div>
  <div class="mc-win-body">
    <ul class="mc-list">
      <li><span class="mc-yes">✔</span> AI 기능이 핵심 — 단순 CRUD·회원관리 아님</li>
      <li><span class="mc-yes">✔</span> Inference만 필요 — 모델 학습 불필요</li>
      <li><span class="mc-yes">✔</span> 외부 API 호출 (Gemini 2.5 Flash)</li>
      <li><span class="mc-yes">✔</span> 한 요청 30초 이내 처리</li>
      <li><span class="mc-yes">✔</span> 영구 저장 불필요 — 메모리 처리 후 즉시 해제</li>
      <li><span class="mc-yes">✔</span> 데이터 출처 적격 (저작권·개인정보 OK)</li>
      <li><span class="mc-yes">✔</span> 완료 조건 한 줄로 명확</li>
    </ul>
  </div>
</div>
