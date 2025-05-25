NHL Analytics Dashboard
An interactive sports analytics dashboard demonstrating end-to-end data analysis skills with configurable team targeting.

Project Overview
This project demonstrates:

Production API Integration: Working with official NHL APIs that power nhl.com
Data Engineering: Data collection, validation, and storage
Sports Analytics: Hockey-specific metrics and insights
Interactive Visualization: Web-based dashboard for data exploration
Current Status: Basic Dashboard Ready
Data Collection Complete:

Team schedules and rosters for multiple teams
Database with teams, players, games, and shot events schema
Play-by-play collection system built
Dashboard Built:

Basic web interface with colored header
Player data table display
Team dropdown (Toronto Maple Leafs / St. Louis Blues)
Responsive table with player information
Quick Start
1. Add Blues Data (if needed)
uv run python add_blues_data.py
2. Run Dashboard
uv run python app.py
3. View Dashboard
Open browser to: http://127.0.0.1:8050

4. Optional: Collect Play-by-Play Data
uv run python scripts/collect_play_by_play.py
Project Structure
nhl-analytics-dashboard/
├── app.py                         # Main dashboard application
├── data/
│   ├── collectors/
│   │   └── web_api_collector.py   # NHL API client
│   ├── database.py                # SQLite database operations
│   └── nhl_api.py                 # Unified API interface
├── scripts/
│   ├── initial_data_load.py       # Team schedule/roster collection
│   └── collect_play_by_play.py    # Game event collection
├── add_blues_data.py              # Add St. Louis Blues data
├── verify_data.py                 # Data verification script
├── check_database.py              # Database contents checker
├── config.py                      # Team and season configuration
└── requirements.txt               # Python dependencies
Technology Stack
Backend: Python + Pandas for data processing
APIs: Official NHL production APIs (api-web.nhle.com)
Database: SQLite (development) → PostgreSQL (production)
Dashboard: Dash + Plotly (Phase 3)
What's Available Now
Dashboard Features:

Colored header bar with NHL branding
Team selection dropdown (Toronto Maple Leafs / St. Louis Blues)
Player data table with complete roster information
Responsive design with sortable columns
Player Data Displayed:

Season information
Position groups (Forwards, Defensemen, Goalies)
Jersey numbers and player names
Physical stats (height, weight)
Birth information and nationality
Shooting/catching preference
Next Development Steps
Collect Shot Data: Run play-by-play collection for game events
Add Visualizations: Shot charts, performance graphs
Enhanced Filtering: Season selection, position filtering
Team Comparisons: Side-by-side team analysis
Configuration
Key settings in config.py:

AVAILABLE_TEAMS: Dictionary of team codes and names
TEAM_CODE: "TOR" (configurable for data collection)
TARGET_SEASONS: ["20232024", "20242025"]
API_RATE_LIMIT_DELAY: 1.0 seconds
CACHE_ENABLED: True
Basic dashboard is functional. Team dropdown switches between Toronto Maple Leafs and St. Louis Blues player data.

