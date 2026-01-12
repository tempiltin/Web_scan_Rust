# Kuchli Web Scanner — GUI Desktop ilova (Rust + Tauri)

Kuchli Web Scanner — bu Rust va Tauri yordamida yaratilgan, zamonaviy veb-ilovalarni tezda tekshirish va skanerlash uchun mo'ljallangan GUI desktop dasturi. Ilova tez, xavfsiz va mahalliy (native) tajriba taqdim etadi: Rust ishlovchi qismi yuqori samaradorlik va xavfsizlikni ta'minlaydi, frontend esa Tauri orqali chiroyli va yengil grafik interfeys bilan birlashadi.

**Asosiy maqsad**: Web-ilovalarning ochiq va ma'lum bo'lgan zaifliklarini avtomatlashtirilgan tarzda aniqlash va natijalarni qulay GUI orqali ko'rsatish.

**Xususiyatlar**
- **Interfeys**: Cross-platform Tauri GUI (Windows, macOS, Linux).
- **Tezlik va barqarorlik**: Ilg'or Rust backend yordamida yuqori tezlikli tarmoq operatsiyalari.
- **Ko'p turdagi tekshiruvlar**: port skan, HTTP/HTTPS endpoint tahlil, basic header/fingerprint, common vulnerability checks (misol: misconfigured headers, exposed directories), va sozlanadigan skriptlar.
- **Raport va eksport**: HTML yoki JSON formatida hisobot yaratish.
- **Konfiguratsiya**: foydalanish oson sozlamalar paneli va profiling.
- **Mas'uliyat va xavfsizlik**: faqat ma'qullangan va huquqiy skanerlash uchun mo'ljallangan — foydalanish qoidalari bilan.

Skrinshotlar
- (Skrinshotlarni `assets/screenshots/` papkasiga joylang va shu yerga bog'lang.)

Talablar
- Rust (stable) va `cargo` (Rust toolchain): tavsiya etiladi `rustup` orqali o'rnatish.
- Node.js (v16+): frontend qaramliklarni o'rnatish uchun (agar frontend Node asosida bo'lsa).
- Tauri CLI (maqsadga muvofiq): `cargo install tauri-cli` yoki `npm i -g @tauri-apps/cli` (Tauri versiyasiga mos ravishda).
- Platformaga mos build toolchain (Linux uchun build-essential, macOS uchun Xcode Command Line Tools, Windows uchun MSVC/Visual Studio).

O'rnatish (manba koddan)
1. Repozitoriyani klonlang:

```bash
git clone https://github.com/tempiltin/Web_scan_Rust.git
cd Web_scan_Rust
```

2. Rust vositalarini o'rnating (agar yo'q bo'lsa):

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update stable
```

3. Node va frontend qaramliklarini o'rnating (agar frontend mavjud bo'lsa):

```bash
# Node o'rnatilgach
npm install
# yoki
yarn install
```

4. Tauri CLI (zarur bo'lsa):

```bash
cargo install tauri-cli
# yoki npm orqali
npm i -g @tauri-apps/cli
```

Ishlatish — rivojlantirish rejimi

```bash
# frontend dev server ishga tushgach (misol uchun npm run dev)
npm run tauri dev
# yoki
yarn tauri dev
```

Release build

```bash
# frontend build qilinadi, so'ngra Tauri yordamida native build
npm run build
npm run tauri build
```

Qo'llanma va foydalanish
- Ilovani ishga tushiring va "New Scan" yoki shunga o'xshash tugma orqali yangi scanning ishini boshlang.
- Maqsad URL yoki IP diapazonini kiriting, scanning profilini (tezkor, chuqur va boshq.) tanlang.
- Skanni ishga tushiring va natijalarni GUI orqali kuzating; kerak bo'lsa, hisobotni eksport qiling.

Konfiguratsiya
- Ilovaning `config/` papkasida (yoki `tauri.conf.json`) sozlamalar mavjud bo'lishi mumkin. Bu fayllar orqali default skan parametrlarini, eksporter sozlamalarini va log darajasini o'zgartirish mumkin.

Xavfsizlik va etik me'yorlar
- Ushbu vosita kuchli skanerlash imkoniyatiga ega — uni faqat o'zingizga tegishli tizimlar yoki yozma ruxsat olingan tizimlar uchun ishlating.
- Noqonuniy skanerlash qonuniy muammolarga olib kelishi mumkin; doimo tegishli ruxsatnomalarni oling.

Xatoliklar va yordam
- Muammolarni yoki xatoliklarni GitHub Issues sahifasida bildiring.

Hissa qo'shish
- Kontributsiya qoidalari:
	- Fork qiling, yangi branch oching (`feature/your-feature`), o'zgartirishlarni commit qiling va pull request yuboring.
	- Kod standartlari va testlar qo'llanilsa, ularni bajaring.

Litsenziya
- Loyihaning asosiy litsenziyasi: MIT (yoki siz tanlagan boshqa litsenziyani shu yerga yozing).

Muallif va aloqa
- Muallif: tempiltin (GitHub: https://github.com/tempiltin)
- Elektron pochta yoki boshqa aloqa usuli uchun README yoki repo profilingizda ko'rsating.

Qo'shimcha eslatma
- README ichidagi ba'zi buyruqlar va skriptlar sizning repoingizdagi `package.json` va `tauri.conf.json` ga bog'liq. Agar frontend yoki build skriptlari boshqa nomda bo'lsa, mos ravishda komandalarni o'zgartiring.

Rahmat — xavfsiz va mas'uliyatli skanerlashni unutmang.
