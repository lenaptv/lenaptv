### Hi there 👋

<!--
**lenaptv/lenaptv** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Краткое описание основных проектов
Язык: Python

# NLP-hot
Материалы и доклады с выступлений по NLP-темам:

1) Доклад по пониманию интуиции работы трансформеров с помощью инструментов линейной алгебры и теории вероятностей (разбор домашнего задания курса Стэнфорда cs224n)
2) Презентация по теме "Chain-of-Thought: новый подход в prompt-engineering" к докладу для Data-завтрака, прошедшего в г. Екатеринбурге 18.02.23 

## Tiny-GPT "AI-да Пушкин!"
Tiny-GPT: трансформер своими лапками. 

Написала  с нуля на PyTorch генеративную модель: decoder-only, character-based трансформер на основе статьи "Attention is all you need", 2017
(https://arxiv.org/pdf/1706.03762v5.pdf)
и двух видео от Андрея Карпаты
1) https://www.youtube.com/watch?v=kCc8FmEb1nY&t=1s

2) https://www.youtube.com/watch?v=XfpMkf4rD6E&list=PLoROMvodv4rNiJRchCzutFw5ItR_Z27CM&index=11

Для ускорения процесса обучения использовала torch.compile() из PyTorch 2.0.

В качестве обучающего датасета был выбран роман в стихах А. С. Пушкина "Евгений Онегин" (файл в данном репозитории "input_Onegin.txt").
Для обучения использовала Т4 на Google Colab. С использованием torch.compile() процесс обучения длился менее 5ти минут.

В результате модель генерирует некое (конечно, очень отдаленное и слабое) подобие стихов Пушкина, так как все-таки это character-based трансформер, который был обучен на небольшом датасете и при минимальных затратах временных и вычислительных ресурсов.
Но все же некоторые слова похожи на оригинал и есть некий ритм стихов Пушкина.

## NLP Disaster Post

Это решение задачи с Kaggle: https://www.kaggle.com/competitions/nlp-getting-started/overview
По тексту поста надо определить, идет ли речь о реальной катастрофе или же нет (например, "небо в огне" может быть метафорой красивого заката).
Для решения задачи дообучила на тренировочном датасете 3 encoder-only базовых трансформера, которые затем обьединила в ансамбль. 
Также в процессе сравнила новый оптимизатор LION с широко используемым в NLP оптимизатором AdamW (спойлер: LION эффективнее только при размерах batch более 64).

## :fork_and_knife: SmartMenu and NutrisionistBot 
Представляет собой прототип рекомендательной системы рецептов
(включая соответствующий телеграм-бот для взаимодействия с
пользователем ). Программа работает в 2х вариантах:
1) дает прогноз о том, насколько вкусным может быть блюдо, приготовленное из имеющихся у пользователя ингредиентов, выдает
подробную информацию о составе нутриентов для данных продуктов и
дает ссылки на подходящие рецепты;
2) составляет разное меню (одновременно питательное и вкусное) на
каждый день со ссылками на рецепты, данными по ингредиентам и
пищевой ценности предлагаемых блюд. Инструменты: Jupiter notebook (исследования), Pycharm (программа)
Библиотеки: pandas, numpy, sklearn, argparse, joblib, requests, urllib, bs64,
json, time, PyTelegramBotAPI и др

## 🚀 Pipeline for ML process 
Предположим, что с определенной периодичностью у вас появляются
новые данные, и, следовательно, появляется необходимость обновить
прогноз, в том числе актуализировать ранее выбранную модель
машинного обучения. В таком случае было бы здорово автоматизировать данный процесс:
предобработку данных, обнаружение и OneHotEncoding категориальных
признаков, разбивку датасета на подвыборки, поиск наилучшего
алгоритма на основе кросс-валидации, финальный расчет метрик и
сохранение выбранной модели. Именно это и делает данная программа. Инструменты: Pycharm
Библиотеки: pandas, numpy, sklearn, joblib

## :e-mail: Email auto-sending 
Автоматизация рассылок на Tilda с помощью YandexCloudFunctions. Библиотеки: requests, urllib, base64, sys

## :movie_camera: Pepsi or Cola? Neural network knows!
Нейросеть (на фреймворке PyTorch) по изображению с веб-камеры (с
помощью openCV) определяет напиток: pepsi или cola. Инструменты: Jupiter notebook (исследования), Pycharm (программа)

## :ghost: Horror-Author-Identification 
LSTM нейросеть (на фреймворке TensorFlow) определяет писателя жанра ужасов по одному предложению.

## :bar_chart: Data visualization
Примеры визуализации и анализа данных с помощью mathplotlib
(тепловая карта, матрица рассеяния, гистограмма).

---

### :hammer_and_wrench: Инструменты и библиотеки :
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/anaconda/anaconda-original-wordmark.svg" title="Anaconda" alt="Anaconda" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/jupyter/jupyter-original-wordmark.svg" title="Jupyter" alt="Jupyter" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/pycharm/pycharm-original-wordmark.svg" title="pycharm" alt="pycharm" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/python/python-original-wordmark.svg" title="python" alt="python" width="40" height="40"/>&nbsp;   
  <img src="https://github.com/devicons/devicon/blob/master/icons/pandas/pandas-original-wordmark.svg" title="Pandas" alt="Pandas" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/numpy/numpy-original-wordmark.svg" title="Numpy" alt="Numpy" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/opencv/opencv-original-wordmark.svg" title="OpenCV" alt="OpenCV" width="40" height="40"/>&nbsp;
 <img src="https://github.com/devicons/devicon/blob/master/icons/tensorflow/tensorflow-original-wordmark.svg" title="tensorflow" alt="tensorflow" width="40" height="40"/>&nbsp; 
 <img src="https://github.com/devicons/devicon/blob/master/icons/pytorch/pytorch-original-wordmark.svg" title="pytorch" alt="pytorch" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/sqlite/sqlite-original-wordmark.svg" title="sqlite" alt="sqlite" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postgresql/postgresql-original-wordmark.svg" title="postgresql" alt="postgresql" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/kaggle/kaggle-original-wordmark.svg" title="Kaggle" alt="Kaggle" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original-wordmark.svg" title="Git" alt="Git" width="40" height="40"/>
</div>
