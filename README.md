I can provide you with a textual representation of the use-case diagram using Astah UML notation:

```plaintext
@startuml

!define STUDENT class Student {
  -StudentID
  -Name
  -BorrowedBooks
}

!define LIBRARYSTAFF class LibraryStaff {
  -StaffID
  -Records
}

!define LIBRARIAN class Librarian {
  -StaffID
}

!define SYSTEM class LibraryManagementSystem {
  -Database
}

!define SECTIONHEAD class SectionHead {
  -SectionID
}

!define SECURITYDESK class SecurityDesk {
  -DeskID
}

!define CAMPUSDIRECTOR class CampusDirector {
  -DirectorID
}

LIBRARYSTAFF --|> SYSTEM
LIBRARIAN --|> SYSTEM
SECTIONHEAD --|> SYSTEM
SECURITYDESK --|> SYSTEM
CAMPUSDIRECTOR --|> SYSTEM

LIBRARYSTAFF --|> STUDENT : Manages
LIBRARIAN --|> LIBRARYSTAFF : Manages
SECTIONHEAD --|> LIBRARYSTAFF : Receives Defaulter List
SECURITYDESK --|> SECTIONHEAD : Receives Defaulter List
CAMPUSDIRECTOR --|> LIBRARIAN : Manages Budget

STUDENT -- (Borrow Book)
STUDENT -- (Return Book)
STUDENT -- (Read Newspapers/Magazines)
STUDENT -- (Access Ebook Database)
STUDENT -- (Access E-Journal Database)
LIBRARYSTAFF -- (Maintain Student Records)
LIBRARYSTAFF -- (Maintain Issued Books Records)
LIBRARYSTAFF -- (Charge Fine)
LIBRARYSTAFF -- (Generate Defaulter List)
LIBRARIAN -- (Manage Staff)
LIBRARIAN -- (Check Records)
LIBRARIAN -- (Prepare Reports)

@enduml
```

Please note that you can use this textual representation in Astah UML to create the corresponding diagram.
