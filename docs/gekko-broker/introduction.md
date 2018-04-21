# Gekko Broker

Order execution library for bitcoin and crypto exchanges. This library is Gekko's execution engine for all live orders (simulated orders go through the paper trader, which is a separate module). This library is intended for developers of trading systems in need for advanced order types on multiple exchanges over a unified API.

## Introduction

This library makes it easy to do (advanced) orders all crypto exchanges where Gekko can live trade at. See the complete list here: https://gekko.wizb.it/docs/introduction/supported_exchanges.html

This library allows you to:

- Get basic market data
  - ticker (BBO)
  - orderbook (TODO)
  - historical trades
- Get portfolio data
- Do an (advanced) order:
  - Submit the order to the exchange
  - Receive events about the status of the order:
    - submitted
    - open (accepted)
    - partially filled
    - rejected
    - completed
  - Mutate the order
    - cancel
    - amend
      - move
      - move limit
- Tracks orders submitted through the library.

## Status

Early WIP. All communication is via the REST APIs of exhanges. Not all exchanges are supported.

## Order types

This library aims to offer advanced order types, even on exchanges that do not natively support them by tracking the market and supplimenting native order support on specific exchanges.

WIP:

- Base orders
  - Limit Order
  - [Sticky Order](./sticky_order.md)

TODO:

- Base orders:
  - Market Order
- Triggers:
  - Stop
  - If Touched (stop but opposite direction)
  - Time

### TODO

- finish all exchange integrations that gekko supports
- finsih all order types and triggers (under todo)
- implement websocket support (per exchange)
- 