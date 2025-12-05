🎲 Tenzies Game – React Project

A fun, interactive dice game built with React, Vite, and nanoid, featuring holdable dice, confetti when the player wins, and smooth gameplay.

<details> <summary>📌 What is Tenzies?</summary>

Tenzies is a dice game where the goal is simple:

Roll the dice until all dice show the same number.

Click a die to hold (freeze) its value.

Roll again to update only the un-held dice.

When all dice match AND all are held → 🎉 You win!

</details>
✨ Features

🎯 Click dice to hold/unhold

🔄 Roll button re-rolls only un-held dice

🎉 Confetti animation when all dice match

🔢 Unique IDs for each die using nanoid

⚡ Built with Vite for fast development

📱 Responsive and simple UI

📸 Live Demo (Optional)

(Add your Vercel/Netlify link here once deployed)

https://your-tenzies-app-url.com

📁 Project Structure
src/
│── App.jsx          # main game logic
│── dice.jsx         # Die component
│── index.css        # Styling
│── main.jsx         # React DOM mount
│── assets/          # optional images or icons

🚀 Installation & Setup

Clone the repository:

git clone https://github.com/your-username/tenzies-react.git
cd tenzies-react


Install dependencies:

npm install


Run development server:

npm run dev


Build for production:

npm run build


Preview production build:

npm run preview

🧩 How It Works (Game Logic Explained)
1. Each die is an object:
{
  value: number,
  isHeld: boolean,
  id: nanoid()
}

2. hold(id)

Toggles a die’s isHeld value.

3. rollDice()

If game not won → rolls only un-held dice

If won → resets game with fresh dice

4. Win Condition:
const gameWon =
  dice.every(die => die.isHeld) &&
  dice.every(die => die.value === dice[0].value)

🧨 Dependencies
Package	Purpose
React	UI rendering
Vite	Fast bundler/dev server
nanoid	Create unique IDs
react-confetti	Victory animation

Install manually if needed:

npm install nanoid react-confetti

🎨 Styling

The index.css file contains:

Dice grid layout

Roll button styles

Held-dice green color

Main layout and typography

📦 Deployment

You can deploy easily on:

Vercel (Recommended)

Push to GitHub

Import repo into Vercel

Build command: npm run build

Output: dist

Netlify

Drag & drop dist/ folder
or

Connect Git repo directly

📜 License

This project is open-source and available for personal or educational use.

👨‍💻 Author

Jayram Sangawat
Feel free to reach out for improvements or suggestions!