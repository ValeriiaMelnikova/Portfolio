Как решать задачи моделирования течений со свободной поверхностью в OpenFOAM® 4.1
---------------------------------------------------------------------------------

**Преподаватель:** Виктория Корчагова, ИСП РАН (Россия)

**Сложность модуля:** Средняя

**Тип модуля:** Лекция с примерами

**Программное обеспечение:** OpenFOAM 4.1, OpenFOAM 3.0.x

**Разработчики модуля:**

* В. Корчагова, Россия

**Сайт команды разработчиков:** <http://unicfd.ru>

**Язык презентации:** English

**Описание:**

В связи с изменениями, внесёнными в численную схему для расчёта
течений с межфазной поверхностью в OpenFOAM версии 2.3 и более
новых важно понимать как настройки задачи окажут влияние на
численное решение. Целью данного учебного является анализ настроечных
параметров решателя **interFoam** для корректного решение задачи
моделирования течения со свободной поверхностью.

Данное занятие является смешанным: первая часть представляет собой
лекцию, вторая часть состоит из практических примеров для выполнения.
В лекции рассматриваются вопросы принципа работы модели **interFoam**:
базовые уравнения, аппроксимирующие выражения. В практической части
рассматриваются задачи моделирования водосброса (Spillway) и неустойчивости
Рэлея-Тэйлора, см. рисунки ниже.

<div style="width:500px">
<img src="../Fig/freeSurfaceFlows/spillway-problemStatement.png" style="width:100%" />
</div>

<div style="width:100px">
<img src="../Fig/freeSurfaceFlows/RT-problemStatement.png" style="width:100%" />
</div>

Структура учебного модуля следующая.

1. Введение: течения со свободной поверхностью как область интересов исследователей 
и область применения инженеров; почему в данном учебном курсе основное внимание уделяется
граничным условиям, используемым в OpenFOAM при постановке задач из данной области.
2. Обзор принципов работы и устройства решателя **interFoam**.
3. Описание тестового примера модели водосброса - "Spillway".
4. Обзор этапов для решения примера "Spillway":
    (a) утилита **blockMesh** и настроечный файл blockMeshDict;
    (b) утилиты **snappyHexMesh** и **extrudeMesh**;
    (c) настройка граничных условий для гидродинамических величин (объёмная доля, скорость, давление);
    (d) Файлы настройки численных схем fvSchemes и fvSolution;
    (e) запуск **interFoam**, сопоставление результатов полученных в различных версиях
        OpenFOAM, см. результаты ниже.
5. Запуск примера с задачей гидродинамической неустойчивости Рэлея-Тэйлора (см. результаты ниже).
6. Подведение итогов и обсуждение.

<div style="width:500px">
<img src="../Fig/freeSurfaceFlows/res-spillway.png" style="width:100%" />
</div>

<div style="width:100px">
<img src="../Fig/freeSurfaceFlows/res-RT.png" style="width:100%" />
</div>

После проведения расчётов будут получены поля гидродинамических величин (скорость, давление
и объёмная доля жидкой фазы) для задач неустойчивости Рэлея-Тэйлора и водосброса (Spillway).
Изменение этих величин во времени представлено в анимационных роликах ниже.

<iframe width="420" height="315"
src="https://www.youtube.com/embed/OHoaa4xCMeM">
</iframe>

<iframe width="420" height="315"
src="https://www.youtube.com/embed/mwarxIXO_Q0">
</iframe>

Слушателям будет предложено выполнить указанные выше шаги самостоятельно в процесс
учебного курса. Исходные данные для задачи моделирования водосброса приводятся здесь:
<https://www.hpc.ntnu.no/display/hpc/OpenFOAM+-+Spillway+Tutorial>.


Учебные материалы расположены на git архиве в свободном доступе и могут быть загружены
с ресурса <http://www.github.com>:

* Для OpenFOAM 4.1 at <https://github.com/unicfdlab/TrainingTracks/tree/master/OpenFOAM/freeSurfaceFlows-0F4.1>
* Для OpenFOAM 3.0.0 at <https://github.com/unicfdlab/TrainingTracks/tree/master/OpenFOAM/freeSurfaceFlows-0F3.0.0>
