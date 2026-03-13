# AURUM — Next-Gen Premium Messenger Blueprint

## 1) Название, бренд и идея

**Название:** **AURUM**  
Короткое, международное, технологичное, премиальное.

**Слоган:** **"Calm communication, engineered to think."**

**Бренд-месседж:**  
AURUM — это «iPhone среди мессенджеров»: радикально чистый интерфейс, мгновенная связь, приватность по умолчанию и интеллектуальные функции, которые помогают, а не мешают.

**Логомарк и app icon:**
- Базовая форма: мягкий скруглённый квадрат (superellipse).
- Внутри: минимальный символ диалога из двух смещённых дуг (без клише “облака”).
- Стиль: монохром + акцентный ледяной синий в динамических состояниях.

---

## 2) Позиционирование

AURUM — премиальный мессенджер для людей, которым нужен **визуальный покой**, **скорость**, **приватность** и **профессиональный уровень общения**.

**ЦА:** дизайнеры, фаундеры, креаторы, digital professionals, студенты и массовый пользователь, уставший от перегруженных мессенджеров.

**Ключевое отличие от Telegram/WhatsApp/Discord:**
1. Визуально чище и спокойнее.
2. Сильнее в voice UX (запись, транскрипция, поиск по голосовым).
3. Умнее в “catch-up” (что я пропустил).
4. Лучше в сохранении личного контента (личный архив/knowledge inbox).
5. Более нативный premium feel на iOS/Android/Desktop.

---

## 3) Дизайн-философия

**Принципы:**
- Content first, chrome last.
- Один акцент на экран.
- Большой воздух, ясная иерархия, микро-анимации вместо визуального шума.
- AI как слой тишины: полезный, опциональный, деликатный.

**Запреты:** кислотные цвета, кричащие градиенты, тяжёлые тени, неон, визуальная каша, “игровая” стилистика.

---

## 4) Визуальная система: цвета и темы

### Базовая палитра (tokens)
- `bg/pure`: `#FFFFFF`
- `bg/graphite`: `#15171A`
- `bg/black`: `#0B0C0E`
- `surface/cool`: `#F3F5F7`
- `surface/dark`: `#1C2024`
- `text/primary-light`: `#111317`
- `text/primary-dark`: `#F5F7FA`
- `accent/ice-blue`: `#4C8DFF`
- `accent/silver-blue`: `#8FAECC`
- `success`: `#2DBE7F`
- `warning`: `#F2A93B`
- `error`: `#E45858`
- `recording`: `#FF453A`

### Темы
1. **Light Pure** — белые слои, тонкие серые разделители.
2. **Dark Graphite** — глубокие графитовые поверхности, low-glow акценты.
3. **Midnight Black** — OLED-оптимизированный чистый чёрный.
4. **Frosted Glass** — аккуратная полупрозрачность панелей (без перегруза).
5. **Titanium** — нейтральный металлический холодный серый.
6. **Soft Blue Night** — ночная тема с мягким синим температурным балансом.

Каждая тема меняет: фон, пузырьки, панели, карточки, статусы, voice player, call UI, навигацию.

---

## 5) Типографика

**Шрифт:** SF Pro / Inter fallback (sans-serif).  
**Ритм:** плотность умеренная, высокая читаемость.

- Display: 34/40 semibold
- H1: 28/34 semibold
- H2: 22/28 semibold
- H3: 18/24 semibold
- Body: 16/22 regular
- Secondary: 15/20 regular
- Caption: 13/18 regular
- Meta (время/статусы): 12/16 medium
- Button: 15/20 semibold
- Input: 16/22 regular

---

## 6) Дизайн-система (4/8-grid)

### Пространство и формы
- База: `4pt`, основной шаг: `8pt`.
- Радиусы: 10 / 14 / 18 / 24.
- Иконки: 18, 20, 24.
- Tap targets: минимум 44x44.

### Компоненты
- **Buttons:** primary / secondary / ghost / destructive.
- **Tab bar:** 5 секций, активный индикатор в виде тонкой капсулы.
- **Inputs:** single-line, multiline, validation states.
- **Cards:** low-contrast surface + hairline border.
- **Bottom sheets:** snap points 25/50/90%.
- **Toasts:** 2.5 сек, свайп для dismiss.
- **Context menus:** blur backdrop + haptic tick.
- **Segmented controls:** compact + scrollable variants.
- **Mini-player:** voice/call persistent strip.
- **Search bar:** universal, sticky, inline filter chips.

Состояния всех компонентов: default / hover (desktop) / pressed / active / disabled / loading.

---

## 7) Информационная архитектура

Нижняя навигация:
1. **Chats**
2. **Calls**
3. **People**
4. **Channels**
5. **Settings**

**Глобальные паттерны:**
- Universal Search доступен из любого таба (gesture pull + command bar).
- FAB “New” контекстный: чат, звонок, группа, канал.
- Быстрые жесты: swipe on chat item (mute/pin/archive/read).

---

## 8) User Flow (первый вход → ежедневное использование)

1. Splash (логотип + мягкое появление 500ms).
2. Welcome (1 сильная фраза + 2 CTA: Continue / Sign in).
3. Auth (phone/email + OTP auto-fill).
4. Профиль (avatar, username, display name, bio).
5. Тема по умолчанию (Light/Dark + preview).
6. Мягкий импорт контактов (skip без наказания).
7. Home (чат-лист + smart prompt “What did I miss?”).
8. Daily loop: read → reply/voice → calls → save/organize → AI catch-up.

---

## 9) Экран списка чатов

**Строка чата:**
- Аватар, имя, превью последнего сообщения.
- Тип-контент индикатор (voice/photo/file/call).
- Время, unread badge, mute/pin/draft/delivery state.

**Дополнительно:**
- Smart folders: All / Personal / Work / Groups / Channels.
- “Recent calls” как компактный горизонтальный блок (опционально).
- Empty state: “Start with one calm conversation.”

---

## 10) Экран чата (эталон)

- Top bar: avatar + name + status + call/video/menu.
- Scroll behavior: sticky date, jump-to-latest button.
- Message style: тонкое отличие incoming/outgoing, без контрастного шума.
- Bubble radii: 18, умные стыки для серий сообщений.
- Meta: суперчистый timestamp + delivery ticks.
- Reply/forward/edited/pinned/search/media overview/date jump.

**Micro-interactions:**
- Отправка: 120ms scale/fade.
- Новое сообщение: subtle slide + opacity.
- Реакция: haptic + micro-burst (без “фейерверка”).

---

## 11) Composer bar

- Слева: `+` attachments.
- Центр: multiline input (до 6 строк).
- Справа: dynamic button (voice/send).
- Long press voice → swipe to cancel / swipe up to lock.
- Slash-команды: `/remind`, `/translate`, `/summarize`, `/poll`.
- Состояния: reply/edit/recording/attachment preview.

---

## 12) Голосовые сообщения (лучше Telegram)

**Запись:** hold-to-record, lock, pause/resume, waveform live preview.  
**Перед отправкой:** trim, denoise, voice enhance.  
**После отправки:** transcript, translate, searchable transcript index.

**Voice player:** waveform, scrubbing, speed (1x/1.25x/1.5x/2x), skip silence, queue, memory position, mini-player.

---

## 13) Медиа и вложения

Поддержка: фото/видео/документы/аудио/ссылки/контакты/гео/события/опросы/GIF/реакции.

**UX:**
- Unified media picker (recent + albums + files).
- Batch upload с прогрессом и приоритетом.
- Original quality toggle.
- Safe file mode для suspicious files.
- Link preview с privacy-safe prefetch.

---

## 14) Calls UX (voice/video)

### Voice
- Instant connect, latency-adaptive UI.
- Быстрые toggles: mute/speaker/bluetooth/hold/add person/transfer.
- Ongoing-call banner + seamless return to chat.

### Video
- PiP, blur background, noise suppression, live captions.
- Screen share, grid/focus mode, low-bandwidth mode.
- Call handoff между устройствами без обрыва.

---

## 15) Groups, Channels, Communities

### Groups
- Roles: owner/admin/moderator/member.
- Permissions matrix (media, links, invites, slow mode).
- Quiet join onboarding (без спама системными сообщениями).

### Channels
- Clean reading mode, author cards, pinned collections.
- Delayed posting, creator analytics, audio/video/longform posts.
- Лёгкая монетизация (подписки/донаты) без агрессивного paywall UX.

### Communities (новый слой)
- Topic rooms + temporary event rooms.
- Focus/study/audio rooms.
- Навигация легче Discord: максимум 2 уровня вложенности.

---

## 16) People и Profile

### People
- Contacts, suggested, recent interactions, QR profile, username link.
- Favorite contacts + “note about person”.

### Profile
- Большой аватар, имя, username, bio, статус.
- Mutual groups, shared media, optional voice intro.
- Действия: message/call/video/mute/block/report.
- Per-chat theme + per-chat wallpaper.

---

## 17) Saved Space (личное пространство)

**AURUM Vault:**
- Saved messages
- Voice notes to self
- Links bucket
- Files bucket
- Tagged collections
- Private drafts
- AI summaries
- Reminders

Это не просто “избранное”, а персональный knowledge inbox.

---

## 18) Поиск (лучший в классе)

Ищет по людям, чатам, сообщениям, файлам, ссылкам, медиа, голосовым, транскриптам, каналам, датам, тегам, pinned.

**Фичи:**
- Natural language search: “найди голосовое про дизайн от Маши в феврале”.
- Semantic index + быстрые фильтры.
- Search within chat + jump-to-result preview.

---

## 19) AI-слой (деликатный)

- Missed chat summaries.
- “What did I miss?”
- Voice transcript + summary + translation.
- Smart reply (optional).
- Action extraction (tasks/reminders/meetings).
- Spam/abuse detection.

**Принцип:** AI не перехватывает управление, а аккуратно помогает в нужный момент.

---

## 20) Notifications, sound, haptics

- Priority chats, quiet mode, grouped notifications.
- Lock-screen privacy levels.
- Reply inline.
- Premium sound pack: soft, short, non-fatiguing.
- Haptic grammar: send/record/call/connect/error.

---

## 21) Motion system

- Duration: 120–240ms (UI), 280–360ms (screen transitions).
- Curves: ease-out for entry, ease-in-out for context shifts.
- Shared element transitions for avatar/media/profile.
- Reduce motion mode respected system-wide.

---

## 22) Empty states

Минимум текста, максимум ясности.

Примеры:
- No chats: “Start your first conversation.”
- No search results: “Nothing yet. Try a name, date, or keyword.”
- Offline: “You’re offline. Messages will send automatically.”

---

## 23) Settings & privacy architecture

Секции:
- Account
- Appearance
- Notifications
- Privacy
- Security
- Devices
- Storage & Data
- Calls & Voice
- Language
- Accessibility
- AI
- Premium
- Help & About

**Security core:** E2EE, passcode, Face ID/Touch ID, 2FA, session management, trusted devices, phishing alerts, disappearing messages, granular visibility rules.

---

## 24) Мультидевайсность

Платформы: iOS, Android, iPad, Mac, Windows, Web.

Синхронизируется:
- Drafts
- Playback position
- Read state
- Calls
- Notifications preference

Desktop/web: multi-column layout, hotkeys, drag&drop, split view, pop-out calls.

---

## 25) Performance principles

- 60fps UI budget.
- Offline-first cache + sync queue.
- Lazy loading list/media.
- Delta sync + ack protocol.
- WebSocket resilience + fast reconnect.
- Adaptive media compression.

---

## 26) Production architecture

### Клиенты
- iOS (SwiftUI)
- Android (Kotlin + Jetpack Compose)
- Web (React + TypeScript)
- Desktop (Tauri shell + web app)

### Backend (microservices)
- Auth Service
- Messaging Service
- Realtime Gateway
- Media Service
- Call Signaling Service
- Notification Service
- Search Service
- AI Service
- Moderation Service
- Analytics/Event Service

### Data layer
- PostgreSQL (primary relational)
- Redis (presence/cache/queues)
- Object Storage (S3-compatible)
- CDN (media delivery)
- Kafka/NATS (event bus)
- OpenSearch (full-text + semantic index)

### Realtime
- WebSocket channels per user/device/chat
- Delivery ACK + read receipts
- Presence/typing/reactions events
- Push fallback (APNs/FCM/WebPush)

### Calls
- WebRTC SFU architecture
- STUN/TURN
- Region-aware routing
- QoS adaptation

---

## 27) Tech stack rationale

- **iOS:** SwiftUI — нативность, скорость, премиальные анимации.
- **Android:** Kotlin Compose — современный native UX parity.
- **Web:** React TS — скорость разработки и надёжная компонентность.
- **Backend core:** Go (realtime/high concurrency) + Rust (media crypto/perf critical paths).
- **Infra:** Docker + Kubernetes, GitHub Actions, ArgoCD, Prometheus/Grafana, Sentry, LaunchDarkly/Unleash.

---

## 28) Message engine

Поддерживает:
- text/media/reply/forward/reactions/mentions/threads
- edit/delete (for me / for everyone)
- scheduled/silent send
- draft recovery
- retry/resend/offline queue
- message versioning + deduplication

Статусы: queued → sent → delivered → read → played (voice).

---

## 29) Почему AURUM лучше Telegram

1. Более спокойный, премиальный и чистый визуальный язык.
2. Voice UX: запись/обрезка/улучшение/транскрипт/поиск.
3. AI catch-up без навязчивости.
4. Search: семантический и по транскриптам.
5. Saved space как личная система знаний.
6. Call UX с device handoff и live captions.
7. Communities без Discord-хаоса.

---

## 30) Premium и монетизация

### Premium (деликатно)
- Extra storage
- Advanced themes
- AI minutes + advanced search
- Creator analytics/tools
- Voice enhancement pro

### Монетизация
- Subscription
- Paid channels / creator memberships
- Business profiles + automation
- Tips/microtransactions

Без рекламного визуального шума и агрессивных апсейлов.

---

## 31) Tone of voice

Спокойный, интеллигентный, уверенный, тёплый, краткий.  
Никакого “маркетингового крика”.

**Microcopy examples:**
- “Sent” / “Delivered” / “Read”
- “Recording locked”
- “You can keep talking. We’ll send when online.”
- “Summarize unread messages”

---

## 32) API modules (v1)

- `/auth/*` login/otp/sessions
- `/users/*` profile/privacy/devices
- `/chats/*` chat lifecycle
- `/messages/*` CRUD/reactions/search index hooks
- `/media/*` upload/download/transcode
- `/calls/*` signaling/session QoS
- `/channels/*` posts/analytics/subscriptions
- `/communities/*` rooms/events
- `/ai/*` summary/transcript/semantic search
- `/admin/*` moderation/abuse/rate limits

---

## 33) Database (high-level schema)

- `users`
- `profiles`
- `devices`
- `sessions`
- `contacts`
- `chats`
- `chat_members`
- `messages`
- `message_versions`
- `attachments`
- `reactions`
- `voice_transcripts`
- `calls`
- `call_participants`
- `channels`
- `channel_posts`
- `communities`
- `rooms`
- `notifications`
- `privacy_settings`
- `feature_flags`

---

## 34) Компонентная структура UI

- `AppShell`
- `MainTabBar`
- `ChatListScreen` / `ChatRow`
- `ChatScreen`
- `MessageBubble`
- `ComposerBar`
- `VoiceRecorderSheet`
- `VoicePlayer`
- `MediaPicker`
- `ProfileScreen`
- `CallScreen`
- `UniversalSearch`
- `AIVaultPanel`
- `SettingsScreen`

---

## 35) Onboarding copy examples

- Welcome headline: **“Communication, in its calmest form.”**
- Card 1: “Private by design.”
- Card 2: “Fast voice, instantly searchable.”
- Card 3: “Perfect sync across every device.”
- CTA: “Continue” / “Create account” / “Sign in”.

---

## 36) MVP → V2 → V3 roadmap

### MVP (0–6 months)
- Core chats + media + voice notes
- Calls (voice/video basic)
- Search (keyword)
- Groups/channels basic
- Multi-device sync basic
- E2EE + 2FA + passcode

### V2 (6–12 months)
- AI summaries + transcript search
- Communities + topic rooms
- Advanced call UX (captions, handoff)
- Vault (saved intelligence)
- Creator analytics and premium tools

### V3 (12–24 months)
- Full semantic graph search
- Deep business layer (automation APIs)
- Smart collaboration spaces
- Cross-app communication extensions

---

## 37) Launch strategy

1. **Design-led beta** (invite-only: designers, founders, creators).
2. **Signature feature marketing:** “Voice that thinks” (transcript + summary + search).
3. **Campus + creator seeding** (high frequency communities).
4. **Referral loops:** theme packs + premium trial.
5. **Country-by-country reliability rollout** (quality-first expansion).

---

## 38) Финальная формула продукта

**AURUM = Calm UI + Realtime speed + Privacy core + Voice intelligence + Cross-device elegance.**

Это не “ещё один мессенджер”, а новая среда общения, которую хочется открывать даже без уведомлений.
