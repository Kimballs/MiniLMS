# Development Notes

This document is a collection of random notes related to the Mini Library Management System (MiniLMS) project.

## Log Entries

### Sunday, November 6th
- Entries pending for the day.

### Sunday, November 5th
Note 1: Discovered the usefulness of the Markdown language for documentation, which uses the `.md` extension.

Note 2: Utilized Git for version control. Used the commands `git add .` to stage changes and `git commit -m "Initial commit"` to commit the staged changes with a descriptive message.

Note 3: Additional notes or observations for the day can be added here.

Note 4: Updated the 'Z_master_development_plan'. The 'Z_' prefix, while unconventional, ensures easy access to the file. Added detailed information about Git usage for Markdown. Revised section for "Version Control" within the development plan:
  - ### Version Control
    - [x] **Task: Initialize Git Repository**
      - [x] Utilize PyCharm's VCS integration to initialize a Git repository.
      - [x] Utilize GitKraken's VCS integration to initialize a Git repository.
      - [x] Used Bash for Git commands.
      - [ ] Regularly commit with descriptive messages. 

### Note 5: Visualization of Classes with PlantUML

Added PlantUML code to try and visualize classes within the IDE/PyCharm, avoiding the need for a subscription service. Here's the current UML representation:

### Note 6: UML Structure
# UML Outline for Library Management System

## Parent Class
- `LibraryItem`
  - Attributes: `item_id`, `title`, `genre`, `location`
  - Methods: `add_item()`, `remove_item()`, `find_item()`

## Child Classes

### Book (inherits from LibraryItem)
- Additional Attributes: `author`, `ISBN`, `publication_year`
- Additional Methods: `check_availability()`, `reserve_book()`
- Subclasses:
  - `FictionBook` (inherits from Book)
    - Additional Attributes: `subgenre`
  - `NonFictionBook` (inherits from Book)
    - Additional Attributes: `field`
  - `ReferenceBook` (inherits from Book)
    - Additional Attributes: `is_for_lending`

### Member (inherits from LibraryItem)
- Additional Attributes: `member_id`, `name`, `email`, `membership_type`
- Additional Methods: `register_member()`, `update_info()`, `deactivate_member()`
- Subclasses:
  - `AdultMember` (inherits from Member)
    - Additional Attributes: `fines_owed`
  - `ChildMember` (inherits from Member)
    - Additional Attributes: `guardian_name`
  - `SeniorMember` (inherits from Member)
    - Additional Attributes: `discount_rate`

### BorrowingRecord (inherits from LibraryItem)
- Additional Attributes: `record_id`, `member_id`, `borrow_date`, `due_date`, `return_date`
- Additional Methods: `create_record()`, `update_record()`, `calculate_fine()`
- Subclasses:
  - `CurrentBorrowing` (inherits from BorrowingRecord)
    - Additional Attributes: `is_overdue`
  - `HistoricalBorrowing` (inherits from BorrowingRecord)
    - Additional Attributes: `was_fine_paid`
  - `ReservedBorrowing` (inherits from BorrowingRecord)
    - Additional Attributes: `reservation_date`, `expiration_date`
