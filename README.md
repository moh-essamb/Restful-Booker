📚 Restful Booker API Testing Project
This project uses Postman and Newman to automate API testing for the Restful Booker service.

🧾 Repository Content

File/Folder	Description
Restful Booker.postman_collection.json	Postman collection containing all API requests (Create, Get, Update, Delete Booking, Authentication).
Test.postman_environment.json	Postman environment variables (like base URL and token) used during testing.
Run.bat	Batch file to execute the collection automatically using Newman.
newman/	Folder containing test reports generated after running the collection (e.g., HTML or JSON reports).
🛠️ How to Run the Tests
Clone the repository

bash
Copy
Edit
git clone https://github.com/moh-essamb/restful-booker-api-testing.git
Install Newman globally (if you haven't already)

bash
Copy
Edit
npm install -g newman
Run the collection manually with Newman:

bash
Copy
Edit
newman run "Restful Booker.postman_collection.json" -e "Test.postman_environment.json"
Or run using the batch file (Windows only):

bash
Copy
Edit
Run.bat
Note: Make sure your Run.bat points to the correct collection and environment files.

📋 APIs Covered
POST /auth → Create Token

POST /booking → Create Booking

GET /booking/{id} → Get Booking by ID

PUT/PATCH /booking/{id} → Update Booking

DELETE /booking/{id} → Delete Booking

📈 Sample Test Flow
Authenticate → Get Token

Create a Booking → Store Booking ID

Retrieve Booking → Validate Booking Details

Update Booking → Validate Changes

Delete Booking → Validate Deletion

📄 Example Response
json
Copy
Edit
{
  "bookingid": 2940,
  "booking": {
    "firstname": "Tyrique",
    "lastname": "Dickens",
    "totalprice": 538,
    "depositpaid": true,
    "bookingdates": {
      "checkin": "2025-06-02",
      "checkout": "2025-06-04"
    },
    "additionalneeds": "Lunch"
  }
}
🧪 Prerequisites
Node.js installed

Newman installed (npm install -g newman)

Postman (optional, for local test/debugging)

📂 Reports
After running the collection, the generated reports (e.g., HTML, JSON) will be stored inside the newman/ folder.

🙌 Author
Moh Essamb
GitHub: moh-essamb
