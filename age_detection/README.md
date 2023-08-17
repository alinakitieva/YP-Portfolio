# Обработка фотографий покупателя

## Статус проекта
Завершен

## Задачи проекта
Определение возраста по фотографии

## Описание проекта
Сетевой супермаркет внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять
возраст клиентов, чтобы анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы и контролировать
добросовестность кассиров при продаже алкоголя. Строится модель, которая по фотографии определит приблизительный возраст человека. В вашем распоряжении
набор фотографий людей с указанием возраста.

## Ключевые слова
обработка изображений, нейронные сети

## Описание данных
Данные взяты с сайта ChaLearn Looking at People. Они находятся в папке /datasets/faces/.  
В вашем распоряжении одна папка со всеми изображениями (/final_files) и CSV-файл labels.csv с двумя колонками: file_name и real_age. 

## Вывод
Модель, основанная на архитектуре ResNet50, была обучена в течение 10 эпох. Наблюдалась стабильная убывающая тенденция в потерях как на тренировочном, так и на валидационном наборе данных. loss на тренировочном наборе уменьшился с 235 до 7, а средняя абсолютная ошибка с 11 до 2. По результатам валидации loss снизился до 77, а средняя абсолютная ошибка составила 6.8.

Эти результаты свидетельствуют о том, что модель обучилась предсказывать возраст с достаточной точностью, и MAE на валидационном наборе данных оказалась ниже 8. 

С точки зрения бизнеса модель может использоваться для анализа покупок в разных возрастных группах и для предложения товаров, которые могут заинтересовать покупателей конкретных возрастных категорий. Ошибка в 6.8 лет может быть приемлемой для разделения на более обобщенные группы, такие как дети, подростки, взрослые и пожилые. Возможность определения возраста также может использоваться для ограничения продажи алкоголя несовершеннолетним. Однако потребуется дополнительная проверка точности модели в диапазоне возрастов около законного возраста для покупки алкоголя.