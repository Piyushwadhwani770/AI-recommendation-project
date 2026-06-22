# AI Recommendation Logic 

# Project Title

*Personalized Movie Recommendation System Using Python*

# Objective

The objective of this project is to develop a simple recommendation system that suggests movies to users based on their interests. The system uses pattern matching and similarity logic to compare user preferences with movie categories and recommend the most suitable options.

# Introduction

Recommendation systems are widely used in platforms such as Netflix, YouTube, Amazon, and Spotify. They help users discover relevant content according to their preferences. In this project, a basic recommendation engine is created using Python. The system asks users about their interests and recommends movies that match those interests.

# Problem Statement

Users often spend a lot of time searching for content that matches their preferences. The aim of this project is to automate the process by recommending movies based on selected interests.

# Methodology

1. Create a dataset containing movies and their genres.
2. Take user interests as input.
3. Compare user interests with movie genres.
4. Calculate similarity using matching logic.
5. Display recommended movies.

# Python Source Code

```python
movies = {
    "Interstellar": ["science", "space", "adventure"],
    "Avengers Endgame": ["action", "superhero", "adventure"],
    "The Conjuring": ["horror", "thriller"],
    "3 Idiots": ["comedy", "education", "drama"],
    "Dangal": ["sports", "drama", "motivation"],
    "Bahubali": ["action", "history", "adventure"]
}

print("Available Interests:")
print("action, comedy, horror, science, sports, education, adventure")

user_input = input("Enter your interests separated by commas: ")
user_interests = [interest.strip().lower() for interest in user_input.split(",")]

recommendations = []

for movie, genres in movies.items():
    score = len(set(user_interests) & set(genres))
    if score > 0:
        recommendations.append((movie, score))

recommendations.sort(key=lambda x: x[1], reverse=True)

print("\nRecommended Movies:")
for movie, score in recommendations:
    print(movie, "- Match Score:", score)
```

# Sample Input

```text
action, adventure
```

# Sample Output

```text
Recommended Movies:
Avengers Endgame - Match Score: 2
Bahubali - Match Score: 2
Interstellar - Match Score: 1
```

# Results

The system successfully recommends movies based on user interests. Higher match scores indicate stronger similarity between user preferences and movie genres.

# Applications

* Movie Recommendation Systems
* E-commerce Product Suggestions
* Music Streaming Platforms
* Online Learning Platforms
* Social Media Content Recommendations

# Future Enhancements

* Use larger datasets.
* Add machine learning algorithms.
* Implement user ratings.
* Store user history for better recommendations.
* Develop a graphical user interface.

# Conclusion

This project demonstrates the basic working of a recommendation system using pattern matching and similarity logic. It successfully identifies user preferences and recommends relevant movies. The project helps in understanding the fundamentals of recommendation engines used in modern AI applications.
