# test_al

Streamlit-приложение, которое предсказывает вид пингвина (Adelie, Chinstrap, Gentoo)
по шести признакам с помощью модели случайного леса, обученной на датасете
[Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/).

## Файлы

| Файл | Назначение |
|------|------------|
| `penguins_streamlit_cloud.py` | Основное приложение: форма ввода, прогноз и графики |
| `penguins.csv` | Датасет для гистограмм распределений признаков |
| `random_forest_penguin.pickle` | Обученный классификатор Random Forest |
| `output_penguin.pickle` | Соответствие индексов модели названиям видов |
| `feature_importance.png` | График важности признаков, показываемый в приложении |
| `beginner.ipynb` | Блокнот для экспериментов и обучения модели |
| `requirements.txt`, `runtime.txt` | Зависимости и версия Python для Streamlit Cloud |

## Запуск локально

1. Установите зависимости:

   ```bash
   pip install matplotlib pandas scikit-learn==1.1.3 seaborn streamlit
   ```

2. Приложение защищено паролем. Создайте файл `.streamlit/secrets.toml`:

   ```toml
   passwordcd = "ваш_пароль"
   ```

3. Запустите приложение:

   ```bash
   streamlit run penguins_streamlit_cloud.py
   ```

После ввода пароля заполните форму — приложение покажет предсказанный вид
и гистограммы, на которых отмечены введённые значения.
