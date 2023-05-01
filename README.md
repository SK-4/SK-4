import datetime
import random
import requests

# Hello there! 👋

# SK-4: passionate Python developer and data science enthusiast. Pursuing Honours in AI and enjoys learning about data structures, algorithms, and ML.

## 🔭 I’m currently working on
# Interesting Python, Django, and ML projects. Check out my repositories to learn more!

## 🌱 I’m currently learning
# Data Science, Machine Learning, and Django. Always looking to improve my skills and build better applications.

## 👯 I’m looking to collaborate on
# New and exciting Python projects with Django. Reach out to me if you have any interesting ideas or projects.

## 💬 Ask me about
# Python, Django, Data Science, or Machine Learning. Happy to help and share my knowledge.

## 📫 How to reach me
# Contact me via my LinkedIn profile: https://www.linkedin.com/in/soham-kshirsagar4/. Let's connect and discuss some exciting new projects!

## ⚡ Fun fact
# Apart from coding, I love to play typing games and improve my typing speed.

# Add some dynamic elements
now = datetime.datetime.now()
hour = now.hour
greetings = ["Good morning!", "Hello there!", "Good afternoon!", "Hey, how's it going?"]
greeting = random.choice(greetings)

if hour >= 5 and hour < 12:
    greeting = "Good morning!"
elif hour >= 12 and hour < 17:
    greeting = "Good afternoon!"
elif hour >= 17 and hour < 21:
    greeting = "Good evening!"
else:
    greeting = "Hello there!"

# Display the dynamic elements
print(f"{greeting} I'm SK-4, and this is my profile!")
print("Let's work together to build some amazing applications using Python and Django! 😃")

# Display some of your recent GitHub commits
print("\nHere are some of my latest commits:")
url = "https://api.github.com/users/SK-4/events"
response = requests.get(url)
events = response.json()

commits = []
for event in events:
    if event["type"] == "PushEvent":
        for commit in event["payload"]["commits"]:
            commits.append(commit["message"])
        if len(commits) >= 3:
            break

for commit in commits:
    print(f"- {commit}")

# Display your achievements
print("\nHere are some of my achievements:")
achievements = ["Published a research paper on ML in a top-tier conference", "Built a recommendation engine with Django and ML", "Won a hackathon with my team using Python and Django"]

for i, achievement in enumerate(achievements, 1):
    print(f"{i}. {achievement}") 

