# Мета роботи

Розібрати принципи та базові команди для роботи з git. Створити опис для свого акаунта GitHub.

# Хід роботи

1. Створити обліковий запис GitHub

![](account.png)

2. Встановити CHOCOLATEY за допомогою powershell:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```


3. Встановити git на комп'ютер за допомогою Chocolatey:
```
choco install git -y
```
Перевіряємо правильність установки. Для цього дізнаємось версію встановленого гіт.

![](gitversion.png)

4. Налаштувати гіт за своїми даними:
```
git config --global user.name "MykolaOverko"
git config --global user.email m.v.overko@student.khai.edu
```

5. Згенерувати новий SSH ключ:
```
ssh-keygen -t ed25519 -C "m.v.overko@student.khai.edu"
```

Ключ було згенеровано за шляхом "H:\orchad\work\.ssh\" у файлі id_ed25519.pub

6. Додати ключ до облікового запису Github:

![](sshkey.png)

7. Створити новий репозиторій з назвою такою ж як і назва акаунту:

![](repository.png)

8. Склонувати репозиторій за допомогою git clone на локальний пк та відредагувати README.md:

![](readme.png)

9. Завантажити опис профілю:
```
git add .
git commit -m "Add your comment"
git push
```

![](page.png)

Висновок

Після виконання лабораторної роботи було здобуто знання щодо використання git та GitHub. Засвоєно принципи роботи з репозиторіями та необхідні дії для зміни, додання або видалення файлів з них. Розглянуто форматування тексту для файлу README.md.
