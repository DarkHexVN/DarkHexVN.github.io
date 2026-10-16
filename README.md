# All In One — Shadowrocket Config (Self-Hosted on GitHub)

Module All In One tự chứa, ghép toàn bộ script vào **1 file `all-in-one.js`** duy nhất.
Không phụ thuộc link `raw.githubusercontent.com/duyvinh09/...` khi runtime — code đã được inline.

## Files

| File | Mô tả |
|------|------|
| `All_In_One.conf` | File cấu hình Shadowrocket — trỏ `script-path` tới `all-in-one.js` |
| `all-in-one.js` | Dispatcher 4.5 MB chứa 25 handler (YouTube, Spotify, VSCO, Locket, ...) |

## Cách upload

### Cách 1: Web GitHub (nhanh nhất)
1. Tạo repo public mới (vd: `shadowrocket-config`).
2. Bấm **Add file → Upload files**.
3. Kéo 2 file `All_In_One.conf` + `all-in-one.js` vào.
4. Commit.

### Cách 2: Git CLI
```bash
git clone https://github.com/DarkHexVN/DarkHexVN.github.io.git
cd DarkHexVN.github.io
# Copy 2 file vào đây
git add .
git commit -m "Add All In One config"
git push
```

## Cách dùng trong Shadowrocket

1. Mở Shadowrocket → **Config** → dấu **+** → **URL**
2. Dán link raw của file `.conf`:
   ```
   https://cdn.jsdelivr.net/gh/DarkHexVN/DarkHexVN.github.io@main/All_In_One.conf
   ```
3. Bấm **Download** → chọn file vừa tải → **Edit**
4. Bật **HTTPS Decryption (MITM)** & cấp chứng chỉ cho các hostname trong `[MITM]`
5. Bật module là xong!

## Link raw (đã chuẩn bị sẵn cho repo này)

- **Config (.conf):** `https://cdn.jsdelivr.net/gh/DarkHexVN/DarkHexVN.github.io@main/All_In_One.conf`
- **Script (all-in-one.js):** `https://cdn.jsdelivr.net/gh/DarkHexVN/DarkHexVN.github.io@main/all-in-one.js`

> Repo: `DarkHexVN/DarkHexVN.github.io` (branch `main`)

## Cập nhật code

Khi muốn update script mới nhất từ `duyvinh09/Module_IOS` + `sub-store-org/Sub-Store`:
1. Chạy lại build script ở máy local: `bun run scripts/build-aio.ts --force`
2. Copy đè `public/all-in-one.js` vào repo
3. Commit & push — Shadowrocket sẽ tự tải bản mới (jsDelivr cache ~10 phút).

## Tác giả & nguồn

- Module by: **mora_23099**
- Sub-Store: [sub-store-org/Sub-Store](https://github.com/sub-store-org/Sub-Store)
- Repack self-hosted by Z.ai

## Lưu ý

Đây là module cá nhân. Vui lòng không bán hoặc phân phối trái phép. Tuân thủ điều khoản của các ứng dụng.
