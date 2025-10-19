CPU Jumper:
An interactive, retro-arcade platformer designed to simulate and teach the Shortest Remaining Time First (SRTF) CPU scheduling algorithm. 

🎮 Concept Explained
Shortest Remaining Time First (SRTF) is a preemptive scheduling algorithm where the process with the smallest remaining execution time is selected to run next. If a new process arrives with a shorter remaining time than the one currently running, the CPU is preempted (taken away) from the current process and given to the new, shorter one.

This game turns that concept into a fast-paced platformer:
-You are the CPU Dispatcher.
-The "Jobs" (blocks) are Processes moving along the ready queue.
-The number on each block is its Remaining Time (RT).
-Jumping is how you ignore an arriving job.
-Staying on the ground means you intercept and consider a job for processing.
-The goal is to always be processing the job with the lowest remaining time, even if it means preempting your current job for a new, shorter one.

🕹️ Gameplay & Objective
The goal is not just to get a high score, but to achieve the lowest possible Average Wait Time (AWT). A low AWT proves your scheduling decisions were efficient!

How to Play
Start: Click the START RUNNER button.
Jump: Press the SPACEBAR or UP ARROW key to jump over incoming jobs. You have a triple-jump!
Schedule: When a job block reaches you, the game automatically makes the SRTF decision:
If your CPU is idle, you will automatically start processing the job.
If you are busy and the new job's RT is less than your current job's RT, you will preempt and switch to the new, shorter job.
If you are busy and the new job's RT is longer, you will take a penalty! Your only way to avoid this is to jump over the longer job.

Game Elements
Green Blocks (Short Jobs): Low remaining time. Usually safe to process.
Gray Blocks (Medium Jobs): Moderate remaining time.
Red Blocks (Long Jobs): High remaining time. These are dangerous! Avoid them if you're already processing a shorter job.
Patience Meter: The bar above each job. If it runs out while a job is waiting, the job "corrupts" and the game ends!
Average Wait Time (AWT): Your primary performance metric. Keep this as low as possible! The game ends if your AWT gets too high.

✨ Features
Interactive SRTF Simulation: Learn a core Operating Systems concept through engaging gameplay.
Endless Survival Mode: The game gets progressively faster and harder. How long can you manage the queue?
Persistent High Scores: Your best performance (lowest AWT) is saved automatically.
Global Leaderboard: Compete with others for the most efficient scheduling score, powered by Google Firestore.
Post-Game Gantt Chart: After a game ends, click the GANTT CHART button to see a visual analysis of your scheduling decisions.
Pause & Resume: Take a break anytime by pressing the PAUSE button or the 'P' key.

🛠️ Tech Stack
Frontend: HTML5, CSS3, Vanilla JavaScript
Backend & Database: Google Firestore (for leaderboard and high score storage)
Font: Press Start 2P by Google Fonts

🚀 How to Run Locally
Clone the repository:

Bash

git clone https://github.com/your-username/your-repo-name.git
Navigate to the project directory:

Bash

cd your-repo-name
Open index.html:

Simply open the index.html file in your web browser. The game is fully client-side and will run instantly.

Note: The leaderboard and high score saving features require a Firebase configuration. The game is coded to handle a missing configuration gracefully and will still be playable.

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.
