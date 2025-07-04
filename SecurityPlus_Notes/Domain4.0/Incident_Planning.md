# Incident Response Testing & Threat Hunting

## Training & Exercising
- **Pre-Incident Preparation**  
  - Limited on-the-job training during actual events  
  - Essential training areas:  
    • Initial response protocols  
    • Investigation methodologies  
    • Incident documentation/reporting  
  - Cost scales with team size  

- **Testing Framework**  
  | Exercise Type       | Frequency         | Key Rules                      |
  |---------------------|-------------------|--------------------------------|
  | Scheduled Drills    | Annual/semi-annual| Never touch production systems |
  | Scenario-based Tests| Time-limited      | Evaluate/document outcomes     |

## Exercise Methodologies
### Tabletop Exercises
- **Advantages over full-scale drills**:  
  - Cost-effective (no physical resources required)  
  - Time-efficient (hours vs. days)  
  - Collaborative problem-solving with key stakeholders  
- **Process**:  
  1. Simulate disaster scenarios  
  2. Walk through response procedures  
  3. Identify process gaps  

### Simulation Testing
- **Common Simulations**:  
  - Phishing campaigns  
  - Password reset social engineering  
  - Simulated data breaches  
- **Phishing Test Framework**:  
  ```mermaid
  graph LR
  A[Create phishing email] --> B[Send to users]
  B --> C{Filter effectiveness?}
  C -->|Bypassed| D[User clicks?]
  D -->|Yes| E[Flag for training]
  D -->|No| F[Validate awareness]
