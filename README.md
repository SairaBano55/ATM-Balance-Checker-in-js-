# 🏦 ATM Withdrawal Simulator | JavaScript State Management

## 📌 Description
This repository features a JavaScript practice file that simulates a standard automated teller machine (ATM) transaction system. The script manages a user's account balance, evaluates conditional constraints during withdrawal requests (such as negative inputs or overdraft limits), updates the state dynamically, and outputs structured transaction confirmations.

---

## ⚡ Key Programming Concepts Applied
* 💵 **State Mutation:** Performing basic arithmetic operations (`balance - withdraw`) to update system states dynamically.
* 🔀 **Multi-Tier Validation:** Cascading through a highly reliable `if-else if-else` chain to filter out illegal user operations.
* 🛠️ **Logical Boundary Checks:** Enforcing boundary guards such as non-negative amounts (`<= 0`) and balance limits (`> balance`).
* 📟 **System Event Logs:** Communicating transaction state feedbacks to the developer console interface.

---

## 💻 Source Code

Here is the exact code structured in this repository:

```javascript
let balance = 50000;
let withdraw = 12000;

if(withdraw <= 0){
    console.log("Invalid Amount");
}
else if(withdraw > balance){
    console.log("Insufficient Balance");
}
else if(withdraw === balance){
    console.log("Account Balance is now 0");
}
else{
    balance = balance - withdraw;
    console.log("Withdraw Succesfull");
}
```

---

## 📊 Transaction Validation Matrix

| Withdrawal Condition | System Logic Evaluation | Terminal Response Log | State Update Action |
| :--- | :--- | :--- | :--- |
| 🚫 **`withdraw <= 0`** | Attempting an invalid or negative amount | `"Invalid Amount"` | Transaction aborted; balance unchanged |
| 📉 **`withdraw > balance`**| Overdraft check / Exceeding total funds | `"Insufficient Balance"` | Transaction aborted; balance unchanged |
| 🎯 **`withdraw === balance`**| Requesting exact total account holdings | `"Account Balance is now 0"`| Balance becomes `0` |
| ✅ **`withdraw < balance`** | Standard valid withdrawal operation | `"Withdraw Succesfull"` | Deducts funds: `balance = balance - withdraw` |

---

## 🖥️ Expected Execution Feedback

Based on the initialized data values inside this script (`balance = 50000`, `withdraw = 12000`):

```text
Withdraw Succesfull
```

### 💡 Quick State Verification:
* After execution, the current value of the `balance` variable is updated to: **`38000`**
* If you alter `let withdraw = 60000;`, the output changes to: `Insufficient Balance`

---

## 🚀 Execution Guide

### Method 1: Node.js Terminal Environment
1. Save the snippet into a script named `atm.js`.
2. Fire up your machine terminal in the same path.
3. Type and execute:
   ```bash
   node atm.js
   ```

### Method 2: Web Developer Console
1. Open any working web browser tab interface.
2. Toggle Developer Tools by striking `F12` (or Right-Click ➡️ **Inspect**).
3. Select the **Console** sub-tab layer view.
4. Paste the entire script block inside the text prompt line and hit **Enter**.

---
<p align="center">
  🚀 <i>Simulating real-world transactional rules is a huge step toward building safe financial APIs! Keep mastering your crafts.</i>
</p>

## ✍️ Author
- GitHub: [SairaBano55](https://github.com/SairaBano55)
