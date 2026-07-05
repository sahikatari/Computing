# ⚖️ Components of AWS Load Balancer

An **AWS Load Balancer** distributes incoming traffic across multiple EC2 instances to improve **availability, scalability, and fault tolerance**.

---
# 📦 Components of a Load Balancer

| Component | Description |
|------------|-------------|
| ⚖️ **Load Balancer** | Receives incoming traffic and distributes it across multiple targets. |
| 🎯 **Listener** | Checks incoming requests on a specific protocol and port (e.g., HTTP:80, HTTPS:443). |
| 📜 **Listener Rules** | Defines how requests are routed based on conditions like URL path or hostname (ALB only). |
| 🎯 **Target Group** | A group of registered targets (EC2, IP addresses, Lambda) that receive traffic. |
| 🖥️ **Targets** | Backend resources such as EC2 instances, containers, or Lambda functions. |
| ❤️ **Health Checks** | Periodically checks whether targets are healthy before sending traffic. |
| 📈 **Auto Scaling Group (Optional)** | Automatically adds or removes EC2 instances based on demand. |
| 🌐 **Availability Zones (AZs)** | Distributes traffic across multiple AZs for high availability. |

---

# 🔍 Component Explanation

### 1️⃣ Load Balancer
- Entry point for client requests.
- Distributes traffic across healthy targets.
- Improves application availability and reliability.


### 2️⃣ Listener
A **Listener** waits for incoming connections on a specific **protocol** and **port**.

**Examples**

| Protocol | Port |
|----------|------|
| HTTP | 80 |
| HTTPS | 443 |
| TCP | 3306 |
| UDP | 53 |


### 3️⃣ Listener Rules (ALB Only)

Listener rules decide **where the request should go**.

### Example

| Request | Target Group |
|----------|--------------|
| `/api/*` | API Servers |
| `/images/*` | Image Servers |
| `/` | Web Servers |


### 4️⃣ Target Group

A **Target Group** is a collection of backend resources that receive traffic.

Supported Targets:
- 🖥️ EC2 Instances
- 🌐 IP Addresses
- ⚡ Lambda Functions


### 5️⃣ Targets

Targets are the actual backend resources that process user requests.

Examples:
- EC2 Instances
- ECS Tasks
- Lambda Functions
- IP Addresses


### 6️⃣ Health Checks

The Load Balancer continuously checks whether targets are healthy.

If a target becomes unhealthy:
- ❌ Stops sending traffic to it.
- ✅ Routes traffic only to healthy targets.



### 7️⃣ Auto Scaling Group (Optional)

Works together with the Load Balancer to automatically:
- ➕ Launch new EC2 instances during high traffic.
- ➖ Terminate extra EC2 instances during low traffic.


### 8️⃣ Availability Zones (AZs)

A Load Balancer can distribute traffic across multiple Availability Zones.

Benefits:
- High Availability
- Fault Tolerance
- Better Reliability

---
