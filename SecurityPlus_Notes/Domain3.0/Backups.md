
# Backup and Data Recovery Strategies

This video outlines essential strategies for creating, storing, and testing data backups to ensure business continuity and disaster recovery.

---

## 1. Importance of Backups

- **Purpose**: Recover critical data and maintain business operations during disasters.
- **Factors to Consider**:
  - Total volume of data.
  - Type and media of backup.
  - Storage location (on-site, off-site, cloud).
  - Backup software and frequency.

---

## 2. Onsite vs. Offsite Backups

- **Onsite Backups**:
  - Immediate access.
  - No internet needed.
  - Typically less costly.
- **Offsite Backups**:
  - Transferred via WAN or internet.
  - Accessible after a disaster from any location.
- **Best Practice**: Use both to increase redundancy and recovery flexibility.

---

## 3. Frequency of Backups

- **Intervals**: Weekly, daily, hourly depending on system needs.
- **Strategies**:
  - Daily, weekly, and monthly backup sets.
  - Tailor based on how often data changes.
- **Planning**:
  - Multiple backup sets and types of media.
  - Different strategies for different systems.

---

## 4. Snapshots

- **Use Case**: Common in virtualized/cloud environments.
- **What It Does**:
  - Captures system state at a point in time.
  - Allows rollback to previous states.
- **Frequency**:
  - Typically daily.
  - Stores only changes since the last snapshot.

---

## 5. Recovery Testing

- **Why It Matters**: A backup is only useful if it can be restored.
- **Testing Methods**:
  - Simulate disasters and restore processes.
  - Confirm data and application functionality.
- **Audit Regularly**: Weekly, monthly, or quarterly checks to verify integrity.

---

## 6. Replication

- **Definition**: Real-time or near real-time data copy across locations.
- **Advantages**:
  - Data always available.
  - Useful for disaster recovery and high availability.
  - Enables quick failover to hot sites.

---

## 7. Journaling

- **Purpose**: Prevent corruption during unexpected shutdowns (e.g., power loss).
- **Method**:
  - Write intent to a journal first.
  - Commit to storage after journal entry.
  - Recover from journal after power is restored.

---
