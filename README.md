git clone https://github.com/yourgithubusername/akiya-crisis.git
cd akiya-crisis
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
pip install -r requirements.txt
DATABASE_URL=your_database_connection_string
FLASK_SECRET_KEY=your_secret_key
PORT=5000
flask run
docker build -t akiya-crisis-backend .
docker run -d -p 5000:5000 --env-file .env akiya-crisis-backend
