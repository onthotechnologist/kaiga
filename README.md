# Кайга

Вики сеттинга для Cairn на [Just the Docs](https://github.com/just-the-docs/just-the-docs).

## Структура

- **Home**
- **Принципы сеттинга**
- **Кайга: о мире** (Кланы, Хлад, Слово)
- **Механики** → Отмеченные (Память, Знак, Плоть, Железо); Отряды
- **Глоссарий**

## Локально

```bash
bundle install
bundle exec jekyll serve
```

## GitHub Pages

1. Обновите `url`, `baseurl` и `repository` в `_config.yml`.
2. **Settings → Pages → Source: GitHub Actions**.
3. Залейте изменения в `main` (см. ниже).

## Обновление через drag and drop

1. Отредактируйте файлы в корне проекта (`mir/`, `mekhaniki/` и т.д.) или перенесите готовое из `progress/`.
2. Соберите папку для загрузки:

```bash
./prepare-upload.sh
```

3. На GitHub откройте репозиторий → **Add file → Upload files**.
4. Перетащите **содержимое** папки `_upload/` (не саму папку `_upload`) в корень `main`.
5. Подтвердите commit — GitHub Actions соберёт и опубликует сайт.

Папка `_upload/` создаётся локально и не попадает в git: в репозитории не будет второй копии сайта.
