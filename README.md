# 🌐 Language / Язык

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## <a name="russian"></a> 

# Разведочный анализ данных авиакомпаний и аэропортов

## 📌 О проекте

Проект выполнен в рамках курса **"Исследование данных и визуализация"** (Майнор НИУ ВШЭ, 1 семестр).  

**Задача:**  
На основе данных об оценках работы аэропортов и авиалиний (Skytrax reviews) провести разведочный анализ и ответить на вопросы заказчика:

- какие проблемы есть в авиаперевозках  
- какие улучшения можно предложить на основе выводов по данным

**Источник данных:**  
[Skytrax reviews dataset](https://github.com/quankiquanki/skytrax-reviews-dataset/blob/master/README.md)

> ⚠️ **Важно:** Хоть источник данных находится в открытом доступе и приведен выше, исходные данные для приведенной работы (то есть конкретная выборка) хранились на университетском сервере, доступ к которому в настоящее время отсутствует.  
> Поэтому **Rmd-код не может быть выполнен**, но результаты исследования сохранены в HTML-отчёте и дашборде.

---

## 📁 Содержимое репозитория

| Файл | Описание |
|------|----------|
| `analysis.Rmd` | Исходный код на R отчёта |
| `dashboard.html` | **Показательный дашборд** с ключевыми метриками |
| `dashboard_code.Rmd` | Исходный код дашборда |
| `report.html` | **HTML-отчёт** с разведочным анализом, графиками и выводами |
| `Задание.png` | Скриншот задания с платформы ВШЭ |
| `Оценка_отзыв.png` | Скриншот оценки с платформы ВШЭ |

---

## 🔍 Что было сделано

### Анализ (3 исследовательских вопроса)

| Вопрос | Вывод |
|--------|-------|
| **1.** Правда ли оценка ширины кресла выше, если перелет был в летнее время? | **Нет.** Летом оценка ширины кресел ниже, чем в другие месяцы. |
| **2.** В каких самолётах выше оценки удобства пространства для ног — с двумя проходами или с одним? | **С двумя проходами.** Комфорт выше. |
| **3.** Какие лаунж-зоны оценены по чистоте выше, чем аэропорты, в которых они расположены? | Выявлено **217** таких аэропортов. В отчёте приведён топ-5 с наибольшей разницей оценок. |

### Дашборд (flexdashboard)

Включены элементы:

- **ValueBox:** количество проходов, предпочитаемое пассажирами (ответ на вопрос 2)
- **ValueBox:** количество аэропортов, где лаунж-зона чище аэропорта (217)
- **Boxplot:** распределение оценок ширины кресла в зависимости от времени года
- **Bar chart:** топ-5 аэропортов с наибольшей разницей между чистотой лаунж-зоны и чистотой аэропорта

---

## 🎓 Оценка и отзыв преподавателя

**Оценка:** 9.5 / 10.0  
**Преподаватель:** Суворова Алёна Владимировна  

**Отзыв:**  
> *Отличная работа! Четко прослеживается логика, хорошие графики.*

**Замечания, учтённые в финальной версии:**
- Вопрос 3: вместо ссылки на переменную (`otv`) выведен **топ-5** аэропортов с наибольшей разницей оценок
- Изменена цветовая гамма графиков (улучшена контрастность, убран серый контур у пурпурных столбцов)

---

## 🚀 Как просмотреть результат

- Откройте **`report.html`** в браузере — полный отчёт с выводами  
- Откройте **`dashboard.html`** — интерактивный дашборд с ключевыми метриками

---

## 🛠 Инструменты

- R  
- dplyr, ggplot2, lubridate, stringr  
- flexdashboard  
- html_document

---

## 📌 Автор

Подолин Дмитрий   
НИУ ВШЭ, курс "Исследование данных и визуализация"

---

## <a name="english"></a> 🇬🇧 English

# Exploratory Data Analysis of Airlines and Airports

## 📌 About the project

The project was completed as part of the **"Data Research and Visualization"** course (HSE Minor, 1st semester).

**Task:**  
Based on data on the performance of airports and airlines (Skytrax reviews), conduct an exploratory analysis and answer the client's questions:

- what problems exist in air transportation  
- what improvements can be proposed based on the data findings

**Data source:**  
[Skytrax reviews dataset](https://github.com/quankiquanki/skytrax-reviews-dataset/blob/master/README.md)

> ⚠️ **Important:** Although the data source is publicly available and provided above, the specific dataset used for this work was stored on a university server that is currently inaccessible.  
> Therefore, **the Rmd code cannot be executed**, but the results are preserved in the HTML report and dashboard.

---

## 📁 Repository contents

| File | Description |
|------|-------------|
| `analysis.Rmd` | R source code for the report |
| `dashboard.html` | **Demonstration dashboard** with key metrics |
| `dashboard_code.Rmd` | Dashboard source code |
| `report.html` | **HTML report** with exploratory analysis, graphs, and conclusions |
| `Задание.png` | Screenshot of the assignment from the HSE platform |
| `Оценка_отзыв.png` | Screenshot of the grade from the HSE platform |

---

## 🔍 What was done

### Analysis (3 research questions)

| Question | Conclusion |
|----------|------------|
| **1.** Is it true that seat width ratings are higher for flights taken in summer? | **No.** In summer, seat width ratings are lower than in other months. |
| **2.** Which aircraft have higher legroom comfort ratings — those with two aisles or one? | **Two aisles.** Comfort is higher. |
| **3.** Which lounges are rated higher for cleanliness than the airports they are located in? | **217** such airports were identified. The report includes the top 5 with the largest rating differences. |

### Dashboard (flexdashboard)

Includes:

- **ValueBox:** preferred number of aisles (answer to question 2)
- **ValueBox:** number of airports where lounge cleanliness exceeds airport cleanliness (217)
- **Boxplot:** distribution of seat width ratings by season
- **Bar chart:** top 5 airports with the largest difference between lounge and airport cleanliness ratings

---

## 🎓 Grade and instructor feedback

**Grade:** 9.5 / 10.0  
**Instructor:** Alena V. Suvorova  

**Feedback:**  
> *Excellent work! Clear logic, good graphics.*

**Comments addressed in the final version:**
- Question 3: instead of referencing a variable (`otv`), a **top-5** airports with the largest rating difference is shown
- Color scheme improved (better contrast, removed gray outline from purple bars)

---

## 🚀 How to view the results

- Open **`report.html`** in your browser — full report with conclusions  
- Open **`dashboard.html`** — interactive dashboard with key metrics

---

## 🛠 Tools

- R  
- dplyr, ggplot2, lubridate, stringr  
- flexdashboard  
- html_document

---

## 📌 Author

Dmitrii Podolin  
HSE University, "Data Research and Visualization" course
