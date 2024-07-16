# Lrimport sqlite3
from datetime import datetime

# Improvement Projects Management
def create_improvement_projects_database(db_name='improvement_projects.db'):
    conn = sqlite3.connect(db_name)
    cursor = conn.cursor()
    cursor.execute('''
    CREATE TABLE IF NOT EXISTS projects (
        id INTEGER PRIMARY KEY,
        name TEXT,
        description TEXT,
        start_date TEXT,
        end_date TEXT
    )
    ''')
    conn.commit()
    conn.close()

def add_improvement
