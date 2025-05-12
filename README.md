# Hashtag Journal Plugin for Obsidian

The **Hashtag Journal Plugin** enhances your journaling workflow in Obsidian by automatically processing hashtags and links with a custom activation symbol (e.g., `\`) in journal notes. It organizes them into dedicated hashtag notes and linked notes, streamlining note-taking and organization.

## Demo / Демонстрация

![Demo](demo/12.05.2025%2020-32-32.gif)  
*See the plugin in action with hashtag and link processing!*

---

## Плагин Hashtag Journal для Obsidian

**Плагин Hashtag Journal** улучшает процесс ведения журнала в Obsidian, автоматически обрабатывая хэштеги и ссылки с пользовательским символом активации (например, `\`) в заметках журнала. Он организует их в отдельные заметки для хэштегов и связанные заметки, упрощая создание и структурирование заметок.

---

## Features / Возможности

### English
- **Automatic Hashtag Processing**: Extracts hashtags (e.g., `#tag\`) from journal notes and appends text to corresponding hashtag notes in a specified folder.
- **Link Processing**: Processes Obsidian links (e.g., `[[Note]]\`) with the activation symbol, appending text to the linked note.
- **Block Capture**: Captures multi-paragraph text blocks starting with a block capture symbol (e.g., `\`) until a hashtag or link, including headers and empty lines.
- **Customizable Settings**: Configure journal and hashtag folders, activation symbols, cleaning options, date headers, and more.
- **Multilingual Support**: Supports English and Russian for settings and notifications.
- **Date Headers**: Optionally adds timestamped headers (e.g., `#### YYYY-MM-DD HH:MM`) to hashtag and linked notes.
- **Duplicate Prevention**: Checks for duplicate text to avoid redundant entries.
- **Flexible Processing Modes**: Process notes in the journal folder, hashtag folder, or the entire vault.

### Русский
- **Автоматическая обработка хэштегов**: Извлекает хэштеги (например, `#тег\`) из заметок журнала и добавляет текст в соответствующие заметки хэштегов в указанной папке.
- **Обработка ссылок**: Обрабатывает ссылки Obsidian (например, `[[Заметка]]\`) с символом активации, добавляя текст в связанную заметку.
- **Захват блоков**: Захватывает многострочные блоки текста, начиная с символа захвата (например, `\`), до хэштега или ссылки, включая заголовки и пустые строки.
- **Настраиваемые параметры**: Настройка папок журнала и хэштегов, символов активации, опций очистки, заголовков дат и прочего.
- **Многоязычная поддержка**: Поддержка английского и русского языков для настроек и уведомлений.
- **Заголовки дат**: Опционально добавляет временные метки (например, `#### ГГГГ-ММ-ДД ЧЧ:ММ`) в заметки хэштегов и связанные заметки.
- **Предотвращение дублирования**: Проверяет дубли текста, чтобы избежать повторных записей.
- **Гибкие режимы обработки**: Обработка заметок в папке журнала, папке хэштегов или во всем хранилище.

---

## Installation / Установка

### English: Manual Installation
1. Download the latest release from the [GitHub Releases page](https://github.com/mobmankin/hashtag-journal-plugin/releases).
2. Extract the archive and copy the `hashtag-journal-plugin` folder to your Obsidian vault's plugin directory: `<vault>/.obsidian/plugins/`.
3. Enable the plugin in Obsidian under **Settings > Community Plugins**.

### Русский: Ручная установка
1. Скачайте последнюю версию с [страницы релизов на GitHub](https://github.com/mobmankin/hashtag-journal-plugin/releases).
2. Распакуйте архив и скопируйте папку `hashtag-journal-plugin` в папку плагинов вашего хранилища Obsidian: `<хранилище>/.obsidian/plugins/`.
3. Включите плагин в Obsidian в разделе **Настройки > Плагины сообщества**.

### English: Via BRAT (Beta Reviewers Auto-update Tool)
1. Install the **Obsidian42 - BRAT** plugin from the Obsidian Community Plugins.
2. Go to **Settings > BRAT > Add Beta Plugin**.
3. Enter the repository URL: `https://github.com/mobmankin/hashtag-journal-plugin`.
4. Follow the prompts to install and enable the plugin.

### Русский: Через BRAT (Инструмент автоматического обновления для бета-тестеров)
1. Установите плагин **Obsidian42 - BRAT** из раздела Плагины сообщества в Obsidian.
2. Перейдите в **Настройки > BRAT > Добавить бета-плагин**.
3. Введите URL репозитория: `https://github.com/mobmankin/hashtag-journal-plugin`.
4. Следуйте инструкциям для установки и активации плагина.

---

## Usage / Использование

### English
**Important: Always create a backup of your Obsidian vault before using this plugin to prevent data loss.**

1. **Configure Settings**:
   - Open **Settings > Hashtag Journal Plugin**.
   - Set the **Journal Folder** (e.g., `Journal`) and **Hashtag Folder** (e.g., `Hashtags`).
   - Choose an **Activation Symbol** (e.g., `\`) and **Block Capture Symbol** (e.g., `\`).
   - Select a **Processing Mode** (All Vault, Journal Folder, or Both Folders).
   - Enable/disable options like **Clean Daily Notes**, **Date Headers**, **Notifications**, and **Language** (English or Russian).

2. **Writing Journal Notes**:
   - In a note within the configured journal folder, add hashtags or links with the activation symbol. Examples:
     ```
     This is a note about productivity. #productivity\
     ```
     ```
     Meeting notes for [[ProjectX]]\
     ```
     ```
     \This is a multi-line block
     with some text
     #task\
     ```
   - Use a space before the activation symbol (e.g., `#tag \`) to open the corresponding note after processing (if **Enable Note Opening** is enabled).

3. **Processing**:
   - The plugin automatically processes modified notes in the configured folders.
   - Alternatively, use the command **Process Tag Commands** from the Command Palette to manually process notes.
   - Hashtags are organized into notes in the `Hashtags` folder (e.g., `Hashtags/productivity.md`).
   - Links append text to the linked note (e.g., `ProjectX.md`).

4. **Output**:
   - Hashtag notes are structured with optional date headers and tag hierarchies:
     ```
     # productivity
     #### 2025-05-11 10:30
     This is a note about productivity.
     ```
   - Linked notes receive text with optional date headers:
     ```
     #### 2025-05-11 10:30
     Meeting notes for ProjectX
     ```

### Русский
**Важно: Перед использованием плагина делайте резервную копию хранилища Obsidian, чтобы избежать потери данных.**

1. **Настройка параметров**:
   - Откройте **Настройки > Плагин Hashtag Journal**.
   - Укажите **Папку журнала** (например, `Journal`) и **Папку хэштегов** (например, `Hashtags`).
   - Выберите **Символ активации** (например, `\`) и **Символ захвата блока** (например, `\`).
   - Выберите **Режим обработки** (Всё хранилище, Папка журнала или Обе папки).
   - Включите/отключите опции, такие как **Очистка ежедневных заметок**, **Заголовки дат**, **Уведомления** и **Язык** (английский или русский).

2. **Создание заметок журнала**:
   - В заметке в папке журнала добавляйте хэштеги или ссылки с символом активации. Примеры:
     ```
     Заметка о продуктивности. #продуктивность\
     ```
     ```
     Заметки о встрече для [[ПроектX]]\
     ```
     ```
     \Это многострочный блок
     с текстом
     #задача\
     ```
   - Используйте пробел перед символом активации (например, `#тег \`), чтобы открыть соответствующую заметку после обработки (если включена опция **Включить открытие заметок**).

3. **Обработка**:
   - Плагин автоматически обрабатывает измененные заметки в указанных папках.
   - Также можно использовать команду **Обработать команды тегов** из палитры команд для ручной обработки.
   - Хэштеги организуются в заметки в папке `Hashtags` (например, `Hashtags/продуктивность.md`).
   - Ссылки добавляют текст в связанную заметку (например, `ПроектX.md`).

4. **Результат**:
   - Заметки хэштегов структурированы с опциональными заголовками дат и иерархией тегов:
     ```
     # продуктивность
     #### 2025-05-11 10:30
     Заметка о продуктивности.
     ```
   - Связанные заметки содержат текст с опциональными заголовками дат:
     ```
     #### 2025-05-11 10:30
     Заметки о встрече для ПроектX
     ```

---

## Examples / Примеры

### English: Example 1 - Hashtag with Text
**Input** (in `Journal/2025-05-11.md`):
```
Focus on writing today. #writing\
```

**Output** (in `Hashtags/writing.md`):
```
# writing
#### 2025-05-11 09:00
Focus on writing today.
```

**Journal Note** (if Clean Daily Notes is enabled):
```
[Empty or removed]
```

### Русский: Пример 1 - Хэштег с текстом
**Вход** (в `Journal/2025-05-11.md`):
```
Сосредоточьтесь на писательстве сегодня. #писательство\
```

**Выход** (в `Hashtags/писательство.md`):
```
# писательство
#### 2025-05-11 09:00
Сосредоточьтесь на писательстве сегодня.
```

**Заметка журнала** (если включена очистка):
```
[Пусто или удалено]
```

### English: Example 2 - Link with Block Capture
**Input** (in `Journal/2025-05-11.md`):
```
\Project planning meeting
Attendees: Alice, Bob
[[ProjectX]]\
```

**Output** (in `ProjectX.md`):
```
#### 2025-05-11 10:00
Project planning meeting
Attendees: Alice, Bob
```

### Русский: Пример 2 - Ссылка с захватом блока
**Вход** (в `Journal/2025-05-11.md`):
```
\Встреча по планированию проекта
Участники: Алиса, Боб
[[ПроектX]]\
```

**Выход** (в `ПроектX.md`):
```
#### 2025-05-11 10:00
Встреча по планированию проекта
Участники: Алиса, Боб
```

### English: Example 3 - Nested Hashtag
**Input** (in `Journal/2025-05-11.md`):
```
Debugging session notes. #coding/debug\
```

**Output** (in `Hashtags/coding.md`):
```
# debug
#### 2025-05-11 11:00
Debugging session notes.
```

### Русский: Пример 3 - Вложенный хэштег
**Вход** (в `Journal/2025-05-11.md`):
```
Заметки о сессии отладки. #код/отладка\
```

**Выход** (в `Hashtags/код.md`):
```
# отладка
#### 2025-05-11 11:00
Заметки о сессии отладки.
```

---

## Development / Разработка

### English
To build the plugin locally:
1. Clone the repository:
   ```bash
   git clone https://github.com/mobmankin/hashtag-journal-plugin.git
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Build the plugin:
   ```bash
   npm run build
   ```
4. Copy the built files (`main.js`, `styles.css`, `manifest.json`) to your Obsidian plugins folder.

### Русский
Для локальной сборки плагина:
1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/mobmankin/hashtag-journal-plugin.git
   ```
2. Установите зависимости:
   ```bash
   npm install
   ```
3. Соберите плагин:
   ```bash
   npm run build
   ```
4. Скопируйте собранные файлы (`main.js`, `styles.css`, `manifest.json`) в папку плагинов Obsidian.

---

## Contributing / Вклад в проект

### English
Contributions are welcome! Please submit issues or pull requests on [GitHub](https://github.com/mobmankin/hashtag-journal-plugin).

### Русский
Приветствуется любой вклад! Пожалуйста, отправляйте вопросы или запросы на включение изменений на [GitHub](https://github.com/mobmankin/hashtag-journal-plugin).

---

## License / Лицензия

### English
This plugin is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

### Русский
Этот плагин распространяется под лицензией MIT. Подробности смотрите в файле [LICENSE](LICENSE).

---

## Support / Поддержка

### English
For questions or issues, please open an issue on the [GitHub repository](https://github.com/mobmankin/hashtag-journal-plugin/issues).

### Русский
По вопросам или проблемам, пожалуйста, создайте запрос в [репозитории на GitHub](https://github.com/mobmankin/hashtag-journal-plugin/issues).