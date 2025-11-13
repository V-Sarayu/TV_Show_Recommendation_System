# Movie & TV Show Recommendation System  
### *A Streamlit + MySQL Powered OTT Analytics Dashboard*

---

##  Overview  
This project is a **Movie & TV Show Recommendation System** built using **Streamlit** for the frontend and **MySQL** for the backend. It allows users to:

- Register new users  
- Log movie/TV show watch history  
- Rate movies and write reviews  
- View personalized recommendations (via SQL triggers & logic)  
- Explore an analytics dashboard with computed insights  

The application demonstrates a full-stack DBMS project with real-time interactions, SQL-based recommendation logic, and an intuitive user interface.

---

## Tech Stack  
- **Frontend:** Streamlit  
- **Backend:** Python  
- **Database:** MySQL  
- **UI Components:** `streamlit-option-menu`, custom CSS styling  
- **DBMS Features:**  
  - Stored Functions  
  - Joins & Aggregations  
  - Triggers for automatic recommendation generation  
  - User-watch analytics  

---

## Features Breakdown  

###  **1. Add User**  
- Create new user profiles  
- Stores Name, Email, Age, Country, Subscription Type  
- Auto-generates **User ID**  
- Displays confirmation with balloons 🎉  

###  **2. Watch Movie**  
- Select user & movie  
- Log watch duration and timestamp  
- Updates `WATCH_HISTORY` table  

###  **3. Rate Movie**  
- Users can rate movies from 0.0–5.0  
- Add text reviews  
- Triggers may generate new recommendations  

###  **4. View Recommendations**  
- Fetches recommendations from the `RECOMMENDATION` table  
- Displays movie title, reason, and content ID with a styled card UI  

###  **5. Analytics Dashboard**  
Shows personalized insights using SQL functions:

- Total Movies Watched  
- Favorite Genre  
- Average Rating  

Uses:
- `GetUserWatchCount(user_id)`
- `GetFavoriteGenre(user_id)`
- `AVG(Rating_Value)`  

---

##  Database Requirements  

### Required Tables:
- `USER`
- `MOVIE`
- `WATCH_HISTORY`
- `RATING`
- `RECOMMENDATION`

### Required Stored Functions:
- `GetUserWatchCount(USER_ID)`
- `GetFavoriteGenre(USER_ID)`

### Optional DBMS Enhancements:
- Recommendation triggers  
- Movie similarity table  
- Genre classification  


