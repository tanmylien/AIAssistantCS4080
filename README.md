# Assignment #2 AI ASSISTANT

## 📦 How to Run the Program

### Step 1: Clone this repository
Open your terminal and run:

**git clone https://github.com/your-username/AIAssistantCS4080.git**
**cd AIAssistantCS4080/source_code**

Make sure Python is installed

### Step 2: Run the assistant
In the source_code folder, launch the assistant with:

**python main.py**

### Step 3: Interact with the assistant
The program will prompt you for your name, age, and whether you’re a premium user.
Then you can type in requests like:
	•	_"Play me something calm"_
	•	_"I want to build muscle"_
	•	_"Help me study for math"_
	•	_"Recommend a good fantasy book"_
	•	_"I'm feeling overwhelmed"_

**Free vs Premium Users**
	•	Free users can interact with assistants, but are limited to 3 high-level requests per session.
	•	Premium users have unlimited access.

## 🔍 Overview of the Assistant Functionality

This AI Assistant simulates a modular, multi-functional virtual assistant that can interact with users across various domains. Based on user input and preferences, it dynamically selects the appropriate assistant subclass to handle specific types of requests. Each assistant responds with customized messages and behaviors based on the context.

### Supported Functionalities:
	•	🎵 **Music Assistant (MUSIC)**
Recommends music playlists based on the user’s current mood, favorite artists, or activities. Offers a wide variety of emotional tones and genres to suit personal preferences.
	•	💪 **Fitness Assistant (FITNESS)**
Suggests fitness plans, workout schedules, and exercises tailored to the user’s body goals and available time. Differentiates plans based on intensity and user fitness level.
	•	📚 **Study Assistant (STUDY)**
Helps users study smarter by offering personalized study tips, topic explanations, and the ability to schedule sessions based on areas of difficulty.
	•	🧠 **Psychology Assistant (PSYCHOLOGY)**
Acts as a conversational AI psychologist. Listens to the user’s thoughts, offers helpful coping strategies for stress, burnout, or mild depression, and provides insights into psychological phenomena when users are curious.
	•	📖 **Book Assistant (BOOK)**
Recommends books using keywords in user descriptions and genre preferences. Also provides online links to read or purchase recommended books.
	•	💬 **General Assistant (GENERAL)**
Handles general, undefined inputs in a friendly, helpful way when no specific category is matched. Ensures the conversation continues smoothly even with vague or ambiguous requests.

## Concepts Implemented
	•	**Custom Data Types**:
Defined UserProfile, Request, and Response in models.py using @dataclass.
	•	**Validation / Type-Safety:**
Validation logic is in the __post_init__ methods of the data classes to ensure correct data types and constraints.
	•	**Enumeration:**
CommandType enum in models.py defines valid request types (e.g., MUSIC, STUDY).
	•	**Inheritance & Polymorphism:**
AIAssistant is the base class in base_assistant.py.
MusicAssistant, FitnessAssistant, and others override handleRequest() and greetUser() for customized responses.
	•	**Dynamic Behavior & Object Simulation:**
In main.py, multiple user profiles are created and handled dynamically using their command types to choose the appropriate assistant.
	•	**Command Parsing (Bonus):**
classify_command() in main.py uses string matching to simulate intent recognition.
