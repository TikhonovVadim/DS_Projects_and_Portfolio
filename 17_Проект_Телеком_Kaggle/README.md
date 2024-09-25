## данный проект решен на kaggle.com

https://www.kaggle.com/c/advanced-dls-spring-2021/leaderboard

Достижение - 65 место в leaderboard из более 5000 участников

## Проект - Телеком: Предсказание оттока пользователей

## Цель проекта 
Построить и выбрать лучщую ML-модель классификации

## Описание проекта
Это соревнование является домашним заданием к 3 модулю продвинутого потока DLS. 
Вам предстоит научитсья моделировать отток клиентов телеком компании. 
Эта задача очень важна на практике и алгоритмы для ее решения используются в реальных телеком компаниях, ведь если мы знаем, что клиент собирается уйти от нас, то мы попытаться удержать его, предложив какие-то бонусы

## Задачи проекта
- изучить данные, провести предобработку данных
- сформировать и отобрать признаки
- провести обучение на нескольких моделях(ML) с подбором гипперпараметров на кроссвалидации
- выбрать лучшую модель ML и проверить на тестовой выборке, проверить константную модель
- выделить наиболее важные признаки, составить отчет для Заказчика

## Описание данных
- ClientPeriod                
- MonthlySpending             
- TotalSpent                  
- Sex                         
- IsSeniorCitizen             
- HasPartner                  
- HasChild                    
- HasPhoneService             
- HasMultiplePhoneNumbers     
- HasInternetService          
- HasOnlineSecurityService    
- HasOnlineBackup             
- HasDeviceProtection         
- HasTechSupportAccess        
- HasOnlineTV                 
- HasMovieSubscription        
- HasContractPhone            
- IsBillingPaperless          
- PaymentMethod               
- Churn 

# Основные выводы
1. лучшая оценка auc_roc на обучающей выборке у модели CatBoostClassifier  =  0.858

- параметры модели:

    - catboost.core.CatBoostClassifier
    - {'auto_class_weights': 'Balanced', 'depth': 2, 'iterations': 200, 'learning_rate': 0.1}

2. десять наиболее значимых признаков в данных для решения задачи:
    - 'HasContractPhone'
    - 'ClientPeriod'
    - 'HasOnlineSecurityService'
    - 'HasInternetService'
    - 'TotalSpent'
    - 'MonthlySpending'
    - 'HasTechSupportAccess'
    - 'PaymentMethod'
    - 'IsBillingPaperless'
    - 'HasOnlineTV'
