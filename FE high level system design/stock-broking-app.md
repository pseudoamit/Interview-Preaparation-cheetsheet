# Frontend System Design Interview Questions (Senior React / Frontend Engineer)

This document contains **high-level system design questions** commonly asked in interviews for **Senior Frontend Engineers (7+ years)**.  
The questions focus on **architecture, API design, data flow, scalability, and real-time UI systems**.

---

# 1. Stock Trading Platform (Groww-like Application)

Design a **high-level system architecture for a stock trading application similar to Groww**.

The system should support the following capabilities:

## Core Features

1. Display a user's **stock holdings**.
2. Show **real-time stock price updates**.
3. Display **price changes and percentage movements**.
4. Show **top-performing and worst-performing stocks**.
5. Allow users to **schedule buy and sell orders**.
6. Display **portfolio performance analytics**.

## System Design Considerations

While designing the system, explain the following:

### Frontend Architecture

- How would you structure the **frontend architecture** for such an application?
- How would the UI handle **real-time stock price updates**?
- How would you efficiently update the UI when **stock prices change frequently**?

### API Design

Design the APIs required for:

- Fetching user portfolio holdings
- Fetching stock market data
- Placing buy/sell orders
- Scheduling buy/sell orders
- Fetching top-performing and worst-performing stocks

### Data Flow

Explain:

- How the **frontend communicates with backend services**
- How **stock market data flows through the system**
- How **real-time updates are pushed to users**
- How **How do you sync the data through out the multiple tabs that every tabs reflect the same price or data**

### Real-Time Updates

How would you implement **real-time stock price updates**?

Consider approaches such as:

- WebSockets
- Server-Sent Events
- Polling strategies

### Scalability

How would the system handle:

- Millions of users
- High-frequency stock price updates
- Peak trading hours

### Data Storage

What type of data storage would you use for:

- User portfolio data
- Transaction history
- Market data
- Cached stock prices

### Performance Optimization

How would you optimize:

- Rendering performance
- Data updates
- Network usage
- API requests

---
