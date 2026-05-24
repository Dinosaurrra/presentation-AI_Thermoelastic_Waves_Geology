# Prompt: improve Overleaf Beamer presentation

Привет. Нужно доработать Beamer-презентацию для дипломной работы в Overleaf.

Overleaf project:
https://www.overleaf.com/project/6a0d4535ec3f6b0fcdef34ce

Тема дипломной работы:
“AI Directional Prediction of Thermoelastic Wave Propagation in Geological Media”

Репозиторий с дипломом:
https://github.com/MIKU-7437/AI_Termoelastic_Waves_Geology

Основной файл диплома:
`main.tex`

## Общая задача

Изучи текущую Beamer-презентацию и диплом через `main.tex` и подключенные `.tex` файлы. Затем аккуратно улучши содержание, структуру и визуальное оформление презентации.

Презентация должна оставаться академической, спокойной и неброской, но при этом выглядеть цельно, уверенно и визуально приятно. Слайды должны вызывать доверие и симпатию у комиссии: чистая структура, понятные формулировки, аккуратные изображения, хорошие отступы, единый стиль.

Не нужно делать PowerPoint. Работать только с LaTeX Beamer в Overleaf.

## Важные ограничения

- Не менять научный смысл дипломной работы.
- Не делать проект похожим на полноценный численный симулятор.
- Не утверждать, что модель полностью решает задачу термоупругих волн.
- Не писать, что система field-validated.
- Не перегружать слайды текстом.
- Не использовать слишком яркий дизайн.
- Не использовать случайные неподтвержденные утверждения.
- Не использовать 3D-визуализации, если они не нужны.
- Не проговаривать начальные условия в тексте выступления.
- Избегать аббревиатур. Если аббревиатура нужна, при первом упоминании писать полную расшифровку в скобках.

## Правильное позиционирование работы

Использовать формулировки:

- AI-assisted directional prediction framework
- research prototype
- comparative framework
- surrogate modelling approach
- physics-informed baseline
- directional prediction of thermoelastic wave propagation
- model-based calculation
- simplified modelling assumptions
- the prototype estimates/predicts
- the results suggest

Не использовать формулировки:

- fully solves thermoelastic wave propagation
- complete geophysical simulator
- field-validated prediction system
- replaces numerical simulation
- guarantees physical correctness
- PINN completely solves the governing equations

## Список правок

### 1. Добавить изображения гор, пород и геологической среды

Добавить спокойные, уместные изображения:
- горные массивы;
- геологические породы;
- разрезы/структуры пород;
- каменные текстуры;
- геологическая среда.

Важно:
- не генерировать изображения через AI;
- не делать изображения самостоятельно;
- использовать только уже доступные изображения из проекта/диплома или открытые изображения с корректной лицензией;
- изображения должны быть фоном или аккуратной иллюстрацией, а не главным декоративным элементом;
- дизайн должен оставаться строгим и академическим.

Если подходящих изображений нет, лучше поставить аккуратный placeholder/TODO-комментарий в LaTeX, чем использовать случайную картинку.

### 2. Slide “Aim and tasks”

На слайде “Aim and tasks” явно написать, на каких породах проводились расчеты/тестирование.

Указать породы, если они есть в дипломе/коде/таблицах, например:
- sandstone;
- basalt;
- granite;
- limestone.

Формулировка должна быть осторожной:

> The calculations were performed for representative geological materials, including sandstone, basalt, granite, and limestone.

Если список пород в дипломе отличается, использовать именно список из диплома.

### 3. Slide “Working position of this thesis”

Этот слайд может вызвать вопросы комиссии, поэтому его нужно сделать особенно уверенным и понятным.

Нужно объяснить, что работа:
- не является полноценным промышленным симулятором;
- не заменяет численные методы;
- рассматривает simplified modelling assumptions;
- делает AI-assisted directional prediction;
- сравнивает несколько моделей как surrogate approaches;
- использует PINN как physics-informed baseline.

Тон должен быть уверенный, без извиняющихся формулировок.

Пример идеи:

> This thesis is positioned as a research prototype for AI-assisted directional prediction of thermoelastic wave propagation. The focus is not on replacing numerical solvers, but on comparing neural surrogate approaches under simplified assumptions.

### 4. Slide “Research problem”

Слайд должен быть сформулирован так, чтобы было понятно: именно эту проблему работа и решает.

Не писать слишком общую проблему, которую проект не может решить полностью.

Лучше сформулировать так:

> The research problem is to estimate directional characteristics of thermoelastic wave propagation in geological media using an AI-assisted comparative framework under simplified physical assumptions.

Сделать связку:
- проблема;
- почему она важна;
- что именно делает эта работа;
- что не заявляется как результат.

### 5. Все формулы: добавить пояснение переменных и единиц измерения

На всех слайдах, где есть формулы, добавить расшифровку каждого символа.

Для каждой формулы указывать:
- что означает каждый символ;
- единицы измерения, если применимо;
- физический смысл формулы в 1–2 предложениях.

Пример формата:

```latex
egin{itemize}
    \item $\sigma_{ij}$ — stress tensor, Pa;
    \item $\varepsilon_{ij}$ — strain tensor, dimensionless;
    \item $\lambda, \mu$ — Lamé parameters, Pa;
    \item $\delta_{ij}$ — Kronecker delta.
\end{itemize}
```

Если единицы измерения зависят от нормализации данных, написать это явно.

### 6. Slide “Thermoelastic coupling logic”

На этом слайде формулу нужно не только показать, но и написать текстом, что она означает.

Добавить простое объяснение:

- temperature change causes thermal strain;
- thermal strain contributes to stress;
- stress affects displacement and wave propagation;
- therefore thermal and elastic fields are coupled.

Не просто вставить формулу, а объяснить связь словами.

Пример:

> The formula describes how mechanical stress depends not only on elastic deformation, but also on temperature-induced expansion. This is the main physical reason why thermal and elastic fields cannot be treated as fully independent in thermoelastic media.

### 7. Таблица параметров пород

В таблице параметров пород добавить видимые границы между колонками, чтобы значения и размерности не смешивались.

Нужно:
- сделать таблицу читаемой;
- разделить колонки вертикальными линиями или более аккуратным spacing;
- отдельно указать units;
- не перегружать таблицу;
- проверить, чтобы таблица не выходила за границы слайда.

Если таблица слишком широкая:
- уменьшить количество колонок;
- разделить на две таблицы;
- использовать `\resizebox{\textwidth}{!}{...}` только если текст остается читаемым.

### 8. Написать про упрощение допущениями

Добавить отдельный слайд или блок на существующем слайде про assumptions/simplifications.

Нужно указать:
- locally homogeneous medium;
- isotropic approximation;
- simplified material representation;
- representative rock parameters;
- two-dimensional directional analysis, если это соответствует диплому;
- model-based prediction rather than full numerical simulation.

Формулировка должна быть уверенной:

> These assumptions are used to keep the problem suitable for comparative AI-based directional prediction and to make the results interpretable within the scope of a bachelor thesis.

### 9. Slide “Key physical parameters”

Переименовать формулу/заголовок формулы так, чтобы было понятно, что именно показывается.

Не оставлять слишком общий заголовок “Formula”.

Варианты:
- “Elastic wave velocity relation”
- “Longitudinal wave velocity”
- “Thermoelastic stress relation”
- “Material parameter relation”

Выбрать название по фактической формуле на слайде.

### 10. Slide 11: Hooke’s law

На 11 слайде явно указать Hooke’s law.

Если там используется связь напряжения и деформации, добавить заголовок:

> Hooke’s law for an isotropic elastic medium

Если в формуле есть термоупругое расширение, назвать точнее:

> Thermoelastic extension of Hooke’s law

И обязательно добавить расшифровку переменных и единиц.

### 11. Slides 14 and 15 объединить

Объединить слайды 14 и 15 в один логичный слайд.

Цель:
- убрать повторение;
- сделать переход более компактным;
- оставить одну основную мысль.

После объединения проверить нумерацию всех следующих слайдов и обновить `speaker_notes.tex`.

### 12. Не проговаривать начальные условия

В `speaker_notes.tex` не нужно подробно проговаривать initial conditions.

Если начальные условия есть на слайде, их можно оставить кратко, но в тексте выступления не читать и не объяснять подробно.

Фраза для выступления:

> The initial and boundary assumptions are used only to define a consistent calculation setting and are not the main focus of the presentation.

### 13. Slides 16 and 17 объединить

Объединить слайды 16 и 17 в один слайд, если они повторяют одну и ту же идею.

После объединения:
- убрать дублирование;
- сохранить только важные тезисы;
- обновить переходы между слайдами;
- обновить `speaker_notes.tex`.

### 14. Расписать все модели: одна модель — один слайд

Сделать отдельный слайд для каждой модели.

Для каждой модели указать:
- полное название модели;
- роль модели в работе;
- что она принимает на вход;
- что она возвращает;
- почему она включена в сравнение;
- короткое ограничение модели.

Пример структуры одного слайда:

```text
Model name
Role in this thesis:
Input:
Output:
Why it is used:
Limitation:
```

Модели описывать без лишнего углубления в код.

Обязательно:
- PINN — Physics-Informed Neural Network, physics-informed baseline;
- FNO — Fourier Neural Operator, neural operator surrogate;
- MeshGraphNet — graph-based surrogate model;
- Transformer-style model — attention-based experimental/baseline surrogate.

Если в дипломе используются другие названия моделей, синхронизировать с дипломом.

### 15. Избегать аббревиатур

Проверить все слайды и `speaker_notes.tex`.

При первом использовании:
- PINN → Physics-Informed Neural Network (PINN);
- FNO → Fourier Neural Operator (FNO);
- AI → artificial intelligence (AI);
- PDE → partial differential equation (PDE), если используется;
- 2D → two-dimensional (2D).

Если аббревиатура не нужна, лучше заменить ее полным названием.

### 16. В конце заменить “Experiment” на “Calculation”

В финальных слайдах и заголовках заменить слово “Experiment” на “Calculation”, если речь идет о модельных расчетах, а не о лабораторном или полевом эксперименте.

Примеры:
- “Experimental setup” → “Calculation setup”
- “Experiment results” → “Calculation results”
- “Experiment summary” → “Calculation summary”

Если где-то действительно описывается экспериментальная часть, оставить “experiment”, но для этой работы предпочтительно использовать “calculation”.

## Требования к speaker_notes.pdf

После изменения слайдов обновить отдельный файл с текстом выступления:

- `speaker_notes.tex`
- `speaker_notes.pdf`

В тексте выступления:
- синхронизировать нумерацию слайдов;
- убрать подробное проговаривание initial conditions;
- добавить уверенное объяснение “Working position of this thesis”;
- добавить пояснение всех формул простыми словами;
- для моделей объяснять роль, а не кодовую реализацию;
- в конце заменить “experiment” на “calculation”, где это нужно.

## Требования к дизайну

Дизайн должен быть:
- clean academic;
- неброский;
- светлый фон;
- темный текст;
- один спокойный акцентный цвет;
- хорошие отступы;
- единый стиль заголовков;
- читаемые таблицы;
- аккуратные формулы;
- изображения должны поддерживать смысл, а не отвлекать.

Не использовать:
- кислотные цвета;
- сильные градиенты;
- декоративные шрифты;
- случайные иконки;
- перегруженные рамки;
- слишком много текста на одном слайде.

## Финальная проверка

После правок проверить:

1. Презентация компилируется в Overleaf.
2. `speaker_notes.tex` компилируется в отдельный PDF.
3. Нумерация слайдов совпадает с notes.
4. Все формулы имеют расшифровку переменных и единиц.
5. Все модели описаны отдельно.
6. Слайды 14–15 объединены.
7. Слайды 16–17 объединены.
8. “Experiment” заменено на “Calculation”, где нужно.
9. Таблицы читаемые и не выходят за границы.
10. Дизайн спокойный, академический и визуально приятный.

## Что выдать в ответе

После выполнения выдать:

1. Список измененных файлов.
2. Кратко, что было изменено по каждому пункту.
3. Какие слайды были объединены.
4. Какие изображения добавлены и откуда они взяты.
5. Какие формулы получили пояснения.
6. Подтверждение, что презентация и `speaker_notes.pdf` компилируются.
