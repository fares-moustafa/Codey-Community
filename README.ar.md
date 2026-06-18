<div align="center" dir="rtl">

# مجتمع Codey

**المنصة الرسمية لإصدارات Codey وتحديثاته ومجتمع المطوّرين.**

[![أحدث إصدار](https://img.shields.io/github/v/release/fares-moustafa/Codey-Community?label=latest&color=orange)](https://github.com/fares-moustafa/Codey-Community/releases/latest)
[![التنزيلات](https://img.shields.io/github/downloads/fares-moustafa/Codey-Community/total?color=orange)](https://github.com/fares-moustafa/Codey-Community/releases)
[![الرخصة: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE)

[التثبيت](#-التثبيت) · [التحديث](#-البقاء-على-آخر-إصدار) · [التوثيق](./docs) · [خارطة الطريق](./ROADMAP.md) · [المساهمة](./CONTRIBUTING.md) · [English](./README.md)

</div>

---

<div dir="rtl">

## 🤖 ما هو Codey؟

**Codey** هو وكيل برمجة ذكي مبني للعمل من الطرفية (Terminal) — واجهة نصية سريعة تعتمد على لوحة المفاتيح، بالإضافة إلى تطبيق سطح مكتب يعمل على جميع المنصّات. يساعدك على قراءة الكود وكتابته وإعادة هيكلته، وتشغيل الأوامر، وإدارة الاختبارات، وتنفيذ المهام المتعددة الخطوات عبر **بروتوكول سياق النموذج (MCP)**.

هذا المستودع — **مجتمع Codey** — هو الواجهة العامة للمشروع، ويحتوي على:

- 📦 **الإصدارات** — كل نسخة من Codey (ملفات CLI التنفيذية + مثبّتات سطح المكتب) تُنشر هنا.
- 🔄 **التحديثات** — أداة التحديث الذاتي في CLI ومحدّث سطح المكتب كلاهما يتحقّق من هذا المستودع.
- 🐛 **المشاكل والملاحظات** — تقارير الأخطاء وطلبات الميزات.
- 💬 **النقاشات** — أسئلة وأجوبة، ومشاركة الأعمال، والأفكار.
- 📚 **التوثيق والمساهمات** — أدلة، وقوالب وكلاء، ومطالبات (prompts)، ومهارات، وسير عمل n8n.

> الكود المصدري لتطبيق Codey موجود في مستودع منفصل. هذا المستودع هو بوابة **التوزيع والمجتمع**.

---

## 📥 التثبيت

### تثبيت سريع (macOS / Linux / WSL)

```bash
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash
```

تثبيت نسخة محدّدة:

```bash
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash -s -- --version 3.5.1
```

### عبر مديري الحزم

```bash
# npm
npm install -g codey

# bun
bun install -g codey

# yarn
yarn global add codey

# Homebrew
brew install fares-moustafa/tap/codey
```

### الإصدارات الجاهزة (تطبيق سطح المكتب)

حمّل المثبّت المناسب لنظامك من صفحة [**الإصدارات**](https://github.com/fares-moustafa/Codey-Community/releases/latest):

| النظام | الملف |
| :--- | :--- |
| **macOS** (Apple Silicon) | `Codey-desktop-darwin-aarch64.dmg` |
| **macOS** (Intel) | `Codey-desktop-darwin-x86_64.dmg` |
| **Windows** | `Codey-desktop-windows-x86_64-setup.exe` |
| **Linux** | `Codey-desktop-linux-x86_64.AppImage` |

راجع [**docs/installation.md**](./docs/installation.md) لمعرفة كل طرق التثبيت.

---

## 🔄 البقاء على آخر إصدار

يحافظ Codey على تحديث نفسه تلقائيًا:

- **تحديث ذاتي لـ CLI** — عند التشغيل، يتحقّق Codey من هذا المستودع (أو npm / Homebrew حسب طريقة التثبيت) بحثًا عن نسخة أحدث ويمكنه الترقية تلقائيًا.
- **تحديث تلقائي لسطح المكتب** — يستخدم تطبيق سطح المكتب محدّث Tauri الموجّه إلى ملف `latest.json` في هذا المستودع.
- **ترقية يدوية**:

  ```bash
  codey upgrade            # الترقية إلى أحدث نسخة
  codey upgrade 3.5.1      # الترقية/الرجوع إلى نسخة محدّدة
  ```

سلوك التحديث قابل للضبط (`autoupdate`: `true` | `"notify"` | `false`)، ويمكن التراجع عن أي ترقية فاشلة. التفاصيل الكاملة في [**docs/updating.md**](./docs/updating.md).

---

## 📚 التوثيق

| الدليل | المحتوى |
| :--- | :--- |
| [البدء السريع](./docs/getting-started.md) | المتطلّبات، أول تشغيل، أول مهمة |
| [التثبيت](./docs/installation.md) | كل طرق التثبيت بالتفصيل |
| [التحديث](./docs/updating.md) | القنوات، التحديث الذاتي، `codey upgrade`، التراجع |
| [آلية الإصدار](./docs/release-process.md) | كيف تتدفّق الإصدارات إلى هذا المستودع |
| [إعداد الوكلاء](./docs/configure-agents.md) | الوكلاء المخصّصون، المطالبات، صلاحيات الأدوات |
| [دليل WorkPilot](./docs/workpilot-guide.md) | منظومة أتمتة الطرفية |
| [مرجع API و MCP](./docs/api-reference.md) | الأدوات و MCP وبروتوكول المحدّث |

---

## 🧩 مساهمات المجتمع

- 🤖 [قوالب الوكلاء](./contributions/agent-templates.md)
- 🧩 [المطالبات والمهارات](./contributions/prompts-and-skills.md)
- 🔗 [سير عمل n8n](./contributions/n8n-workflows.md)

تصفّح [فهرس المساهمات](./contributions/README.md) أو أضف مساهمتك عبر Pull Request.

---

## 🤝 المساهمة والدعم

- 🐛 وجدت خطأً؟ [افتح issue](https://github.com/fares-moustafa/Codey-Community/issues/new/choose).
- 💡 لديك فكرة؟ ابدأ [نقاشًا](https://github.com/fares-moustafa/Codey-Community/discussions).
- 📖 تريد المساهمة؟ اقرأ [دليل المساهمة](./CONTRIBUTING.md).
- ❓ تحتاج مساعدة؟ راجع [الدعم](./SUPPORT.md).

يُرجى الالتزام بـ [قواعد السلوك](./CODE_OF_CONDUCT.md). للمشاكل الأمنية راجع [سياسة الأمان](./SECURITY.md).

---

## 📄 الرخصة

يُصدر مجتمع Codey تحت [رخصة MIT](./LICENSE).

</div>

<div align="center">
<sub>صُنع بحب بواسطة Fares Moustafa ومجتمع Codey.</sub>
</div>
