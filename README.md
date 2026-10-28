# tfjzl-final-cloud-app-with-database

Django Online Course app with an assessment (exam) feature: questions with choices, learner
submissions, and an exam result page.

## Run locally

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python3 manage.py makemigrations onlinecourse
python3 manage.py migrate
python3 manage.py createsuperuser
python3 manage.py runserver
```

- Site: http://127.0.0.1:8000/
- Admin: http://127.0.0.1:8000/admin/ (add a course with an image, lessons, questions and choices)

## Where the exam code lives

- `onlinecourse/models.py` - `Question`, `Choice`, `Submission`
- `onlinecourse/admin.py` - `QuestionInline`, `ChoiceInline`, `QuestionAdmin`, `LessonAdmin`
- `onlinecourse/views.py` - `submit`, `show_exam_result`
- `onlinecourse/urls.py` - routes for `submit` and `show_exam_result`
- `onlinecourse/templates/onlinecourse/course_details_bootstrap.html` - course page with lessons and exam
- `onlinecourse/templates/onlinecourse/exam_result_bootstrap.html` - exam result page
