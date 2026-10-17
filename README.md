# Судова практика Верховного Суду / Ukrainian Judicial Practice
## Оновлення від 17.10.2026 / Updated 17.10.2026

**GitHub repository guide for AI agents and researchers / Інструкція для AI-агентів і дослідників**  
**Languages / Мови:** [Українська](#українська--інструкція-для-ai) · [English](#english--instructions-for-ai)  
**Primary data source / Основне джерело даних:** [База правових позицій Верховного Суду — https://lpd.court.gov.ua/](https://lpd.court.gov.ua/)  
**Document catalogue / Каталог документів:** https://lpd.court.gov.ua/documents  
**API reference / API-інструкція:** [`api.md`](api.md) (if present / якщо є в репозиторії)

> **UA:** Це інструкція з пошуку у вашому репозиторії, а не підтвердження того, що кожен локальний файл вже існує. Перед цитуванням AI **має знайти та прочитати файл**. Не вигадуйте судових рішень, URL, дат, сторінок або висновків.  
> **EN:** This guide explains how to search your repository. It does not certify that every local file is present. Before citing anything, the AI **must locate and read the actual file**. Never invent judgments, URLs, dates, page numbers, or legal holdings.

## Description для GitHub / GitHub repository description

**Українська (UA):** Огляди та дайджести судової практики Верховного Суду, ЄСПЛ і Суду ЄС у PDF та Markdown. Джерело: https://lpd.court.gov.ua/

**English (EN):** Searchable reviews and digests of Ukrainian Supreme Court, ECtHR and EU Court case law in PDF and Markdown. Source: https://lpd.court.gov.ua/

**Двомовний короткий варіант / Short bilingual version (GitHub About):**

> Огляди судової практики ВС, ЄСПЛ і Суду ЄС у PDF/Markdown · Searchable judicial practice reviews and digests. Source: https://lpd.court.gov.ua/

## Джерело, авторство та статус / Source attribution and repository status

**Українська:**

- **Джерело даних:** [База правових позицій Верховного Суду](https://lpd.court.gov.ua/), зокрема [каталог документів](https://lpd.court.gov.ua/documents).
- PDF-документи та їхні назви/метадані взято з посилань, оприлюднених у цьому каталозі та/або отриманих через його API. Відповідні локальні `.md` — текстові версії PDF, створені для пошуку й роботи AI; **не слід вважати їх офіційно оприлюдненими Markdown-файлами суду**.
- Цей GitHub-репозиторій є **неофіційною систематизацією/дзеркалом для пошуку**. Він не є офіційним сайтом суду, і сам факт посилання на першоджерело не означає схвалення чи підтримки репозиторію Верховним Судом.
- У публікаціях, відповідях AI та похідних даних зазначайте першоджерело: **«Джерело: База правових позицій Верховного Суду — https://lpd.court.gov.ua/»**. Для конкретного документа додавайте посилання на його оригінальний PDF, якщо воно відоме.
- Текст `.md` може містити помилки перетворення чи розпізнавання. У разі розбіжності звіряйтеся з оригінальним PDF. Огляди/дайджести не замінюють тексти судових рішень і чинні нормативні акти.

**English:**

- **Data source:** [The Supreme Court Legal Positions Database](https://lpd.court.gov.ua/), particularly its [document catalogue](https://lpd.court.gov.ua/documents).
- PDF documents, their titles and metadata are drawn from links published in that catalogue and/or retrieved through its API. The accompanying `.md` files are search-oriented text conversions of the PDFs; **they must not be represented as court-published official Markdown files**.
- This GitHub repository is an **independent, unofficial index/mirror for research and search**. It is not a court-operated website, and citing the source does not imply that the Supreme Court endorses or sponsors this repository.
- AI-generated answers and derivative outputs must credit the source: **“Source: Supreme Court Legal Positions Database — https://lpd.court.gov.ua/”**. For an individual document, include its original PDF URL when available.
- Markdown conversion or OCR may introduce errors. Resolve discrepancies against the original PDF. Reviews and digests do not replace the primary judgments or legislation.

---

# Українська — інструкція для AI

## 1. Призначення і принципи

Цей репозиторій містить **огляди й дайджести судової практики**, джерелом яких є [https://lpd.court.gov.ua/](https://lpd.court.gov.ua/), у двох форматах:

- **`.md` (Markdown)** — основний формат для швидкого повнотекстового й семантичного пошуку.
- **`.pdf` (PDF)** — відповідний оригінальний документ для перевірки формулювань, структури, таблиць, приміток і номерів сторінок.

**Головне правило:** два файли одного документа розміщуються **в тій самій папці** й мають **однакову назву без розширення**.

```text
KKS/Oglyad_KKS_07_2026.md
KKS/Oglyad_KKS_07_2026.pdf
```

Наведена пара — приклад схеми іменування. Перевіряйте фізичну наявність обох файлів у репозиторії. Не виводьте назву файлу лише із заголовка документа; не вважайте два документи однаковими тільки через збіг назв.

**Важливе розрізнення:** огляд або дайджест — узагальнення практики; він **не замінює** текст конкретної постанови суду, чинне законодавство чи офіційний висновок у певній справі. У відповідях чітко зазначайте тип джерела.

## 2. Структура GitHub-репозиторію

```text
repository-root/
├── readme_github.md        # Ця двомовна інструкція
├── api.md                  # Опис API й оновлення каталогу (якщо є)
├── ESPL/                   # ЄСПЛ — European Court of Human Rights
│   ├── <filename>.md
│   └── <filename>.pdf
├── KAS/                    # КАС — Касаційний адміністративний суд
├── KCS/                    # КЦС — Касаційний цивільний суд
├── KGS/                    # КГС — Касаційний господарський суд
├── KKS/                    # ККС — Касаційний кримінальний суд
├── Sud_ES/                 # Суд ЄС — суди Європейського Союзу
└── Velyka_Palata/          # Велика Палата Верховного Суду
```

| Папка | Категорія в каталозі | Переважний напрям пошуку |
|---|---|---|
| `Velyka_Palata/` | **Велика Палата** | Юрисдикція, відступи від практики, висновки Великої Палати |
| `KAS/` | **КАС** | Адміністративні спори, податки, органи влади, публічно-правові відносини |
| `KGS/` | **КГС** | Господарські спори, банкрутство, корпоративні правовідносини |
| `KKS/` | **ККС** | Кримінальне право і кримінальний процес |
| `KCS/` | **КЦС** | Цивільне, сімейне, трудове право, майнові спори |
| `ESPL/` | **ЄСПЛ** | Європейська конвенція з прав людини, практика ЄСПЛ |
| `Sud_ES/` | **Суд ЄС** | Право ЄС, практика Суду ЄС та інших судів ЄС |

Ці напрямки — **орієнтири, а не обмеження**. Якщо питання міжюрисдикційне, потрібно перевіряти кілька або всі сім папок.

## 3. Ручний перегляд категорій оглядів / дайджестів (PDF)

На сторінці [Бази правових позицій Верховного Суду](https://lpd.court.gov.ua/documents) передбачені **п'ять тематичних груп ручного перегляду**. Вони **не тотожні** семи швидким фільтрам і не обов'язково мають однозначну відповідність одній папці репозиторію.

| Іконка | Група на сайті | Де шукати в репозиторії |
|---|---|---|
| ![Іконка дайджестів Великої Палати](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/b8bfa49029ea2a959fd4b5f09e69b9df.png) | **Дайджести судової практики Великої Палати Верховного Суду** | Передусім `Velyka_Palata/` |
| ![Іконка міжюрисдикційних дайджестів](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/e2f90f944460100dcae7950788c3d251.png) | **Міжюрисдикційні дайджести судової практики Верховного Суду** | Шукати за назвою й змістом у **всіх семи папках**; окремої папки `Mizhjurysdyktsiini/` не заявлено |
| ![Іконка оглядів касаційних судів](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/a6193a48ae7dbc6b13b109aa5a8188db.png) | **Огляди судової практики касаційних судів** | `KAS/`, `KGS/`, `KKS/`, `KCS/` |
| ![Іконка оглядів рішень ЄСПЛ](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/fdfa6e0851bc7815604263231c20aea4.png) | **Огляди рішень Європейського суду з прав людини** | Передусім `ESPL/` |
| ![Іконка оглядів практики Суду ЄС](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/2ea5c626e280ceb2ae27605dfdcca924.png) | **Огляди практики Суду Європейського Союзу** | Передусім `Sud_ES/` |

Ці URL — **посилання на зображення іконок**, а не посилання на сторінки з відфільтрованими результатами. Для ручного перегляду відкрийте **сам каталог** й оберіть потрібну групу. Не вигадуйте окремих URL для груп без перевірки на сайті.

### Швидкі фільтри на сайті

Сім швидких фільтрів каталогу — саме в такому порядку:

**Велика Палата → КАС → КГС → ККС → КЦС → ЄСПЛ → Суд ЄС**.

На сторінці також є поле пошуку, кнопки **«Шукати»** та **«Скинути фільтри»**. Для пошуку за категорією користувач може вибрати відповідний швидкий фільтр і натиснути «Шукати»; для повернення до повного переліку — «Скинути фільтри».

API повертає метадані типу `typeLabel`, наприклад:

```text
КГС • Тематичний огляд • PDF
Велика Палата • Тематичний дайджест • PDF
ЄСПЛ • Періодичний огляд • PDF
```

**Правило для AI:** перша частина `typeLabel` визначає **категорію/папку**; друга — **вид огляду або дайджесту**. Не плутайте п'ять груп ручного перегляду із сімома юрисдикційними фільтрами. Міжюрисдикційність документа не можна достовірно встановлювати лише за назвою папки.

## 4. Алгоритм пошуку AI — обов'язковий порядок

1. **Зрозуміти запит.** Визначити правову проблему, статті законів, судову юрисдикцію, часовий період, синоніми й потрібний тип відповіді (список джерел / короткий аналіз / точна цитата).
2. **Вибрати початкові папки.** Скористатися таблицею категорій, але за потреби розширити пошук на всі сім.
3. **Знайти реальні `.md`.** Шукати в назвах і повному тексті, а не лише серед PDF-файлів або назв в API.
4. **Прочитати контекст.** Заголовок розділу, абзаци до й після збігу, винятки та застереження. Зіставити релевантність із запитом.
5. **Знайти парний `.pdf`.** Та сама папка + та сама назва без розширення. Перевірити його існування.
6. **Перевірити доказ.** Точне формулювання, дату рішення, номер справи, сторінку й посилання — тільки за прочитаним джерелом; сторінку цитувати **лише після перевірки PDF**.
7. **Порівняти джерела.** Переглянути альтернативні та новіші огляди, не припускати автоматичного «скасування» старішої практики.
8. **Відповісти з посиланнями.** Навести точну назву документа, категорію, коротку підставу релевантності, підтверджений висновок і посилання на `.md` та `.pdf`.
9. **Позначити межі перевірки.** Якщо файл, PDF, сторінка або дата не перевірені — чітко вказати це.

### Пошук назв файлів і Markdown (Linux / macOS / Git Bash)

```bash
# Перелік наявних Markdown-файлів
rg --files ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata -g '*.md'

# Пошук за назвою файлу (всі формати)
rg --files ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata \
  | rg -i 'servitut|сервітут|земел|zemel'

# Пошук у повному тексті Markdown з контекстом
rg -n -i -C 4 --glob '*.md' 'земельн|сервітут|речові права' \
  ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata

# Адміністративні спори
rg -n -i -C 4 --glob '*.md' 'податков(а|ої|их) перевір|рішення податков' KAS/

# Права людини
rg -n -i -C 4 --glob '*.md' 'стаття 6|ст\. 6|Article 6|справедливий суд' ESPL/
```

Команди є прикладами для середовища, де встановлено `rg` (ripgrep) і де папки дійсно існують. Якщо `rg` недоступний, використовуйте локальний індекс, пошук GitHub або інші доступні засоби. Не стверджуйте, що пошук виконано, якщо його не було.

### Синоніми та двомовні запити

- Українська морфологія: `банкрутство / банкрутства`, `сервітут / сервітуту`, `право власності / захист власності`.
- Абревіатури: `ВП ВС`, `КАС`, `КГС`, `ККС`, `КЦС`, `ЄСПЛ`, `ЄКПЛ`.
- `КАС` може означати **Касаційний адміністративний суд** або **Кодекс адміністративного судочинства України** — розрізняйте за контекстом.
- Варіації апострофів, тире, Unicode і транслітерації в назвах файлів.
- Для англомовного запиту **також перекладайте правові терміни українською** для пошуку у `.md` (наприклад, *fair trial* → `справедливий суд`, *property rights* → `право власності`).

## 5. Приклади маршрутизації запитів

| Запит | Початкові папки | Пошукові слова |
|---|---|---|
| Земельний сервітут | `KGS`, `KCS`, `Velyka_Palata` | `сервітут`, `земельн`, `речові права` |
| Податкові перевірки | `KAS`, `Velyka_Palata` | `податкових перевірок`, `процедурні порушення` |
| Банкрутство та зловживання правами | `KGS`, `Velyka_Palata` | `банкрутств`, `зловживання правами` |
| Обчислення строків досудового розслідування | `KKS`, `Velyka_Palata` | `досудов`, `строк`, `розслідуван` |
| Поділ майна подружжя | `KCS`, `Velyka_Palata` | `спільна сумісна власність`, `поділ майна` |
| Право на справедливий суд | `ESPL`, релевантні національні папки | `стаття 6`, `справедливий суд` |
| Право Європейського Союзу | `Sud_ES`, інші за потреби | `директива`, `регламент`, назва акта ЄС |
| Міжюрисдикційний дайджест | **Усі сім папок** | `міжюрисдикційн`, назва правової теми |

Це **стратегія пошуку**, а не підтвердження існування певної тези у конкретному файлі.

## 6. Як зіставляти PDF і Markdown

```python
from pathlib import Path

md = Path('KKS/Oglyad_KKS_07_2026.md')
pdf = md.with_suffix('.pdf')

if md.is_file():
    print('Markdown:', md.as_posix())
    print('PDF:', pdf.as_posix() if pdf.is_file() else 'не знайдено')
else:
    print('Markdown не знайдено')
```

- Не замінюйте назви на `digestId.pdf`: оригінальний файл має зберігатися під назвою з `externalUrl` (наприклад, `Oglyad_KKS_07_2026.pdf`), а `.md` — мати такий самий stem.
- За конфлікту однакових назв різних PDF використовуйте стабільний унікальний суфікс, **однаковий для `.pdf` і `.md`**; документуйте відповідність у маніфесті за `digestId`.
- Якщо один з двох файлів відсутній, **не посилайтеся на нього як на наявний**.
- Не змінюйте архівні PDF або Markdown під час звичайного пошуку.

## 7. Стандарт цитування й відповіді

Шаблон відповіді (шляхи нижче слід **замінити на фактично перевірені**):

```markdown
## Результати пошуку: <тема>

**Перевірені категорії:** <список папок>
**Стан синхронізації:** <час останнього успішного оновлення, якщо відомий>

### 1. <Точна назва документа>
- **Категорія:** <фактична>
- **Чому релевантний:** <обґрунтування за текстом>
- **Правова позиція:** <перевірений переказ без доданих тез>
- **Місце в документі:** <заголовок / розділ; сторінка PDF лише після перевірки>
- **Джерела:** [Markdown](KKS/<real_filename>.md) · [PDF](KKS/<real_filename>.pdf)

**Обмеження:** <що не перевірено>
```

Потрібно наводити **повну назву документа**, а якщо знайдено постанову — її **номер справи й дату лише з реально прочитаного джерела**. Номер рядка Markdown **не дорівнює** сторінці PDF. Не приписуйте оглядам статусу першоджерела судового рішення.

**GitHub:** з кореневого `readme_github.md` використовуйте відносні посилання на `KKS/file.md` та `KKS/file.pdf`. За межами GitHub можна створювати абсолютні URL **лише після встановлення дійсного `OWNER/REPO/branch`**. Не вигадуйте назву репозиторію або SHA commit.

Приклади пошуку через GitHub (замініть `OWNER/REPO` на справжній):

```text
repo:OWNER/REPO path:KGS/ сервітут
repo:OWNER/REPO path:ESPL/ "справедливий суд"
repo:OWNER/REPO extension:md "банкрутство"
```

Пошук GitHub може не індексувати вміст PDF; пріоритет — читання Markdown з локального checkout або пошукового індексу.

## 8. Оновлення щомісяця та виявлення нових файлів

Сайт оновлює каталог. **Не припускайте, що історична кількість документів є постійною.** На 16.10.2026 надана відповідь містила 883 записи у семи категоріях; це лише контрольний знімок.

### Підтверджений базовий запит

```http
POST https://lpd-api-prod.court.gov.ua/api/v1/digest/search
Content-Type: application/json
Accept: application/json
```

```json
{
  "query": "",
  "filters": [],
  "digestIds": [],
  "excludeDigestIds": [],
  "searchScope": "all"
}
```

**Статус:** це спостережений інтерфейс вебсайту, а не офіційна гарантована специфікація. Додаткові параметри (пагінація, `updatedAt`, дати публікації, фільтри за групами) у наданих даних **не підтверджено**. Докладніша схема в [`api.md`](api.md), якщо файл існує.

### Робочий цикл синхронізації

1. Отримати актуальний JSON, перевірити `results`, `digestId`, `title`, `typeLabel`, `hasPdf`, `pdfUrl` і, якщо є, `externalUrl`.
2. Перевірити повноту відповіді: співвіднести `results.length`, `totalMatches` і `totalDigests`; неповну або помилкову відповідь **не приймати як новий повний знімок**.
3. Зіставити два **успішні** знімки за `digestId`: нові ID, зміни метаданих, ID, що зникли. Зникнення — **сигнал для перевірки**, не команда на видалення.
4. Для нових/оновлених документів визначити назву PDF із **останнього сегмента `externalUrl`**, якщо він існує. За відсутності `externalUrl` створити безпечну стабільну назву з `title` і зберегти її в маніфесті.
5. Завантажити PDF з перевіреного оригінального HTTPS-джерела або через `pdfUrl` із офіційного API, перевірити `%PDF-`, зберегти в потрібну категорію й створити **парний `.md` з тим самим stem**.
6. Для визначення **змін у вмісті за незмінного ID** порівняти хеші **SHA-256** фактично завантажених PDF. Сам API не надає підтвердженого `updatedAt` / контрольного хешу.
7. Повторно індексувати лише нові або змінені `.md`; зберігати історію синхронізацій та журнал помилок.
8. Звіт за місяць: категорія, назва, `digestId`, стан (`new`, `metadata_changed`, `pdf_changed`, `missing_from_api`, `unchanged`), шлях `.md`, шлях `.pdf`, оригінальна URL (якщо є), час **виявлення**.

Не прирівнюйте дату в назві документа до фактичної дати опублікування. Уникайте зайвого навантаження на сервер: помірна частота запитів, обробка HTTP 403/429, повтори з backoff, без обходу обмежень.

## 9. Вимоги до пошуку AI / RAG

- Індексувати **текст `.md`**, розбиваючи на чанки за заголовками і змістовими абзацами.
- У метаданих кожного чанка зберігати: `category`, `mdPath`, `pdfPath`, перевірену назву документа, `digestId` (лише за наявності достовірного зіставлення), час індексації та SHA-256 тексту.
- Повернувши релевантний чанк, **прочитати оригінальний Markdown-фрагмент**; для сторінок і точних цитат відкрити PDF.
- Не використовувати embedding score як доказ правильності правової тези. Не вигадувати номери справ чи дати.
- Якщо заголовки однакові, розрізняти документи за **категорією + шляхом + `digestId`**, а не лише за назвою.

> **Обов’язкова атрибуція / Required attribution:** у кожній підсумковій відповіді за матеріалами цього репозиторію вказуйте офіційне джерело `https://lpd.court.gov.ua/`, а також конкретні перевірені локальні `.md`/`.pdf` посилання.

## 10. Готовий системний промпт (українською)

```text
Ти — AI-помічник з пошуку й аналізу судової практики у GitHub-репозиторії.
Основні папки: ESPL, KAS, KCS, KGS, KKS, Sud_ES, Velyka_Palata.
У кожного документа зазвичай два файли з однаковою назвою в одній папці:
.md для пошуку і .pdf для перевірки оригіналу.

1. Визнач правове питання, релевантні юрисдикції, синоніми й часові межі.
2. Шукай спершу у справжніх .md, читай контекст, а не лише пошукові фрагменти.
3. Для міжюрисдикційних запитів перевіряй усі релевантні папки.
4. Перевір існування парного PDF перед наданням посилання.
5. Точні цитати і сторінки звіряй із PDF; не вигадуй номери справ, дати чи позиції.
6. Розрізняй огляд практики, текст конкретного рішення та чинне законодавство.
7. Наводь точну назву, категорію, перевірений висновок, локальні посилання .md/.pdf.
8. Якщо джерело відсутнє або не перевірене, чесно зазначай обмеження.
9. Нові документи визначай лише порівнянням двох повних знімків API, за digestId.
10. Відповідай мовою користувача, за замовчуванням українською.
Не змінюй і не видаляй джерела без окремого запиту.
```

---

# English — instructions for AI

## 1. Purpose and core rules

This repository archives **Ukrainian judicial-practice reviews and digests** as paired files:

- **`.md` Markdown** is the preferred searchable text for full-text and semantic retrieval.
- **`.pdf` PDF** is the corresponding original-format publication for checking exact language, page numbers, tables, notes, and formatting.

**Mandatory pairing convention:** the two files for one document are in the **same directory** with the **same filename stem**:

```text
KKS/Oglyad_KKS_07_2026.md
KKS/Oglyad_KKS_07_2026.pdf
```

This is a filename example; confirm both files exist before linking. Never generate repository paths from a title alone. Do not treat an editorial review/digest as a substitute for the original court judgment or currently applicable legislation.

## 2. Repository directories and jurisdiction filters

```text
repository-root/
├── readme_github.md
├── api.md                 # API and monthly sync instructions, if present
├── ESPL/                  # European Court of Human Rights (ECtHR)
├── KAS/                   # Cassation Administrative Court
├── KCS/                   # Cassation Civil Court
├── KGS/                   # Cassation Commercial Court
├── KKS/                   # Cassation Criminal Court
├── Sud_ES/                # Court of Justice / courts of the European Union
└── Velyka_Palata/         # Grand Chamber of the Supreme Court
```

| Folder | Ukrainian filter | Primary research area |
|---|---|---|
| `Velyka_Palata/` | **Велика Палата** | Grand Chamber rulings, jurisdictional issues, significant legal approaches |
| `KAS/` | **КАС** | Administrative disputes, tax, public authorities |
| `KGS/` | **КГС** | Commercial litigation, insolvency, company law |
| `KKS/` | **ККС** | Criminal law and criminal procedure |
| `KCS/` | **КЦС** | Civil, family, labor, property disputes |
| `ESPL/` | **ЄСПЛ** | European Convention on Human Rights, ECtHR case-law reviews |
| `Sud_ES/` | **Суд ЄС** | EU law, Court of Justice and EU courts |

The **seven quick filters** on https://lpd.court.gov.ua/documents appear in this order:

**Grand Chamber (Велика Палата) → KAS (КАС) → KGS (КГС) → KKS (ККС) → KCS (КЦС) → ECtHR (ЄСПЛ) → EU Court (Суд ЄС).**

Search across directories whenever a topic overlaps jurisdictions.

## 3. Manual browsing: PDF reviews and digests

The official website also presents **five manual browsing groups**. They are **different from** the seven jurisdiction filters, and one manual group does not necessarily map to exactly one repository folder.

| Official icon | Original Ukrainian group label | English description | Where to search locally |
|---|---|---|---|
| ![Grand Chamber digests icon](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/b8bfa49029ea2a959fd4b5f09e69b9df.png) | **Дайджести судової практики Великої Палати Верховного Суду** | Grand Chamber of the Supreme Court case-law digests | Start with `Velyka_Palata/` |
| ![Cross-jurisdiction digests icon](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/e2f90f944460100dcae7950788c3d251.png) | **Міжюрисдикційні дайджести судової практики Верховного Суду** | Cross-jurisdiction Supreme Court case-law digests | Search **all seven directories** by title and content |
| ![Cassation courts reviews icon](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/a6193a48ae7dbc6b13b109aa5a8188db.png) | **Огляди судової практики касаційних судів** | Cassation courts case-law reviews | `KAS/`, `KGS/`, `KKS/`, `KCS/` |
| ![ECtHR reviews icon](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/fdfa6e0851bc7815604263231c20aea4.png) | **Огляди рішень Європейського суду з прав людини** | Reviews of decisions of the European Court of Human Rights | Start with `ESPL/` |
| ![EU Court reviews icon](https://lpd-api-prod.court.gov.ua/api/v1/digest/icon/2ea5c626e280ceb2ae27605dfdcca924.png) | **Огляди практики Суду Європейського Союзу** | Reviews of case law of the Court of Justice of the European Union | Start with `Sud_ES/` |

The five icon URLs are **image resources**, **not** links to separate filtered-results pages. To browse manually, open the [official documents catalogue](https://lpd.court.gov.ua/documents), choose the relevant group and use the search field and the original Ukrainian controls **«Шукати» (Search)** / **«Скинути фільтри» (Reset filters)**.

In API metadata, `typeLabel` looks like:

```text
КГС • Тематичний огляд • PDF
ЄСПЛ • Періодичний огляд • PDF
Велика Палата • Тематичний дайджест • PDF
```

The part **before the first bullet separator** is the jurisdiction/category; the next part describes the review/digest type. **Do not conflate** the five manual browsing groups with the seven quick jurisdiction filters. Cross-jurisdiction coverage cannot be determined reliably from the folder name alone.

## 4. Required AI search procedure

1. **Interpret the question:** legal issue, legal provisions, relevant court(s), period, synonyms, and desired output (source list, analysis, exact citation).
2. **Select candidate folders**, but expand to other folders for overlapping or cross-jurisdiction questions.
3. **Discover actual `.md` files** and search their contents; do not rely on PDF filenames or API titles alone.
4. **Read adequate context** around each hit, including heading, preceding/following passages, exceptions, and caveats.
5. **Find the paired PDF** in the same directory using the same stem. Verify its existence.
6. **Check the evidence**: exact wording, PDF page, case number, judgment date, and legal proposition must be directly supported by the content you actually read.
7. **Cross-check** other pertinent or newer reviews. Do not infer that newer coverage automatically overrules older case law.
8. **Provide evidence-backed results** with exact title, category, short relevance rationale, supported summary, and verified MD/PDF links.
9. **State limitations** if a source, page, file pair, or freshness cannot be verified.

### Search commands (Linux / macOS / Git Bash)

```bash
# Enumerate real Markdown files
rg --files ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata -g '*.md'

# Filenames in either format
rg --files ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata \
  | rg -i 'servitut|сервітут|zemel|земел'

# Full-text search with surrounding context
rg -n -i -C 4 --glob '*.md' 'сервітут|земельн|речові права' \
  ESPL KAS KCS KGS KKS Sud_ES Velyka_Palata

# ECtHR / right to a fair trial
rg -n -i -C 4 --glob '*.md' 'стаття 6|ст\. 6|Article 6|справедливий суд' ESPL/
```

These commands require `ripgrep` and access to the repository; never claim you executed them unless you did. GitHub search may not search PDF binaries. Search the checked-out Markdown or a generated text index when precision matters.

### English-to-Ukrainian query expansion

Because the document texts are frequently in Ukrainian, search Ukrainian variants even if the user writes in English:

| English concept | Useful Ukrainian search phrases |
|---|---|
| Land easement / servitude | `земельний сервітут`, `сервітуту`, `речові права` |
| Insolvency / bankruptcy | `банкрутство`, `неплатоспроможність` |
| Fair trial | `справедливий суд`, `стаття 6`, `ЄКПЛ` |
| Search and seizure | `обшук`, `огляд`, `слідчі дії` |
| Tax audit | `податкова перевірка`, `податкових перевірок` |
| Marital property division | `поділ майна подружжя`, `спільна сумісна власність` |
| Cross-jurisdiction practice | `міжюрисдикційні`, `юрисдикція`, `відступ від висновку` |

Consider inflected Ukrainian forms, alternative apostrophes and dashes, transliterated basenames, and abbreviations. `КАС` may mean either the Cassation Administrative Court or the Code of Administrative Procedure, depending on context.

## 5. Pairing Markdown and PDF correctly

```python
from pathlib import Path

md = Path('KKS/Oglyad_KKS_07_2026.md')
pdf = md.with_suffix('.pdf')

if md.is_file():
    print('Markdown:', md.as_posix())
    print('PDF:', pdf.as_posix() if pdf.is_file() else 'NOT FOUND')
else:
    print('Markdown: NOT FOUND')
```

Use the **original PDF basename** from `externalUrl` whenever available, rather than saving as `<digestId>.pdf`. The extracted Markdown must retain the **same stem**. If filenames collide for different documents, add a stable disambiguation suffix to **both** counterparts and record `digestId → mdPath/pdfPath` in a manifest. Never assume a missing counterpart exists or link to an unverified path.

## 6. How AI should cite results

Use real relative repository links when the files have been found:

```markdown
## Search results: <topic>

**Directories searched:** <verified list>
**Last successful catalogue synchronization:** <if known>

### 1. <Exact document title>
- **Category:** <verified category>
- **Relevance:** <why this source answers the question>
- **Supported finding:** <accurate paraphrase of the actual text>
- **Location:** <verified heading; PDF page only if checked>
- **Sources:** [Markdown](KKS/<actual_filename>.md) · [PDF](KKS/<actual_filename>.pdf)

**Limitations:** <anything unavailable or unchecked>
```

Do not confuse Markdown line numbers with PDF page numbers. Verify case numbers, dates, quotations, and holdings in the material before making precise claims. Cite the review as a review; cite an actual judgment separately if that is needed.

On GitHub, root-relative file paths in this guide are portable from the repository root. Outside GitHub, construct absolute links **only after** determining the real `OWNER/REPO/branch`; do not fabricate a remote repository URL.

GitHub search examples (replace the placeholder with the verified repo identifier):

```text
repo:OWNER/REPO path:KGS/ сервітут
repo:OWNER/REPO path:ESPL/ "справедливий суд"
repo:OWNER/REPO extension:md "банкрутство"
```

## 7. Monthly updates and detecting new documents

The online catalog is updated, so treat local files as a **snapshot**, not proof of the most current position. An API response supplied on **2026-10-16** contained **883 records**; this historical count is not a fixed limit.

**Observed, verified baseline request:**

```http
POST https://lpd-api-prod.court.gov.ua/api/v1/digest/search
Content-Type: application/json
Accept: application/json
```

```json
{
  "query": "",
  "filters": [],
  "digestIds": [],
  "excludeDigestIds": [],
  "searchScope": "all"
}
```

The source API response contains `results[]` items with `digestId`, `title`, `typeLabel`, `hasPdf`, `pdfUrl`, and an **optional** `externalUrl`. This is a **reverse-observed interface**, not a guaranteed official contract; do not invent pagination, `updatedAt`, group filter parameters, or other undocumented fields. Consult [`api.md`](api.md) when available.

**Synchronization procedure:**

1. Fetch the whole response and validate that `results.length`, `totalMatches`, and `totalDigests` are coherent. Never accept an incomplete or failed response as a complete new baseline.
2. Compare two **successful** snapshots by `digestId`: new IDs, changed metadata, IDs absent in the latest snapshot. Missing IDs are a **review signal**, not an automatic deletion instruction.
3. Prefer `externalUrl` as the PDF source and original basename; fall back to the verified API `pdfUrl` if needed. For entries without `externalUrl`, derive a safe stable name from `title`, store it in a manifest, and reuse it.
4. Download only what is necessary, validate actual PDF bytes (`%PDF-`), and place the paired `.pdf` and `.md` in the correct category directory with **identical stems**.
5. Compare **SHA-256 of downloaded PDF bytes** to detect binary revisions even when `digestId` stays unchanged. The observed API has no confirmed `updatedAt` or authoritative file hash.
6. Re-index new or changed Markdown only, preserve earlier successful snapshots, and produce a dated report by jurisdiction.
7. Do not infer a publication date from the month or year embedded in a PDF filename or review title. Track **when a change was detected** separately.
8. Honor server restrictions and error responses (notably HTTP 403 and 429). Use conservative request rates and retry backoff; do not bypass access controls.

## 8. AI / RAG index design

For each Markdown section/chunk, retain its `category`, `mdPath`, `pdfPath`, verified document title, optionally matched `digestId`, heading/chunk identifier, index timestamp, and text SHA-256. The **actual text** is the evidence, not its embedding similarity score. On retrieval, reread the original passage and open the paired PDF if an exact quotation, page number, or OCR ambiguity matters.

Do not deduplicate records by title alone. Use a stable combination such as **category + actual source path + verified `digestId`** when available.

> **Required attribution:** when answering from repository materials, credit `https://lpd.court.gov.ua/` and provide actual verified local `.md`/`.pdf` source links.

## 9. Ready-to-use AI system prompt (English)

```text
You are an evidence-based assistant searching a GitHub repository of Ukrainian
judicial-practice reviews and digests.
The source folders are ESPL, KAS, KCS, KGS, KKS, Sud_ES and Velyka_Palata.
Each document normally has paired same-stem .md and .pdf files in one folder.

1. Determine the legal question, categories, query variants, and date limits.
2. Search actual Markdown content first; read context beyond result snippets.
3. For cross-jurisdiction issues, include every relevant directory.
4. Check the matching PDF exists before linking to it.
5. Verify precise quotations, court cases, judgment dates, and pages in sources.
6. Distinguish judicial reviews from primary judgments and current law.
7. Provide exact titles, supported findings, and verified MD/PDF source links.
8. Never invent documents, case numbers, page numbers, dates, or paths.
9. Determine new documents only by comparing two complete API snapshots by
   digestId; verify PDF changes using hashes when needed.
10. Respond in the user's language (Ukrainian by default).
Always credit the original data source: https://lpd.court.gov.ua/.
Do not change or delete source documents without an explicit request.
```

---

## Підсумкова перевірка / Final checklist

- [ ] **UA:** Перевірені потрібні папки та, за потреби, міжюрисдикційні джерела.  
      **EN:** Relevant folders, including cross-jurisdiction sources, were searched.
- [ ] **UA:** Прочитано повний контекст Markdown; не лише пошукові збіги.  
      **EN:** Full Markdown context, not just search hits, was read.
- [ ] **UA:** Перевірено парний PDF у тій самій папці з тим самим stem.  
      **EN:** The same-stem PDF counterpart was verified in the same folder.
- [ ] **UA:** Сторінки, цитати, дати та номери справ не вигадані.  
      **EN:** Page numbers, quotations, dates and case identifiers are substantiated.
- [ ] **UA:** Не переплутано 5 груп ручного перегляду із 7 швидкими фільтрами.  
      **EN:** The five manual browsing groups were not confused with seven quick filters.
- [ ] **UA:** Збережено точні назви файлів і перевірені посилання.  
      **EN:** Original filenames and verified source links were retained.
- [ ] **UA:** Стан актуальності зазначено без вигаданих дат публікації.  
      **EN:** Freshness limits are explicit; publication dates were not inferred.

**Для супроводу / Maintainers:** тримайте джерела в семи папках, інструкцію пошуку тут, деталі API в `api.md` (якщо є), а знімки й індекси — окремо.  
**For maintainers:** keep source documents in the seven folders, search policy in this file, API details in `api.md` (if available), and generated indexes/snapshots separately.
