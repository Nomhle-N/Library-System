# 3rd Year AppDev Library System

## Group Members
- Leader: [TIYANI NGWANA]       231266731 - Category and Publisher Entity
- Member 2: [ABULELE NTWANAMBI] 218276400 - Reservation Entity
- Member 3: [NOMHLE NJENGELE]   216227488 - Book Entity
- Member 4: [OWENKOSI NXASANA]  230240887 - Publisher Entity
- Member 5: [SINAZO NTSIMBI]    222765208 - Loan Entity
- Member 6: [SINETHEMBA NYIMBINYA] 220085870 - Librarian Entity

## Domain
A specialized library for 3rd Year Application Development students at CPUT.
Contains programming books for final year modules.

## Entities
- **Book**: Textbooks available in the library
- **Member**: 3rd year students who can borrow books
- **Loan**: Records of books borrowed
- **Librarian**: Staff who manage the library
- **Category**: Book categories (Software Eng, Mobile, Web, etc.)
- **Publisher**: Book publishers

## UML Diagram

┌─────────────────────────────────────────────────────────────────────────────────────┐
│                        3RD YEAR APPDEV LIBRARY SYSTEM                                │
│                            CLASS DIAGRAM                                             │
└─────────────────────────────────────────────────────────────────────────────────────┘

┌──────────────────┐          ┌──────────────────┐          ┌──────────────────┐
│     Member       │          │      Loan        │          │      Book        │
│──────────────────│          │──────────────────│          │──────────────────│
│ - memberId: String│1        *│ - loanId: String │*        1│ - bookId: String │
│ - studentNumber:  │◄─────────│ - loanDate: Local│─────────►│ - isbn: String   │
│   String          │          │   Date           │          │ - title: String  │
│ - name: String    │          │ - dueDate: Local │          │ - author: String │
│ - email: String   │          │   Date           │          │ - publisher:     │
│ - phone: String   │          │ - returnDate:    │          │   String         │
│ - joinDate: Local │          │   Local Date     │          │ - publicationYear│
│   Date            │          │ - status:        │          │   : int          │
│ - status: String  │          │   LoanStatus     │          │ - category:      │
└──────────────────┘          └──────────────────┘          │   String         │
         │                                                    │ - edition: String│
         │                                                    │ - totalCopies:   │
         │                                                    │   int            │
         │                                                    │ - availableCopies│
         │                                                    │   : int          │
         │                                                    └────────┬─────────┘
         │                                                              │
         │                                                              │
         │              ┌──────────────────┐          ┌────────────────┴────────────────┐
         │              │    Librarian      │          │            Category             │
         │              │──────────────────│          │─────────────────────────────────│
         └─────────────►│ - librarianId:    │          │ - categoryId: String            │
                        │   String           │          │ - name: String                  │
                        │ - employeeNumber:  │          │ - description: String           │
                        │   String           │          └─────────────────────────────────┘
                        │ - name: String     │                          ▲
                        │ - email: String    │                          │
                        │ - phone: String    │                          │
                        │ - role: String     │                          │
                        │ - hireDate: Local  │                          │
                        │   Date             │                          │
                        └──────────────────┘                          │
                                                                       │
                                                            ┌──────────┴──────────┐
                                                            │      Publisher      │
                                                            │─────────────────────│
                                                            │ - publisherId:      │
                                                            │   String            │
                                                            │ - name: String      │
                                                            │ - address: String   │
                                                            │ - email: String     │
                                                            │ - phone: String     │
                                                            └─────────────────────┘
