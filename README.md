
# 🧪 Restful Booker API Testing

This repository contains a Postman test collection for the [Restful Booker API](https://restful-booker.herokuapp.com).

## 📂 Repository Contents

| Name                          | Description                           |
|-------------------------------|---------------------------------------|
| `Restful Booker.postman_collection.json` | Postman collection with API requests |
| `Test.postman_environment.json`          | Postman environment variables        |
| `Run.bat`                               | Batch file to run tests with Newman |
| `newman/`                               | (Optional) Directory for Newman reports (e.g., HTML reports) |

> **Note**: If the `newman` folder is missing, create it manually or let Newman generate it after running the tests.

---

## 🚀 How to Run the Tests

### 🔧 Prerequisites

- [Postman](https://www.postman.com/downloads/) (for manual execution)
- [Node.js](https://nodejs.org/) and [Newman](https://www.npmjs.com/package/newman) installed globally:
  ```bash
  npm install -g newman
  ```

### ▶️ Run with Newman

```bash
newman run "Restful Booker.postman_collection.json" -e "Test.postman_environment.json" -r cli,html --reporter-html-export newman/report.html
```

Or just double-click the `Run.bat` file (on Windows).

---

## 📊 Features Tested

- ✅ Authentication (token generation)
- ✅ Create Booking
- ✅ Get Booking by ID
- ✅ Update Booking
- ✅ Delete Booking

---

## 👤 Author

**GitHub**: [moh-essamb](https://github.com/moh-essamb)
