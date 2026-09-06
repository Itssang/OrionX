<div align="center">

<img src="https://raw.githubusercontent.com/Itssang/OrionX/main/Information/Logo.png" width="150" alt="OrionX Avatar"/>

# 〄 OrionX Discord Bot

**Bot Discord Economy dành cho cộng đồng Việt Nam**

[![Discord](https://img.shields.io/badge/Discord-Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://dsc.gg/itssang)
[![GitHub](https://img.shields.io/badge/GitHub-Open%20Source-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Itssang/OrionX)
[![Owner](https://img.shields.io/badge/Made%20in-Itssang-DA251D?style=for-the-badge)](https://github.com/Itssang)

<img src="https://raw.githubusercontent.com/ItssangX/OrionX/main/OrionX%20Banner%20GIf.gif" width="600" alt="OrionX Banner"/>

</div>

---

## 📌 Giới thiệu

**OrionX** là một Discord Bot đa năng được phát triển bởi **Nguyen Hoang Sang**, được thiết kế để phục vụ cộng đồng Discord Việt Nam. Dự án được công khai mã nguồn với mong muốn các developer bot tại Việt Nam có thể học hỏi, cải tiến và cùng nhau phát triển ngành dev bot Discord ngày càng lớn mạnh hơn.

> 💡 **Mục tiêu:** Góp phần xây dựng một cộng đồng dev bot Discord Việt Nam vững mạnh — nơi mọi người có thể tự do fork, chỉnh sửa và phát triển theo ý muốn.

---

## 🌟 Tính năng nổi bật

| Danh mục             | Mô tả                                       |
| -------------------- | ------------------------------------------- |
| 💰 **Xcoin Economy** | Hệ thống kinh tế nội bộ với đồng tiền Xcoin |
| 🛡️ **Moderation**    | Quản lý server: ban, kick, mute, warn...    |
| 🎮 **Mini Games**    | Các trò chơi giải trí trong Discord         |
| 📊 **Leveling**      | Hệ thống cấp độ & kinh nghiệm (XP)          |
| 🎵 **Music**         | Phát nhạc từ YouTube / Spotify              |
| 🔧 **Utility**       | Các lệnh tiện ích đa năng                   |

---

## 🚀 Cài đặt & Chạy Bot

### Yêu cầu hệ thống

- [Node.js](https://nodejs.org/) `v18.0.0` trở lên
- [npm](https://www.npmjs.com/) hoặc [yarn](https://yarnpkg.com/)
- Discord Bot Token (lấy tại [Discord Developer Portal](https://discord.com/developers/applications))

### Các bước cài đặt

**1. Clone repository**

```bash
git clone https://github.com/Itssang/OrionX.git
cd OrionX
```

**2. Cài đặt dependencies**

```bash
npm install
```

**3. Cấu hình bot**

Vào folder `OrionX File`, tìm file cấu hình và điền thông tin của bạn:

```env
TOKEN=your_discord_bot_token_here
CLIENT_ID=your_client_id_here
GUILD_ID=your_guild_id_here
PREFIX=!
```

**4. Deploy Slash Commands (nếu có)**

```bash
node deploy-commands.js
```

**5. Khởi động bot**

```bash
node index.js
```

hoặc dùng `nodemon` để auto-restart khi phát triển:

```bash
npx nodemon index.js
```

---

## 📁 Cấu trúc thư mục

```
OrionX/
├── 📂 OrionX/              # Mã nguồn chính của bot
│   ├── commands/           # Các lệnh của bot
│   ├── events/             # Xử lý sự kiện Discord
│   ├── handlers/           # Handler cho commands & events
│   └── index.js            # File khởi động chính
├── 📂 OrionX File/         # File cấu hình & dữ liệu
├── 🖼️ Orion Avatar.png     # Avatar bot
├── 🖼️ Orion Banner.png     # Banner bot
├── 💰 Xcoin.png            # Icon đồng tiền Xcoin
└── 📄 README.md
```

---

## 💰 Hệ thống Xcoin

<div align="center">
  <img src="https://raw.githubusercontent.com/Itssang/OrionX/main/Information/Xcoin.png" width="80" alt="Xcoin"/>
</div>

**Xcoin** là đồng tiền ảo nội bộ của OrionX, cho phép người dùng:

- 💵 Kiếm Xcoin qua các hoạt động hàng ngày
- 🛒 Mua vật phẩm trong cửa hàng server
- 🎰 Tham gia mini-games để nhân đôi Xcoin
- 🏆 Cạnh tranh trên bảng xếp hạng giàu nhất server

---

## 🔧 Tùy chỉnh & Phát triển

OrionX được thiết kế để dễ dàng tùy chỉnh. Dưới đây là một số gợi ý:

### Thêm lệnh mới

```javascript
// commands/ten-lenh.js
const { SlashCommandBuilder } = require("discord.js");

module.exports = {
  data: new SlashCommandBuilder()
    .setName("ten-lenh")
    .setDescription("Mô tả lệnh của bạn"),
  async execute(interaction) {
    await interaction.reply("Hello từ lệnh mới!");
  },
};
```

### Thêm sự kiện mới

```javascript
// events/ten-event.js
const { Events } = require("discord.js");

module.exports = {
  name: Events.MessageCreate,
  async execute(message) {
    // Xử lý sự kiện tại đây
  },
};
```

---

## 🤝 Đóng góp cho dự án

Mình rất hoan nghênh mọi đóng góp từ cộng đồng! Đây là cách bạn có thể tham gia:

1. **Fork** repository này về tài khoản của bạn
2. **Tạo branch** mới: `git checkout -b feature/ten-tinh-nang`
3. **Commit** thay đổi: `git commit -m 'feat: thêm tính năng xyz'`
4. **Push** lên branch: `git push origin feature/ten-tinh-nang`
5. Tạo **Pull Request** và mô tả những gì bạn đã thêm

### Các loại đóng góp được chào đón:

- 🐛 Báo cáo & sửa lỗi
- ✨ Thêm tính năng mới
- 📝 Cải thiện tài liệu
- 🌐 Dịch thuật
- ⚡ Tối ưu hiệu năng

---

## 📜 Giấy phép

Dự án này được phát hành theo giấy phép **MIT** — bạn hoàn toàn tự do sử dụng, chỉnh sửa và phân phối lại, miễn là giữ nguyên thông tin tác giả gốc.

---

## 👨‍💻 Tác giả

<div align="center">

**ItssangX** / **Itssang**

[![GitHub](https://img.shields.io/badge/GitHub-Itssang-181717?style=flat-square&logo=github)](https://github.com/Itssang)

_"Hy vọng dự án này sẽ là bước đệm để cộng đồng dev bot Discord Việt Nam ngày càng phát triển mạnh mẽ hơn."_

</div>

---

## ⭐ Ủng hộ dự án

Nếu dự án này có ích cho bạn, hãy để lại một ⭐ **Star** trên GitHub nhé! Điều đó giúp dự án được nhiều người biết đến hơn và khích lệ mình tiếp tục phát triển.

<div align="center">

[![Star History](https://img.shields.io/github/stars/Itssang/OrionX?style=social)](https://github.com/Itssang/OrionX/stargazers)

**Cảm ơn bạn đã ghé thăm OrionX! 🚀**

<img src="https://raw.githubusercontent.com/Itssang/OrionX/main/Information/Logo.png" width="80" alt="OrionX"/>

</div>
