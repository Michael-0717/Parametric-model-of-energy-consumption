# Параметрическая модель энергопотребления.  Построим модели линейной регрессии по обогащенным данным.
## Задание
Получите данные по энергопотреблению первых 20 зданий (building_id от 0 до 19).
Заполните отсутствующие значения по погоде интерполяционными данными.
Разделите данные на обучающие/проверочные в пропорции 80/20.
Постройте и найдите общее качество модели линейной регрессии, построенной по часам для каждого из первых 20 зданий по следующим параметрам: air_temperature, dew_temperature, cloud_coverage, wind_speed, precip_depth_1_hr, sea_level_pressure, is_holiday. Всего требуется построить 480 моделей линейной регрессии, вычислить по ним проверочные значения энергопотребления и получить итоговую оценку качества такой модели.
Для расчета последнего параметра (is_holiday) используйте график публичных выходных в США: USFederalHolidayCalendar
Исходные данные:
•	video.ittensive.com/machine-learning/ashrae/building_metadata.csv.gz
•	video.ittensive.com/machine-learning/ashrae/weather_train.csv.gz
•	video.ittensive.com/machine-learning/ashrae/train.0.csv.gz
___
## Решение
1) Подключим необходимые библиотеки, загрузим данные. 
Загрузка данных, отсечение 20 зданий, объединение и оптимизация.
2) Добавим час и праздники в данные.
Добавим час и праздники в данные.
3) Проведем интерполяция данных.
Проведём интерполяцию данных, используя метерологические данные.
Заменим отсутствующие данные предсказанными исходя из тренда.
4) Разделим данные.
Разеделим данные на обучающие и проверочные в пропорции 80 на 20.
5) Построим массив моделей линейной регрессии - по зданию и часу, всего 480 моделей.
6) Рассчитаем качество построенных моделей. 
Для расчета качества метрики переберем все серии данных модели и умножим на соответсвующий коэффициент.

Качество линейной регрессии, 20 зданий: 0.2607817873183314 0.3


