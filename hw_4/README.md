
# Домашнє завдання: Лінійна регресія

## Опис проєкту
У цьому проєкті було виконано задачі з побудови лінійної регресії для прогнозування цільової змінної `MedHouseVal` з датасету California Housing. Проєкт включає етапи обробки даних, видалення викидів, видалення високо корельованих ознак, нормалізацію даних та побудову моделі.

---

## Виконані кроки

### 1. Імпорт необхідних пакетів
Здійснено імпорт усіх бібліотек, зокрема `pandas`, `numpy`, `scikit-learn` та інших.

### 2. Завантаження даних
Завантажено датасет California Housing через `fetch_california_housing`.

### 3. Обробка даних
- **Очистка викидів:** Видалено викиди в колонках `AveRooms`, `AveBedrms`, `AveOccup`, `Population` за допомогою методу Z-score.
- **Видалення ознак:** Видалено ознаки `Longitude`, `Latitude` та додаткову найменш суттєву ознаку, базуючись на кореляційній матриці.

### 4. Нормалізація даних
Дані нормалізовані за допомогою `StandardScaler`.

### 5. Побудова моделі
- Використано модель `LinearRegression` для навчання.
- Проведено прогнозування на тестових даних.
- Враховано рекомендацію обмежити передбачені значення в межах [min, max] тренувальних даних.

### 6. Оцінка моделі
Обчислено метрики:
- **R² (тренувальні дані):** 0.64
- **R² (тестові дані):** 0.65
- **MAE (середня абсолютна похибка):** 0.51
- **MAPE (середня абсолютна похибка у відсотках):** 29.79%

### Порівняння з результатами конспекту:

- **Конспект:**
  - R²: 0.61
  - MAE: 0.52
  - MAPE: 31%

- **Висновок:**
  - Результати моделі покращилися в порівнянні з конспектом за всіма метриками, що свідчить про якісну оптимізацію даних.


---

## Візуалізації
### Матриця кореляції
![Матриця кореляції](matrix_correlation.png)
### Графік справжніх значень vs передбачені (обмежені)
![Графік: Справжні значення vs Передбачені](graph.png)

### Графік залишків
![Графік залишків](residuals.png)

---

## Висновки
- Мій результат на тренувальних та тестових даних перевершує метрику з конспекту, що свідчить про краще узгодження моделі.
- Моє значення MAE трохи краще, ніж у конспекті, що вказує на меншу абсолютну похибку передбачень.
- Мої значення MAPE також нижче, що вказує на зменшення відносної похибки передбачень.

---

## Інструкція для запуску
1. Встановіть необхідні пакети з файлу `requirements.txt`.
2. Запустіть ноутбук `dz_topic_4_БабенкоАнтонІванович.ipynb`.
