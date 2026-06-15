<style>
/* ── SkinForge Contents ── */

/* 섹션 헤더 */
.sf-h {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #f97316;
  font-size: 1rem;
  font-weight: 700;
  font-family: 'Courier New', monospace;
  letter-spacing: 0.5px;
  margin: 2.4rem 0 0.9rem;
}
.sf-h::after {
  content: '';
  flex: 1;
  height: 1px;
  background: linear-gradient(90deg, rgba(249,115,22,0.5), transparent);
}

/* 강조 박스 */
.sf-box {
  background: rgba(0,0,0,0.30);
  border-left: 4px solid #f97316;
  border-radius: 0 6px 6px 0;
  padding: 0.85rem 1.2rem;
  color: rgba(255,255,255,0.9);
  font-size: 0.97rem;
  line-height: 1.65;
  margin-bottom: 0.5rem;
}
.sf-box.blue  { border-color: #0ea5e9; }
.sf-box.green { border-color: #10b981; }
.sf-box.gold  { border-color: #f0c040; }

/* 핵심 기능 그리드 */
.sf-feat-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
  gap: 0.7rem;
  margin-bottom: 0.5rem;
}
.sf-feat {
  background: rgba(0,0,0,0.28);
  border: 1px solid rgba(255,255,255,0.12);
  border-radius: 6px;
  padding: 0.75rem 1rem;
  display: flex;
  gap: 0.65rem;
  align-items: flex-start;
}
.sf-feat-n {
  color: #f0c040;
  font-weight: 700;
  font-family: 'Courier New', monospace;
  font-size: 1.05rem;
  flex-shrink: 0;
  min-width: 1.4rem;
}
.sf-feat-t {
  color: rgba(255,255,255,0.8);
  font-size: 0.88rem;
  line-height: 1.55;
}
.sf-feat-t strong { color: #fff; }

/* ── Minecraft Advancements ── */
.mc-wrap {
  background: #1c1814;
  border: 3px solid #6a5518;
  box-shadow: inset 0 0 40px rgba(0,0,0,0.7), 0 0 0 1px #2a2008;
  border-radius: 3px;
  padding: 1rem 1.4rem 1.4rem;
  overflow-x: auto;
  margin-bottom: 0.5rem;
}
.mc-head {
  color: #f0f0e0;
  font-family: 'Courier New', monospace;
  font-size: 0.82rem;
  font-weight: bold;
  letter-spacing: 2px;
  text-transform: uppercase;
  border-bottom: 1px solid #3a3020;
  padding-bottom: 0.55rem;
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
  width: 52px;
  height: 52px;
  background: #141210;
  border: 2px solid #c8a42a;
  box-shadow: 0 0 0 1px #5a4008, inset 0 0 10px rgba(0,0,0,0.8);
  border-radius: 2px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.75rem;
  cursor: default;
  transition: border-color 0.15s, box-shadow 0.15s;
  position: relative;
}
.mc-node:hover .mc-box {
  border-color: #ffe566;
  box-shadow: 0 0 12px rgba(200,164,42,0.65), 0 0 0 1px #5a4008, inset 0 0 8px rgba(0,0,0,0.6);
}
.mc-lbl {
  color: #8a7860;
  font-family: 'Courier New', monospace;
  font-size: 0.62rem;
  text-align: center;
  white-space: nowrap;
  max-width: 62px;
  line-height: 1.3;
  transition: color 0.15s;
}
.mc-node:hover .mc-lbl { color: #d0b880; }

.mc-line {
  width: 32px;
  height: 3px;
  background: linear-gradient(90deg, #4a3808, #c8a42a 50%, #4a3808);
  box-shadow: 0 1px 0 #0a0800;
  flex-shrink: 0;
}

/* 툴팁 */
.mc-tip {
  visibility: hidden;
  opacity: 0;
  position: absolute;
  bottom: calc(100% + 10px);
  left: 50%;
  transform: translateX(-50%);
  background: #0e0900;
  border: 1px solid #c8a42a;
  padding: 6px 10px;
  z-index: 30;
  white-space: nowrap;
  pointer-events: none;
  box-shadow: 2px 2px 0 #000, 0 0 12px rgba(200,164,42,0.3);
  transition: opacity 0.12s;
  min-width: 110px;
}
.mc-node:hover .mc-tip {
  visibility: visible;
  opacity: 1;
}
.mc-tip::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 5px solid transparent;
  border-top-color: #c8a42a;
}
.mc-tip-t { color: #ffe566; font-size: 0.78rem; font-family: 'Courier New', monospace; font-weight: bold; display: block; }
.mc-tip-d { color: #7ec8ff; font-size: 0.70rem; font-family: 'Courier New', monospace; display: block; margin-top: 2px; }

/* 기술 스택 그리드 */
.sf-stack {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(195px, 1fr));
  gap: 0.6rem;
  margin-bottom: 0.5rem;
}
.sf-stack-item {
  background: rgba(0,0,0,0.28);
  border: 1px solid rgba(255,255,255,0.10);
  border-radius: 5px;
  padding: 0.6rem 0.9rem;
}
.sf-stack-k {
  color: #f0c040;
  font-size: 0.68rem;
  font-family: 'Courier New', monospace;
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  display: block;
  margin-bottom: 3px;
}
.sf-stack-v {
  color: rgba(255,255,255,0.75);
  font-size: 0.83rem;
  line-height: 1.45;
}

/* 적격성 체크리스트 */
.sf-checks {
  list-style: none;
  padding: 0;
  margin: 0 0 0.5rem;
  background: rgba(0,0,0,0.25);
  border: 1px solid rgba(255,255,255,0.10);
  border-radius: 6px;
  overflow: hidden;
}
.sf-checks li {
  display: flex;
  align-items: flex-start;
  gap: 0.7rem;
  padding: 0.55rem 1rem;
  border-bottom: 1px solid rgba(255,255,255,0.06);
  color: rgba(255,255,255,0.78);
  font-size: 0.88rem;
  line-height: 1.5;
}
.sf-checks li:last-child { border-bottom: none; }
.sf-chk { color: #10b981; font-size: 1rem; flex-shrink: 0; }
</style>

# 마인크래프트 스킨 변환기

---

<div class="sf-h">🎯 주제 한줄요약</div>

<div class="sf-box">
AI로 전신 사진을 나만의 마인크래프트 스킨으로 — 사진 업로드 한 번으로 피부톤·헤어·의상이 반영된 64×64 스킨을 자동 생성, 4방향 미리보기·PNG 다운로드 제공
</div>

---

<div class="sf-h">⚠️ 주요 문제</div>

<div class="sf-box blue">
마인크래프트는 전 세계적으로 가장 많이 플레이되는 게임 중 하나로, 스킨은 핵심 자기표현 수단이다. 그러나 64×64 UV 맵이라는 기술적 진입 장벽 때문에 일반 사용자가 직접 제작하기 어렵고, 사진 한 장으로 나만의 스킨을 빠르게 얻을 수단이 없다.
</div>

---

<div class="sf-h">👤 타깃 사용자</div>

<div class="sf-box blue">
마인크래프트를 플레이하거나 관심 있는 일반 사용자 — 자신만의 스킨을 원하지만 픽셀 아트 편집 경험이 없는 사람
</div>

---

<div class="sf-h">⚙️ 핵심 기능</div>

<div class="sf-feat-grid">
  <div class="sf-feat">
    <span class="sf-feat-n">①</span>
    <span class="sf-feat-t">전신 사진 업로드 → <strong>Gemini 2.5 Flash</strong>가 피부톤·헤어·의상 색상·스타일 특징을 <strong>JSON</strong>으로 추출</span>
  </div>
  <div class="sf-feat">
    <span class="sf-feat-n">②</span>
    <span class="sf-feat-t">추출 특징으로 레퍼런스 베이스 선택 → <strong>HSV 재채색 + 명암 템플릿</strong>(numpy/Pillow)으로 64×64 스킨 합성</span>
  </div>
  <div class="sf-feat">
    <span class="sf-feat-n">③</span>
    <span class="sf-feat-t">앞·오른쪽·뒤·왼쪽 <strong>4방향 2D 캐러셀 미리보기</strong> + PNG 다운로드</span>
  </div>
</div>

---

<div class="sf-h">🗺️ 동작 흐름</div>

<div class="mc-wrap">
  <div class="mc-head">SkinForge — Advancements</div>
  <div class="mc-chain">

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">사진 업로드</span>
        <span class="mc-tip-d">전신 사진을 올려 주세요</span>
      </div>
      <div class="mc-box">📸</div>
      <div class="mc-lbl">사진<br>업로드</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">Gemini 2.5 Flash</span>
        <span class="mc-tip-d">Vision으로 이미지 분석</span>
      </div>
      <div class="mc-box">🤖</div>
      <div class="mc-lbl">Gemini<br>Vision</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">특징 JSON 추출</span>
        <span class="mc-tip-d">피부·헤어·의상 데이터</span>
      </div>
      <div class="mc-box">📋</div>
      <div class="mc-lbl">특징<br>JSON</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">베이스 스킨 선택</span>
        <span class="mc-tip-d">가장 유사한 레퍼런스</span>
      </div>
      <div class="mc-box">🎯</div>
      <div class="mc-lbl">베이스<br>선택</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">HSV 재채색 합성</span>
        <span class="mc-tip-d">numpy / Pillow 픽셀 처리</span>
      </div>
      <div class="mc-box">🎨</div>
      <div class="mc-lbl">HSV<br>합성</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">64×64 PNG 생성</span>
        <span class="mc-tip-d">마인크래프트 스킨 완성</span>
      </div>
      <div class="mc-box">🧱</div>
      <div class="mc-lbl">64×64<br>PNG</div>
    </div>

    <div class="mc-line"></div>

    <div class="mc-node">
      <div class="mc-tip">
        <span class="mc-tip-t">미리보기 · 다운로드</span>
        <span class="mc-tip-d">앞·뒤·좌·우 + PNG 저장</span>
      </div>
      <div class="mc-box">👁️</div>
      <div class="mc-lbl">미리보기<br>다운로드</div>
    </div>

  </div>
</div>

---

<div class="sf-h">🛠️ 기술 스택</div>

<div class="sf-stack">
  <div class="sf-stack-item">
    <span class="sf-stack-k">UI</span>
    <span class="sf-stack-v">Gradio 5.x · gr.Blocks · 커스텀 다크 테마</span>
  </div>
  <div class="sf-stack-item">
    <span class="sf-stack-k">AI 분석</span>
    <span class="sf-stack-v">Gemini 2.5 Flash · google-genai SDK · Vision → JSON</span>
  </div>
  <div class="sf-stack-item">
    <span class="sf-stack-k">스킨 합성</span>
    <span class="sf-stack-v">Python · numpy (HSV 재채색) · Pillow (UV 맵 픽셀)</span>
  </div>
  <div class="sf-stack-item">
    <span class="sf-stack-k">미리보기</span>
    <span class="sf-stack-v">Pillow 2D 캐러셀 · base64 data URI 임베드</span>
  </div>
  <div class="sf-stack-item">
    <span class="sf-stack-k">인프라</span>
    <span class="sf-stack-v">OCI E2.1.Micro · Docker · docker-compose · nginx</span>
  </div>
  <div class="sf-stack-item">
    <span class="sf-stack-k">CI/CD</span>
    <span class="sf-stack-v">GitHub Actions · push → 자동 배포</span>
  </div>
</div>

---

<div class="sf-h">📦 데이터 출처</div>

<div class="sf-box">
<ul style="margin:0;padding-left:1.1rem;line-height:1.8;font-size:0.9rem;">
<li>레퍼런스 베이스 스킨 및 명암 템플릿 — <strong>본인 직접 제작</strong></li>
<li>인물 사진 — 사용자가 직접 업로드 (서버에 영구 저장하지 않음)</li>
<li style="color:#f0c040;">⚠️ 업로드 사진은 Gemini API 호출 후 메모리에서 즉시 해제</li>
</ul>
</div>

---

<div class="sf-h">✅ 완료 조건</div>

<div class="sf-box gold">
인물 전신 사진을 업로드하고 버튼을 누르면 <strong>30초 이내</strong>에 피부톤·헤어·의상 특징이 반영된 <strong>64×64 마인크래프트 스킨 PNG</strong>가 생성되고, 4방향 미리보기와 다운로드 버튼이 활성화된다.
</div>

---

<div class="sf-h">🔍 적격성 자가진단</div>

<ul class="sf-checks">
  <li><span class="sf-chk">✔</span> AI 기능이 핵심 — 단순 CRUD·회원관리 아님</li>
  <li><span class="sf-chk">✔</span> Inference만 필요 — 모델 학습 불필요</li>
  <li><span class="sf-chk">✔</span> 외부 API 호출 (Gemini 2.5 Flash)</li>
  <li><span class="sf-chk">✔</span> 한 요청 30초 이내 처리</li>
  <li><span class="sf-chk">✔</span> 영구 저장 불필요 — 메모리 처리 후 즉시 해제</li>
  <li><span class="sf-chk">✔</span> 데이터 출처 적격 (저작권·개인정보 OK)</li>
  <li><span class="sf-chk">✔</span> 완료 조건 한 줄로 명확</li>
</ul>
