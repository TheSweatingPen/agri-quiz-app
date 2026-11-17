# Frontend UI & Folder Structure

## Next.js App Router Structure
```text
app/
├── (auth)/
│   ├── login/page.tsx          # Matric No + Password
│   └── register/page.tsx       # Student sign up
├── (dashboard)/
│   ├── layout.tsx              # Sidebar & Header for logged-in users
│   ├── page.tsx                # Student Home (Streak, XP, Quick Play)
│   ├── quizzes/
│   │   ├── page.tsx            # List of available quizzes
│   │   └── [id]/page.tsx       # Active Quiz interface (Timer, Questions)
│   ├── leaderboard/page.tsx    # Tabs: Per-Quiz, Daily, All-Time
│   ├── analytics/page.tsx      # Charts: Accuracy, Weak Topics
│   └── admin/                  # Protected for Class Rep & Admin only
│       ├── page.tsx            # Admin Dashboard
│       ├── students/page.tsx   # Manage students / Approve regs
│       └── questions/page.tsx  # Add/Edit past questions
