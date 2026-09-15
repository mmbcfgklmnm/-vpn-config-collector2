# 🛡️ VPN Config Collector

کانفیگ‌های VLESS جمع‌آوری‌شده از منابع عمومی که از یک pipeline شش‌لایه
عبور کرده‌اند: فرمت → حذف تکراری → TCP → TLS → Geo → HTTP واقعی.

## آمار آخرین اجرا

<!-- STATS_START -->
| فیلد | مقدار |
|------|-------|
| آخرین آپدیت | 2026-09-15 23:19:52 UTC |
| مدت اجرا | 301.8s |
| جمع‌آوری | 3286 |
| ✅ معتبر | **112** |
| لایه ۱ فرمت | 2490 |
| لایه ۲ dedup | 2278 |
| لایه ۳ TCP | 1631 |
| لایه ۴ TLS | 1490 |
| لایه ۵ Geo | 1475 |
| لایه ۶ HTTP | 112 |
<!-- STATS_END -->

## استفاده

لینک subscription:

```
https://raw.githubusercontent.com/<owner>/<repo>/main/configs/valid.txt
```

- `configs/valid.txt` — کانفیگ‌هایی که همه لایه‌ها را پاس کرده‌اند
- `configs/all.txt` — همه‌ی کانفیگ‌های خام جمع‌آوری‌شده
- `configs/stats.json` — آمار کامل اجرا

## اجرای محلی

```bash
pip install -r requirements.txt
SKIP_TELEGRAM=true SKIP_XRAY=true python -m src.main
```

برای اجرای لایه ۶ باینری xray لازم است و مسیرش با `XRAY_BINARY_PATH` تنظیم می‌شود.
