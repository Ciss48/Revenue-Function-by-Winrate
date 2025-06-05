# Revenue-Function-by-Winrate

Đây là 1 framework cố gắng tối ưu doanh thu bằng cách điều chỉnh level design (hay còn gọi là winrate). Hàm này hoạt động dựa trên nguyên lý: 
- Revenue level 1 = U1 * ARPU1 (U1: SỐ user start tại level 1)
- Revenue level 2 = U2 * ARPU2 = U1 * (1 - D1) * ARPU2 (D1: Droprate tại level 1)
- Revenue level 3 = U3 * ARPU3 = U1 * (1 - D1) * (1 - D2) * ARPU3
- ......
- Revenue level n = Un * ARPUn = U1 * (1 - D1) * (1 - D2) * ... * (1-Dn-1) * ARPUn
- Total Revenue = Rev1 + Rev2 + ... + Revn

=> Về bản chất các rev đang có biến là D1,D2,... và ARPU1, ARPU2,.... 
Ta có thể viết D và ARPU được theo winrate (vì bản chất 2 cái này bị ảnh hưởng bởi winrate 
- D = f(w)
- ARPU = f(w)

Ý tưởng của cách làm này là từ dữ liệu quá khứ, đưa vào mô hình huấn luyện để tìm hàm phù hợp

