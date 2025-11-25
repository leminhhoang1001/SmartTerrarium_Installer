# 🌿 Smart Terrarium - Web Installer

![GitHub Pages](https://img.shields.io/badge/Deployment-GitHub%20Pages-blue?style=flat-square&logo=github)
![Platform](https://img.shields.io/badge/Platform-ESP32-green?style=flat-square&logo=espressif)
![License](https://img.shields.io/badge/License-MIT-orange?style=flat-square)

<div align="center">
  <h3>
    <a href="#-tiếng-việt">🇻🇳 Tiếng Việt</a> | <a href="#-english">🇺🇸 English</a>
  </h3>
</div>

---

<a name="-tiếng-việt"></a>
## 🇻🇳 Tiếng Việt

Chào mừng đến với trang cài đặt tự động của dự án **Smart Terrarium**. Đây là công cụ giúp bạn nạp phần mềm (Firmware) cho mạch ESP32 trực tiếp từ trình duyệt web mà không cần cài đặt phần mềm lập trình phức tạp.

👉 **TRUY CẬP TRANG CÀI ĐẶT TẠI ĐÂY:** [Link GitHub Pages của bạn]
*(Ví dụ: https://leminhhoang1001.github.io/SmartTerrarium_Installer/smartterra-installer)*

### 📖 Giới Thiệu Dự Án
**Smart Terrarium** là hệ thống AIoT chuyên nghiệp để chăm sóc bể bán cạn, Vivarium hoặc Paludarium.

#### 1. Giao Diện & Điều Khiển
- **Web Dashboard:** Truy cập qua `http://smartsystemterrarium.local`.
- **Đa Ngôn Ngữ:** Hỗ trợ Tiếng Việt & Tiếng Anh.
- **Chế độ Kép:** Tự động (Auto) hoàn toàn hoặc Thủ công (Manual) có khóa an toàn.

#### 2. Logic Tự Động Hóa
- **Môi trường:** Tự động cân bằng Nhiệt độ/Độ ẩm bằng Quạt và Phun sương.
- **Ánh sáng:** Mô phỏng bình minh/hoàng hôn (Dimming/Fading) mượt mà.
- **Mưa:** Lập lịch phun mưa tự động, thông minh tự ngắt nếu dự báo thời tiết có mưa thật.

#### 3. Kết Nối Dễ Dàng (WiFi Provisioning)
- Không cần sửa code để nhập mật khẩu WiFi.
- Khi mới mua về hoặc đổi mạng, thiết bị tự phát WiFi để bạn cấu hình qua điện thoại.

### 🛠️ Yêu Cầu Phần Cứng

| Linh kiện | Số lượng | Ghi chú |
| :--- | :---: | :--- |
| **ESP32 DevKit V1** | 1 | Vi điều khiển trung tâm |
| **Cảm biến DHT22** | 1 | Đo nhiệt độ & độ ẩm |
| **Module Relay** | 2 | Điều khiển Bơm Mưa & Phun Sương |
| **Module MOSFET** | 4 | Điều khiển tốc độ Quạt & Độ sáng Đèn |
| **Nguồn 12V DC** | 1 | Cấp nguồn toàn hệ thống |

### 🔌 Sơ Đồ Kết Nối (Pinout)

Kết nối các chân GPIO của ESP32 với các module như sau:

| GPIO | Thiết Bị | Loại Module | Ghi chú |
| :---: | :--- | :--- | :--- |
| **25** | Cảm biến DHT22 | Sensor | Chân Data |
| **32** | Bơm Mưa (Rain) | Relay | Mức thấp (Active LOW) |
| **33** | Phun Sương (Mist) | Relay | Mức thấp (Active LOW) |
| **13** | Đèn Trắng (White) | MOSFET | Điều khiển sáng/tối (PWM) |
| **18** | Đèn Tím/UV (Purple) | MOSFET | Điều khiển sáng/tối (PWM) |
| **26** | Quạt Hút (Fan In) | MOSFET | Điều chỉnh tốc độ (PWM) |
| **27** | Quạt Thổi (Fan Out) | MOSFET | Điều chỉnh tốc độ (PWM) |

### 🚀 Hướng Dẫn Nạp Phần Mềm (Flash)

**Lưu ý:** Vui lòng sử dụng trình duyệt **Google Chrome**, **Microsoft Edge** hoặc **Opera** trên máy tính (Windows/Mac/Linux).

1.  **Kết nối:** Cắm mạch ESP32 vào máy tính qua cáp USB.
2.  **Truy cập:** Vào đường link trang cài đặt (ở đầu bài viết).
3.  **Bắt đầu:** Nhấn nút **"KẾT NỐI & CÀI ĐẶT"** (hoặc "CONNECT").
4.  **Chọn cổng:** Một cửa sổ hiện ra, chọn cổng COM (Serial Port) của mạch ESP32 và nhấn **Connect**.
5.  **Cài đặt:** Chọn **"INSTALL SMART TERRARIUM"** và chờ quá trình hoàn tất (khoảng 2 phút).

> **Sau khi nạp xong:**
> 1. Thiết bị sẽ phát WiFi tên: `SmartTerrarium_Setup`.
> 2. Kết nối điện thoại vào WiFi đó để cài đặt WiFi nhà bạn.
> 3. Sau khi kết nối xong, truy cập `http://smartsystemterrarium.local` để sử dụng.

---
---

<a name="-english"></a>
## 🇺🇸 English

Welcome to the **Smart Terrarium Web Installer**. This tool allows you to flash the firmware directly to your ESP32 board from your web browser, eliminating the need for complex IDE installations.

👉 **ACCESS INSTALLER HERE:** [Your GitHub Pages Link]
*(E.g., https://leminhhoang1001.github.io/SmartTerrarium_Installer/smartterra-installer)*

### 📖 Project Overview
**Smart Terrarium** is a professional AIoT system designed for automated care of Terrariums, Vivariums, or Paludariums.

#### 1. Interface & Control
- **Web Dashboard:** Accessible via `http://smartsystemterrarium.local`.
- **Bilingual:** Full support for English & Vietnamese.
- **Dual Modes:** Fully Automatic or Manual Override with safety timeout features.

#### 2. Automation Logic
- **Climate:** Automatically balances Temperature/Humidity using Fans and Mist makers.
- **Lighting:** Smooth Day/Night simulation (Dimming/Fading).
- **Rain:** Scheduled rain cycles with "Smart Delay" (pauses if real rain is forecast via API).

#### 3. Easy Connectivity (WiFi Provisioning)
- No hardcoding required.
- On first use or network change, the device broadcasts a WiFi hotspot for easy configuration via phone.

### 🛠️ Hardware Requirements

| Component | Qty | Note |
| :--- | :---: | :--- |
| **ESP32 DevKit V1** | 1 | Main Controller |
| **DHT22 Sensor** | 1 | Temp & Humidity |
| **Relay Module** | 2 | For Rain Pump & Mist Maker |
| **MOSFET Module** | 4 | PWM for Fans & LEDs |
| **12V DC Supply** | 1 | System Power |

### 🔌 Wiring Diagram (Pinout)

Connect ESP32 GPIO pins to your modules as follows:

| GPIO | Device | Module Type | Note |
| :---: | :--- | :--- | :--- |
| **25** | DHT22 Sensor | Sensor | Data Pin |
| **32** | Rain Pump | Relay | Active LOW |
| **33** | Mist Maker | Relay | Active LOW |
| **13** | White LED | MOSFET | PWM Dimming |
| **18** | UV/Purple LED | MOSFET | PWM Dimming |
| **26** | Fan In | MOSFET | PWM Speed Control |
| **27** | Fan Out | MOSFET | PWM Speed Control |

### 🚀 Flashing Instructions

**Note:** Please use **Google Chrome**, **Microsoft Edge**, or **Opera** on a Desktop (Windows/Mac/Linux).

1.  **Connect:** Plug your ESP32 board into your computer via USB.
2.  **Access:** Open the Installer Link (provided at the top).
3.  **Start:** Click the **"CONNECT & INSTALL"** button.
4.  **Select Port:** A popup will appear. Select your ESP32's COM Port and click **Connect**.
5.  **Install:** Select **"INSTALL SMART TERRARIUM"** and wait for the process to finish (~2 minutes).

> **After Flashing:**
> 1. The device will broadcast a WiFi named: `SmartTerrarium_Setup`.
> 2. Connect your phone to this WiFi to configure your home network credentials.
> 3. Once connected, access `http://smartsystemterrarium.local` to start using the system.

---

<div align="center">
  <p>Developed with ❤️ by Luc4sL3e</p>
  <p>
    <a href="[Link to Source Code Repo]">View Source Code</a>
  </p>
</div>
