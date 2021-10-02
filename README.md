# 基於PIC18F4520的打地鼠遊戲
## 工具
- FPGA板
- 點矩陣
- 七段顯示器
## 遊戲規則
- 遊戲時間30秒，由七段顯示器顯示
- 點矩陣顯示地鼠位置，按壓對應位置按鈕可以打擊地鼠
- 打中地鼠可以加一分，分數由七段顯示器顯示
- 地鼠只會顯示0.5秒
- 時間結束時，會有"GG"的字樣往左滑動離開
- 按下button0即可reset遊戲

## Module 說明
- matrixKeyboard_drive & keypad：檢測哪個按鈕被按下
- hit_gopher：處理打到地鼠的訊號
- random_gen_state：隨機產生下個地鼠
- dot_displayer：點矩陣顯示器控制
- SevenSegment：七段顯示器控制
- gg：呈現遊戲結束時的GG畫面
- whack_a_hole：連結各module使遊戲運行
