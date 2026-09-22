# LAB_AT_BMHTTT
# LAB3 - Nhận diện và ứng phó các mối đe dọa đến ATTT

Họ tên: Hoàng Minh Thắng
MSSV: 1150080116
Lab: Lab 3 - Nhận diện và ứng phó các mối đe dọa đến an toàn thông tin

## 1. Phiên bản môi trường thực hành
- Windows 11 Pro, Version 25H2 (OS Build 26200.9457)

## 2. Cách dựng môi trường
- Tạo VM Windows 11 25H2 x64 trên VMware Workstation: 2 vCPU, 6GB RAM, 64GB đĩa.
- Network Adapter: tạm dùng NAT để cài đặt công cụ và Windows Update, 
  sau đó chuyển về Host-only theo yêu cầu bài lab.
- Cài đặt: Windows Update đầy đủ, VMware Tools, Python 3.14.7, 
  Wireshark 4.6.8 (+ Npcap).
- Tải bộ Sysinternals (Sysmon, Autoruns, Process Explorer) từ 
  download.sysinternals.com.
- Giải nén gói LAB3_Threats_Assets.zip vào C:\LAB3, kiểm tra SHA-256 
  trước khi giải nén.
- Tạo snapshot LAB3_CLEAN_20260914 trước khi bắt đầu các tình huống.

## 3. Các tình huống đã thực hiện
- [ ] TH1 - Vulnerability/Threat/Risk/Attack + phân loại 5 nguồn đe dọa
- [ ] TH2 - Malware (EICAR)
- [ ] TH3 - Tấn công mật khẩu / keylogging
- [ ] TH4 - Backdoor (persistence + listener)
- [ ] TH5 - Sniffing/MITM/Spoofing (HTTP vs HTTPS)
- [ ] TH6 - DoS/DDoS/Mail bombing
- [ ] TH7 - Social Engineering/Phishing

## 4. Kết quả PASS/FAIL
| Tình huống | Kết quả | Ghi chú |
|---|---|---|
| TH1 |pass | |
| TH2 | FAIL| |
| TH3 |FAIL| |
| TH4 |FAIL | |
| TH5 | FAIL| |
| TH6 | FAIL| |
| TH7 | FAIL| |

## 5. Lỗi gặp phải và cách khắc phục
- Lỗi: sau khi cài Windows, mạng Host-only không có Internet để tải 
  công cụ. → Khắc phục: tạm chuyển Network Adapter sang NAT để cài đặt, 
  sau đó chuyển lại Host-only.
- Lỗi: màn hình cài Windows yêu cầu bắt buộc đăng nhập Microsoft account. 
  → Khắc phục: dùng lệnh `start ms-cxh:localonly` (Shift+F10 mở cmd) để 
  tạo local account.
- Lỗi: copy-paste lệnh PowerShell từ tài liệu vào VM bị mất ký tự 
  (dấu `\`, `;`), gây lỗi tạo sai đường dẫn thư mục C:\LAB3. 
  → Khắc phục: gõ tay từng lệnh thay vì paste khối lệnh dài, hoặc paste 
  từng dòng ngắn riêng lẻ.
