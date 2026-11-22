# Calorie Tracker

A simple website that works out how many calories you should eat each day to lose weight, and lets you log what you eat.

## What it does

1. **Questionnaire.** The first time you open it, it asks for your sex, age, weight, height, how active you are and how fast you want to lose weight. It then works out your daily calorie goal.
2. **Daily food log.** Type what you ate and how many calories it had, and pick the meal (breakfast, lunch, dinner or snack).
3. **Today's progress.** A ring shows how much of your goal you've eaten and how many calories you have left. Use the arrows to look back at earlier days.
4. **One-tap re-adding.** Foods you've logged before appear as buttons, so you can add your usual breakfast in one tap. Typing a food you've had before fills in its calories for you.
5. **Settings.** Change your goal by hand, redo the questionnaire as your weight drops, or save and restore a backup file.

## Talking to it

Under **What did you eat?**, tap **Talk** and say what you had, for example "two eggs, a slice of toast with butter and a coffee with milk", or just type it. It recognises about 150 common foods, your regular meals and anything you've logged before, and shows the calories for you to check before adding. Foods it doesn't know yet are listed with an empty box: type the calories once and it remembers them next time. Tick **Remember this as a regular meal** to add the whole meal in one tap later.

Talking uses your phone browser's own free speech-to-text (Chrome on Android works best). If the Talk button doesn't appear, use the microphone on your phone's keyboard instead.

A smarter version that also understands photos and any dish, powered by Claude, runs inside Claude (see the project thread).

## How to open it

**On your computer:** download `index.html` from this repository and double-click it. It opens in your web browser. No installation is needed.

**On your phone (recommended):** put it online for free with GitHub Pages:

1. On this repository's GitHub page, go to **Settings → Pages**.
2. Under "Branch", choose the branch with `index.html` (usually `main`) and the folder `/ (root)`, then press **Save**.
3. After a minute or two, GitHub shows your website's address, which looks like `https://kyriakoss99.github.io/calorie-tracker/`.
4. Open that address on your phone. To make it feel like an app:
   - **iPhone (Safari):** tap the Share button, then **Add to Home Screen**.
   - **Android (Chrome):** tap the ⋮ menu, then **Add to Home screen** (or **Install app**).

   It then opens full screen with its own icon, like a normal app, and keeps working without an internet connection.

## Where your data is kept

Everything you enter stays on your own phone or computer, inside your browser. Nothing is sent to a server, and nobody else can see it. This also means:

- Your phone and your computer each keep their own separate log.
- If you clear your browser's history or site data, your log is erased. Use **Settings → Save a backup file** now and then to keep a copy.

## How the goal is calculated

- **Resting burn (BMR)** uses the Mifflin-St Jeor formula: 10 × weight(kg) + 6.25 × height(cm) − 5 × age, then +5 for men or −161 for women.
- **Daily burn (TDEE)** is the resting burn multiplied by your activity level (1.2 for mostly sitting up to 1.9 for extremely active).
- **Weight-loss cut:** about 7,700 kcal equals 1 kg of body fat, so losing 0.25 / 0.5 / 0.75 kg a week means eating about 275 / 550 / 825 kcal a day less.
- **Safety limits:** the cut is never more than 25% of your daily burn, and the goal never goes below 1,500 kcal for men or 1,200 kcal for women. If your BMI is already under 18.5, it suggests keeping your weight steady instead. Under-18s can only choose "keep my weight the same".

This is an estimate, not medical advice. If your weight hasn't changed after 3–4 weeks, redo the questionnaire or lower your goal by 100–200 kcal.
