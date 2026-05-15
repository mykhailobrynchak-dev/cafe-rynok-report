# CAFE RYNOK — Бізнес-огляд

Автоматизований бізнес-огляд для мережі CAFE RYNOK (Львів) × Bolt Food UA.

**Live:** https://mykhailobrynchak-dev.github.io/cafe-rynok-report/

## Структура звіту

Звіт містить три вкладки:

1. **Місячні дані** — фінансові та операційні показники за місяць
2. **Тижневі дані** — деталізація за останні 4 тижні
3. **Аналіз локацій** — ефективність окремих закладів з WoW порівнянням

## Файли

| Файл | Призначення |
|------|-------------|
| `generate_report.py` | Databricks SQL → `index.html` |
| `template.html` | HTML-шаблон із Chart.js |
| `report_data.json` | Кешовані дані |
| `index.html` | Готовий звіт |

## Автоматичне оновлення

Щопонеділка о 07:00 за Києвом через GitHub Actions.

### Необхідні Secrets

| Секрет | Значення |
|--------|----------|
| `DATABRICKS_HOST` | `bolt-common.cloud.databricks.com` |
| `DATABRICKS_TOKEN` | Databricks Personal Access Token |
| `DATABRICKS_WAREHOUSE_ID` | `b39957853740b21d` |
