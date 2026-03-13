# website-blocker-using-python


This Python script is your digital parent (but cooler because you coded it yourself). It automatically blocks distracting websites during your working hours by messing with your computer's host file.

Websites it blocks:

Facebook (because doom-scrolling kills productivity)

Other distracting sites you add to the list

🧠 What I learned building this
This project made me feel like a hacker (even though it's super simple). I figured out:

The Host File exists?! - Every computer has this secret file that maps website names to IP addresses

File manipulation in Python - Reading, writing, and truncating files like a pro

Scheduling scripts - Making code run automatically (no more "oh I forgot to run it")

Windows Task Scheduler - That thing nobody uses but actually kinda useful

Time-based logic - Checking if it's work hours vs. fun hours

⚙️ How it works (the magic behind the curtain)
The host file is like your computer's phonebook:

Normally: facebook.com → Facebook's actual server

With my script: facebook.com → 127.0.0.1 (your own computer)

So when you try to visit Facebook, your computer just talks to itself. Embarrassing but effective!

🕒 During work hours:
Script adds website entries to host file

Websites = blocked

You = productive (hopefully)

🌙 After work hours:
Script removes those entries

Websites = accessible

You = free to waste time guilt-free

🚀 How to set it up
bash
# Just run the script (but there's more to it...)
python website_blocker.py
For it to work automatically:
Change your script extension from .py to .pyw (so it runs silently in background)

Open Windows Task Scheduler (search for it in Start menu)

Create a new task with:

Name: "Website Blocker" (or something dramatic)

Check "Run with highest privileges" (needs admin access to edit host file)

Trigger: "At startup" (so it's always running)

Action: Point to your .pyw file

Conditions: Uncheck power stuff so it runs even on laptop

Restart your computer and watch the magic happen!

📁 Important paths (from the PDF)
Host file locations:

Windows: C:\Windows\System32\drivers\etc\hosts

Mac/Linux: /etc/hosts

📸 About those PDF screenshots
The PDF has like 8 pages with screenshots of Task Scheduler. I was REALLY proud of figuring out how to schedule tasks. "Look everyone, my script runs AUTOMATICALLY now!"

Future me looking back: "Why did I take screenshots of every single dialog box?"
Also future me: "Actually... this is kind of helpful for remembering the steps" 😅

⚠️ Note to future self
Running this as administrator, editing system files, scheduling tasks - this was my "I'm basically a sysadmin now" era. The script probably needs paths updated if you ever get a new computer, but the concept still works!

💭 College Kid Logic
"Instead of just... not going to Facebook during work hours, I'll spend 5 hours coding a script to block it for me."

Peak productivity irony. No regrets.
