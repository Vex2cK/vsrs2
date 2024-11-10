1) Чекать распределение фичей
2) Учить модель запонять NaN
3) Проверяем отличие теста от трейна:
    - Трейн - левее по таймлайну, тест соответственно правее. Т.е. проверяем как меняются фичи со временем
    - В трейне ставим target = 1 & в тесте ставим target = 0
    - Учим градбуст
    - Меряем ROC-AUC
    - если он = 0.5 => модель не понимает че изменилось, значит с данными всё ок
    - Если модель смогла чето предиктить и там рок аук скажем 0.9 значит беда, данные отличаются
4) Если в п. 3 беда, тогда:
    - считаем feature importance (`eda.ipynb` => `Фишки Catboost`)
    - Выкидываем сильные фичи И фичи которые с ними сильно коррелируют
5) Катбуст очень любит переобучаться. Параметр: early-stopping-round (число)
6) Первым слоем можно ставить BatchNorm
7) Обязательно фиксируем сиды!


### Ссылочки

time series 

m5 
- https://www.kaggle.com/code/kneroma/m5-first-public-notebook-under-0-50 
- https://www.kaggle.com/code/kyakovlev/m5-three-shades-of-dark-darker-magic/notebook 

cfavorita 
- https://www.kaggle.com/code/ceshine/lgbm-starter 

mms 

petfinder 
- https://www.kaggle.com/competitions/petfinder-adoption-prediction/discussion/88773 
- https://www.kaggle.com/competitions/petfinder-adoption-prediction/discussion/88740 

avito 
- https://www.kaggle.com/competitions/avito-demand-prediction/discussion?sort=votes 

geo time  

dataset 
- https://www.kaggle.com/datasets/thedevastator/best-location-for-a-gaming-company/data 

nfl 
- https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/discussion?sort=votes