WISNU AGUSTYA RIZKYAWAN  
Fullstack Developer / Backend Engineer

---

## Tentang Saya
Saya adalah Fullstack Developer / Backend Engineer dengan pengalaman 3–7 tahun dalam merancang, membangun, dan memelihara sistem enterprise serta ERP/internal systems. Saya berfokus pada desain API yang dapat diskalakan, pemrosesan data yang andal, optimasi performa, dan penulisan kode yang mudah diuji serta dipelihara. Saya berpengalaman bekerja pada tim lintas-fungsi dan menerapkan praktik terbaik untuk reliability, keamanan, dan continuous delivery.

---

## Tech Stack

- **Backend:** PHP (Yii2), Node.js, REST API design
- **Frontend:** Vue.js, DataTables
- **Database:** MySQL, PostgreSQL
- **Tools & Infra:** Git, Docker (basic), Linux, Postman, CI/CD (konsep)

Badges:
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white) ![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=flat&logo=vue.js&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

---

## Pengalaman & Fokus Pengembangan

- Pengalaman 3–7 tahun pada pengembangan backend dan solusi fullstack untuk perusahaan menengah hingga enterprise.
- Fokus kerja:
  - Enterprise system & ERP / internal systems
  - Desain dan implementasi API (REST) untuk integrasi layanan
  - Data processing dan batch reconciliation
  - Performance tuning, caching, dan maintainable code

---

## Project Highlights (Contoh realistis)

- **ERP Inventory Management — Perusahaan Manufaktur**  
  Peran: Backend Lead. Mengembangkan modul inventory, integrasi barcode, dan batch processing untuk rekonsiliasi stok. Teknologi: PHP (Yii2), MySQL, Redis (caching). Hasil: Mengurangi mismatch stok dan mempercepat proses rekonsiliasi.

- **Internal HRIS & Payroll Integration**  
  Peran: Fullstack Developer. Membangun API integrasi payroll dan UI admin dengan Vue.js + DataTables. Teknologi: Node.js (Express), PostgreSQL, Vue.js. Hasil: Menyederhanakan alur approval dan ekspor data payroll.

- **Payment & Reconciliation Service**  
  Peran: Backend Engineer. Membangun endpoint webhook, validasi transaksi, dan job rekonsiliasi terjadwal. Teknologi: Node.js, PostgreSQL, Docker. Hasil: Meningkatkan throughput pemrosesan transaksi dan menurunkan error reconciliation.

---

## Contoh Kode Singkat

Node.js (Express) — contoh endpoint webhook:
\`\`\`javascript
// routes/webhook.js
const express = require('express');
const router = express.Router();

router.post('/payments/webhook', async (req, res) => {
  try {
    const { transactionId, status } = req.body;
    // validasi dan simpan ke DB
    await savePaymentRecord({ transactionId, status });
    // enqueue job untuk proses lanjutan
    enqueueReconciliationJob(transactionId);
    return res.status(200).json({ ok: true });
  } catch (err) {
    console.error('webhook error', err);
    return res.status(500).json({ ok: false });
  }
});

module.exports = router;
\`\`\`

Yii2 (PHP) — contoh action untuk membuat resource:
\`\`\`php
public function actionCreate()
{
    Yii::$app->response->format = \\yii\\web\\Response::FORMAT_JSON;
    $model = new Item();
    $model->load(Yii::$app->request->post(), '');
    if ($model->save()) {
        return ['success' => true, 'id' => $model->id];
    }
    return ['success' => false, 'errors' => $model->getErrors()];
}
\`\`\`

---

## GitHub Stats
![GitHub stats](https://github-readme-stats.vercel.app/api?username=wisnu-agustya&show_icons=true&theme=default)

---

## Cara Menghubungi
- LinkedIn: https://www.linkedin.com/in/wisnu-agustya
- Email: wisnu.agustya@example.com

---

## Penutup
Saya terbuka untuk peluang kolaborasi pada proyek enterprise, integrasi API, dan optimasi performa. Jika Anda ingin melihat portofolio atau berdiskusi teknis lebih lanjut, silakan hubungi melalui LinkedIn atau email di atas.
