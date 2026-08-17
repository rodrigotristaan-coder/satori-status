# satori-status

Vigía externo de disponibilidad (GitHub Actions, cada 10 min): hace ping a los
servicios públicos de Satori y avisa por Telegram si alguno no responde.

Es la **capa de respaldo** del monitor local (que corre cada 5 min): este vigía
vive fuera de nuestra infraestructura, así que sigue funcionando aunque la red
local o la Mac estén apagadas.

- Repo público a propósito: los minutos de Actions son ilimitados y aquí no hay
  nada sensible — solo URLs públicas. Las credenciales de Telegram viven en
  GitHub Secrets (cifradas, nunca aparecen en logs).
- Prueba manual: pestaña Actions → vigia → Run workflow → `test_alert: si`.
