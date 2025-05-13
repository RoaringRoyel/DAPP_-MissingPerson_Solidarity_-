# DAPP_-MissingPerson_Solidarity_-
# Missing Persons Management System (Smart Contract + DApp)

A decentralized application (DApp) built on Ethereum using **Solidity**, **Truffle**, and **Ganache**, designed to manage and facilitate missing persons' search and recovery efforts. The system supports three types of users: **Admin**, **Reporter**, and **Investigator**.

## 📌 Features

### 🔐 User Roles
- **Admin**: Assigns investigators, updates missing person status, and receives appointment payments.
- **Reporter**: Reports missing persons, books investigation slots.
- **Investigator**: Tracks assigned cases and maintains an appointment schedule.

---

### ✅ Functionalities

#### 1. User Registration
- All users must register using the smart contract with the following info:
  - NID
  - Name
  - Role (Admin/Reporter/Investigator)
  - Address (Ethereum wallet)

#### 2. Add Missing Person (Reporter Only)
- Add details like:
  - Name, Age, Height
  - Description, Last Seen Location (Division)
  - Relative’s Contact Number
- Auto-generated **Case ID**
- System automatically calculates **Urgency Level**:
  - High: age < 18
  - Medium: age > 50
  - Low: age between 18 and 50

#### 3. Update Missing Person Status (Admin Only)
- Only Admins can mark a person as "found".
- Status once marked as "found" cannot revert to "missing".
- Invalid statuses are rejected with error messages.

#### 4. Assign Investigator (Admin Only)
- Admin can assign an investigator to a case.
- Investigators can handle multiple cases.
- Cannot assign the same investigator to the same case more than once.

#### 5. Search Missing Persons
- Filter missing persons by **division**.
- Display count of missing persons in each of the 8 divisions of Bangladesh.
- Sort results in ascending/descending order of missing counts.

#### 6. Book Investigation Slot (Reporter Only)
- Reporters can book an urgent investigation appointment.
- Requires payment (via MetaMask) to an Admin.
- Time slots are 10 minutes each (e.g., 4:00 PM - 4:10 PM).
- Only one appointment allowed per time slot per investigator.
- Automated interface update upon successful booking.

#### 7. View Appointment Schedule
- All users can view the complete appointment schedules of all investigators.

#### 💡 Bonus Feature:
- Investigators can notify Admins if a missing person is found to trigger a status update.

---

## 🛠️ Tech Stack

- **Smart Contract**: Solidity
- **Development Framework**: Truffle
- **Local Blockchain**: Ganache
- **Frontend**: JavaScript (with support for ReactJS if preferred)
- **Wallet Integration**: MetaMask

> ⚠️ **No external databases** (e.g., MongoDB, MySQL) are used. All data is stored and retrieved via the smart contract.

---

## 🚀 Getting Started

### Prerequisites
- Node.js
- Truffle
- Ganache
- MetaMask browser extension
