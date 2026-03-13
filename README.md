# financial_scoring_tool

EXCEL link:
https://docs.google.com/spreadsheets/d/1kiyKR2DOoUx4sqiwdC6cRs3luHbCwhsRQYU0-j_b_xg/edit?usp=sharing

# PL: 
Zautomatyzowany model scoringowy spółek notowanych na giełdzie w oparciu o dane finansowe pobrane z yfinance (Yahoo Finance) oraz ocenę jakościową, dokonaną w pełni przez LLM (ChatGPT). Uzyskane wyniki pozwalają na dokonanie lepszej decyzji inwestycyjnej podczas zakupu akcji.

- Model ocenia firmy w czterech wymiarach finansowych – wzrostu, kondycji finansowej, stabilności oraz aktualnej wyceny – połączonych w znormalizowany, wieloczynnikowy wynik.
- Uwzględnia on również cztery filary jakościowe (technologia, strategia, trend, konkurencyjność), wyrażone w skali 0 - 100 (0 - najgorzej, 100 - najlepiej) w oparciu o szeroką gamę podkategorii.
- Finalny wynik jest średnią ważoną trzech parametrów: Wyceny, Oceny Finansowej oraz Oceny Jakosciowej, prowadzący do uzyskania decyzji typu BUY, SELL lub HOLD.
- Model został stworzony głównie do nauki języka Python, interfejsów API oraz platformy n8n, z drugorzędnym naciskiem na finanse i inwestowanie. W związku z tym, nie należy go traktować jako bezpośrednie narzędzie inwestycyjne ze względu na ograniczony zakres analizy.

ZAKŁADKI W GOOGLE SHEETS:

A) GŁÓWNE
1. FINALNA ANALIZA (final analysis) - wyniki modelu dla poszczególnych spółek. Zakładka zawiera także listę wzorów użytych w modelu
2. Qualitative_Assesment - wielowymiarowa analiza jakościowa dla poszczególnych spółek, dokonana w pełni przez ChatGPT via API.

B) DODATKOWO
1. surowe_dane (raw data) - dane finansowe spółek przed obrobieniem
2. fx_adjusted - dane finansowe spółek przewalutowane na USD
3. percentrank - dane finansowe spółek znormalizowane za pomocą funkcji PERCENTRANK (konieczne dla możliwości porównania)
4. surowe_dane_opis (raw data description) - opis danych finansowych, wraz z interpretacją


# ENG: 
An automated scoring model for publicly traded companies based on financial data sourced from yfinance (Yahoo Finance) and a qualitative assessment performed entirely by LLM (ChatGPT). The results allow for better investment decisions when purchasing shares.

- The model evaluates companies across four financial dimensions – growth, financial condition, stability, and current valuation – combined into a standardized, multi-factor score.
- It also considers four qualitative pillars (technology, strategy, trend, competitiveness), expressed on a scale of 0-100 (0 - worst, 100 - best) based on a wide range of subcategories.
- The final score is a weighted average of three parameters: Valuation, Financial Rating, and Qualitative Rating, leading to a BUY, SELL, or HOLD decision.
- The model was created primarily for learning Python, APIs, and n8n platform, with a secondary focus on finance and investing. Therefore, it should not be considered a direct investment tool due to its limited scope of analysis.

GOOGLE SHEETS TABS:

A) MAIN
1. FINALNA ANALIZA (final analysis) - model results for individual companies. This taab also contains a list of formulas used in the model.
2. Qualitative_Assessment - multidimensional qualitative analysis for individual companies, performed entirely by ChatGPT via the API.

B) ADDITIONALLY
1. surowe_dane (raw data) - company financial data before processing
2. fx_adjusted - company financial data converted to USD
3. percentrank - company financial data normalized using the PERCENTRANK function (required for comparison)
4. surowe_dane_opis (raw data description) - description of the financial data, along with its interpretation
   
