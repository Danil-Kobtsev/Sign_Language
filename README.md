# Sign_Language
## 1. Структура проекта
  
    ├── data                        <- Папка в которую требуется загрузить данные
    ├── model                       <- Jupyter Notebook в котором содержится код программы
    └── README.md
## 2. Загрузка данных проекта
  Для того, что бы скачать данные для данной задачи необходимо:
  1. Перейти по [ссылке](https://www.kaggle.com/datasets/datamunge/sign-language-mnist)
  2. Скачать файлы: sign_mnist_test.csv, sign_mnist_train.csv
  3. Поместить данные в папку /data
## 3. Подготовка и запуск проекта
### Создать виртуальное окружение
Создать виртуально окружение с именем dvc-venv

    python3 -m venv dvc-venv
    echo "export PYTHONPATH=$PWD" >> dvc-venv/bin/activate
    source dvc-venv/bin/activate
    
Загрузить все библиотеки

    pip install -r requirements.txt

Добавить виртуальное окружение в jupiter notebook

    python -m ipykernel install --user --name=dvc-venv
    
### Запуск ноутбука
Код хранится в папке `/models`. Для копирования ноутбука:
  1. Добавьте строку к `gitignore`

    model/*
    git add .gitignore
    git commit -m "Update .gitignore: add model/* " 
 
  2. Переместите ноутбук и закомментируйте это:

    git rm --cached model/*
    git commit -m "Unstage notebooks" 
  
  3. Запустите ноутбук:

    jupyter notebook
  
    
