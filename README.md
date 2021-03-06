# rnn_algo_exchange_lorenz_henrik
Austauschplattform im Rahmen von Lorenz' Masterthesis: Algorithmen um die NASA Datensätze im Bereich der PHM auszuwerten. 

Verlauf:

- Beispiel von https://machinelearningmastery.com/multivariate-time-series-forecasting-lstms-keras/ funktionsfähig übertragen

Weiteres Vorgehen:

- Eigene Daten in Beispiel übertragen (zunächst eine Triebwerke inkl. ihrer Zyklen, weiteres Vorgehen wird überdacht, Arbeit von Heimes mit einbeziehen, anderes Stichwort: Multivariate Timeseries)
  - Heimes: die ersten 30 Zyklen identifizieren ein gesundes Triebwerk, die letzten 30 ein kaputtes
  --> Betrachtung ermöglicht gleiche Zyklenlänge für alle Triebwerke

- RUL Berechnung realisieren (keine Vorhersage aus Beispiel direkt ersichtlich)
  - Daten auf einen HI reduzieren, Vorgehen in [Guo17] und [Bek17] beschrieben
    - Bek17: Therefore, this paper only uses the variables in which an exponential growth or decays occurs
    - The curves of engine data series are sometimes inconsistent to wear like trajectories, acting like exponential decays as seen                                 on Figure 2, so the decaying curves (blue) are required to be transformed into exponentially growing curves (black). 
    

(PDF) NARX Time Series Model for Remaining.... Available from: https://www.researchgate.net/publication/317267762_NARX_Time_Series_Model_for_Remaining_Useful_Life_Estimation_of_Gas_Turbine_Engines [accessed Jul 25 2018].

- Übertragung auf mehrere Triebwerke

(- Pytorch Beispiel http://chandlerzuo.github.io/blog/2017/11/darnn)

- Datenproblem: https://datascience.stackexchange.com/questions/27563/multi-dimentional-and-multivariate-time-series-forecast-rnn-lstm-keras --> https://1.bp.blogspot.com/-7P_ZGBc8s3c/V4TWwNokHpI/AAAAAAAABsk/P0KChOrEYkAEOFmQNE_EMkrjNAnnruluACLcB/s1600/concat.tif

- Beispiel: Wettervorhersage https://github.com/Hvass-Labs/TensorFlow-Tutorials/blob/master/23_Time-Series-Prediction.ipynb
  - Städte = Triebwerke
  - Vorhersage für eine Stadt/Triebwerk 
