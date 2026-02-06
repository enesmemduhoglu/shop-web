# Shop Web Projesi

Bu proje, **Spring Boot (Backend)** ve **React (Frontend)** tabanlı, Docker ile konteynerize edilmiş bir web uygulamasıdır. Proje monorepo yapısında organize edilmiştir ve tüm servisler `docker-compose` ile tek komutla ayağa kaldırılabilir.

---

## 📁 Proje Yapısı

```
shop-web/
│
├── backend/              # Spring Boot backend uygulaması
│   ├── Dockerfile
│   └── .env
│
├── frontend/             # React frontend uygulaması
│   ├── Dockerfile
│   └── .env
│
├── docs/                 # Proje dokümantasyonları ve diyagramlar
│   ├── cloud-architecture.png
│   ├── object-diagram.png
│   ├── sequence.png
│   ├── state-diagram.png
│   ├── use-case-diagram.png
│   └── swot.png
│
├── docker-compose.yml    # Tüm servislerin merkezi yönetimi
└── README.md
```

---

## 🧩 Kullanılan Teknolojiler

### Backend

* Java 17
* Spring Boot
* Spring Data JPA
* Spring Data Elasticsearch
* PostgreSQL
* Redis

### Frontend

* React
* Node.js 18

### Altyapı

* Docker
* Docker Compose
* Elasticsearch
* Kibana

---

## 🚀 Uygulamayı Çalıştırma

### Gereksinimler

* Docker
* Docker Desktop (Windows / macOS için)

### Çalıştırma

Proje kök dizinindeyken aşağıdaki komutu çalıştırmanız yeterlidir:

```bash
docker compose up --build
```

Bu komut aşağıdaki servisleri ayağa kaldırır:

* PostgreSQL
* Elasticsearch
* Redis
* Kibana
* Backend (Spring Boot)
* Frontend (React)

---

## 🌐 Servis Erişim Adresleri

| Servis        | URL                                            |
| ------------- | ---------------------------------------------- |
| Frontend      | [http://localhost:3000](http://localhost:3000) |
| Backend API   | [http://localhost:8080](http://localhost:8080) |
| PostgreSQL    | localhost:5432                                 |
| Elasticsearch | [http://localhost:9200](http://localhost:9200) |
| Kibana        | [http://localhost:5601](http://localhost:5601) |

---

## 🐳 Docker Mimarisi

* Tüm servisler aynı **bridge network** üzerinde çalışır
* Servisler arası iletişim container isimleri üzerinden sağlanır
* Backend, Elasticsearch ve PostgreSQL'e `localhost` yerine servis isimleriyle bağlanır

---

## 📊 Dokümantasyon

`docs/` klasörü altında proje için hazırlanan mimari ve analiz diyagramları bulunmaktadır:

* Cloud Architecture Diagram
* Use Case Diagram
* Sequence Diagram
* State Diagram
* Object Diagram
* SWOT Analizi

Bu diyagramlar bitirme projesi ve teknik raporlar için referans olarak kullanılabilir.

---

## 🧪 Notlar

* Elasticsearch bağlantısı Docker ortamı için yapılandırılmıştır
* Local çalışmada `application.properties` üzerinden override edilebilir
* Gerekirse Elasticsearch repository'leri devre dışı bırakılabilir

---

## 👤 Geliştirici

**Enes**

