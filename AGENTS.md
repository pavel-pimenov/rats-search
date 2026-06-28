# Rats Search

P2P-торрент поисковик с десктопным GUI на Qt6/C++17.

## Сборка

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build -j$(nproc)
```

Бинарник: `build/bin/RatsSearch`

## Зависимости (Ubuntu)

```bash
sudo apt install cmake g++ qt6-base-dev qt6-websockets-dev qt6-tools-dev
```

## Структура

- `src/` — исходники приложения
- `src/librats/` — сабмодуль библиотеки librats (P2P/торрент движок)
- `src/api/` — REST API, конфиг, фиды, обновления
- `resources/` — ресурсы (иконки, qrc)
- `translations/` — переводы (.ts)
- `imports/` — бинарные зависимости (manticore)

## Ветки

- `master` — основная ветка
