# Segmenting and Controlling Networks

## Segmenting the Network
- **Types**: Physical, logical, or virtual segmentation (e.g., devices, VLANs, virtual networks)
- **Performance**: Useful for isolating high-bandwidth applications
- **Security**: 
  - Users should not directly communicate with database servers
  - Only core apps like SQL and SSH should reside in secure segments
- **Compliance**: 
  - PCI compliance mandates segmentation
  - Eases change control procedures

## Access Control Lists (ACLs)
- **Purpose**: Allow or disallow traffic based on criteria
- **Criteria**: Source/destination IP, port, time, application, etc.
- **Access Restriction**: Can be limited by IP, user type, or identifiers
- **Warning**: Misconfiguration may lock out access

## ACL Examples
- Permissions can be assigned per user and IP:
  - Bob: read files
  - Fred: access network
  - James: access 192.168.1.0/24 on ports 80, 443, 8088
- Common in OS-level file access

## Application Allow List / Deny List
- **Danger**: Any app can contain vulnerabilities or malware
- **Security Policy**: Uses allow lists or deny lists
  - **Allow List**: Only explicitly approved apps can run
  - **Deny List**: Everything can run except apps on the block list

## Allow/Deny List Examples
- **Decision Points**:
  - **Application hash**: Unique identifier for app integrity
  - **Certificate**: Digitally signed apps only
  - **Path**: Apps must run from allowed directories
  - **Network Zone**: Execution limited to specific zones (e.g., private/public)
