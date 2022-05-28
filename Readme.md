Nama : Christio Danny Gratia Ambarita
NIM : 14117153

Judul Program : Aliens.py

Deskripsi Program : 

Cara menjalankan Container :

1. Pertama membuat folder app, kemudian masukkan file aliens.py ke dalam folder tersebut
2. Setelah itu tekan "ctrl + shift + p" dan ketik "Python: Create Terminal"
3. Setelah masuk ke terminal python, ketik "python -m venv venv" (untuk Windows)
4. Lalu aktifkan venv tadi dengan mengetik ". venv/Scripts/activate" (untuk Windows)
5. Setelah itu tekan "pip install uvicorn", "pip install fastapi", dan "pip install pygame"
6. masukkan kode berikut ke dalam aliens.py :

        from fastapi import FastAPI

        import uvicorn

        app = FastAPI()

        dibagian awal

        dan 

        if __name__ == '__main__': uvicorn.run(app, port=8000, host="0.0.0.0")

        dibagian akhir
7. Setelah itu, input "pip freeze > requirements.txt" pada terminal
8. Kemudian buat file bernama "Dockerfile" dan isilah file tersebut dengan kode berikut :

        FROM python:3.10

        WORKDIR /fastapi-app

        COPY requirements.txt . 

        RUN pip install -r requirements.txt

        COPY ./app ./app

        CMD ["python", "./app/aliens.py"]

9. Lalu input "docker build -t python-fastapi ."
10. Lalu input "docker run -p 8000:8000 python-fastapi" dan tekan "ctrl + left klik" pada link yang tersedia.