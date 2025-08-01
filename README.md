# 📊 Проект: Анализ резюме с HeadHunter

Добро пожаловать в мой первый проект в рамках курса **Data Science** от [SkillFactory](https://skillfactory.ru/).  
В этом проекте проводится **разведывательный анализ (EDA)** данных о соискателях вакансий с сайта HeadHunter.

---

## 🧠 Цель проекта

Изучить датасет с резюме, обработать его, очистить от выбросов и аномалий, провести базовую статистику и визуализацию, а также:
- преобразовать текстовые данные;
- заполнить пропуски;
- выявить выбросы (в т.ч. по z-отклонениям);
- понять структуру и закономерности в данных.

---

## 🗃️ Датасеты

### 📥 Основной датасет с резюме:
- [Скачать с Google Drive](https://drive.google.com/file/d/1Kb78mAWYKcYlellTGhIjPI-bCcKbGuTn/view?usp=sharing)

### 💱 Дополнительный датасет — курсы валют:
- [Скачать ExchangeRates.zip (SkillFactory)](https://lms-cdn.skillfactory.ru/assets/courseware/v1/15abf80f45a2f3e93c3274101b451c67/asset-v1:SkillFactory+DSPR-2.0+14JULY2021+type@asset+block/ExchangeRates.zip)

---

## 🧾 Содержание ноутбука

### 1. 📥 Загрузка и первичная очистка данных
- Загрузка данных о резюме.
- Просмотр структуры, типов данных, пропусков.

### 2. 🛠️ Обработка признаков
- Преобразование "Опыт работы" из строкового формата в **количество месяцев**.
- Удаление ненужных колонок.

### 3. 🧹 Заполнение пропусков и фильтрация
- Пропуски в **"Опыт работы (месяц)"** заполняются **медианой**.
- Удаляются строки с пустыми значениями в **"Последнее место работы"** и **"Последняя должность"**.

### 4. 📏 Удаление выбросов
- Заработная плата: удаляются значения < 1 000 или > 1 000 000 руб.
- Логическая ошибка: опыт > возраст — удаляются.
- Возраст: используется логарифм + метод z-отклонения (асимметрия вправо, выбросы с +4σ).

### 5. 📈 Визуализация
- Построение графиков распределения возраста (в логарифмах).
- Линии среднего и ±3σ на графике.
- Комментарии по асимметрии и структуре данных.

---

## 📌 Инструкция по запуску

1. Установи зависимости:

```bash
pip install pandas numpy matplotlib seaborn
