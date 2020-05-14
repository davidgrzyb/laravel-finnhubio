# A Simple Finnhub.io Package for Laravel

[![Latest Version on Packagist](https://img.shields.io/packagist/v/davidgrzyb/laravel-finnhubio.svg?style=flat-square)](https://packagist.org/packages/davidgrzyb/laravel-finnhubio)
[![Build Status](https://img.shields.io/travis/davidgrzyb/laravel-finnhubio/master.svg?style=flat-square)](https://travis-ci.org/davidgrzyb/laravel-finnhubio)
[![Quality Score](https://img.shields.io/scrutinizer/g/davidgrzyb/laravel-finnhubio.svg?style=flat-square)](https://scrutinizer-ci.com/g/davidgrzyb/laravel-finnhubio)
[![Total Downloads](https://img.shields.io/packagist/dt/davidgrzyb/laravel-finnhubio.svg?style=flat-square)](https://packagist.org/packages/davidgrzyb/laravel-finnhubio)

This Laravel package simplifies the usage of Finnhub.io's API for getting stock, forex and crypto data. Currently only the Stock Price, Forex and Crypto endpoints are supported.

## Installation

You can install the package via composer:

```bash
composer require davidgrzyb/laravel-finnhubio
```

## Usage

### Stock Prices

``` php
// Quote endpoint:
Finnhubio::stock()->getQuote('AAPL');
// Candles endpoint:
Finnhubio::stock()->getCandles('AAPL', 'D', now()->subDays(2), now(), 'json', false);
// Dividends endpoint:
Finnhubio::stock()->getDividends('AAPL', now()->subYear(1), now());
// Splits endpoint:
Finnhubio::stock()->getSplits('AAPL', );
```

### Forex

``` php
// Exhanges endpoint:
Finnhubio::forex()->getExchanges();
// Symbols endpoint:
Finnhubio::forex()->getSymbols('oanda');
// Candles endpoint:
Finnhubio::forex()->getCandles('AAPL', 'D', now()->subDays(1), now(), 'json');
// All rates endpoint:
Finnhubio::forex()->getRates();
```

### Crypto

``` php
// Exchanges endpoint:
Finnhubio::crypto()->getExchanges();
// Symbols endpoint:
Finnhubio::crypto()->getSymbols('binance');
// Candles endpoint:
Finnhubio::crypto()->getCandles('AAPL');
```

<!-- ### Testing

``` bash
composer test
``` -->

<!-- ### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently. -->

<!-- ## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details. -->

<!-- ### Security

If you discover any security related issues, please email grzybdavid@gmail.com instead of using the issue tracker. -->

<!-- ## Credits

- [David Grzyb](https://github.com/davidgrzyb)
- [All Contributors](../../contributors) -->

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

## Laravel Package Boilerplate

This package was generated using the [Laravel Package Boilerplate](https://laravelpackageboilerplate.com).