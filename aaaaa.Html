<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
<title>ROWARIOR - The Forgotten Kingdom (ProMax)</title>
<style>
  :root {
    --gold: #f0cf85;
    --gold-dark: #9c7538;
    --glass: rgba(12, 18, 30, 0.8);
    --glass-border: rgba(240, 207, 133, 0.38);
  }
  * {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
    user-select: none;
    -webkit-user-select: none;
  }
  body {
    margin: 0;
    overflow: hidden;
    background: #060a12;
    color: #fff;
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    touch-action: none;
  }
  canvas {
    display: block;
    width: 100vw;
    height: 100vh;
  }
  button {
    background: linear-gradient(145deg, #b38742, #543918);
    border: 1px solid var(--gold);
    color: #fff;
    padding: 10px 14px;
    border-radius: 12px;
    font-weight: 700;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.45);
    transition: transform 0.1s ease, filter 0.15s ease;
  }
  button:active {
    transform: scale(0.93);
    filter: brightness(1.15);
  }

  /* Màn hình Loading */
  #loading {
    position: fixed;
    inset: 0;
    z-index: 999;
    background: radial-gradient(circle at center, #162238 0%, #060a12 100%);
    display: grid;
    place-content: center;
    text-align: center;
    gap: 12px;
  }
  #loading .title {
    font-family: Georgia, serif;
    font-size: clamp(32px, 6vw, 56px);
    letter-spacing: 6px;
    color: var(--gold);
    text-shadow: 0 0 25px rgba(240, 207, 133, 0.5);
  }

  /* Hiệu ứng chuyển màn mượt mà */
  #fadeOverlay {
    position: fixed;
    inset: 0;
    background: #04070d;
    opacity: 0;
    pointer-events: none;
    z-index: 80;
    transition: opacity 0.4s ease;
  }
  #fadeOverlay.active {
    opacity: 1;
  }

  /* HUD Tổng thể */
  #hud {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 10;
  }
  .top {
    position: absolute;
    top: max(12px, env(safe-area-inset-top));
    left: max(12px, env(safe-area-inset-left));
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    max-width: 65%;
  }
  .pill {
    background: var(--glass);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border: 1px solid var(--glass-border);
    border-radius: 12px;
    padding: 8px 12px;
    font-size: 13px;
    font-weight: 600;
    box-shadow: 0 4px 15px rgba(0,0,0,0.35);
  }
  .menu {
    position: absolute;
    top: max(12px, env(safe-area-inset-top));
    right: max(12px, env(safe-area-inset-right));
    display: flex;
    gap: 6px;
    pointer-events: auto;
  }
  .menu button {
    padding: 8px 11px;
    font-size: 12px;
    background: var(--glass);
    backdrop-filter: blur(10px);
  }

  /* Thông báo Toast */
  #toast {
    position: absolute;
    top: 68px;
    left: 50%;
    transform: translateX(-50%) translateY(-10px);
    background: rgba(12, 18, 30, 0.92);
    backdrop-filter: blur(12px);
    border: 1px solid var(--gold);
    padding: 10px 20px;
    border-radius: 14px;
    opacity: 0;
    transition: opacity 0.25s ease, transform 0.25s ease;
    text-align: center;
    font-size: 14px;
    font-weight: 600;
    color: #fff6e0;
    box-shadow: 0 8px 25px rgba(0,0,0,0.5);
    max-width: 88%;
  }
  #toast.show {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }

  /* Tiêu đề sảnh chính */
  #center {
    position: absolute;
    top: 23%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    text-shadow: 0 4px 20px rgba(0,0,0,0.9);
    pointer-events: none;
  }
  #center h1 {
    font: bold clamp(28px, 6vw, 58px) Georgia, serif;
    letter-spacing: 6px;
    margin: 0;
    background: linear-gradient(to bottom, #fff5d6, #d9a74a);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  #center p {
    color: #e7d9b5;
    margin: 6px 0;
    font-size: clamp(12px, 2vw, 15px);
  }

  /* Nút tương tác nổi khi lại gần 3 cửa góc phải / rương / cửa qua màn */
  #interactPrompt {
    position: absolute;
    bottom: 24%;
    left: 50%;
    transform: translateX(-50%);
    pointer-events: auto;
    display: none;
    align-items: center;
    gap: 10px;
    background: linear-gradient(135deg, rgba(28, 38, 58, 0.94), rgba(14, 20, 32, 0.96));
    border: 2px solid var(--gold);
    box-shadow: 0 0 25px rgba(240, 207, 133, 0.45);
    padding: 12px 22px;
    border-radius: 50px;
    font-size: 15px;
    color: #fff;
    animation: pulsePrompt 1.6s infinite ease-in-out;
  }
  #interactPrompt.visible {
    display: flex;
  }
  @keyframes pulsePrompt {
    0%, 100% { box-shadow: 0 0 18px rgba(240, 207, 133, 0.35); }
    50% { box-shadow: 0 0 32px rgba(240, 207, 133, 0.75); }
  }

  /* Vùng cảm ứng xoay camera trên Mobile (nửa phải màn hình) */
  #touchLookZone {
    position: fixed;
    top: 0;
    right: 0;
    width: 55vw;
    height: 100vh;
    z-index: 5;
    display: none;
  }

  /* Bố cục điều khiển Mobile chuyên biệt */
  #mobileControls {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 15;
    display: none;
  }
  /* Joystick góc trái dưới */
  #joy {
    position: absolute;
    bottom: max(22px, env(safe-area-inset-bottom));
    left: max(24px, env(safe-area-inset-left));
    width: 112px;
    height: 112px;
    border-radius: 50%;
    border: 2px solid rgba(240, 207, 133, 0.45);
    background: radial-gradient(circle, rgba(255,255,255,0.08), rgba(10,16,28,0.45));
    backdrop-filter: blur(4px);
    pointer-events: auto;
  }
  #knob {
    position: absolute;
    width: 44px;
    height: 44px;
    left: 32px;
    top: 32px;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #fff4d4, #c99b42);
    box-shadow: 0 4px 12px rgba(0,0,0,0.6);
    pointer-events: none;
  }

  /* Nút Nhảy ở trên, Nút Ngồi ở dưới — nằm phía trên gần góc trái dưới */
  .left-stance-btns {
    position: absolute;
    bottom: calc(max(22px, env(safe-area-inset-bottom)) + 126px);
    left: max(28px, env(safe-area-inset-left));
    display: flex;
    flex-direction: column;
    gap: 10px;
    pointer-events: auto;
  }
  .stance-btn {
    width: 52px;
    height: 52px;
    border-radius: 50%;
    padding: 0;
    background: var(--glass);
    backdrop-filter: blur(8px);
    border: 1.5px solid var(--gold);
    font-size: 20px;
    display: grid;
    place-items: center;
  }
  .stance-btn.active {
    background: linear-gradient(135deg, #c99b42, #6e4c1e);
    box-shadow: 0 0 15px rgba(240, 207, 133, 0.6);
  }

  /* Cụm nút chiến đấu góc phải dưới cho Mobile */
  .right-combat-btns {
    position: absolute;
    bottom: max(24px, env(safe-area-inset-bottom));
    right: max(24px, env(safe-area-inset-right));
    display: flex;
    gap: 14px;
    align-items: flex-end;
    pointer-events: auto;
  }
  .combat-btn {
    width: 62px;
    height:
