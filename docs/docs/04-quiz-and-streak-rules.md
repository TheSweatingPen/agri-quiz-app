# Quiz & Streak Logic

## How Instant Ranking Works
- **Per-Quiz Rank:** When a student finishes a quiz, we compare their `score` and `timeTaken` against everyone else who took *that exact quiz*. Highest score wins. If tied, fastest time wins.
- **Daily Rank:** Resets at 00:00 (Africa/Lagos time). Sum of all XP earned that day.
- **All-Time Rank:** Total XP accumulated since registration.

## How the Streak Works
- A student opens the app and completes at least one quiz.
- The system checks `lastStreakDate`. 
- If `lastStreakDate` was **yesterday**, `currentStreak` increases by 1.
- If `lastStreakDate` was **today**, nothing changes.
- If `lastStreakDate` was **before yesterday**, `currentStreak` resets to 1.
- **Reward:** For every day of the streak, they earn `currentStreak * 10` XP. (e.g., Day 3 = 30 XP).

## Analytics Tracking
- Accuracy = (Total Correct Answers / Total Questions Answered) * 100
- Weak Topics = Any topic where the student's accuracy is below 50%.
