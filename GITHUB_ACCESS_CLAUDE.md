# 🤖 Инструкция для работы Claude с GitHub

## 📋 Что нужно для работы с GitHub через Claude:

### 1. **Структура репозитория**
```
/Users/alexey/Downloads/affiliateplatform/sdk/
├── .git/                    # Git репозиторий
├── web/                     # Web SDK
├── react-native/           # React Native SDK
└── GITHUB_ACCESS_CLAUDE.md # Этот файл
```

### 2. **Информация о репозитории**
- **GitHub URL**: `https://github.com/UniversalSDK/events-sdk.git`
- **Альтернативный URL**: `https://github.com/Sattva12345/events-sdk.git`
- **Основная ветка**: `main`

### 3. **Команды для Claude**

#### Проверка статуса:
```bash
cd /Users/alexey/Downloads/affiliateplatform/sdk
git status
git remote -v
```

#### Получение последних изменений:
```bash
git fetch origin
git pull origin main
```

#### Внесение изменений:
```bash
# 1. Редактирование файлов
# Claude может редактировать файлы через команды Edit/Write

# 2. Добавление изменений
git add .

# 3. Коммит
git commit -m "Описание изменений"

# 4. Отправка на GitHub
git push origin main
```

#### Если возникают конфликты:
```bash
# Вариант 1: Принять наши изменения
git push origin main --force

# Вариант 2: Слить изменения
git pull origin main --rebase
# Разрешить конфликты
git add .
git rebase --continue
git push origin main
```

## 🔑 Что уже настроено:

1. **Git Credential Helper**: `osxkeychain` - автоматически использует сохраненные пароли
2. **Доступ к файловой системе**: Claude может читать/писать файлы
3. **Выполнение команд**: Claude может выполнять bash команды

## 📝 Примеры задач для Claude:

### "Обнови SDK и выгрузи на GitHub"
```
1. Отредактируй файлы SDK
2. Проверь изменения: git status
3. Закоммить: git add . && git commit -m "Update SDK"
4. Выгрузи: git push origin main
```

### "Проверь что в GitHub репозитории"
```
1. git fetch origin
2. git log origin/main --oneline -10
3. git diff HEAD origin/main
```

### "Синхронизируй с GitHub"
```
1. git pull origin main
2. Если конфликты - разреши их
3. git push origin main
```

## ⚡ Быстрые команды:

```bash
# Обновить и выгрузить SDK одной командой
cd /Users/alexey/Downloads/affiliateplatform/sdk && \
git add . && \
git commit -m "Update SDK" && \
git push origin main
```

## 🚨 Важные моменты:

1. **Путь к SDK**: `/Users/alexey/Downloads/affiliateplatform/sdk/`
2. **НЕ коммитить node_modules**: Они в .gitignore
3. **Всегда проверять статус**: `git status` перед push
4. **Remote уже настроен**: origin → UniversalSDK/events-sdk

## 💡 Подсказка для общения с Claude:

Просто скажите: "Посмотри файл GITHUB_ACCESS_CLAUDE.md в папке sdk и обнови SDK на GitHub"

Claude автоматически:
- Найдет этот файл
- Поймет структуру
- Выполнит необходимые команды
- Обновит код на GitHub

---

Последнее обновление: 2025-07-04
Репозиторий: https://github.com/UniversalSDK/events-sdk