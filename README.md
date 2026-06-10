# SNAPFD – Order Processing Microservices System

A lightweight Go-based microservices system for handling order creation and processing in a decoupled architecture.

The system is split into independent services:
- **Order Service**: responsible for creating and receiving orders via REST API
- **Order Processing Service**: responsible for processing incoming orders

---

## API Reference

### Create Order

```bash
POST /api/v1/order
```

Creates a new order in the system and forwards it for processing.

---

## Architecture

The system follows a microservices-style architecture where order creation and order processing are separated into independent components to improve scalability and separation of concerns.

---

## Deployment

Clone and run the application:

```bash
git clone https://github.com/farhadiis/snapfd-go.git
cd snapfd-go
sudo ./build.sh
sudo ./run.sh
```

---

## Testing

Run unit tests for each service:

```bash
go test ./order/tests -v
go test ./order-process/tests -v
```
