<style>
.mc-card { background: rgba(28,26,24,0.80); margin: 2.2rem 0; overflow: hidden; }
.mc-card-h { background: rgba(0,0,0,0.28); border-bottom: 1px solid rgba(255,255,255,0.07); padding: 8px 14px; color: #b8b8b8; font-family: Inter, 'Segoe UI', ui-sans-serif, system-ui, -apple-system, sans-serif; font-size: 0.82rem; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; }
.mc-card-b { padding: 14px 16px; color: #b8b8b8; font-size: 0.92rem; line-height: 1.70; background: rgba(58,55,50,0.72); }
.mc-card-b b { color: #eee; }

.mc-rows { display: flex; flex-direction: column; gap: 5px; }
.mc-row { display: flex; align-items: flex-start; gap: 10px; background: rgba(0,0,0,0.28); padding: 10px 13px; }
.mc-num { background: #4e4e4e; color: #fff; font-weight: 700; font-size: 11px; font-family: 'Courier New', monospace; padding: 2px 7px; border-radius: 2px; flex-shrink: 0; margin-top: 2px; }
.mc-row-t { color: #d0d0d0; font-size: 0.9rem; line-height: 1.55; }
.mc-row-t b { color: #fff; }

.mc-tech-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(185px, 1fr)); gap: 5px; }
.mc-tech { background: rgba(0,0,0,0.28); padding: 8px 12px; }
.mc-tech-k { display: block; color: #0ea5e9; font-family: 'Courier New', monospace; font-size: 0.63rem; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 3px; }
.mc-tech-v { color: #b0b0b0; font-size: 0.82rem; line-height: 1.4; }

.mc-done { background: rgba(8,40,12,0.55); border-left: 3px solid #10b981; padding: 12px 16px; color: #c0e8b8; font-size: 0.91rem; line-height: 1.65; }
.mc-done b { color: #fff; }

.mc-chk-rows { display: flex; flex-direction: column; }
.mc-chk-row { display: flex; align-items: flex-start; gap: 10px; background: rgba(0,0,0,0.22); padding: 9px 12px; border-bottom: 1px solid rgba(255,255,255,0.05); color: #c8c8c8; font-size: 0.9rem; line-height: 1.5; }
.mc-chk-row:last-child { border-bottom: none; }
.mc-chk { color: #10b981; font-weight: 700; flex-shrink: 0; }

.mc-tip { background: #1e1600; border-left: 3px solid #f9a825; color: #f9a825; padding: 10px 13px; font-size: 0.84rem; line-height: 1.55; }

.mc-adv { background: rgba(14,12,8,0.90); padding: 1rem 1.3rem 1.3rem; overflow-x: auto; }
.mc-adv-hd { color: #d0ccc0; font-family: 'Courier New', monospace; font-size: 0.72rem; font-weight: 700; letter-spacing: 3px; text-transform: uppercase; border-bottom: 1px solid #302a10; padding-bottom: 0.5rem; margin-bottom: 1rem; }
.mc-chain { display: flex; align-items: center; width: fit-content; margin: 0 auto; }
.mc-node { display: flex; flex-direction: column; align-items: center; gap: 5px; position: relative; }
.mc-box2 { width: 52px; height: 52px; background: #100e08; border: 2px solid #c8a42a; box-shadow: 0 0 0 1px #5a4008, inset 0 0 10px rgba(0,0,0,0.85); border-radius: 2px; display: flex; align-items: center; justify-content: center; font-size: 1.75rem; cursor: default; transition: border-color 0.15s, box-shadow 0.15s; }
.mc-node:hover .mc-box2 { border-color: #ffe566; box-shadow: 0 0 12px rgba(200,164,42,0.6), 0 0 0 1px #5a4008, inset 0 0 8px rgba(0,0,0,0.7); }
.mc-lbl2 { color: #7a6848; font-family: 'Courier New', monospace; font-size: 0.60rem; text-align: center; white-space: nowrap; max-width: 60px; line-height: 1.3; transition: color 0.15s; }
.mc-node:hover .mc-lbl2 { color: #c0a060; }
.mc-line2 { width: 32px; height: 3px; background: linear-gradient(90deg, #4a3808, #c8a42a 50%, #4a3808); box-shadow: 0 1px 0 #060400; flex-shrink: 0; }
.mc-tp { visibility: hidden; opacity: 0; position: absolute; bottom: calc(100% + 9px); left: 50%; transform: translateX(-50%); background: #0c0800; border: 1px solid #c8a42a; padding: 5px 10px; z-index: 30; white-space: nowrap; pointer-events: none; box-shadow: 2px 2px 0 #000; transition: opacity 0.12s; min-width: 105px; }
.mc-node:hover .mc-tp { visibility: visible; opacity: 1; }
.mc-tp::after { content: ''; position: absolute; top: 100%; left: 50%; transform: translateX(-50%); border: 4px solid transparent; border-top-color: #c8a42a; }
.mc-tp-t { color: #ffe566; font-size: 0.75rem; font-family: 'Courier New', monospace; font-weight: 700; display: block; }
.mc-tp-d { color: #7ec8ff; font-size: 0.68rem; font-family: 'Courier New', monospace; display: block; margin-top: 2px; }
</style>

# 마인크래프트 스킨 변환기

<div class="mc-card">
<div class="mc-card-h">🎯 주제 한줄요약</div>
<div class="mc-card-b">AI로 전신 사진을 나만의 마인크래프트 스킨으로 — 사진 업로드 한 번으로 피부톤·헤어·의상이 반영된 64×64 스킨을 자동 생성, 4방향 미리보기·PNG 다운로드 제공</div>
</div>

<div class="mc-card">
<div class="mc-card-h">⚠️ 주요 문제</div>
<div class="mc-card-b">마인크래프트에서 스킨은 핵심적인 자기표현 수단이다. 그러나 64×64 UV 맵이라는 기술적 진입 장벽 때문에 일반 사용자가 직접 제작하기 어렵고, 사진 한 장으로 자신만의 스킨을 빠르게 얻을 수단이 없다.</div>
</div>

<div class="mc-card">
<div class="mc-card-h">👤 타깃 사용자</div>
<div class="mc-card-b">마인크래프트를 플레이하거나 관심 있는 일반 사용자 — 자신만의 스킨을 원하지만 픽셀 아트 편집 경험이 없는 사람</div>
</div>

<div class="mc-card">
<div class="mc-card-h">⚙️ 핵심 기능</div>
<div class="mc-card-b">
<div class="mc-rows">
<div class="mc-row"><span class="mc-num">1</span><span class="mc-row-t">전신 사진 업로드 → <b>Gemini 2.5 Flash</b>가 피부톤·헤어·의상 색상을 <b>JSON</b>으로 추출</span></div>
<div class="mc-row"><span class="mc-num">2</span><span class="mc-row-t">추출 특징으로 레퍼런스 베이스 선택 → <b>HSV 재채색 + 명암 템플릿</b>(numpy / Pillow)으로 64×64 합성</span></div>
<div class="mc-row"><span class="mc-num">3</span><span class="mc-row-t">앞·오른쪽·뒤·왼쪽 <b>4방향 2D 캐러셀</b> 미리보기 + PNG 다운로드</span></div>
</div>
</div>
</div>

<div class="mc-card">
<div class="mc-card-h">🗺️ 동작 흐름</div>
<div class="mc-adv">
<div class="mc-adv-hd">SkinForge — Advancements</div>
<div class="mc-chain">
<div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">사진 업로드</span><span class="mc-tp-d">전신 사진을 올려 주세요</span></div><div class="mc-box2">📸</div><div class="mc-lbl2">사진<br>업로드</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">Gemini 2.5 Flash</span><span class="mc-tp-d">Vision으로 이미지 분석</span></div><div class="mc-box2">🤖</div><div class="mc-lbl2">Gemini<br>Vision</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">특징 JSON 추출</span><span class="mc-tp-d">피부·헤어·의상 데이터</span></div><div class="mc-box2">📋</div><div class="mc-lbl2">특징<br>JSON</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">베이스 스킨 선택</span><span class="mc-tp-d">가장 유사한 레퍼런스</span></div><div class="mc-box2">🎯</div><div class="mc-lbl2">베이스<br>선택</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">HSV 재채색 합성</span><span class="mc-tp-d">numpy / Pillow 픽셀 처리</span></div><div class="mc-box2">🎨</div><div class="mc-lbl2">HSV<br>합성</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">64×64 PNG 생성</span><span class="mc-tp-d">마인크래프트 스킨 완성</span></div><div class="mc-box2">🧱</div><div class="mc-lbl2">64×64<br>PNG</div></div><div class="mc-line2"></div><div class="mc-node"><div class="mc-tp"><span class="mc-tp-t">미리보기 · 다운로드</span><span class="mc-tp-d">앞·뒤·좌·우 + PNG 저장</span></div><div class="mc-box2">👁️</div><div class="mc-lbl2">미리보기<br>다운로드</div></div>
</div>
</div>
</div>

<div class="mc-card">
<div class="mc-card-h">🛠️ 기술 스택</div>
<div class="mc-card-b">
<div class="mc-tech-grid">
<div class="mc-tech"><span class="mc-tech-k">UI</span><span class="mc-tech-v">Gradio 5.x · gr.Blocks · 커스텀 다크 테마</span></div>
<div class="mc-tech"><span class="mc-tech-k">AI 분석</span><span class="mc-tech-v">Gemini 2.5 Flash · google-genai SDK · Vision → JSON</span></div>
<div class="mc-tech"><span class="mc-tech-k">스킨 합성</span><span class="mc-tech-v">Python · numpy (HSV 재채색) · Pillow (UV 맵 픽셀)</span></div>
<div class="mc-tech"><span class="mc-tech-k">미리보기</span><span class="mc-tech-v">Pillow 2D 캐러셀 · base64 data URI 임베드</span></div>
<div class="mc-tech"><span class="mc-tech-k">인프라</span><span class="mc-tech-v">OCI E2.1.Micro · Docker · docker-compose · nginx</span></div>
<div class="mc-tech"><span class="mc-tech-k">CI/CD</span><span class="mc-tech-v">GitHub Actions · push → 자동 배포</span></div>
</div>
</div>
</div>

<div class="mc-card">
<div class="mc-card-h">📦 데이터 출처</div>
<div class="mc-card-b">레퍼런스 베이스 스킨 및 명암 템플릿은 <b>본인 직접 제작</b>. 인물 사진은 사용자가 직접 업로드하며 서버에 영구 저장하지 않습니다.</div>
<div class="mc-tip">💡 업로드 사진은 Gemini API 호출 후 메모리에서 즉시 해제됩니다.</div>
</div>

<div class="mc-card">
<div class="mc-card-h">✅ 완료 조건</div>
<div class="mc-card-b">
<div class="mc-done">인물 전신 사진을 업로드하고 버튼을 누르면 <b>30초 이내</b>에 피부톤·헤어·의상 특징이 반영된 <b>64×64 마인크래프트 스킨 PNG</b>가 생성되고, 4방향 미리보기와 다운로드 버튼이 활성화된다.</div>
</div>
</div>

<div class="mc-card">
<div class="mc-card-h">🔍 적격성 자가진단</div>
<div class="mc-card-b" style="padding:0;">
<div class="mc-chk-rows">
<div class="mc-chk-row"><span class="mc-chk">✔</span> AI 기능이 핵심 — 단순 CRUD·회원관리 아님</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> Inference만 필요 — 모델 학습 불필요</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> 외부 API 호출 (Gemini 2.5 Flash)</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> 한 요청 30초 이내 처리</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> 영구 저장 불필요 — 메모리 처리 후 즉시 해제</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> 데이터 출처 적격 (저작권·개인정보 OK)</div>
<div class="mc-chk-row"><span class="mc-chk">✔</span> 완료 조건 한 줄로 명확</div>
</div>
</div>
<div class="mc-tip">💡 TIP: 단색 배경, 정면 포즈 사진이 가장 정확한 스킨을 만들어냅니다.</div>
</div>
