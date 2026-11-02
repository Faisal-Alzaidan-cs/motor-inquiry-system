# Motor Inquiry System 

A simplified backend simulation of the BCare motor insurance inquiry journey, built as part of the .NET Trainees assignment.

##  Architecture & Solution Structure

The solution follows strict **Clean Architecture** principles across two main APIs communicating exclusively through `HttpClientFactory` (no direct database sharing):

* **Motor.Inquiry API**: Represents the insurance platform orchestrating the inquiry flow (`API`, `Application`, `Domain`, `Infrastructure`).
* **Yaqeen API**: Represents government services providing citizen and vehicle data (`API`, `Application`, `Domain`, `Infrastructure`).

##  Tech Stack & Libraries

* **Framework:** .NET 8, ASP.NET Core
* **ORM:** Entity Framework Core (SQL Server)
* **Validation:** FluentValidation
* **Mailing/Mapping:** AutoMapper
* **Logging:** Serilog
* **Communication:** HttpClientFactory
* **Documentation:** Swagger / OpenAPI

##  User Stories & Features

* **US1 & US2:** Inquire about vehicles using either sequence number or plate number.
* **US3:** Validate customer National ID (10 digits) and Date of Birth.
* **US4 & US5:** Retrieve vehicle information and verify ownership against citizen data.
* **US6:** Store inquiry history and comprehensive request/response logs via Serilog.

##  Technical Requirements Implemented

* Global Exception Handling Middleware
* Strict input validation rules
* Comprehensive request/response logging
* Database migrations with EF Core

---
*Developed by Faisal Alzaidan as part of the .NET application programming training.*
