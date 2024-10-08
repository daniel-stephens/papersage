# **PaperSage**

PaperSage is a Django-based web application that leverages GPT, LangChain, and a Retrieval-Augmented Generation (RAG) model to assist users in reviewing research papers. The app features a chat interface for interactive paper analysis, a section for selecting research papers as context, and a repository of previous conversations.

## **Features**

- **Chat Interface**: Engage with an AI to analyze research papers interactively.
- **Context Selection**: Select research papers to use as context for the conversation.
- **Conversation History**: Review and revisit previous conversations for further insights.

---

## **Getting Started**

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### **Prerequisites**

- Python 3.8 or higher
- Django 4.0 or higher
- OpenAI API Key (for GPT)
- LangChain (for seamless integration of the RAG model)
- PostgreSQL or SQLite (for database)

### **Installation**

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/papersage.git
cd papersage
```
2. **Create and activate a virtual environment**
```bash
   python3 -m venv env
   source env/bin/activate
```
3. **Install dependencies**
```bash
pip install -r requirements.txt
```
Make sure to include necessary libraries in the requirements.txt:
```bash
  Django>=4.0
  openai
  langchain
  djangorestframework
  psycopg2 (if using PostgreSQL)
```
Create a .env file in the project root and add your OpenAI API Key and other relevant configurations:

4. **Set up environment variables**
   ```bash
      OPENAI_API_KEY=your_openai_api_key
      DJANGO_SECRET_KEY=your_secret_key
      DEBUG=True
      DATABASE_URL=your_database_url (if using PostgreSQL)
   ```
5. ** Run migrations **
  ``` bash
      python manage.py migrate
  ```
6. ** Create a superuser (to access the Django admin) **
  ```bash
      python manage.py createsuperuser
  ```
7. **Run the development server**
  ``` bash
      python manage.py runserver
      The app should now be running at http://localhost:8000/.
  ```

  ### **Project Structure**
  ``` bash
    papersage/
    │
    ├── app/
    │   ├── models.py          # Models for research papers, chat history, etc.
    │   ├── views.py           # View logic for chat, paper selection, etc.
    │   ├── urls.py            # URL routing
    │   ├── templates/         # HTML templates for the frontend
    │   └── static/            # Static files (CSS, JS)
    │
    ├── chat/
    │   ├── gpt_integration.py  # GPT and LangChain RAG model integration
    │   └── conversation.py     # Logic to manage chat history
    │
    ├── manage.py              # Django management script
    ├── requirements.txt       # Required dependencies
    └── .env                   # Environment variables
```
    
  License
  This project is licensed under the MIT License – see the LICENSE file for details.
  
  Acknowledgements
  OpenAI for GPT-3.
  LangChain for RAG model support.
  Django for the web framework.
    
    
