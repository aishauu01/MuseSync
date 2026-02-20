🎵 MuseSync
MuseSync is a futuristic, AI-powered music recommendation agent. It combines vector-based semantic search with a conversational LLM to find the perfect tracks for your mood.

MuseSync UI (Note: Add a screenshot of your app here)

✨ Features
Mood-Based Recommendations: Chat with the bot to describe your vibe, and get semantically matched song suggestions from a vector database.
Conversational AI: Powered by Gemma 3 (via Ollama) to explain why a song fits your mood.
Glassmorphism UI: A sleek, dark-mode interface with animated backgrounds and particle effects.
Split-Screen Design:
Left: Persistent chat interface with a fixed input box.
Right: Scrollable playlist with one-click Spotify playback.
"I'm Feeling Lucky": Randomly generates a mood prompt to discover new music.
Spotify Integration: Embeds a Spotify player directly in the app.
🛠️ Tech Stack
Frontend: Streamlit
LLM: Ollama (Model: gemma3:latest)
Vector DB: ChromaDB
Orchestration: LangChain
Data Processing: Pandas
🚀 Getting Started
Prerequisites
Install Python 3.10+
Install Ollama: Download from ollama.com.
Pull the Model:
ollama pull gemma3:latest
Note: You can change the model in main.py if you prefer another one like llama3.
Installation
Clone the repository (or download files):

git clone <your-repo-url>
cd muse-sync
Install Dependencies:

pip install -r requirements.txt
Prepare Data:

Ensure you have a deduplicated_music_data.csv (or similar dataset) in the project root.
Run the vector ingestion script (only needed once to build chroma_music_mood_db):
python vector.py
Running the App
streamlit run main.py
The app will open in your browser at http://localhost:8501.

📂 Project Structure
main.py: The main Streamlit application (UI and Logic).
vector.py: Handles data loading, embedding generation, and ChromaDB management.
requirements.txt: Python package dependencies.
chroma_music_mood_db/: Directory containing the vector database (generated).
🎨 Customization
UI Tweaks: Check the CSS block in main.py to adjust colors, animations, or layout.
Prompt Engineering: Modify the ChatPromptTemplate in main.py to change how the bot speaks.
🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

📄 License
MIT# MuseSync
