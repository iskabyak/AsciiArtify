kubectl ## 11. GitOps validation (MVP)

Для перевірки GitOps моделі було створено тестовий застосунок nginx.

ArgoCD Application було підключено до GitHub репозиторію:

- repository: AsciiArtify
- path: nginx
- branch: main

ArgoCD автоматично:
- синхронізує стан кластеру з Git
- виконує деплой застосунку
- забезпечує self-healing та drift correction

---

## 12. Підсумковий результат

PoC підтверджує повний GitOps цикл:

Git (source of truth) → ArgoCD → Kubernetes deployment

Система готова до переходу в MVP фазу.
