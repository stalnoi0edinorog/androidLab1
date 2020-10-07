# Лабораторная работа №2. Activity Lifecycle. Alternative resources.  
## Цели  
* Ознакомиться с жизненным циклом Activity  
* Изучить основные возможности и свойства alternative resources  
  
## Задачи  
### Задача 1. Activity  
#### Задание  
Продемонстрировать жизненный цикл Activity на любом нетривиальном примере.  
  

### Задача 2. Alternative Resources  
#### Задание  
Продемонстрировать работу альтернативного ресурса ** UI mode ** на каком-либо примере.  
  

### Задача 3. Best-matching resource  
Для заданного набора альтернативных ресурсов, предоставляемых приложением, и заданной конфигурации устройства объяснить, какой ресурс будет выбран в конечном итоге. Ответ доказать.
#### Вариант 8. 
Конфигурация устройства
- LOCALE_LANG: fr
- LOCALE_REGION: rFR
- SCREEN_SIZE: normal
- SCREEN_ASPECT: notlong
- ROUND_SCREEN: notround
- ORIENTATION: land
- UI_MODE: television
- NIGHT_MODE: notnight
- PIXEL_DENSITY: tvdpi
- TOUCH: notouch
- PRIMARY_INPUT: qwerty
- NAV_KEYS: nonav
- PLATFORM_VER: v26

Конфигурация ресурсов:
- (default)
- round-port-watch-ldpi-v25
- rFR-watch-dpad
- long-notround-night
- rFR-notround-notnight-xhdpi-v25
- rCA-xlarge-notround-television-night-nokeys-wheel-v25
- en-round-vrheadset-nokeys
- en-long-port-nodpi-trackball
- notround-nokeys
- en-normal-notouch
- en-rCA-notlong

### Задача 4. Сохранение состояние Activity.  
Студент написал приложение: [continuewatch](continuewatch). Это приложение [по заданию](continuewatch/README.md) должно считать, сколько секунд пользователь провел в этом приложении.  

Найдите ошибки в этом приложении и исправьте их.
