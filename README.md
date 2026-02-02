<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

---
<br>


# Livewire + Laravel Coding Test – Crypto Price Dashboard


<div align="center">

| Role            | Laravel Developer Role     |
|-----------------|-----------------------------------|
| Team            | Backend (Web) Development Team    |
| Reports To      | Head of Software Development      |
| Time Allocation | 60 min                            |

</div>

<br>

This task is designed to take **45–60 minutes**, depending on your experience.

The goal is not perfection, but to understand **how you approach problems**, structure code, consume 3rd party APIs and use Livewire effectively.

---

## Goal

Build a small **crypto prices dashboard** using **Laravel + Livewire** that displays current market data from the **CoinGecko API**.


The dashboard should show live (or near-live) data without requiring full page reloads.

---

## What We’re Looking For

- Effective use of **Livewire reactivity**
- Clean separation of concerns
- Responsible external API usage (caching, rate awareness)
- Clear, readable, maintainable code
- Ability to explain design decisions

---

## Functional Expectations

Your solution should:

- Display data for **~5 major cryptocurrencies** in USD (API prices are in USD)
- Show key market information such as:
  - Coin name / symbol
  - Current price
  - 24h price change percentage
  - Market cap (nicely formatted)
- Keep data reasonably fresh (automatic or manual refresh is fine)
- Include **at least one interactive element** that affects what is displayed (for example: selecting a coin, highlighting it, showing details, etc.)
- ** We do not expect you to style the application, we are only interested in the code quality and the way you use Livewire and Laravel. **, unless you want to.

How you structure components and manage state is up to you.

---

## Technical Constraints

- Framework: **Laravel + Livewire**
- External data source: **CoinGecko API** (free tier, no API key required)
- Use Laravel’s `Http` client for API requests
- No database or authentication required
- No external JavaScript libraries beyond what Livewire / Alpine already provide

---

## API Reference

You may use CoinGecko’s public API.  
For example, this endpoint returns market data for several coins:

[https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=bitcoin,ethereum,solana,ripple,cardano&order=market_cap_desc&per_page=5&page=1&sparkline=false&price_change_percentage=24h](https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=bitcoin,ethereum,solana,ripple,cardano&order=market_cap_desc&per_page=5&page=1&sparkline=false&price_change_percentage=24h)

---

## Optional Task

If time allows, add **one automated test** that demonstrates how your code behaves when the external API is unavailable.

For example:
- Simulate the CoinGecko API being down or timing out
- Verify that cached data is still returned if available

You may use Laravel’s HTTP fakes and cache helpers.

This is optional and mainly intended to show how you think about reliability and failure scenarios.
