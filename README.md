# Cloud-Native RBAC & Authorization Framework 

## Overview 
This project focuses on designing a cloud-native authorization system inspired by Grafana's (versio >= 12.0) RBAC model.
The main goal is to enable fine-grained access control for APIs, resources, and services, using a Java Spring ecosystem.
It is intended as a foundation for building multi-tenant, secure, and cloud-compatible applications. 

---

## Objectives 
### Role-Based Access Control (RBAC)
- Define roles and permissions for system users and service accounts. 
- Map roles to resources and allowed actions at a granular level (create, read, update, delete, etc.).
- Support hierarchical roles and inheritance where needed. 


### Authorization Mechanism 
- Centralize authentication and authorization logic.
- Enforce policy decisions consistently across services.
- Integrate with Spring Security for web endpoints and API gateway enforcement.


### Token Management 
- Use tokens for user and service account authentication.
- Support long-lived and short-lived tokens for different scenaros.
- Enable token revocation, rotation, and auditing.
- Ensure compatibility with cloud-native, identity providers if needed. 


### API-Level Role Enforcement
- Apply role-based permissions directly on API endpoints
- Differentiate between resource types (dashboards, folders, data sources, etc.).
- Enable per-organization and per-user scoping of API operations. 
- Provide audit logs and visibility for token usage and access patterns. 


### Cloud-Native Design Considerations
- Ensure the system is compatible with Kubernetes and service mesh environments. 
- Support multi-tenant deployments with isolated authorization contexts. 
- Design for observability: logs, metrics, and tracing of authorization decisions.
- Future-proof the system for integration with other cloud-native applications and services. 


---
## Reference Architecture
- **Identity Layer**: Handles authentication, token issuance, and session management. 
- **Policy Layer**: Centralized policy definitions based on roles, permissions, and resources. 
- **Enforcement Layer**: Intercepts API calls and validates tokens and role permissions.
- **Audit & Monitoring**: Tracks access requests, token usage, and policy violations.

---


## Goals for Implementation 
- Enable consistent and centralized RBAC enforcement for all microservices. 
- Provide extensible for new roles, resources, and permissions. 
- Achieve separation of concerns between authentication, authorization, and business logic.
- Prepare the system for cloud-native deployment scenarios and multi-tenant architectures. 