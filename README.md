## ai-homeworks

###1) 8pzl_solver
   Това е конзолен 8-puzzle Solver. Включва пет реализации - IDDFS с хеширане на дълбочината, "чист" BFS, А\*, IDA\* и Beam Search с Манхатанско разстояние. Стартира се с *dsolve(x)* за IDDFS, *bsolve(x)* за BFS, *asolve(x)* за A\*, *idasolve(x)* за IDA\* и *bmsolve(x)* за Beam Search, където *x* е началната позиция.
  
    6 5 3
    2 4 8
    7   1

  Ако това е началната позиция, решението се търси например чрез *bsolve('653248701')*, където *0* е празното квадратче.

###2) 15pzl
   Това е стандратният 15 puzzle. Generate създава нова дъска, Solve решава текущата дъска чрез Beam Search с beamSize = 1000 и тройно Манхатанско разстояние. Това е силен overestimate на реалното разстояние, така че оптималност се постига само за много къси пъзели (решими в малко ходове). Тази евристика дава средно 20-30 хода повече от оптималното решение, но за разлика от него се смята мигновено!

###3) knight (това май не е от домашните)
   Това е път на коня на шахматна дъска. Пътят се показва с команда *path(s,x,y,ms)*, където *s* е размерът на дъската (до 40), *x* и *y* са началните полета на коня, а *ms* е милисекунди на ход. Използва евристика на Warnsdorf.

###4) queenz
   Това е наредба на N царици на шахматна дъска NxN, така че никои две от тях да не се бият. Изполва MinConflicts алгоритъм. Старира се с *queenz(x, steps)*, където *x* е размерът на дъската и *steps* е брой стъпки. Визуализацията е до 40 царици. За по-големи дъски извежда решението под формата на масив. За дъска 15000x15000 и 10000 стъпки намира решение за около 4 сек. Използва и изображението *qq.png*

###5) knap_ga
   Това е 0-1 KnaspSack. Включва реализация чрез генетичен алгоритъм и стандартен Dynamic Approach. Индивидите представляват string-ове със символи 0 и 1 относно принадлженост на item. За Crossover използва половината string на родителите, а за мутация - промяна на принадлежност на някой item. Командите са *knap_gen()* за генетичния алгоритъм и *knap_dyn()* за динамичния.
   
###6) 9sqr
   Това е игра Tic-Tac-Toe срещу компютър. Реализирана е чрез MiniMax стратегия с α–β отсичане и хеширане на резултатите.

###7) iris_knn
   kNN класификатор за файла iris.js. Файлът представлява данни за три вида растения ирис. Командата е *kNN(x,k)*, където *x* е масив с характеристики, а *k* е броят на съседите.

###8) iris_bayes
   Naive Bayes класификатор за файла iris.js. Реализиран е с хипотеза за нормално разпределение на всички характеристики. Командата е *prob(x)*, където *x* е масив с характериситки.