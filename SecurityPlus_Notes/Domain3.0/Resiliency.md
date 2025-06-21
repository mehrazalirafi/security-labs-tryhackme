
# High Availability and Resiliency Strategies

## High Availability (HA)
- Redundancy ≠ Always Available (manual intervention may be required)
- HA ensures systems are always on and accessible
- Often involves multiple components (e.g., Active/Active setups)
- Higher availability generally increases cost due to extra components, power, and maintenance

## Server Clustering
- Combines multiple servers into one logical unit
- Appears as a single device to users
- Improves scalability and availability
- Requires identical OS configurations and shared storage

## Load Balancing
- Distributes traffic across multiple servers
- Servers are unaware of each other
- Allows use of different operating systems
- Load balancer adds/removes devices as needed
- Ensures continued availability if one server fails

## Site Resiliency
- Prepares a recovery site with synchronized data
- Used during disasters (failover process)
- Revert back to primary once issues are resolved

## Recovery Site Types
### Hot Site
- Fully operational duplicate of the primary site
- Automatically updated hardware/software/data

### Cold Site
- Empty facility (no hardware, no data, no personnel)
- Requires manual setup during a disaster

### Warm Site
- Hybrid between hot and cold
- Some equipment and data are available
- Additional components must be brought in

## Geographic Dispersion
- Recovery sites should be in physically separate locations
- Reduces risk from natural disasters (e.g., floods, hurricanes)
- Introduces logistical challenges (equipment and personnel transport)

## Platform Diversity
- Use different OS/platforms to reduce shared vulnerabilities
- Example: mixing Windows, Linux, macOS for clients and servers

## Multi-Cloud Systems
- Use multiple cloud providers (AWS, Azure, Google Cloud, etc.)
- Provides fault tolerance in case one provider fails
- Data and services are dispersed geographically and across providers

## COOP (Continuity of Operations Planning)
- Alternative workflows for when tech systems fail
- Includes manual transactions, paper receipts, and phone verifications
- Must be pre-documented and tested

---
