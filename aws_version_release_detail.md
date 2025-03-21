### **5.19.0 (2025-02-12)**
#### **Features**
- **Enhancing VPC Security with Amazon VPC Block Public Access (#1159) (387f5ee)**
  - This update adds an important security feature that allows users to block public access to VPCs. 
  - It likely introduces new settings to restrict unintended public exposure of resources within the VPC.

---

### **5.18.1 (2025-01-28)**
#### **Bug Fixes**
- **Fixed `service_region` argument in the VPC endpoint module (#1162) (5415dee)**
  - The update corrects an issue where the `service_region` argument for VPC endpoints was not functioning correctly.
  - This fix ensures that VPC endpoints are properly associated with the intended AWS region.

---

### **5.18.0 (2025-01-27)**
#### **Features**
- **Support for cross-region VPC endpoints (#1161) (7e205ad)**
  - Introduces the ability to create VPC endpoints that work across different AWS regions.
  - This is useful for multi-region architectures where services in one region need to connect to resources in another.

---

### **5.17.0 (2024-12-18)**
#### **Features**
- **Define default name for VPC endpoint (#1151) (41348d3)**
  - Adds a feature to automatically assign a default name to VPC endpoints.
  - This helps with easier identification and management of endpoints without requiring manual naming.

---

### **5.16.0 (2024-11-18)**
#### **Features**
- **Added additional conditions into Flow Log IAM Role Assumption Policy (#1138) (7744d3f)**
  - Enhances security by adding more conditions to the IAM policy for assuming roles related to VPC Flow Logs.
  - Likely prevents unauthorized access and enforces stricter security policies.

---

### **5.15.0 (2024-11-03)**
#### **Features**
- **Add option to create/delete NAT Gateway route for private route tables (#1127) (f02a1af)**
  - Introduces an option to control the creation and deletion of NAT Gateway routes in private route tables.
  - Helps manage internet connectivity for private subnets more effectively.

---

### **5.14.0 (2024-10-18)**
#### **Features**
- **Add outputs for the full list of subnets created and their attributes (#1116) (e212245)**
  - Enhances visibility by providing a comprehensive output of all created subnets and their details.
  - Useful for infrastructure automation and debugging.

#### **Bug Fixes**
- **Update CI workflow versions to latest (#1125) (b1f2125)**
  - Updates continuous integration (CI) workflow dependencies to the latest versions.
  - Ensures better compatibility and reduces issues in automated testing and deployment.

---

### **5.13.0 (2024-08-16)**
#### **Features**
- **Add support for `ip_address_type` for VPC endpoint (#1096) (d868303)**
  - Allows specifying whether a VPC endpoint should use IPv4, IPv6, or both.
  - Provides more flexibility in network configurations.

---

### **5.12.1 (2024-08-09)**
#### **Bug Fixes**
- **Update flow log ARNs to use partition from `aws_partition` data source (#1112) (72cde38)**
  - Fixes an issue where Flow Log ARNs were not correctly referencing the AWS partition.
  - Ensures compatibility with AWS GovCloud and other partitions.

---

### **5.12.0 (2024-08-03)**
#### **Features**
- **Restrict flow log policy to use log group ARNs (#1088) (9256722)**
  - Enhances security by limiting Flow Log policies to reference only specific log groups.
  - Prevents misconfigurations that could allow logs to be stored in unauthorized locations.

---

### **5.11.0 (2024-08-03)**
#### **Features**
- **Add route to `0.0.0.0/0` & `::/0` (when IPv6 is enabled) on all public route tables (#1100) (b3e7803)**
  - Ensures that public route tables include a default route to the internet for both IPv4 and IPv6.
  - Essential for proper public internet access configurations.

---

### **5.10.0 (2024-08-02)**
#### **Features**
- **Added `ipv6_address_preferred_lease_time` parameter to `aws_vpc_dhcp_options` resource (#1105) (3adb594)**
  - Introduces a new setting to specify the lease time preference for IPv6 addresses in DHCP options.
  - Useful for managing address lifetimes in dynamic environments.

---

### **5.9.0 (2024-07-05)**
#### **Features**
- **Allow custom VPC Flow Log IAM Role name and IAM Policy name (#1089) (f8cd168)**
  - Provides the ability to define custom names for IAM roles and policies related to VPC Flow Logs.
  - Helps in organizing and managing IAM resources more effectively.

---
