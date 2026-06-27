# 𓃥 白六3D訊息雲霄飛車 (White 6 3D Message Coaster)

[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=flat-square&logo=three.js)](https://threejs.org/)
[![Platform](https://img.shields.io/badge/Platform-Mobile%20%7C%20Desktop-orange?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)]()

> 讓文字化身為炫目的立體雲霄飛車，在透明軟管空間中高速衝刺！
> 本專案由靈感標誌 **「奶油色台灣土狗——白六 (White 6)」** 守護，打造極致流暢、百分之百純文字的 3D 空間互動擬真體驗。

---

## 🌟 核心特色 (Core Features)

* **𓃥 白六守護・純淨立體視覺**
  採用物理級像素裁剪技術（Pixel Clipping），100% 徹底移除 Canvas 紋理貼圖常見的半透明方塊背景與陰影折射。利用多層深度疊加（Multi-layer depth stacking），呈現純粹、高透明度且具備厚度質感的發光立體字體。
* **軌道動態佈置模式 (Setup Mode)**
  支援單一節點精細微調或整組軟管快速平移。可自由接續下一段軟管，並透過滑桿即時改變管道段落總長度，隨心所欲建構高低起伏的飛車軌道。
* **字串幾何中心動態跟拍 (String-Center Camera Tracking)**
  捨棄傳統生硬的火車頭跟隨！特製鏡頭跟拍算法會實時計算「整串文字所有車廂的 3D 空間幾何中心點」。無論字串多長、過彎多劇烈，整列文字列車永遠穩居畫面視覺黃金焦點。
* **緊湊感字距設計 (Compact Letter-Spacing)**
  優化文字推移間距（Trail Offset），縮短字與字之間的空隙。在多層立體疊加下，字體銜接更為緊密連貫，過彎滑行時具備極強烈的列車一體感。
* **全面解鎖 3D 自由觀察 (Free Orbit OrbitControls)**
  列車到站後，跟拍鏡頭平穩釋放控制權。使用者可直接透過手指或滑鼠進行自由擴張、捏合放大（Zoom In）、滑動旋轉，全方位無死角欣賞立體字在空間中的姿態。
* **極致防卡死與重生機制 (Context Lost Recovery)**
  針對移動端（如 iOS Safari）進行硬核優化！全面採用不依賴複雜光照計算的 `MeshBasicMaterial`，並注入著色器預熱編譯。內建 `webglcontextlost` 監聽技術，若瀏覽器內存釋放不及導致畫面遺失，將在 0.1 秒內自動完成核心重置與無感重生。
* **一鍵實時錄影下載 (Screen Recording)**
  內建 Canvas 串流錄影功能（MimeType 自動相容切換）。按下錄影並發射列車，到站停靠當下即會自動導出並下載 WebM 高清影片，輕鬆分享飛車奔馳的精彩瞬間。

---

## 🛠️ 技術棧 (Tech Stack)

* **前端核心**：HTML5, CSS3, JavaScript (ES6+)
* **3D 渲染引擎**：[Three.js (r128)](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js)
* **互動控制器**：
  * `OrbitControls.js` (鏡頭軌道控制、雙指縮放)
  * `TransformControls.js` (3D 節點 3 軸拖拽編輯)

---

## 🚀 快速開始 (Quick Start)

專案已完全模組化與單一文件化，無需配置繁瑣的 Webpack 或 Node.js 環境，即開即用：

1. 下載或複製專案中的 `index.html`。
2. 直接在瀏覽器中開啟 `index.html`（推薦使用本地伺服器如 Live Server 開啟以支援完整存檔功能）。
3. **佈置模式**：拖拽紅黃色球體調整軟管外型，點擊「接續下一段軟管」或調整長度。
4. **發射飛車**：輸入您想滑行的文字（例如：`TAIWAN 🚀 TRAIN`），點擊「完成佈置」，接著按下「發射文字列車」，即可享受極速跟拍視覺！

---

## 💾 歷史路徑存檔系統 (Archive System)

本專案內建基於 `localStorage` 的軌道保存機制：
* 佈置完滿意的軟管曲線後，可在選單中點擊 **「儲存此路徑」**。
* 系統會自動記錄所有 3D 節點的空間坐標，並產生帶有時間戳記的歷史列表。
* 下次重新整理開啟網頁時，系統會**自動載入最後一次的歷史存檔**，讓您的創意心血永不流失。

---

## 𓃥 關於白六 (About White 6)

白六是一隻非常有靈性、擁有奶油色美麗毛髮的台灣土狗。本專案的「雲霄飛車貼軌滑行算法」與「緊湊字距速度感」，正是完美致敬了白六在台灣田野間奔跑時，那優雅、流暢且充滿爆發力的靈動身姿。

歡迎一起輸入文字，搭上 **𓃥 白六3D訊息雲霄飛車**！
