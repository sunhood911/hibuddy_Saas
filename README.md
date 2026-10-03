**[English](#english)** | **[繁體中文](#繁體中文)** | **[Русский](#русский)** | **[Español](#español)**

---

## English

**Hibuddy — Let your paid Telegram group "collect money, grant access, and clean up" automatically**

> An automated gatekeeper bot for paid Telegram communities.
> Owners no longer reconcile payments or add members manually — members enter instantly after paying, and expired members are removed automatically.

### 1. What is Hibuddy?

Hibuddy is a **paid-entry bot** running on Telegram.

Simply put, it does three things for group owners:

1. **Collect money** — members place orders and transfer funds inside the bot; the money goes **directly into the owner's own wallet**.
2. **Grant access** — once payment is received, the bot automatically generates a one-time invite link; members tap once to join.
3. **Clean up** — members whose service has expired are automatically removed; they can return after renewing.

The whole process is fully automated — owners don't need to watch the group, reconcile statements, or manually add/remove people.

Currently it supports **USDT (TRON TRC20 and Solana SPL)** for payments, and the interface is available in **English / Chinese / Russian / Spanish**.

### 2. Why we built this

There are plenty of tools for paid groups and subscription content in the market today, but they share common pain points:

- **Too expensive**: typically starting with a **monthly / subscription fee** — often tens of dollars a month, whether or not you make any sales.
- **High and opaque platform cuts**: most platforms **take a cut** from what members pay; member payments go to the platform first, then get settled to you, and it's often unclear how much was deducted.
- **Unfriendly to small owners (important)**: for owners just starting out with few members, the monthly fee alone is a fixed burden.

**Hibuddy aims to do the opposite:**

- **No monthly fee, no subscription fee** — costs are incurred only when a member actually completes a transaction.
- **100% of the member's money goes to the owner's wallet** — the platform never touches it and never takes a cut from members.
- The platform only deducts a service fee from the owner's diamond balance **calculated at a 5% rate** when an order completes (anything under 1 diamond is rounded up to 1 diamond; low unit prices carry a clearly disclosed uplift) — **transparent, predictable, no hidden charges**.

In one sentence: **you pay only when you make a sale, money goes directly to the owner, and the rate is transparent.**

### 3. Goals & pain points solved

**Goal**: let anyone on Telegram turn an ordinary group into an "auto-charging paid group" with zero barriers.

Core pain points it solves:

| Pain point | Traditional approach | Hibuddy's approach |
|------|----------|----------------|
| Manual reconciliation and adding members after payment | Owner checks each payment, then invites manually | Auto-detects arrival, instantly sends invite link |
| Non-payers sneaking into the group | Manual patrol | Only members within the valid period are allowed |
| Expired members overstaying | Manually track time, manually kick | Auto-remove on expiry |
| Heavy monthly fee / platform cut pressure | Fixed monthly fee + cut | No monthly fee; fee calculated at 5% only on completion (rounded up to whole diamonds, disclosed uplift on low prices) |
| Unease about the platform holding funds | Money goes to the platform first, then settles | Money goes directly to the owner's wallet |

### 4. How it works now

Hibuddy's billing unit is called a **Diamond** — this is the "balance" on the owner's side. The logic is simple:

> 💎 **1 diamond ≈ 0.1 USD** (i.e., 1 USD ≈ 10 diamonds).

- Owners **top up diamonds** (via USDT, with top-up bonuses).
- When a member pays to join, the money goes **in full to the owner's wallet**; the platform only deducts the service fee for that order from the owner's diamonds **calculated at a 5% rate** (under 1 diamond counts as 1 diamond; low unit prices come with a clearly disclosed uplift) at the moment of completion.
- No completion, no charge — and no monthly fee at all.

For example: a group sets the entry fee at **20 USD**. A member pays 20 USD (in full to the owner's wallet), and the platform deducts the equivalent of 1 USD (about **10 diamonds**) from the owner as the service fee at 5%. The owner actually receives the member's 20 USD.

After a member pays, the bot automatically identifies which order it is by the **amount precise to the cent** (the same wallet receives transfers from many people at once); once matched, access is granted immediately. So the payment page gives a special reminder: **please transfer the exact amount shown on the page**.

Regarding expiry, the bot reminds members to renew before expiry and automatically removes them after expiry; it also uses a "remove then immediately unban" approach, ensuring expired members can smoothly return after paying again.

### 5. As a member, what do I do?

1. **Enter the bot**: tap the **promotion link** shared by the owner, or search `@hibuddy_ai_bot` on Telegram and send `/start`.
2. **Choose a group**: the bot lists the paid groups you can join, showing the **entry fee** and **service duration**; tap the one you want.
3. **Place an order and pay**: after choosing a payment method, you enter the payment page, which shows the **exact USDT amount** and the **receiving address / QR code**.
4. **Transfer**: open your wallet (TronLink, Trust Wallet, Binance, etc.), choose the **corresponding network (TRON TRC20 or Solana SPL)**, and send the **exact amount shown on the page**.
5. **Wait for auto-access**: the page automatically detects the arrival — **no extra action needed**. After confirmation you'll receive a **one-time invite link**; tap to join.

⚠️ A few reminders:
- Orders are **valid for 15 minutes**; if it times out, please don't pay — just place a new order.
- Be sure to transfer the **exact amount shown on the page** and use the **correct network (TRON TRC20 / Solana SPL)**, otherwise it may not be auto-detected / may cause a loss.
- **Payment goes directly to the owner's wallet** — no extra fees beyond the entry fee shown.

### 6. As a group owner, what do I do?

#### Step 1: Set up (one-time)

1. **Add the bot to your group and set it as admin**, granting three permissions: **ban users / invite users via link / delete messages**.
   → After joining, the bot **auto-binds to you** (bound to whoever invited it), with no extra verification needed.
2. **Message the bot privately** and send `/start`.
3. Tap **"I am a Group Owner"** to enter the group management page.
4. **Add a receiving wallet**: enter your USDT (TRON TRC20 or Solana SPL) receiving address.
   > 💡 The wallet configured by the owner is the payment method for potential members. **Currently supports USDT (TRON TRC20 and Solana SPL)**; **USDT (BSC network) is under development and not yet supported**.
5. **Configure the group**: select the wallet, set the **entry price** and **service duration (days)**, then **enable hosting mode**.

Once configured, your group officially enters "auto-charging" status.

#### Step 2: Daily operation (basically hands-off)

- After a member pays, the system auto-reconciles and grants access; **your wallet receives the full USDT instantly**.
- For each completed order, the system deducts the service fee from your diamonds **calculated at a 5% rate** (under 1 diamond counts as 1 diamond; low unit prices come with a clearly disclosed uplift) — no completion, no deduction.
- Expired members are auto-removed by the system; you don't need to manage manually.

#### Step 3: On-demand actions

- **Diamond top-up**: when your balance is low, initiate a USDT top-up in the dashboard (with bonuses).
- **Balance alerts**: when diamonds are running low, the bot proactively messages you to top up, avoiding impact on member entry.
- **Promotion links**:
    - **Group promotion link**: share with potential members; when they open it they see the list of groups you manage.
    - **Bot referral link**: share with other owners to help them get started too.
- **Pause / resume hosting anytime**: temporarily disable or re-enable a group's auto gatekeeper.

### 7. Limited-time offer

> 🎁 **For a limited time, you can claim 30 diamonds in the bot** — enough to get your group running and try it out at zero cost.
>
> Once this limited-time claim window closes, we'll most likely give existing users a solid subsidy (how exactly — let's figure it out together).
>
> In one sentence: **joining now is a win; early birds don't lose out.**

### 8. Contact

- Bot: [@hibuddy_ai_bot](https://t.me/hibuddy_ai_bot)
- Support / chat: `@hibuddyAi`
- Powered by Hibuddy.org

> If you're also working on Telegram-related projects or crypto payment services, feel free to connect~
>
> Welcome to exchange tech ideas; fellow practitioners can also come discuss and chat, improving together 🚀

---

## 繁體中文

**Hibuddy—讓 Telegram 付費群「自動收錢、自動放行、自動清理」**

> 一個面向 Telegram 付費社群的**自動門禁機器人**。
> 群主不用再手動對帳拉人，成員付完款秒進群，過期的人自動清走。

### 一、Hibuddy 是什麼

Hibuddy 是一個跑在 Telegram 上的**付費入群機器人**。

簡單說，它替群主幹三件事：

1. **收錢** —— 成員在機器人裡下單、轉帳，錢**直接進群主自己的錢包**。
2. **放行** —— 收到款後，機器人自動生成一次性邀請連結，成員點一下就進群。
3. **清理** —— 服務到期的成員自動被移出群，續費後可以再回來。

整個過程全自動，群主不需要盯著群、對帳單、手動拉人踢人。

目前支援 **USDT（TRON TRC20 與 Solana SPL）** 收款，介面支援**英 / 中 / 俄 / 西**四種語言。

### 二、為什麼要做這個

市面上做付費群、訂閱制內容的工具不少，但它們有個共同的痛點：

- **收費太貴**：普遍是**月費 / 訂閱費**起步，動輒每月幾十美金，不管你有沒有成交都要交錢。
- **平台抽成高、且不透明**：多數平台會從成員付的錢裡**抽成**，成員的付款先進平台、再結算給你，中間扣了多少往往說不清。
- **對小群主不友好（重要）**：剛起步、成員不多的群主，光是月費就是一筆固定負擔。

**Hibuddy 想做的正好相反：**

- **不收月費、不收訂閱費**，只有成員真正成交了才產生費用。
- **成員的錢 100% 進群主錢包**，平台不經手、不抽成員的錢。
- 平台只在每單成交時，按 **5% 的費率計算**從群主的餘額裡扣服務費（不滿一顆鑽石按一顆算，低單價時會有明示上浮），**透明、可預期、沒有隱藏收費**。

一句話：**走單才付費，錢直達群主，費率透明。**

### 三、目標 & 解決的痛點

**目標**：讓任何人在 Telegram 上，都能零門檻地把一個普通群變成一個「自動收費的付費群」。

它解決的核心痛點：

| 痛點 | 傳統做法 | Hibuddy 的做法 |
|------|----------|----------------|
| 收款後手動核對、手動拉人 | 群主逐筆對帳，再手動邀請 | 到帳自動識別，秒發邀請連結 |
| 沒付款的人混進群 | 人肉巡查 | 只放行有效期內成員 |
| 過期的人賴著不走 | 手動記時間、手動踢 | 到期自動移出 |
| 平台月費 / 抽成壓力大 | 固定月費 + 抽成 | 無月費，成交才按 5% 費率計算扣費（不滿一顆鑽石按一顆算，低單價有明示上浮） |
| 平台經手資金不放心 | 錢先進平台再結算 | 錢直接進群主錢包 |

### 四、現在是怎麼運作的

Hibuddy 的計費單位叫**鑽石（Diamond）**，這是群主這邊的「餘額」。邏輯很簡單：

> 💎 **1 顆鑽石折合約 0.1 USD**（即 1 USD ≈ 10 顆鑽石）。

- 群主**充值鑽石**（用 USDT 充值，有充值贈送）。
- 成員付費入群時，錢**全額進群主錢包**；平台只在成交那一刻，按 **5% 費率計算**（不滿 1 顆鑽石按 1 顆算，低單價時會有明示上浮）從群主鑽石裡扣掉這一單的服務費。
- 沒有成交就不扣費，也沒有任何月費。

舉個例子：某群入群費設為 **20 USD**，成員付了 20 USD（全額進群主錢包），平台按 5% 扣群主相當於 1 USD（約 **10 顆鑽石**）作為服務費。群主實際到手就是成員的 20 USD。

成員付款後，機器人靠「**精確到分的金額**」來自動識別是哪一筆訂單（同一錢包會同時收到很多人的轉帳），匹配成功後立即放行。所以支付頁會特別提醒：**請轉帳頁面顯示的準確金額**。

到期方面，機器人會在到期前提醒續費，到期後自動把成員移出群；而且採用了「移出後隨即解除拉黑」的方式，保證過期成員重新付款後還能順利回群。

### 五、作為群員，我該怎麼做

1. **進入機器人**：點擊群主分享的**推廣連結**，或在 Telegram 搜尋 `@hibuddy_ai_bot` 發送 `/start`。
2. **選群**：機器人會列出可加入的付費群，顯示**入群費用**和**服務時長**，點你想進的那個。
3. **下單付款**：選擇支付方式後進入支付頁，頁面會顯示**準確的 USDT 金額**和**收款地址 / 二維碼**。
4. **轉帳**：打開你的錢包（TronLink、Trust Wallet、幣安等），選**對應網路（TRON TRC20 或 Solana SPL）**，轉出**頁面顯示的精確金額**。
5. **等自動放行**：頁面會自動偵測到帳，**無需任何額外操作**。確認後你會收到一個**一次性邀請連結**，點擊即可進群。

⚠️ 幾個小提醒：
- 訂單**有效期 15 分鐘**，超時請勿付款，重新下單即可。
- 一定要轉**頁面顯示的準確金額**、用**正確的網路（TRON TRC20／Solana SPL）**，否則可能無法自動識別 / 造成損失。
- **付款直達群主錢包**，除顯示的入群費外，沒有額外費用。

### 六、作為群主，我該怎麼做

#### 第一步：開通配置（一次性）

1. **把機器人拉進群並設為管理員**，授予三項權限：**封禁使用者 / 透過連結邀請使用者 / 刪除訊息**。
   → 機器人入群後會**自動綁定給你**（誰邀請的就綁給誰），無需額外驗證。
2. **私聊機器人**，發送 `/start`。
3. 點擊 **「我是群主」**，進入群組管理頁面。
4. **新增收款錢包**：填入你的 USDT（TRON TRC20 或 Solana SPL）收款地址。
   > 💡 群主配置的收款錢包，即潛在群員的支付方式。**目前支援 USDT（TRON TRC20 與 Solana SPL）交易**；**USDT（BSC 網路）正在開發中，暫不支援**。
5. **配置群組**：勾選錢包、設定**入群價格**與**服務時長（天數）**，然後**開啟託管模式**。

配置完成，你的群就正式進入「自動收費」狀態了。

#### 第二步：日常營運（基本無感）

- 成員付款後系統自動對帳、放行，**你錢包即時收到全額 USDT**。
- 每成交一單，系統按 **5% 費率計算**扣你鑽石作為服務費（不滿 1 顆按 1 顆算，低單價時會有明示上浮），沒有成交不扣。
- 成員到期由系統自動移出，你無需手動管理。

#### 第三步：按需操作

- **鑽石充值**：餘額不足時，在後台發起 USDT 充值（含贈送）。
- **餘額預警**：鑽石快用完時，機器人會主動私信提醒你充值，避免影響成員入群。
- **推廣連結**：
    - **群組推廣連結**：分享給潛在成員，他們點開後能看到你管理的群組列表。
    - **機器人推薦連結**：分享給其他群主，幫他們也開始用。
- **隨時暫停 / 恢復託管**：可臨時停用或重新啟用某個群的自動門禁。

### 七、限時福利

> 🎁 **限時在機器人中可領取 30 顆鑽石**，夠你先把群跑起來、零成本試水。
>
> 限時領取結束後，大概率會給老用戶做實在的補貼（具體怎麼補，大家一起想想）。
>
> 一句話：**現在進來就是賺到，早鳥不虧。**

### 八、聯絡方式

- Bot：[@hibuddy_ai_bot](https://t.me/hibuddy_ai_bot)
- 客服 / 交流：`@hibuddyAi`
- Powered by Hibuddy.org

> 如果你也在做 Telegram 相關項目或幣圈支付相關服務，歡迎交流～
>
> 歡迎大家來交流技術，有同行也可以來討論吹水，互相進步 🚀

---

## Русский

**Hibuddy — пусть ваша платная Telegram-группа «сама принимает деньги, сама пропускает и сама удаляет»**

> Автоматический бот-шлагбаум для платных Telegram-сообществ.
> Владельцу больше не нужно вручную сверять платежи и добавлять участников — члены попадают в группу сразу после оплаты, а участники с истёкшим сроком удаляются автоматически.

### 1. Что такое Hibuddy?

Hibuddy — это **бот платного входа**, работающий в Telegram.

Проще говоря, он делает три вещи для владельца группы:

1. **Принимает деньги** — участники оформляют заказ и переводят средства прямо в боте; деньги идут **напрямую на кошелёк владельца**.
2. **Пропускает** — после получения оплаты бот автоматически создаёт одноразовую ссылку-приглашение; участник нажимает один раз и входит.
3. **Удаляет** — участники с истёкшим сроком обслуживания автоматически удаляются; после продления могут вернуться.

Весь процесс полностью автоматизирован — владельцу не нужно следить за группой, сверять выписки, вручную добавлять или удалять людей.

В настоящее время поддерживается приём **USDT (TRON TRC20 и Solana SPL)**, интерфейс доступен на **английском / китайском / русском / испанском**.

### 2. Зачем мы это сделали

На рынке немало инструментов для платных групп и подписочного контента, но у них есть общие недостатки:

- **Слишком дорого**: обычно начинаются с **ежемесячной / подписочной платы** — нередко десятки долларов в месяц, независимо от того, есть ли у вас продажи.
- **Высокая и непрозрачная комиссия платформы**: большинство платформ **берут процент** с платежей участников; деньги сначала поступают на платформу, затем перечисляются вам, и часто непонятно, сколько именно было удержано.
- **Недружелюбно к небольшим владельцам (важно)**: для тех, кто только начинает и имеет мало участников, одна лишь ежемесячная плата — это фиксированное бремя.

**Hibuddy стремится к противоположному:**

- **Без ежемесячной платы, без подписки** — расходы возникают только тогда, когда участник действительно совершает сделку.
- **100% денег участника идут на кошелёк владельца** — платформа не прикасается к ним и не берёт процент с участников.
- Платформа удерживает комиссию с алмазного баланса владельца **по ставке 5%** (сумма менее 1 алмаза округляется до 1 алмаза; при низкой цене применяется явно указанная надбавка) в момент завершения заказа — **прозрачно, предсказуемо, без скрытых платежей**.

Одной фразой: **платите только за совершённые сделки, деньги идут напрямую владельцу, ставка прозрачна.**

### 3. Цели и решаемые проблемы

**Цель**: позволить любому в Telegram без барьеров превратить обычную группу в «платную группу с автоматическим взиманием».

Ключевые проблемы, которые он решает:

| Проблема | Традиционный подход | Подход Hibuddy |
|------|----------|----------------|
| Ручная сверка и добавление участников после оплаты | Владелец проверяет каждый платёж, затем приглашает вручную | Автоматически определяет поступление, мгновенно отправляет ссылку-приглашение |
| Неплательщики проникают в группу | Ручной обход | Пропускаются только участники с действующим сроком |
| Участники с истёкшим сроком остаются | Вручную отслеживать время, вручную удалять | Автоматическое удаление по истечении |
| Давление ежемесячной платы / комиссии платформы | Фиксированная ежемесячная плата + комиссия | Без ежемесячной платы; расчёт по ставке 5% только при завершении (менее 1 алмаза округляется до 1; при низкой цене — явная надбавка) |
| Опасения по поводу удержания средств платформой | Деньги сначала на платформе, затем перечисляются | Деньги идут напрямую на кошелёк владельца |

### 4. Как это работает сейчас

Единица расчёта Hibuddy называется **Алмаз (Diamond)** — это «баланс» на стороне владельца. Логика проста:

> 💎 **1 алмаз ≈ 0,1 USD** (т.е. 1 USD ≈ 10 алмазов).

- Владелец **пополняет алмазы** (через USDT, с бонусами за пополнение).
- Когда участник платит за вход, деньги идут **в полном объёме на кошелёк владельца**; платформа удерживает комиссию за этот заказ с алмазов владельца **по ставке 5%** (менее 1 алмаза считается как 1 алмаз; при низкой цене — явно указанная надбавка) в момент завершения.
- Нет сделки — нет комиссии, и никакой ежемесячной платы.

Например: группа установила плату за вход **20 USD**. Участник платит 20 USD (полностью на кошелёк владельца), платформа удерживает эквивалент 1 USD (около **10 алмазов**) с владельца как комиссию по ставке 5%. Фактически владелец получает 20 USD участника.

После оплаты бот автоматически определяет, к какому заказу относится платёж, по **точной сумме до цента** (на один кошелёк одновременно приходят переводы от многих людей); после совпадения доступ предоставляется немедленно. Поэтому на странице оплаты есть особое напоминание: **переводите точную сумму, указанную на странице**.

Что касается истечения срока, бот напоминает о продлении до истечения и автоматически удаляет участника после истечения; при этом используется подход «удалить и сразу разбанить», что гарантирует беспрепятственное возвращение участника после повторной оплаты.

### 5. Что делать участнику

1. **Войдите в бота**: нажмите **реферальную ссылку**, которой поделился владелец, или найдите `@hibuddy_ai_bot` в Telegram и отправьте `/start`.
2. **Выберите группу**: бот покажет список платных групп, в которые можно вступить, с **платой за вход** и **сроком обслуживания**; выберите нужную.
3. **Оформите заказ и оплатите**: после выбора способа оплаты вы попадёте на страницу оплаты с **точной суммой в USDT** и **адресом получения / QR-кодом**.
4. **Переведите**: откройте кошелёк (TronLink, Trust Wallet, Binance и др.), выберите **соответствующую сеть (TRON TRC20 или Solana SPL)** и отправьте **точную сумму, указанную на странице**.
5. **Дождитесь автоматического доступа**: страница автоматически определит поступление — **никаких дополнительных действий не требуется**. После подтверждения вы получите **одноразовую ссылку-приглашение**; нажмите, чтобы войти.

⚠️ Несколько напоминаний:
- Заказ **действителен 15 минут**; если время вышло, не оплачивайте — просто оформите новый заказ.
- Обязательно переводите **точную сумму со страницы** и используйте **правильную сеть (TRON TRC20 / Solana SPL)**, иначе платёж может не определиться / это может привести к потере средств.
- **Платёж идёт напрямую на кошелёк владельца** — никаких дополнительных комиссий, кроме указанной платы за вход.

### 6. Что делать владельцу группы

#### Шаг 1: Настройка (однократно)

1. **Добавьте бота в группу и назначьте администратором**, предоставив три разрешения: **банить пользователей / приглашать пользователей по ссылке / удалять сообщения**.
   → После входа бот **автоматически привязывается к вам** (к тому, кто его пригласил), без дополнительной проверки.
2. **Напишите боту лично** и отправьте `/start`.
3. Нажмите **«Я владелец группы»**, чтобы перейти на страницу управления группой.
4. **Добавьте кошелёк для приёма**: укажите ваш адрес получения USDT (TRON TRC20 или Solana SPL).
   > 💡 Кошелёк, настроенный владельцем, — это способ оплаты для потенциальных участников. **Сейчас поддерживается USDT (TRON TRC20 и Solana SPL)**; **USDT (сеть BSC) в разработке, но пока не поддерживается**.
5. **Настройте группу**: выберите кошелёк, задайте **цену входа** и **срок обслуживания (в днях)**, затем **включите режим хостинга**.

После настройки ваша группа официально переходит в режим «автоматического взимания».

#### Шаг 2: Повседневная работа (практически незаметно)

- После оплаты участника система автоматически сверяет и предоставляет доступ; **ваш кошелёк мгновенно получает полную сумму в USDT**.
- За каждый завершённый заказ система удерживает с вас алмазы по ставке 5% как комиссию (менее 1 алмаза считается как 1 алмаз; при низкой цене — явно указанная надбавка) — нет сделки, нет удержания.
- Участники с истёкшим сроком автоматически удаляются системой; вам не нужно управлять вручную.

#### Шаг 3: Действия по необходимости

- **Пополнение алмазов**: при недостатке баланса инициируйте пополнение через USDT в панели (с бонусами).
- **Оповещение о балансе**: когда алмазы заканчиваются, бот сам напишет вам с напоминанием пополнить, чтобы не повлиять на вход участников.
- **Реферальные ссылки**:
    - **Ссылка на группу**: поделитесь с потенциальными участниками; открыв её, они увидят список ваших групп.
    - **Ссылка на бота**: поделитесь с другими владельцами, чтобы помочь им тоже начать.
- **Пауза / возобновление хостинга в любое время**: можно временно отключить или снова включить автоматический шлагбаум группы.

### 7. Ограниченное предложение

> 🎁 **Сейчас в боте можно получить 30 алмазов — акция ограничена по времени** — этого достаточно, чтобы запустить группу и попробовать без затрат.
>
> Когда окно ограниченного получения закроется, мы, скорее всего, сделаем действующим пользователям существенную субсидию (как именно — давайте подумаем вместе).
>
> Одной фразой: **войти сейчас — это выгода; ранние участники не прогадают.**

### 8. Контакты

- Бот: [@hibuddy_ai_bot](https://t.me/hibuddy_ai_bot)
- Поддержка / общение: `@hibuddyAi`
- Работает на платформе Hibuddy.org

> Если вы тоже занимаетесь проектами в Telegram или сервисами крипто-платежей, будем рады общению~
>
> Приглашаем обмениваться техническими идеями; коллеги по цеху тоже могут присоединиться к обсуждению и прогрессировать вместе 🚀

---

## Español

**Hibuddy — Haz que tu grupo de pago de Telegram «cobre, dé acceso y limpie» automáticamente**

> Un bot portero automático para comunidades de pago de Telegram.
> El administrador ya no concilia pagos ni añade miembros manualmente — los miembros entran al instante tras pagar, y los que caducan se eliminan automáticamente.

### 1. ¿Qué es Hibuddy?

Hibuddy es un **bot de entrada de pago** que funciona en Telegram.

En pocas palabras, hace tres cosas por los administradores de grupos:

1. **Cobra** — los miembros hacen pedidos y transfieren fondos dentro del bot; el dinero va **directamente a la billetera del administrador**.
2. **Da acceso** — al recibir el pago, el bot genera automáticamente un enlace de invitación de un solo uso; el miembro toca una vez y entra.
3. **Limpia** — los miembros cuyo servicio caducó se eliminan automáticamente; pueden volver tras renovar.

Todo el proceso es completamente automático — el administrador no necesita vigilar el grupo, conciliar estados de cuenta ni añadir/eliminar gente manualmente.

Actualmente admite **USDT (TRON TRC20 y Solana SPL)** para pagos, y la interfaz está disponible en **inglés / chino / ruso / español**.

### 2. Por qué lo creamos

Hay muchas herramientas para grupos de pago y contenido por suscripción en el mercado actual, pero comparten puntos débiles:

- **Demasiado caras**: suelen empezar con una **cuota mensual / de suscripción** — a menudo decenas de dólares al mes, vendas o no.
- **Comisiones de plataforma altas y opacas**: la mayoría de plataformas **retienen un porcentaje** de lo que pagan los miembros; los pagos van primero a la plataforma y luego se te liquidan, y a menudo no está claro cuánto se descontó.
- **Poco amigables con los administradores pequeños (importante)**: para quien empieza y tiene pocos miembros, solo la cuota mensual ya es una carga fija.

**Hibuddy busca lo contrario:**

- **Sin cuota mensual, sin suscripción** — los costes solo se generan cuando un miembro realmente completa una transacción.
- **El 100% del dinero del miembro va a la billetera del administrador** — la plataforma nunca lo toca ni retiene un porcentaje de los miembros.
- La plataforma solo descuenta una comisión del saldo de diamantes del administrador **calculada al 5%** cuando se completa un pedido (lo que no alcance 1 diamante se redondea a 1 diamante; a bajo unitario hay un recargo expresamente indicado) — **transparente, predecible, sin cargos ocultos**.

En una frase: **pagas solo cuando vendes, el dinero va directo al administrador y la tarifa es transparente.**

### 3. Objetivos y puntos débiles que resuelve

**Objetivo**: permitir que cualquiera en Telegram convierta sin barreras un grupo normal en un «grupo de pago con cobro automático».

Puntos débiles clave que resuelve:

| Punto débil | Enfoque tradicional | Enfoque de Hibuddy |
|------|----------|----------------|
| Conciliación y añadido manual de miembros tras el pago | El administrador revisa cada pago y luego invita manualmente | Detecta la llegada automáticamente y envía al instante el enlace de invitación |
| Los que no pagan se cuelan en el grupo | Patrulla manual | Solo se admite a miembros dentro del periodo válido |
| Los miembros caducados se quedan | Controlar el tiempo y expulsar manualmente | Eliminación automática al caducar |
| Presión por cuota mensual / comisión de plataforma | Cuota mensual fija + comisión | Sin cuota mensual; cálculo al 5% solo al completar (menos de 1 diamante cuenta como 1; a bajo precio, recargo indicado) |
| Inquietud por la plataforma reteniendo fondos | El dinero va primero a la plataforma y luego se liquida | El dinero va directo a la billetera del administrador |

### 4. Cómo funciona ahora

La unidad de facturación de Hibuddy se llama **Diamante** — es el «saldo» del lado del administrador. La lógica es sencilla:

> 💎 **1 diamante ≈ 0,1 USD** (es decir, 1 USD ≈ 10 diamantes).

- El administrador **recarga diamantes** (con USDT, con bonos por recarga).
- Cuando un miembro paga por entrar, el dinero va **íntegro a la billetera del administrador**; la plataforma solo descuenta la comisión de ese pedido de los diamantes del administrador **calculada al 5%** (menos de 1 diamante cuenta como 1 diamante; a bajo unitario se indica un recargo expreso) en el momento de completarse.
- Sin transacción no hay cargo, y ninguna cuota mensual.

Por ejemplo: un grupo fija la tarifa de entrada en **20 USD**. Un miembro paga 20 USD (íntegro a la billetera del administrador), y la plataforma descuenta el equivalente a 1 USD (unos **10 diamantes**) del administrador como comisión al 5%. El administrador recibe realmente los 20 USD del miembro.

Tras pagar, el bot identifica automáticamente a qué pedido corresponde mediante el **importe exacto al céntimo** (la misma billetera recibe transferencias de mucha gente a la vez); una vez coincidido, concede acceso de inmediato. Por eso la página de pago recuerda especialmente: **transfiere el importe exacto que muestra la página**.

En cuanto a la caducidad, el bot recuerda renovar antes de caducar y elimina automáticamente al miembro tras caducar; además usa un enfoque de «eliminar y desbloquear de inmediato», garantizando que los miembros caducados puedan volver sin problemas tras pagar de nuevo.

### 5. Como miembro, ¿qué hago?

1. **Entra en el bot**: toca el **enlace de promoción** compartido por el administrador, o busca `@hibuddy_ai_bot` en Telegram y envía `/start`.
2. **Elige un grupo**: el bot lista los grupos de pago a los que puedes unirte, mostrando la **tarifa de entrada** y la **duración del servicio**; toca el que quieras.
3. **Haz el pedido y paga**: tras elegir un método de pago, entras en la página de pago, que muestra el **importe exacto en USDT** y la **dirección de recepción / código QR**.
4. **Transfiere**: abre tu billetera (TronLink, Trust Wallet, Binance, etc.), elige la **red correspondiente (TRON TRC20 o Solana SPL)** y envía el **importe exacto que muestra la página**.
5. **Espera el acceso automático**: la página detecta automáticamente la llegada — **no se necesita ninguna acción extra**. Tras la confirmación recibirás un **enlace de invitación de un solo uso**; toca para entrar.

⚠️ Algunos recordatorios:
- Los pedidos son **válidos durante 15 minutos**; si caduca, no pagues — simplemente haz un pedido nuevo.
- Asegúrate de transferir el **importe exacto de la página** y usar la **red correcta (TRON TRC20 / Solana SPL)**, o puede que no se detecte automáticamente / cause una pérdida.
- **El pago va directo a la billetera del administrador** — sin cargos extra más allá de la tarifa de entrada mostrada.

### 6. Como administrador de grupo, ¿qué hago?

#### Paso 1: Configuración (una sola vez)

1. **Añade el bot a tu grupo y asígnalo como administrador**, concediendo tres permisos: **banear usuarios / invitar usuarios por enlace / eliminar mensajes**.
   → Tras entrar, el bot **se vincula automáticamente a ti** (a quien lo invitó), sin verificación adicional.
2. **Escribe al bot en privado** y envía `/start`.
3. Toca **«Soy administrador de grupo»** para entrar en la página de gestión del grupo.
4. **Añade una billetera de recepción**: introduce tu dirección de recepción de USDT (TRON TRC20 o Solana SPL).
   > 💡 La billetera configurada por el administrador es el método de pago para los miembros potenciales. **Ahora admite USDT (TRON TRC20 y Solana SPL)**; **USDT (red BSC) está en desarrollo pero aún no se admite**.
5. **Configura el grupo**: selecciona la billetera, fija el **precio de entrada** y la **duración del servicio (días)**, y luego **activa el modo de gestión**.

Una vez configurado, tu grupo entra oficialmente en estado de «cobro automático».

#### Paso 2: Operación diaria (prácticamente sin esfuerzo)

- Tras el pago de un miembro, el sistema concilia y concede acceso automáticamente; **tu billetera recibe el USDT completo al instante**.
- Por cada pedido completado, el sistema te descuenta diamantes **calculados al 5%** como comisión (menos de 1 diamante cuenta como 1 diamante; a bajo unitario hay un recargo expreso) — sin transacción, sin descuento.
- Los miembros caducados se eliminan automáticamente; no necesitas gestionar manualmente.

#### Paso 3: Acciones bajo demanda

- **Recarga de diamantes**: cuando el saldo es bajo, inicia una recarga con USDT en el panel (con bonos).
- **Alertas de saldo**: cuando los diamantes se agotan, el bot te escribe proactivamente para recordarte recargar, evitando afectar la entrada de miembros.
- **Enlaces de promoción**:
    - **Enlace del grupo**: compártelo con miembros potenciales; al abrirlo verán la lista de grupos que gestionas.
    - **Enlace del bot**: compártelo con otros administradores para ayudarles a empezar también.
- **Pausar / reanudar la gestión cuando quieras**: puedes desactivar o reactivar temporalmente el portero automático de un grupo.

### 7. Oferta por tiempo limitado

> 🎁 **Ahora puedes reclamar 30 diamantes en el bot — oferta por tiempo limitado** — suficiente para poner en marcha tu grupo y probarlo sin coste.
>
> Cuando se cierre este periodo de reclamación limitada, lo más probable es que demos a los usuarios antiguos una subvención sólida (cómo exactamente — pensadlo con nosotros).
>
> En una frase: **entrar ahora es ganar; los que llegan pronto no pierden.**

### 8. Contacto

- Bot: [@hibuddy_ai_bot](https://t.me/hibuddy_ai_bot)
- Soporte / chat: `@hibuddyAi`
- Desarrollado por [Hibuddy.org](https://hibuddy.org)

> Si también trabajas en proyectos de Telegram o servicios de pago con criptomonedas, ¡conectemos!
>
> Bienvenido a intercambiar ideas técnicas; los colegas del sector también pueden unirse a la discusión y progresar juntos 🚀
