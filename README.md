# 💜 Netra Panel

<p align="center">
  <img src="https://img.shields.io/badge/Cloudflare-Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Cloudflare Workers"> <img src="https://img.shields.io/badge/Cloudflare-Warp-orange?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Warp"><br>
  <img src="https://img.shields.io/badge/Protocol-VLESS-00ADD8?style=for-the-badge&logo=v&logoColor=white" alt="VLESS"> <img src="https://img.shields.io/badge/Protocol-Trojan-00ADD8?style=for-the-badge&logo=trojan&logoColor=white" alt="Trojan"><br>
  <img src="https://img.shields.io/badge/Fragment-Anti--Filtering-blueviolet?style=for-the-badge" alt="Fragment"> <img src="https://img.shields.io/badge/Telegram-Installer%20Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Bot">
</p>

<p align="center">
  <strong>🇬🇧 English</strong> &nbsp;•&nbsp;
  <a href="#lang-fa">🇮🇷 فارسی</a> &nbsp;•&nbsp;
  <a href="#lang-ru">🇷🇺 Русский</a> &nbsp;•&nbsp;
  <a href="#lang-zh">🇨🇳 中文</a>
</p>

A free, self-hosted VLESS / Trojan proxy panel that runs entirely on **Cloudflare Workers**.

---

### Netra Panel

A free, self-hosted VLESS / Trojan proxy panel that runs entirely on **Cloudflare Workers**. No VPS. No server maintenance. No monthly cost — deploy in minutes and manage everything from a clean web panel.

🤖 You can also install it easily using our **Telegram installer bot**: [@irNetra_bot](https://t.me/irNetra_bot).

[Report a Bug](https://github.com/netrair/issues) · [Request a Feature](https://github.com/netrair/issues) · [Telegram Support](https://t.me/NetraIR)

---

### ✨ Features

* ⚡ **Runs on Cloudflare Workers** — no VPS, no Docker, no server to patch or reboot
* **VLESS & Trojan** protocol support out of the box
* **Warp / Warp Pro** integration for extra routing options
* **Subscription links** for Xray-core, sing-box, Clash, and WireGuard-based clients (v2rayNG, Streisand, Clash Meta, Hiddify, NekoBox, and more)
* ️ **Fragment & noise settings** to help traffic blend in on restrictive networks
* ️ **Full web panel** — manage everything (UUID, password, ports, DNS, routing rules, bypass/block lists) without touching code
* **One-click deploy** — works with sensible defaults right after deployment, no separate setup wizard required
* **Optional panel password** — protect your panel, or skip it if you're the only one with the URL

---

### Deploy

1. Click **Deploy to Cloudflare Workers**, or manually create a new Worker in your [Cloudflare dashboard](https://dash.cloudflare.com).
2. Paste the contents of `worker.js` into the Worker editor and deploy.
3. In the Cloudflare dashboard, go to the **Storage & Databases** section and create a new **Workers KV** namespace (any name you like).
4. Go back to your Worker → **Settings → Bindings**, click **Add binding → KV Namespace**, select the KV namespace you just created, and set its **variable name to `kv`**. This name must be exactly `kv` — nothing else.
5. Open your Worker's URL and make sure to add **`/panel`** at the very end of the address (e.g. `https://your-worker.workers.dev/panel`) to open the panel. On first visit you'll be prompted to set a panel password (or skip it).

That's it — the panel works immediately with built-in defaults. You can customize everything (UUID, Trojan password, secure path, ports, routing rules, etc.) from inside the panel afterward.

> ⚠️ **Warning:** If you don't add a **KV Namespace** binding with the variable name **exactly `kv`**, your Worker will throw a **1101 error** and the panel won't work.

---

### Security notes

* If you choose **Skip password**, anyone with your Worker URL can access the panel. Only do this for a private/testing deployment.
* Change the default UUID/Trojan password/secure path from the panel before sharing your subscription link with anyone.
* Treat your Worker URL like a secret — it's the entry point to your panel.

---

### Support

Questions or issues? Reach out on Telegram: **[@NetraIR](https://t.me/NetraIR)**

---

<details>
<summary><strong>🇮🇷 فارسی</strong></summary>
<a id="lang-fa"></a>

### پنل Netra

یک پنل پروکسی VLESS / Trojan رایگان و خودمیزبان که کاملاً روی **Cloudflare Workers** اجرا می‌شه. بدون نیاز به VPS، بدون نگهداری سرور، بدون هزینه‌ی ماهانه — در چند دقیقه دیپلوی کنید و همه‌چیز رو از یک پنل تمیز مدیریت کنید.

🤖 همچنین می‌تونید با **بات نصب‌کننده‌ی تلگرام** [@irNetra_bot](https://t.me/irNetra_bot) به‌سادگی و بدون دردسر نصب کنید.

[گزارش باگ](https://github.com/netrair/issues) · [درخواست ویژگی جدید](https://github.com/netrair/issues) · [پشتیبانی تلگرام](https://t.me/NetraIR)

---

#### ✨ ویژگی‌ها

* ⚡ **کاملاً روی Cloudflare Workers اجرا می‌شه** — بدون VPS، بدون Docker، بدون سروری که نیاز به آپدیت یا ری‌استارت داشته باشه
* پشتیبانی از پروتکل‌های **VLESS** و **Trojan**
* پشتیبانی از **Warp / Warp Pro** برای مسیرهای اضافی
* لینک سابسکریپشن برای کلاینت‌های Xray-core، sing-box، Clash و WireGuard (مثل v2rayNG، Streisand، Clash Meta، Hiddify، NekoBox و...)
* ️ تنظیمات Fragment و نویز برای عبور بهتر از فیلترینگ‌های سخت‌گیرانه
* ️ **پنل وب کامل** — همه‌چیز (UUID، پسورد، پورت‌ها، DNS، قوانین مسیریابی، لیست‌های bypass/block) بدون نیاز به دست‌زدن به کد قابل مدیریته
* **دیپلوی با یک کلیک** — بلافاصله بعد از دیپلوی با مقادیر پیش‌فرض کار می‌کنه، بدون نیاز به Wizard جداگانه
* **رمز پنل اختیاریه** — می‌تونید پنل رو با رمز محافظت کنید یا اگه فقط خودتون آدرسش رو دارید، ردش کنید

---

#### نصب و دیپلوی

1. روی دکمه‌ی **Deploy to Cloudflare Workers** بزنید، یا یک Worker جدید توی [داشبورد Cloudflare](https://dash.cloudflare.com) بسازید.
2. محتوای فایل `worker.js` رو کپی و توی ویرایشگر Worker جای‌گذاری و دیپلوی کنید.
3. توی داشبورد Cloudflare، وارد بخش **Storage & Databases** بشید و یک **Workers KV** جدید بسازید (اسمش هرچی دوست دارید باشه).
4. برگردید توی صفحه‌ی Worker خودتون → **Settings → Bindings**، روی **Add binding → KV Namespace** بزنید، همون KV که ساختید رو انتخاب کنید و **نام وریبل (Variable name) رو `kv`** بذارید. این اسم حتماً باید دقیقاً `kv` باشه، چیز دیگه‌ای قبول نیست.
5. آدرس Worker خودتون رو باز کنید و حتماً در **انتهای آدرس Worker**، عبارت **`/panel`** رو اضافه کنید (مثلاً `https://your-worker.workers.dev/panel`) تا پنل باز بشه. بار اول ازتون خواسته می‌شه یک رمز برای پنل تعیین کنید یا ردش کنید.

همین! پنل بلافاصله با تنظیمات پیش‌فرض کار می‌کنه. بعداً می‌تونید همه‌چیز (UUID، پسورد Trojan، مسیر امن، پورت‌ها، قوانین مسیریابی و...) رو از داخل پنل شخصی‌سازی کنید.

> ⚠️ **هشدار:** اگه در بخش **Binding**، یک **KV namespace** با نام دقیقاً **`kv`** اضافه نکنید، Worker شما خطای **1101** می‌ده و پنل کار نمی‌کنه.

---

#### نکات امنیتی

* اگه گزینه‌ی **Skip password** رو بزنید، هر کسی که آدرس Workerتون رو داشته باشه می‌تونه وارد پنل بشه. این کار رو فقط برای دیپلوی شخصی/تستی بدید.
* قبل از اشتراک‌گذاری لینک سابسکریپشن، UUID/پسورد Trojan/مسیر امن پیش‌فرض رو از پنل عوض کنید.
* با آدرس Workerتون مثل یک اطلاعات محرمانه رفتار کنید — این آدرس دروازه‌ی ورود به پنلتونه.

---

#### 🎬 ویدیو آموزشی

* [آموزش نصب و راه‌اندازی (۱)](https://youtu.be/zhOt8fyHPQE)
* [آموزش نصب و راه‌اندازی (۲)](https://youtu.be/JDDL-gwUkMc)
 
---

#### پشتیبانی

سوال یا مشکلی دارید؟ توی تلگرام پیام بدید: **[@NetraIR](https://t.me/NetraIR)**

</details>

---

<details>
<summary><strong>🇷🇺 Русский</strong></summary>
<a id="lang-ru"></a>

### Netra Panel

Бесплатная self-hosted панель для прокси VLESS / Trojan, которая полностью работает на **Cloudflare Workers**. Без VPS. Без обслуживания сервера. Без ежемесячной платы — разверните за пару минут и управляйте всем через удобную веб-панель.

🤖 Также можно установить панель через нашего **Telegram-бота для установки**: [@irNetra_bot](https://t.me/irNetra_bot).

[Сообщить об ошибке](https://github.com/netrair/issues) · [Предложить функцию](https://github.com/netrair/issues) · [Поддержка в Telegram](https://t.me/NetraIR)

---

#### ✨ Возможности

* ⚡ **Работает на Cloudflare Workers** — не нужен VPS, Docker или обслуживание сервера
* Поддержка протоколов **VLESS и Trojan** из коробки
* Интеграция с **Warp / Warp Pro** для дополнительных маршрутов
* **Ссылки подписки** для Xray-core, sing-box, Clash и WireGuard-клиентов (v2rayNG, Streisand, Clash Meta, Hiddify, NekoBox и др.)
* ️ Настройки **Fragment и noise** для лучшего обхода жёсткой фильтрации трафика
* ️ **Полноценная веб-панель** — управляйте всем (UUID, пароль, порты, DNS, правила маршрутизации, списки bypass/block) без изменения кода
* **Развёртывание в один клик** — работает с готовыми настройками сразу после деплоя, отдельный мастер настройки не требуется
* **Пароль панели — по желанию** — защитите панель паролем или пропустите этот шаг, если только у вас есть ссылка

---

#### Установка

1. Нажмите **Deploy to Cloudflare Workers** или создайте новый Worker вручную в [панели Cloudflare](https://dash.cloudflare.com).
2. Вставьте содержимое файла `worker.js` в редактор Worker и разверните его.
3. В панели Cloudflare перейдите в раздел **Storage & Databases** и создайте новое пространство **Workers KV** (имя может быть любым).
4. Вернитесь в настройки Worker → **Settings → Bindings**, нажмите **Add binding → KV Namespace**, выберите созданный KV и укажите **имя переменной `kv`**. Имя обязательно должно быть точно `kv`.
5. Откройте URL вашего Worker и обязательно добавьте **`/panel`** в самый конец адреса (например, `https://your-worker.workers.dev/panel`), чтобы открыть панель. При первом входе будет предложено задать пароль панели (или пропустить этот шаг).

Готово — панель сразу работает со встроенными значениями по умолчанию. Позже вы сможете настроить всё (UUID, пароль Trojan, секретный путь, порты, правила маршрутизации и т.д.) прямо в панели.

> ⚠️ **Предупреждение:** если в разделе **Bindings** вы не добавите **KV namespace** с именем ровно **`kv`**, ваш Worker выдаст **ошибку 1101**, и панель не будет работать.

---

#### Заметки по безопасности

* Если выбрать **Skip password**, любой, у кого есть ссылка на ваш Worker, сможет открыть панель. Используйте это только для личного/тестового развёртывания.
* Перед тем как делиться ссылкой подписки, измените в панели стандартный UUID/пароль Trojan/секретный путь.
* Относитесь к URL вашего Worker как к секретной информации — это точка входа в вашу панель.

---

#### Поддержка

Вопросы или проблемы? Пишите в Telegram: **[@NetraIR](https://t.me/NetraIR)**

</details>

---

<details>
<summary><strong>🇨🇳 中文</strong></summary>
<a id="lang-zh"></a>

### Netra Panel

一个完全运行在 **Cloudflare Workers** 上的免费自托管 VLESS / Trojan 代理面板。无需 VPS，无需维护服务器，无需每月付费 —— 几分钟内即可部署完成，通过简洁的网页面板管理一切。

🤖 你也可以使用我们的 **Telegram 安装机器人**：[@irNetra_bot](https://t.me/irNetra_bot) 轻松完成安装。

[提交 Bug](https://github.com/netrair/issues) · [功能建议](https://github.com/netrair/issues) · [Telegram 支持](https://t.me/NetraIR)

---

#### ✨ 功能特点

* ⚡ **完全运行在 Cloudflare Workers 上** —— 无需 VPS、Docker，也无需维护或重启服务器
* 开箱即用支持 **VLESS 和 Trojan** 协议
* 集成 **Warp / Warp Pro**，提供更多路由选择
* 为 Xray-core、sing-box、Clash 和 WireGuard 客户端提供**订阅链接**（v2rayNG、Streisand、Clash Meta、Hiddify、NekoBox 等）
* ️ **Fragment 与噪声设置**，帮助流量更好地绕过严格的网络封锁
* ️ **完整的网页面板** —— 无需接触代码即可管理一切（UUID、密码、端口、DNS、路由规则、绕过/屏蔽列表）
* **一键部署** —— 部署后立即使用内置默认配置即可运行，无需单独的设置向导
* **面板密码可选** —— 可为面板设置密码保护，若只有你自己掌握链接，也可以跳过

---

#### 部署方法

1. 点击 **Deploy to Cloudflare Workers**，或前往你的 [Cloudflare 控制台](https://dash.cloudflare.com) 手动创建一个新的 Worker。
2. 将 `worker.js` 的内容复制并粘贴到 Worker 编辑器中，然后部署。
3. 在 Cloudflare 控制台中，进入 **Storage & Databases** 部分，创建一个新的 **Workers KV**（名称随意）。
4. 返回你的 Worker 页面 → **Settings → Bindings**，点击 **Add binding → KV Namespace**，选择刚创建的 KV，并将**变量名称设置为 `kv`**。这个名字必须精确为 `kv`，不能是其他名字。
5. 打开你的 Worker 地址，并务必在**地址最末尾**加上 **`/panel`**（例如 `https://your-worker.workers.dev/panel`）以打开面板。首次访问时会提示你设置面板密码（也可以选择跳过）。

就这么简单 —— 面板会立即使用内置默认配置正常运行。之后你可以在面板内自行自定义所有设置（UUID、Trojan 密码、安全路径、端口、路由规则等）。

> ⚠️ **警告：** 如果你没有在 **Bindings** 部分添加变量名精确为 **`kv`** 的 **KV namespace** 绑定，你的 Worker 将会报 **1101 错误**，面板将无法使用。

---

#### 安全提示

* 如果选择 **Skip password（跳过密码）**，任何拥有你 Worker 地址的人都可以访问面板。请仅在个人/测试部署时使用此选项。
* 在分享订阅链接前，请务必在面板中修改默认的 UUID / Trojan 密码 / 安全路径。
* 请像对待机密信息一样对待你的 Worker 地址 —— 它是进入你面板的入口。

---

#### 🎬 教学视频

* [安装与部署教程](https://youtu.be/TiYE2SF_bwA)

## 📚 中文教程

[完整图文部署教程](https://www.zoio.net/2026/08/netra-panel.html)
---

#### 获取支持

有问题或遇到故障？请通过 Telegram 联系：**[@NetraIR](https://t.me/NetraIR)**

</details>

---

Made with ❤️ for a freer internet.

---
> UI Idea inspired by [BPB-Worker-Panel](https://github.com/bia-pain-bache/BPB-Worker-Panel).
>
> .
