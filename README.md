# 🎤 Sing Out: A Karaoke Queue Manager

A lightweight, interactive CLI application written in Python to manage karaoke night song requests, queue orders, and singer line-ups seamlessly.

---

## 🌟 Features

- **Queue Visualization:** Easily view the current list of queued singers and their chosen tracks in order.
- **Add Singers:** Enqueue new singers with automatic string cleaning and input validation.
- **Next Up (`pop`):** Call up the next singer in line, automatically removing them from the front of the queue.
- **VIP Bump (`move_to_top`):** Priority management to move any queued singer straight to position #1.
- **Remove Singer:** Search and remove a specific singer by name if they change their mind or step out.
- **Input Guarding:** Built-in exception handling for invalid numeric inputs or non-existent singer positions.

---

## 🚀 How It Works

The program uses a Python `list` of `tuples` where each entry represents `("Singer Name", "Song Title")`. 

Commands available during the session:
* `add` - Prompts for a singer's name and song, adding them to the end of the queue.
* `next` - Pops the first singer in line and displays **NOW UP**.
* `top` - Takes a positional number (e.g., `3`) and bumps that singer to #1.
* `remove` - Prompts for a singer's name and removes them from the list.
* `quit` - Exits the application.

---

## 📋 Example Usage

```text
============================================
Welcome to Sing Out: A Karaoke Queue Manager
============================================

Current queue:

1. Annie - Celebration
2. Allen - Get The Party Started
3. Lionel - Dancing On The Ceiling
4. Jenny - Let's Get Loud

Options:  add / next / top / remove / quit
> top
Who do you want to move to the top? Enter a number: 3

Moved Lionel to the top of the queue!

Current queue:

1. Lionel - Dancing On The Ceiling
2. Annie - Celebration
3. Allen - Get The Party Started
4. Jenny - Let's Get Loud

Options:  add / next / top / remove / quit
> next

NOW UP: Lionel - Dancing On The Ceiling
