# AsciiArtify Kubernetes Local Development Concept

## Вступ

Для локальної розробки Kubernetes кластерів розглянуто три інструменти:

- **minikube** — локальний Kubernetes кластер (VM/Container)
- **kind** — Kubernetes in Docker (кластер у контейнерах)
- **k3d** — lightweight Kubernetes (k3s) у Docker

---

## Характеристики

| Інструмент | ОС | Архітектура | Швидкість | Автоматизація | Додаткові функції |
|------------|----|------------|----------|--------------|------------------|
| minikube   | Linux/Mac/Win | amd64/arm | середня | добра | dashboard, addons |
| kind       | Linux/Mac/Win | amd64/arm | швидка | дуже добра | CI/CD friendly |
| k3d        | Linux/Mac/Win | amd64/arm | дуже швидка | дуже добра | lightweight k3s |

---

## Переваги та недоліки

### minikube
**Переваги:**
- простий старт
- багато документації
- вбудований dashboard

**Недоліки:**
- повільний старт
- важчий по ресурсах

---

### kind
**Переваги:**
- ідеальний для CI/CD
- швидкий запуск
- простий у використанні

**Недоліки:**
- менше "фіч" ніж minikube
- залежність від Docker

---

### k3d
**Переваги:**
- дуже швидкий
- мінімальне споживання ресурсів
- добре підходить для PoC

**Недоліки:**
- менш популярний
- потребує розуміння k3s

---

## Docker vs Podman

Docker має ліцензійні обмеження для комерційного використання.

Альтернатива:
- Podman — без daemon, open-source
- підтримується kind/k3d (з обмеженнями)

---

## Демонстрація (k3d)

### Створення кластера
```bash
k3d cluster create asciiartify

##Demo Recording
https://asciinema.org/a/t5hUDV67xV6Ta4Y4
