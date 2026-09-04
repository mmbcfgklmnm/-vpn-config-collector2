# 🛡️ VPN Config Collector

کانفیگ‌های VLESS جمع‌آوری‌شده از منابع عمومی که از یک pipeline شش‌لایه
عبور کرده‌اند: فرمت → حذف تکراری → TCP → TLS → Geo → HTTP واقعی.

## آمار آخرین اجرا

<!-- STATS_START -->
| فیلد | مقدار |
|------|-------|
| آخرین آپدیت | 2026-09-04 00:26:06 UTC |
| مدت اجرا | 137.6s |
| جمع‌آوری | 3502 |
| ✅ معتبر | **277** |
| لایه ۱ فرمت | 2560 |
| لایه ۲ dedup | 2393 |
| لایه ۳ TCP | 1773 |
| لایه ۴ TLS | 1739 |
| لایه ۵ Geo | 1729 |
| لایه ۶ HTTP | 277 |
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
