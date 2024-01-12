FROM tiangolo/uvicorn-gunicorn-fastapi:python3.8

COPY ./app /app
WORKDIR /app

RUN pip install -r requirements.txt

CMD ["alembic", "revision", "--autogenerate", "-m", "initial"]
CMD ["alembic", "upgrade", "head"]
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80", "--reload"]


