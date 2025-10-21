# Mikroservis E-Ticaret Sistemi

Spring Boot, React ve PostgreSQL kullanarak geliştirilmiş basit bir e-ticaret mikroservis uygulaması.

## Teknolojiler
- **Backend:** Spring Boot, Spring Cloud Gateway
- **Frontend:** React
- **Database:** PostgreSQL
- **Containerization:** Docker

## Servisler
- **User Service** (Port: 8081) - Kullanıcı yönetimi
- **Product Service** (Port: 8082) - Ürün yönetimi
- **Order Service** (Port: 8083) - Sipariş yönetimi
- **API Gateway** (Port: 8080) - Ana giriş noktası

## Kurulum

### Gereksinimler
- Java 17+
- Node.js 16+
- Docker & Docker Compose
- PostgreSQL

### Çalıştırma
```bash
# Docker ile veritabanlarını başlat
docker-compose up -d

# Servisleri sırayla başlat
cd services/user-service && ./mvnw spring-boot:run
cd services/product-service && ./mvnw spring-boot:run  
cd services/order-service && ./mvnw spring-boot:run
cd services/api-gateway && ./mvnw spring-boot:run

# Frontend'i başlat
cd frontend/ecommerce-ui && npm start
```

## API Dokümantasyonu
- User Service: http://localhost:8081/swagger-ui.html
- Product Service: http://localhost:8082/swagger-ui.html
- Order Service: http://localhost:8083/swagger-ui.html

## Geliştirme Notları
Bu proje mikroservis mimarisi öğrenmek amacıyla geliştirilmiştir.