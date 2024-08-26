1. Вас пригласили настроить мониторинг на проект. На онбординге вам рассказали, что проект представляет из себя 
платформу для вычислений с выдачей текстовых отчетов, которые сохраняются на диск. Взаимодействие с платформой 
осуществляется по протоколу http. Также вам отметили, что вычисления загружают ЦПУ. Какой минимальный набор метрик вы
выведите в мониторинг и почему?
```
Ответ:
    -- метрика загрузки процессора
    -- метрика работа с диском
    -- метрика по запросам http
```
#
2. Менеджер продукта посмотрев на ваши метрики сказал, что ему непонятно что такое RAM/inodes/CPUla. Также он сказал, 
что хочет понимать, насколько мы выполняем свои обязанности перед клиентами и какое качество обслуживания. Что вы 
можете ему предложить?
```
Ответ:
   Можно предложить воспользоваться метриками SLI,SLO,SLA. Данные метрики связывают технические значения
с бизнес-составляющей.

```
#
3. Вашей DevOps команде в этом году не выделили финансирование на построение системы сбора логов. Разработчики в свою 
очередь хотят видеть все ошибки, которые выдают их приложения. Какое решение вы можете предпринять в этой ситуации, 
чтобы разработчики получали ошибки приложения?
```
Ответ:
      Скорее использовать систему перехватчик-ошибок. Например, Sentry.
```
#
4. Вы, как опытный SRE, сделали мониторинг, куда вывели отображения выполнения SLA=99% по http кодам ответов. 
Вычисляете этот параметр по следующей формуле: summ_2xx_requests/summ_all_requests. Данный параметр не поднимается выше 
70%, но при этом в вашей системе нет кодов ответа 5xx и 4xx. Где у вас ошибка?
```
Ответ:
  Ошибка может содержаться в том, что не все коды ответов учтены в формуле. Нужно проанализировать логи на предмет
наличия отличных от 2xxx, 4xxx, 5xxx кодов ответа и включить их в числитель формулы.
 
```
#
5. Опишите основные плюсы и минусы pull и push систем мониторинга.
```
Ответ:
  pull модель:
     плюсы:
           -- более гибкая настройка мониторинга( мониторим только то что надо и собираем только нужные метрики)
           -- упрощенная отладка получения данных с агентов           
     минусы:
           -- не удобна при большом количестве устройств.
  push модель:
      плюсы:
             -- можно отсылать метрики в несколько систем(на несколько серверов)
             -- модель хорошо подходит для сбора метрик с агентов находящихся где-то в приватной сети не доступной с
                сервера-мониторинга.
      минусы:
             -- менее гибкая
 
```

#
6. Какие из ниже перечисленных систем относятся к push модели, а какие к pull? А может есть гибридные?

    - Prometheus 
    - TICK
    - Zabbix
    - VictoriaMetrics
    - Nagios
```
Ответ:
    - Prometheus (PULL)
    - TICK       (PUSH)
    - Zabbix     (PUSH,PULL)
    - VictoriaMetrics (PUSH,PULL)
    - Nagios (PUSH,PULL)
 
```
#
7.
![изображение](https://github.com/user-attachments/assets/f3c860df-23d1-453b-bda9-e15c9a47d477)
#
8.
![изображение](https://github.com/user-attachments/assets/e639e3f8-5ed9-4bd0-9870-7b4b13313708)
#
9.
![изображение](https://github.com/user-attachments/assets/54190e56-62de-46be-ba0e-39ff06f5677b)



