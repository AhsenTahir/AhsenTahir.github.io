---
title: "Trend-X-BTC — sequence models for cryptocurrency forecasting"
excerpt: "LSTM with multi-head attention for 30-day Bitcoin forecasting over market sentiment, on-chain activity, macro factors, and trading volume.<br/><img src='/images/projects/trendxbtc.jpg'>"
collection: portfolio
---

A 30-day Bitcoin forecasting system built on an LSTM with multi-head attention, trained over four heterogeneous signal families: market sentiment, on-chain activity, macroeconomic factors, and trading volumes ingested from Binance, CryptoCompare, and Google BigQuery.

Predictions refresh daily through a Firebase pipeline. An LLM layer over LLaMA, Gemini, and Mistral overlays real-time market context on the numerical forecast.

**Stack:** PyTorch, LSTM + attention, Next.js, Firebase, Binance API, BigQuery

[Live demo](https://trendxbtc.vercel.app/)
