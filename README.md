# Dev Website

Сайт коммерческой разработки на заказ.

## Разработка

### Первоначальная настройка

```bash
npm install
```

### Работа со стилями

Проект использует Tailwind CSS. Все стили находятся в `src/input.css`, а готовый CSS файл собирается в `assets/style.css`.

Для пересборки CSS после изменений:

```bash
# Для разработки (с watch mode)
npm run build-css

# Для production (минифицированный)
npm run build-css-prod
```

### Структура проекта

```
├── index.html          # Главная страница
├── assets/
│   └── style.css      # Готовый CSS (для GitHub Pages)
├── src/
│   └── input.css      # Исходный CSS с директивами Tailwind
├── tailwind.config.js  # Конфигурация Tailwind
└── package.json        # Зависимости
```

### Deployment

Сайт автоматически деплоится через GitHub Pages. Файл `assets/style.css` должен быть закоммичен в репозиторий.

После изменения стилей:

1. `npm run build-css-prod` - пересобрать CSS
2. Закоммитить изменения включая `assets/style.css`
3. Запушить в master