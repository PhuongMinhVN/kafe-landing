# PMVN Cafe Landing Page (`kafe.omoshop.live`)

Trang web bán phần mềm **PMVN Smart Cafe Suite** dạng tĩnh thuần HTML/CSS, chạy **24/7 miễn phí trên Cloudflare Pages** (giống `omoshop-landing`), không phụ thuộc máy tính Windows có bật hay không.

## Cách đưa lên Cloudflare Pages (2 phút)

1. Tạo repo GitHub mới (vd: `PhuongMinhVN/kafe-landing`) và push toàn bộ nội dung thư mục `kafe-landing/` này lên nhánh `main`.
2. Vào **Cloudflare Dashboard → Compute → Workers & Pages → Create application → Pages → Connect to Git**.
3. Chọn repo `PhuongMinhVN/kafe-landing`:
   - **Framework preset**: `None`
   - **Build command**: *(để trống)*
   - **Build output directory**: `/` (hoặc `.`)
   - Bấm **Save and Deploy**.
4. Sau khi deploy xong (mất ~5 giây), vào tab **Custom domains → Set up a custom domain** → nhập **`kafe.omoshop.live`** → Cloudflare tự cấu hình DNS & SSL HTTPS.
5. *(Tùy chọn cho nút "Dùng thử POS")*: Trong **Cloudflare Tunnels → PhuongMinhVietNam**, thêm 1 route:
   - Subdomain: `demo-kafe` · Domain: `omoshop.live` · Service: `http://localhost:3001`.
