# Automatic Text Summarizer

A user-friendly web app with responsive design.
It was built as a final year project for college.
Key Persons: 
Vijay Shrestha(CSIT):- Front End/Summarizing Algorithm(Word Frequency)
Vijay's Repo: https://github.com/vjstha20

Sudip Basnet(CSIT):- Backend(Database)

## Features:
- Summarize both English and Nepali text.
- Summarize text via either copy-paste paragraph or URL.
- User can save summarized text.
- View top 5 trending summarized news from BBC, CNN and Nagarik News.
- Summarize pdf file to text file.

User can choose one of the following algorithms for text summarization:
- Frequency Algorithm
- Sentence Matching

## Installation

1. Go to folder you want to put the cloned project in your terminal & type:
    `git clone https://github.com/xanjay/Automatic-Text-Summarizer.git`

2. Install the project dependencies:
    `pip install -r requirements.txt`

3. In settings.py, replace value of SECRET_KEY with your own key.
```SECRET_KEY = os.environ.get('SECRET_KEY', '-1')```
- You can generate your secret key [here](https://www.miniwebtool.com/django-secret-key-generator/)

4. Create database named 'text_summarizer' in MySQL via cmd or phpmyadmin.
- Edit your database credentials in following lines in settings.py
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'text_summarizer',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': '',
        'PORT': '',
    }
}
```

5. In the terminal:
    `$ python manage.py migrate` - this will apply migrations to your local MySQL database
    `$ python manage.py createsuperuser` - this will create admin support
    * Run server as: ``` $ python manage.py runserver ```
