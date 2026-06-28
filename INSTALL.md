# Установка зависимостей (Ubuntu)

Проверено на Ubuntu 24.04+.

## Пакеты для сборки

```bash
sudo apt install \
    build-essential \
    cmake \
    git \
    qt6-base-dev \
    qt6-websockets-dev \
    qt6-tools-dev \
    libgl1-mesa-dev \
    libxkbcommon-dev
```

## Пакеты для запуска (runtime)

```bash
sudo apt install \
    libqt6core6t64 \
    libqt6gui6t64 \
    libqt6widgets6t64 \
    libqt6network6t64 \
    libqt6sql6t64 \
    libqt6sql6-mysql \
    libqt6concurrent6t64 \
    libqt6websockets6 \
    libgl1 \
    libxkbcommon0 \
    ca-certificates
```

## Сборка

```bash
# Инициализация сабмодулей (librats)
git submodule update --init --recursive

# Конфигурация и сборка
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build -j$(nproc)
```

Бинарник: `build/bin/RatsSearch`

## Manticore Search

Бинарные файлы Manticore Search (searchd, indexer, indextool) идут в комплекте
в каталоге `imports/` (git-субмодуль).
