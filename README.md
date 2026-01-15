# Travel-Planner-Project

**Overview**
The AI Agentic Travel Planner is a sophisticated, end-to-end automation tool designed to solve the problem of fragmented travel planning. Unlike static travel guides, this application acts as an autonomous agent that conducts real-time web research to provide accurate, up-to-date, and personalized itineraries based on a user's unique profile.

**Approach**

*Agentic Reasoning:* Powered by Google Gemini 2.0 Flash, the agent uses LangChain to process user intent and determine when to trigger external tools.

*Real-Time Research:* Integrated with the Tavily Search API, the system performs targeted searches for current visa requirements, seasonal weather forecasts, and local dining recommendations, effectively eliminating AI "hallucinations".

*Structured State Management:* Uses Python’s TypedDict to maintain a "TravelState," ensuring that data flows fluidly between the search phase and the itinerary generation phase.

*User-Centric Interface:* A multi-step Streamlit dashboard manages the "Hostel Room" of user inputs, providing a seamless experience from questionnaire to a downloadable Markdown itinerary.

**Problem Solved**
Traditional AI often gives outdated travel advice (e.g., suggesting a restaurant that closed in 2023). This project solves that by forcing the LLM to verify facts through an online search loop before drafting the final response. It prioritizes budget-conscious planning and practical logistics like visa entries, making it a "source-world" tool for real travelers.

# Setup and Installation - 

1. **Clone the repository and navigate to the folder:**
   cd travel_planner

2. **Install the dependencies:**
   pip install -r requirements.txt

3. **Configure API Keys:**
   Create a .env file in the root directory and add your keys:
   GEMINI_API_KEY=your_key_here
   TAVILY_API_KEY=your_key_here

4. **Run the application:**
   streamlit run app.py
