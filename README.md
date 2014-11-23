Алгоритмы обработки потоковых данных (англ. Streaming algorithm) - это алгоритмы для обработки потоков данных, в которых входные данные представляют собой последовательность элементов, и элемент такой последовательности необходимо рассмотреть за малое число проходов (обычно, за один). На такие алгоритмы накладываются ограничения по доступной для них памяти (много меньше, нежели размер всех входных данных), а также по времени обработки одного элемента последовательности.

Эти ограничения обычно означают то, что алгоритм формирует приблизительный (аппроксимированный) ответ, основанный на обобщённых характеристиках входных данных или их срезах.

Область исследования потоковых алгоритмов впервые была формализована в работе Нога Алона, Йосси Матиса и Марио Жегеди[1]. 

Производительность алгоритмов, работающих с потоковым данными измеряются тремя основными показателями:
    Число допустимых проходов алгоритма над данными.
    Доступная память.
    Время работы алгоритмы.
  
В модели поотовых данных считается, что часть или весь набор входных данных, над которыми необходимо осуществлять потоковую обработку, не доступен для случайного доступа (с диска или памяти), а поступает в одном или нескольких непрерывных потоках.

Потоки даных могут быть представлены упорядоченной последовательностью точек (или т.н. "обновлений"), доступ к которым может осуществляться по порядку и только один или ограниченное число раз.

Большинство литературы по обработке потоковых данных рассматривают задачу компьютерной статистики над таким распределением данных, которое слишком велико для эффективного хранения. Для данного класса задач предполагается, что вектор a = (a_i ..., a_n) (инициализированный нулевой последовательностью 0) имеет некоторое количество "обновлений" в потоке. Цель таких алгоритмов - вычислить функции от \mathbf{a}, используя много меньше места, чем это потребовало бы точное и полное представление вектора }. Существуют две общих модели обновления таких данных: "касса" (англ. cash register) и "турникет" (англ. turnstile).

В "кассовой" модели каждое "обновление" представляется в форме <i,c> и модифицируют вектор таким образом, что a_i увеличивается на некоторое положительное целое число c. Особым случаем является случай c = 1 (разрешена вставка только одной единицы). В "турникетной" модели каждое "обновление" представляется в форме <i,c> и модифицируют вектор таким образом, что a_i увеличивается на некоторое положительное или отрицательное целое число c. В строгой модели, в любой момент времени a_i не может быть отрицательным.

В ряде источников дополнительно рассматривают "слайд-оконную" модель. В данной модели интересующая функция вычисляется над окном ограниченной размерности из потоковых данных, элементы с конца окна не принимаются во внимание, пока новые данные из потока не займут их место.

В данных алгоритмах рассматриваются не только вопросы, связанные с частотными характеристиками данных, но и ряд других. Много задач на графах решаются в условиях того, что матрица смежности графа потоково подгружается с каком-то неизвестном порядке. Иногда, напротив, необходимо решить задачу оценки порядка данных, например, посчитать число инверсных значений в потоке и найти наибольшую возрастающую последовательность.

1. <a href="http://www.vldb.org/conf/2001/P079.pdf">Gilbert, A. C.; Kotidis, Y.; Muthukrishnan, S.; Strauss, M. J. (2001), Surfing Wavelets on Streams: One-Pass Summaries for Approximate Aggregate Queries</a>
