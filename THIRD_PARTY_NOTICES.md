# Сторонние компоненты

Условия бесплатного использования Lzhecord относятся к самому приложению. У перечисленных компонентов собственные лицензии.

| Компонент | Где используется | Лицензии и сведения |
| --- | --- | --- |
| Electron и Chromium | Desktop-сборки | `LICENSE` и `LICENSES.chromium.html` рядом с `Lzhecord.exe`; [Electron](https://github.com/electron/electron/blob/main/LICENSE) |
| Node.js | Служба браузерной сборки; также входит в Electron | `runtime/LICENSE-Node.txt` в браузерном архиве; [Node.js](https://github.com/nodejs/node/blob/main/LICENSE) |
| .NET | Самодостаточный нативный модуль захвата | [Лицензия .NET 8.0.28](docs/licenses/dotnet-LICENSE.txt) и [уведомления сторонних компонентов](docs/licenses/dotnet-THIRD-PARTY-NOTICES.txt) |

Radmin VPN устанавливается отдельно и не входит в архивы Lzhecord. Его условия определяются разработчиком Radmin VPN. Discord и Nitro не являются компонентами Lzhecord; проект не связан с Discord Inc.

## Дополнительно загружаемые компоненты GPU-режима 0.8.0

Эти компоненты не входят в архив приложения. Ведущий скачивает их с указанных upstream-релизов при первом включении GPU/NVIDIA; приложение проверяет закреплённые SHA-256. Каталоги пакетов сохраняются целиком вместе с их лицензиями и уведомлениями в папке данных media-tools. Зрителям загрузка не нужна.

- **FFmpeg LGPL shared 9.0**, сборка n9.0.2-57-gd838f9f9ae, [пакет и сведения сборки](https://github.com/FFmpeg-Builds/FFmpeg-Builds/releases/tag/autobuild-2026-11-15-12-40), [исходный код FFmpeg](https://github.com/FFmpeg/FFmpeg/tree/d838f9f9ae), [лицензирование FFmpeg](https://ffmpeg.org/legal.html). Используется отдельный процесс и динамические библиотеки из LGPL-пакета; GPL-сборка FFmpeg не поставляется.
- **MediaMTX 1.21.4**, MIT: [релиз и исходный код](https://github.com/bluenviron/mediamtx/releases/tag/v1.21.4), [лицензия](https://github.com/bluenviron/mediamtx/blob/v1.21.4/LICENSE). Локальный компонент передачи готового потока через WebRTC.

Нативные API Windows и NVENC требуют совместимых драйверов и оборудования. Названия NVIDIA и Windows принадлежат соответствующим правообладателям.

## Совместимый пакет в 0.9.0

Для NVIDIA с драйверами 570–609 и для экспериментальных AMD AMF / Intel Quick Sync приложение по требованию загружает **FFmpeg LGPL shared 8.1**, сборка n8.1.3-35-gf1acb0a266: [upstream-релиз](https://github.com/FFmpeg-Builds/FFmpeg-Builds/releases/tag/autobuild-2026-11-15-12-40), [исходный код FFmpeg](https://github.com/FFmpeg/FFmpeg/tree/f1acb0a266). Проверяется закреплённый SHA-256. Лицензии, уведомления и библиотеки остаются в каталоге пакета. Пакет не входит в архив Lzhecord.
