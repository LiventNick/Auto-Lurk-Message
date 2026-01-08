# Twitch Auto Lurk (Toggle + Countdown)

A Twitch userscript that automatically sends periodic chat messages while you lurk — complete with a top‑navigation toggle, countdown timer, tooltip, and stream‑awareness logic.

## ✨ Features

- **Auto Chat Messages**  
  Sends a random message from your custom list every 15–25 minutes (configurable).

- **Top Navigation Toggle**  
  A clean on/off switch appears next to the Twitch Prime icon.

- **Live Countdown Timer**  
  Shows time until the next message, with color‑coded urgency:
  - 🟩 Green — plenty of time  
  - 🟨 Yellow — halfway  
  - 🟥 Red — almost time  

- **Stream Awareness**  
  Auto‑Lurk only runs when the stream is live.  
  Stops automatically when offline.

- **Persistent Settings**  
  Toggle state is saved using `localStorage`.

- **Safe Chat Injection**  
  Messages are pasted into the chat box and sent normally.

## ⭐ Why This Script Exists
Twitch doesn’t officially document how it decides who counts as an active viewer, but recently a lot of community testing has suggested something important:
If you stay inactive for too long, Twitch may quietly stop counting you as a real viewer.

That means:

- **You’re still watching the stream**

- **You’re still supporting the creator**

- **But the viewer count may no longer include you**

People noticed this happening especially when lurking for long periods without chatting or interacting.

So I made this script to help with that.
It sends a small, harmless chat message every once in a while — just enough activity to show Twitch that you’re still present and engaged. This helps ensure you continue to count as a real viewer while you lurk and support your favorite streamers.


---

## 📥 Installation

### **Option 1 — Tampermonkey (Recommended)**
1. Install Tampermonkey:
   - Chrome: https://www.tampermonkey.net/?ext=dhdg&browser=chrome  
   - Firefox: https://www.tampermonkey.net/?ext=dhdg&browser=firefox  
   - Edge: https://www.tampermonkey.net/?ext=dhdg&browser=edge

     I do note that Tampermonkey may not work in browser's like Brave Broswer so I will recommend [ViolentMonkey](https://violentmonkey.github.io/) instead.

2. Click this link to install the script:  
   **[Install Userscript Via GreasyFork](https://greasyfork.org/en/scripts/561777-twitch-auto-lurk-toggle-countdown)**  

3. Approve the installation.

### **Option 2 — Manual Install**
1. Open Tampermonkey → **Create a new script**  
2. Delete everything in the editor  
3. Paste the entire script  
4. Save

---

## ⚙️ Configuration

Inside the script, you can edit:

You can change what messages you want to send

A random delay is picked between the the MAX_DELAY_MINUTES and MIN_DELAY_MINUTES, you can change these values
```
js
const MIN_DELAY_MINUTES = 15;
const MAX_DELAY_MINUTES = 25;

const MESSAGES = [
    "Hey there!",
    "Just Lurking Over here, don't mind me",
    "Do you know the muffin man?",
    "Quackers"
  ];
```
