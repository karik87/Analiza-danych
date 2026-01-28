# Analiza-danych
Projekt na zaliczenie Analizy danych. Karol Janikowski, semestr 5

1. Definicja problemu
Celem projektu jest analiza historycznych notowań giełdowych spółki Apple Inc. oraz próba prognozowania przyszłych cen zamknięcia przy użyciu modeli statystycznych i uczenia głębokiego.

Dlaczego ten temat? Apple to jedna z największych spółek technologicznych na świecie. Jej notowania charakteryzują się dużą zmiennością, ale także silnymi trendami związanymi z cyklami wydawniczymi produktów (np. premiery iPhone'ów).

Cele i Hipotezy:

Cel: Porównanie skuteczności trzech różnych podejść: modelu liniowego (ARIMA), modelu uwzględniającego sezonowość (Prophet) oraz sieci neuronowej (LSTM).

Hipoteza: Klasyczne modele statystyczne (ARIMA) nie poradzą sobie z dużą zmiennością rynku, a najlepsze wyniki osiągnie model LSTM ze względu na zdolność do wychwytywania nieliniowych zależności.

2. Pozyskanie danych
Dane pochodzą z serwisu kaggle (https://www.kaggle.com/datasets/adamvakar/apple-comprehensive-financial-dataset-1980-2026). Zakres danych obejmuje okres od 1980 do 2026 roku (jednak wykorzystalem dane tylko od 2005 do 2026), co pozwala na uchwycenie zarówno trendów długoterminowych, jak i okresowych wahań.

3. Opis obserwacji i wnioski
Model LSTM okazał się najbardziej precyzyjny (MAE: 3.29 USD), co potwierdza hipotezę, że sieci neuronowe najlepiej radzą sobie z nieliniowością rynków finansowych.

Wartość biznesowa Prophet: Mimo większego błędu niż LSTM, model Prophet dostarczył cennych informacji o sezonowości. Wykresy komponentów pokazały powtarzalne wzrosty w IV kwartale każdego roku, co jest skorelowane z okresem świątecznym i premierami nowych produktów Apple.

Słabość ARIMA: Model ARIMA okazał się najmniej użyteczny w prognozowaniu długoterminowym, generując zbyt uproszczoną prognozę, która nie nadążała za dynamiką spółki technologicznej.
