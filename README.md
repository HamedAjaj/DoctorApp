<img width="800" height="812" alt="Screenshot 2025-07-19 123341" src="https://github.com/user-attachments/assets/ca603c41-da2c-48a4-8553-da1831a82d84" />

# DoctorApp  With different architectures
DoctorApp Modular Monolith
DoctorAppointmentApp (Solution)
│
├── DoctorAvailabilityModule      # Layered Architecture
│   ├── Application
│   ├── Domain
│   ├── Infrastructure
│   └── API
│
├── AppointmentBookingModule      # Clean Architecture
│   ├── Application
│   ├── Domain
│   ├── Infrastructure
│   ├── API
│   └── Core (SharedKernel)
│
├── AppointmentConfirmationModule # Simplest Architecture Possible
│   └── API (all in one layer)
│
├── DoctorAppointmentManagement   # Hexagonal Architecture (Ports/Adapters)
│   ├── Domain
│   ├── Application
│   ├── Adapters
│   │   ├── Inbound (API Controllers)
│   │   └── Outbound (Persistence)
│   └── Core (Ports)
│
├── SharedKernel                   # For shared types across modules
│
└── WebApiGateway (Entry point - ASP.NET Minimal API or MVC)
****
