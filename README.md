# 🏓 Gesture Pong

Игра в настольный теннис (Pong), управляемая движением руки через вебкамеру с помощью OpenCV + Mediapipe.
🚀 Полностью локально, без отправки данных в интернет.

---

## 🚀 Быстрый старт

### 1️⃣ Склонируйте репозиторий

```bash
git clone https://github.com/Kb-Kirill/pong-hackathon
cd gesture-pong
```

### 2️⃣ Создайте виртуальное окружение

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3️⃣ Установите зависимости

```bash
pip install -r requirements.txt
```

---

## 🔧 Зависимости

* `pygame` — для визуализации игры
* `opencv-python` — захват и обработка видео
* `mediapipe` — детекция руки (или других частей тела)

См. [`requirements.txt`](./requirements.txt) для версий.

---

## 🖥 Системные пакеты

### Linux (debian-based)

```bash
sudo apt update
sudo apt install libgl1 libgtk-3-dev
```
(необходимы для корректной работы OpenCV, открытия окон и т.д.)

### Linux (RHEL, Fedora, CentOS)
```bash
sudo dnf in mesa-libGL mesa-libGLU gtk3-devel
```

На Windows / MacOS дополнительно ничего не требуется.

---

## ✅ Тест камеры и Mediapipe

Для проверки камеры и распознавания руки используется скрипт `test_camera.py`.

### 📂 Запуск

```bash
python test_camera.py
```

Если рука обнаружена, в консоли будут появляться сообщения:

```
Hand detected: landmark ...
```

а в окне появится видео с камеры.

---

## ⚠ Если камера не открывается

* Закрой другие приложения (Zoom, Discord и др.), которые могут её блокировать.
* Попробуй сменить индекс:

  ```python
  cap = cv2.VideoCapture(1)
  ```
* Для Linux можно посмотреть устройства:

  ```bash
  ls /dev/video*
  ```
---

## 📜 Лицензия

MIT © 2025 — Сделано для хакатона ⚡
