# AI Micro-Entrepreneur Assistant – System Design

## 1. System Overview

AI Micro-Entrepreneur Assistant is a WhatsApp-based AI system designed to help street vendors track sales, calculate profit, manage inventory, forecast demand, and receive intelligent business suggestions.

---

## 2. System Architecture

### 2.1 High-Level Components

- WhatsApp Business API (User Interface)
- Backend Server (FastAPI)
- Database (PostgreSQL)
- AI Engine (Forecasting + Recommendation System)
- Cloud Infrastructure (AWS EC2 + AWS RDS)

---

## 3. Data Flow

1. Vendor sends daily sales message via WhatsApp.
2. WhatsApp Business API forwards message to backend.
3. Backend parses sales data.
4. Data stored in PostgreSQL database.
5. AI engine analyzes sales history.
6. System generates business report.
7. Report sent back to vendor via WhatsApp.

---

## 4. AI Models Used

### 4.1 Demand Forecasting
- Moving Average Model
- ARIMA (Auto-Regressive Integrated Moving Average)

### 4.2 Recommendation Engine
- Rule-based cross-sell logic
- Regression-based demand-price relationship

---

## 5. Database Design

### Tables:

Products:
- product_id
- name
- cost_price
- selling_price
- current_stock

Sales:
- sale_id
- product_id
- quantity
- sale_date

Daily_Report:
- date
- total_revenue
- total_profit

---

## 6. Deployment Architecture

- Backend hosted on AWS EC2
- Database hosted on AWS RDS
- API communication secured via HTTPS
- WhatsApp API integration via Twilio or Meta Cloud API

---

## 7. Scalability Considerations

- Stateless backend architecture
- Horizontal scaling via EC2 auto-scaling
- Database indexing for fast queries

---

## 8. Security Considerations

- Encrypted API communication (HTTPS)
- Secure credential storage
- Role-based access control (future scope)
