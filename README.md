# Deepal Installer

### 📣 [Telegram-канал: @deepal_tools](https://t.me/deepal_tools) &nbsp;·&nbsp; ❤️ [Поддержать проект](https://t.me/tribute/app?startapp=dPI5)

[![Последняя версия](https://img.shields.io/github/v/release/deepaltools/deepal-installer-releases?label=%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F&color=4FA3FF)](https://github.com/deepaltools/deepal-installer-releases/releases/latest)
[![Скачиваний](https://img.shields.io/github/downloads/deepaltools/deepal-installer-releases/total?label=%D1%81%D0%BA%D0%B0%D1%87%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D0%B9&color=4ADE80)](https://github.com/deepaltools/deepal-installer-releases/releases)

**Программа для компьютера, которая ставит приложения на головное устройство Deepal S07.**

Нужна один раз. Она подключается к машине, ставит на неё [Deepal Store](https://github.com/deepaltools/deepal-store-releases)
и выдаёт ему право дальше ставить и обновлять приложения самому. После этого компьютер
больше не нужен — всё делается в машине.

---

## Зачем это

На головном устройстве Deepal установка сторонних приложений закрыта производителем, и
привычного способа разрешить её изнутри машины нет. Deepal Installer делает это с
компьютера по кабелю.

Программа также показывает **код инженерного меню** вашей машины — он нужен, чтобы
включить отладку по ADB. Код программа считает сама, по последним четырём цифрам VIN
вашей машины и её текущей дате, поэтому у каждой машины и каждого дня он свой. Вводить
или подбирать ничего не надо.

## Что нужно

* Deepal S07 с прошивкой 4.0, 4.0.1, 4.1, 4.1.1 или 4.2.1;
* компьютер с macOS или Windows;
* кабель USB.

На прошивке **4.2 (S07 2026, «Laser»)** программа пока не работает. Установка там устроена
иначе — напишите админу в [Telegram-канале](https://t.me/deepal_tools), и он подскажет,
как поставить приложения на 4.2 Laser.

## Установка на macOS

1. Скачайте `Deepal-Installer-1.1-macOS.dmg` со страницы
   [Releases](https://github.com/deepaltools/deepal-installer-releases/releases/latest).
2. Откройте образ и перетащите **Deepal Installer** в «Программы».
3. Первый запуск: правой кнопкой по программе → «Открыть» → «Открыть». Так один раз,
   потому что программа не подписана сертификатом Apple. Дальше открывается обычным
   двойным щелчком.

Если macOS всё равно не пускает, выполните в Терминале:
```bash
xattr -dr com.apple.quarantine "/Applications/Deepal Installer.app"
```

## Установка на Windows

1. Скачайте `Deepal-Installer-1.0-Windows.zip` со страницы
   [Releases](https://github.com/deepaltools/deepal-installer-releases/releases/latest).
2. Распакуйте архив в любую папку.
3. Запустите **Deepal Installer.exe**.
4. Windows SmartScreen может предупредить о неизвестном издателе:
   «Подробнее» → «Выполнить в любом случае». Программа не подписана, поэтому так.

Драйверы ADB уже внутри архива, отдельно ставить ничего не нужно.

## Как пользоваться

1. **Включите отладку по ADB** в инженерном меню машины. Код входа в это меню программа
   показывает сама — он считается по последним четырём цифрам VIN и сегодняшней дате
   машины, так что подсматривать или вводить его не нужно.
2. **Подключите машину** к компьютеру кабелем (или по Wi-Fi, введя IP машины) и нажмите
   «Подключить машину».
3. **Поставьте магазин.** Дальше приложения ставятся и обновляются уже в машине через
   Deepal Store — компьютер не нужен.

Программа умеет ставить и любой другой `.apk` — перетащите файл в окно.

## Как проверить, что файл ваш

Контрольные суммы SHA-256:

```
macOS   4299ef8437dc3f5a5214bad649d489437c7e5977abf8d13ebce80e983f48786e
Windows 11b867a3f70a9f9d42639bcd4ffe2943d842281aad178d95aa982df272e0636d
```

На macOS: `shasum -a 256 Deepal-Installer-1.1-macOS.dmg`
На Windows: `certutil -hashfile Deepal-Installer-1.0-Windows.zip SHA256`

## Исходный код

Здесь его нет. Это репозиторий раздачи готовых сборок.

GitHub прикладывает к каждой метке архивы `Source code (zip)` и `(tar.gz)` — в них
содержимое **этого** репозитория, то есть вот этот README. Исходников программы там нет.

## Обратная связь

Канал и обсуждение: [@deepal_tools](https://t.me/deepal_tools)

---

Deepal Installer — независимый сторонний проект. К компании Changan и марке Deepal
отношения не имеет, официальным программным обеспечением производителя не является.
