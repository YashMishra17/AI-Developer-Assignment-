🚀 Dumroo.ai — AI-Powered Student Query System

✨ Overview

Dumroo.ai lets school admins ask plain English questions about student activity and performance, while enforcing role-based access control (RBAC).

Example queries:

📝 “Which students haven’t submitted their homework yet?”

📊 “Show me performance data for Grade 8 from last week”

🗓️ “List all upcoming quizzes scheduled for next week”

Results are scoped to the admin’s grade, class, and region, ensuring privacy.

⚡ Features

Natural-Language Query Parsing: Rule-based parser detects intent and extracts slots (grade, dates). Upgradeable to LLM/NLP.

Role-Based Access Control (RBAC): Admins see only their assigned students.

Data Operations: Missing homework, performance summaries (count, mean, min, max), upcoming quizzes.

Optional Streamlit Demo: Interactive web UI for live queries.

📂 Dataset

File: data/students_data.csv

Columns: student_name, grade, class, region, homework_submitted, quiz_score, quiz_date, quiz_topic, submission_date

Auto-created if missing; small demo dataset included.

🛠 Installation & Usage

Clone & install dependencies:

git clone https://github.com/YOUR_GITHUB_USERNAME/dumroo-ai-assignment.git
cd dumroo-ai-assignment
pip install -r requirements.txt


Jupyter Notebook: Open dumroo_assignment.ipynb → run all cells.

Streamlit Demo (Optional):

streamlit run streamlit_app.py


Example admin context:

admin = {'name':'Alice','grade':8,'class':'A','region':'East'}
handle_query("Which students haven't submitted their homework yet?", admin)

📈 Example Outputs

Missing homework:

student_name	grade	class	region	homework_submitted
John Doe	8	A	East	No
Anita Rao	8	A	East	No

Performance summary:

{"count":2,"mean":83.5,"min":75,"max":92}


Upcoming quizzes: Shows only quizzes in admin’s scope and next week.
