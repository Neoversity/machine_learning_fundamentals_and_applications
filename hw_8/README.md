
# Модель регресії для прогнозу заробітної плати

## Опис проєкту
Цей домашній проєкт спрямований на прогнозування заробітної плати співробітників на основі їхніх характеристик, таких як досвід, кваліфікація, університет, роль у компанії тощо. Модель побудована за допомогою методу K-найближчих сусідів (KNeighborsRegressor) з використанням двох підходів до обробки числових даних: StandardScaler та PowerTransformer.

## Дані
- **Тренувальний набір:** `mod_04_hw_train_data.csv`
- **Валідаційний набір:** `mod_04_hw_valid_data.csv`
- **Цільова змінна:** `Salary` (рівень заробітної плати)

## Кроки виконання
1. **Імпорт необхідних пакетів.**
2. **Завантаження та попередній аналіз даних (EDA):**
   - Перевірка пропусків.
   - Заповнення пропущених значень.
3. **Обробка даних:**
   - Трансформація числових змінних за допомогою StandardScaler та PowerTransformer.
   - Кодування категоріальних змінних за допомогою OneHotEncoder.
4. **Навчання моделі:**
   - Модель KNeighborsRegressor з параметром `n_neighbors=5`.
5. **Оцінка моделі:**
   - Розрахунок метрик MAPE, MSE та R2.

## Результати
- **Validation MAPE (StandardScaler):** 11.11%
- **Validation MAPE (PowerTransformer):** 11.11%
- **Validation MSE:** 140841428.57
- **Validation R2:** 0.44

## Висновки
1. Обидва методи масштабування показали однакові результати.
2. Значення R2 свідчить про середній рівень пояснювальної здатності моделі.
3. Подальші покращення можуть включати налаштування параметра `n_neighbors`, інженерію ознак або використання інших моделей регресії.

## Використані технології
- Python
- Pandas
- NumPy
- Scikit-learn

## Інструкція для запуску
1. Клонуйте репозиторій.
2. Встановіть необхідні бібліотеки: `pip install -r requirements.txt`
3. Запустіть скрипт для навчання моделі: `python main.py`

## Автор
**Антон Бабенко**


