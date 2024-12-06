# Software Requirements Specification (SRS)  

## 1. Introduction  

### 1.1 Purpose  
The purpose of this document is to define the software requirements for a **Supply Chain Management (SCM)** system. The system will streamline supplier management, order processing, inventory control, logistics, pricing, and reporting, focusing on operational efficiency and cost-effectiveness.  

### 1.2 Scope  
The SCM system will be developed for use within Ho Chi Minh City to manage supply chain activities, including:  
- Supplier management  
- Order management (inbound/outbound)  
- Inventory management  
- Logistics and delivery  
- Pricing and payments  
- Reporting and analytics  

The system will be developed using **Nest.js** for backend, **Next.js** for frontend, and deployed within a tight timeline of **1 month**.  

### 1.3 Key Features  
- Comprehensive order lifecycle management with status tracking.  
- Automatic supplier evaluation and inventory alerts.  
- Integration with **Momo** and **VNPAY** for payment processing.  
- Role-based access with real-time dashboards and visual reporting.  

## 2. Stakeholder Analysis  

### 2.1 Roles and Responsibilities  

| **Role**              | **Key Responsibilities**                                         |  
|-----------------------|------------------------------------------------------------------|  
| **Admin**             | Manage users, orders, inventory, and reports.                    |  
| **Supplier**          | Manage product listings, monitor inbound orders, view ratings.   |  
| **Distributor**       | Place outbound orders, track order statuses, view invoices.      |  
| **Logistics Partner** | Update delivery statuses, manage assigned orders.                |  

### 2.2 Access Permissions  

| **Role**              | **Access**                                | **Actions**                      |  
|-----------------------|-------------------------------------------|----------------------------------|  
| **Admin**             | Full                                      | CRUD on all entities, reporting. |  
| **Supplier**          | Limited to their own products and orders. | Edit products, view ratings.     |  
| **Distributor**       | Outbound orders only.                     | Place, track orders.             |  
| **Logistics Partner** | Assigned deliveries.                      | Update shipment statuses.        |  

## 3. Functional Requirements  

### 3.1 Supplier Management  
- Add/Edit/Delete supplier details (e.g., name, address, MST, payment terms).  
- **Rating System**: Score suppliers on criteria (e.g., timeliness, quality) using a 10-point scale. Ratings computed automatically, adjustable by admin.  

### 3.2 Order Management  

#### Inbound Orders  
- Place orders with suppliers for restocking.  
- Status tracking: **New → Confirmed → In Transit → Delivered → Cancelled**.  
- Notifications via **email** and **SMS** for status updates.  

#### Outbound Orders  
- Place orders for customers/distributors.  
- Status tracking: Same workflow as inbound orders.  

### 3.3 Inventory Management  
- **Tracking**: Real-time inventory by SKU, batch, or product.  
- **Alerts**: Notify admin and suppliers when stock levels fall below a threshold.  
- **Replenishment Recommendations**: Predict inventory needs using historical trends.

### 3.4 Logistics and Delivery  
- Assign deliveries to logistics partners.  
- Status tracking: **Scheduled → Picking Up → In Transit → Delivered → Cancelled**.  
- Manual updates by logistics partners.  
- Future: GPS-based location tracking for shipments.  

### 3.5 Pricing and Payment  
- **Dynamic Pricing**: Configure prices per product and service (e.g., transport, storage).  
- **Online Payments**: Integration with **Momo** and **VNPAY** for seamless transactions.  
- Invoice generation and payment status tracking.  

### 3.6 Reporting and Analytics  
- Reports include:  
  - Inventory levels, stockouts, and expiring items.  
  - Supplier performance (delivery rates, quality scores).  
  - Operational costs (transportation, warehousing).  
- Export formats: **PDF**, **Excel**, and **visual dashboards**.  

## 4. Non-Functional Requirements  

- **Performance**: Support 100 concurrent users, scalable to 500.  
- **Security**:  
  - Role-based access control (RBAC).  
  - Data encryption and secure communication using **SSL/TLS**.  
- **Scalability**: Expandable for additional warehouses, suppliers, and logistics partners.  
- **Localization**: Primary language: **Vietnamese**, with optional **English** support.  

## 5. Assumptions  

1. **Data Initialization:**  
   - Admin will manually input initial datasets for testing and operational readiness.  
2. **System Usage:**  
   - Users will have internet access and compatible devices (desktop or mobile).  
3. **Third-Party Integrations:**  
   - Payment gateways like **Momo** and **VNPAY** provide stable and documented APIs.  

## 6. Risks  

1. **Operational Risks:**  
   - **Unclear Requirements:** May lead to rework.  
     *Mitigation:* Regular meetings to validate features.  
   - **Manual Processes:** Risk of inaccuracy in logistics updates.  
     *Mitigation:* Future-proof system design for GPS tracking.  

2. **Technical Risks:**  
   - **Integration Challenges:** Issues with third-party APIs.  
     *Mitigation:* Test APIs early and maintain fallback mechanisms.  

3. **Resource Risks:**  
   - **Timeline Constraints:** Tight deadline may require trade-offs.  
     *Mitigation:* Define Minimum Viable Product (MVP).  

## 7. UX/UI Requirements  

### 7.1 Dashboard  
- Overview of orders, inventory, supplier ratings, and operational KPIs.  
- Visual elements: **Graphs, Charts, Notifications**.  

### 7.2 Supplier Management  
- **List View**: Filter by ratings, location, or status.  
- **Detail View**: Full profile with ratings and transaction history.  

### 7.3 Order Management  
- **Tabs**: Separate inbound/outbound orders.  
- **Order Details**: View/edit order statuses, send notifications.  

### 7.4 Inventory Management  
- **Stock Overview**: Real-time visibility of all SKUs.  
- **Low Stock Alerts**: Prominent display for urgent actions.  

### 7.5 Logistics  
- **Delivery Overview**: Track deliveries in progress.  
- **Update Form**: Simple interface for status changes.  

## 8. Acceptance Criteria and Deliverables  

### 8.1 Acceptance Criteria  
1. Users can perform end-to-end order management (inbound and outbound orders).  
2. Inventory levels are tracked in real-time with low-stock alerts.  
3. Integration with **Momo** and **VNPAY** for payments.  
4. Generate operational reports in **PDF** and **Excel** formats.  
5. System handles at least **100 concurrent users** and scales to **500 users** without significant latency.  

### 8.2 Deliverables  
1. **Backend Services:** APIs for order management, inventory tracking, and payment processing.  
2. **Frontend Application:** Responsive web interface for all user roles.  
3. **Documentation:** User manual and technical documentation.  
4. **Deployment:** Functional system deployed to staging and live environments.  
5. **Test Results:** Comprehensive test cases and results.  
