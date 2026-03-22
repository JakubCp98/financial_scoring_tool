# PL
Zautomatyzowany pipeline do analizy spółek giełdowych, który pobiera dane finansowe z Yahoo Finance, przetwarza je w modelu wieloczynnikowym oraz rozszerza analizę o ocenę jakościową generowaną przez LLM (ChatGPT).

KLUCZOWE ELEMENTY:
- pobieranie danych via API (yfinance, Python)
- przetwarzanie i normalizacja danych (percentile ranking)
- ocena finansowa (tempo wzrostu, kondycja finansowa, stabilność finansowa, wycena)
- ocena jakościowa via ChatGPT API (technologia, strategia, trend, konkurencyjność)
- finalny wynik stanowi średnią ważoną oceny finansowej, wyceny oraz oceny jakościowej
- system generuje automatyczny sygnał inwestycyjny (BUY / HOLD / SELL)
- raportowanie wyników w Google Sheets (automatyzacja przez n8n)

ZAKŁADKI W GOOGLE SHEETS:

A) GŁÓWNE
1. Finalna_analiza (final_analysis) - wyniki modelu dla każdej z firm. Zakładka zawiera także listę wzorów użytych w modelu.
2. Ocena_jakościowa (qualitative_assesment) - analiza jakościowa dla poszczególnych spółek.

B) DODATKOWO
1. surowe_dane (raw_data) - dane finansowe spółek przed obrobieniem
2. fx_adjusted - dane finansowe spółek przewalutowane na USD
3. percentrank - dane finansowe spółek znormalizowane za pomocą funkcji PERCENTRANK (konieczne dla możliwości porównania)
4. surowe_dane_opis (raw_data_description) - opis danych finansowych, wraz z interpretacją

link: https://docs.google.com/spreadsheets/d/1kiyKR2DOoUx4sqiwdC6cRs3luHbCwhsRQYU0-j_b_xg/edit?usp=sharing

# ENG
An automated pipeline for analyzing publicly traded companies that retrieves financial data from Yahoo Finance, processes it using a multi-factor model, and enhances the analysis with LLM-generated qualitative evaluation (ChatGPT).


KEY COMPONENTS
- data retrieval via API (yfinance, Python)
- data processing and normalization (percentile ranking)
- financial evaluation (growth, financial condition, financial stability, valuation)
- qualitative evaluation via ChatGPT API (technology, strategy, trend, competitiveness)
- final score calculated as a weighted average of financial evaluation, pricing, and qualitative evaluation
- system generates an automated investment signal (BUY / HOLD / SELL)
- reporting in Google Sheets (automation via n8n)

GOOGLE SHEETS TABS:

A) MAIN
1. Finalna_analiza (final_analysis) - model results for individual companies. This taab also contains a list of formulas used in the model.
2. Ocena_jakościowa (qualitative_assesment) - multidimensional qualitative analysis for individual companies, performed entirely by ChatGPT (via API).

B) ADDITIONALLY
1. surowe_dane (raw data) - company financial data before processing
2. fx_adjusted - company financial data converted to USD
3. percentrank - company financial data normalized using the PERCENTRANK function (required for comparison)
4. surowe_dane_opis (raw_data_description) - description of the financial data, along with its interpretation

link: https://docs.google.com/spreadsheets/d/1kiyKR2DOoUx4sqiwdC6cRs3luHbCwhsRQYU0-j_b_xg/edit?usp=sharing
