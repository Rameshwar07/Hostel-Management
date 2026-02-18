Hostel-management/
│
├── app.js / server.js
├── package.json
├── package-lock.json
├── .env  (should be added)
│
├── routes/
│   ├── student.js
│   ├── complaint.js
│   ├── attendance.js
│   ├── auth.js
│
├── controllers/
│   ├── studentController.js
│   ├── complaintController.js
│
├── models/
│   ├── db.js
│
├── views/
│   ├── includes/
│   │   └── sidebar.pug
│   ├── javascript/
│   │   └── plumbingtable.js
│   ├── jquery/
│   │   └── jquery-3.4.1.min.js
│   └── pages.pug
│
├── public/
│   ├── css/
│   ├── js/
│
└── index.html



Browser (Student / Rector)                                                                
        │
        ▼
   Express Server
        │
 ┌──────┼────────┐
 │      │        │
Routes Controllers Views(Pug)
 │      │
 │      ▼
 │   Business Logic
 │
 ▼
MySQL Database


                ┌────────────────────┐
                │      Browser       │
                │  (Student/Rector) │
                └─────────┬──────────┘
                          │ HTTP
                          ▼
                ┌────────────────────┐
                │     Express App    │
                │      app.js        │
                └─────────┬──────────┘
                          │
         ┌────────────────┼────────────────┐
         ▼                ▼                ▼
   ┌──────────┐    ┌──────────┐    ┌──────────┐
   │  Routes  │    │ Sessions │    │  Static  │
   │ index.js │    │ Login    │    │ public/  │
   └─────┬────┘    └─────┬────┘    └──────────┘
         │                 │
         ▼                 ▼
   ┌────────────────────────────┐
   │      Business Logic        │
   │  (CRUD operations etc)     │
   └─────────────┬──────────────┘
                 │
                 ▼
          ┌──────────────┐
          │   MySQL DB   │
          │ students     │
          │ complaints   │
          │ hostel       │
          │ nightout     │
          │ notice       │
          └──────────────┘

                 ▲
                 │
          ┌──────────────┐
          │   Pug Views  │
          │ Rendering UI │
          └──────────────┘


