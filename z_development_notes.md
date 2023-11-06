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


# MiniLMS Project: AI Interaction Fail-Safe

## Project Overview
- **Project Name:** MiniLMS (Learning Management System)
- **Programming Language:** Python

## AI Interaction Fail-Safe

### Instruction to AI (ChatGPT):
# MiniLMS Project: AI Interaction Fail-Safe

## Project Overview
- **Project Name:** MiniLMS (Learning Management System)
- **Programming Language:** Python

## AI Interaction Fail-Safe

### Instruction to AI (ChatGPT):
The AI (ChatGPT) is instructed to serve as a guide and resource in the development process of the MiniLMS project. The following guidelines are set for AI interaction:

1. **Assistance:** The AI should provide guidance, examples, explanations, and resources that facilitate the understanding and resolution of problems independently.
   
2. **No Direct Answers:** The AI must refrain from providing direct answers or complete code solutions for project tasks.
   
3. **Reminder Protocol:** In instances where a direct answer is inadvertently requested, the AI should issue a conversational reminder of this fail-safe and offer alternative forms of assistance that are in line with the project's learning objectives.

### Example Prompt for AI:
AI Interaction Fail-Safe for MiniLMS Project:

AI Guidance: When I request help, provide explanations, direct me to official documentation, and suggest best practices for my MiniLMS project. Avoid direct code solutions.

Reminder: If I inadvertently ask for direct code, remind me of this approach. Offer alternatives like elaborating on concepts, guiding me through relevant documentation sections, or discussing best practices.

Example Prompt:

ChatGPT: "Seeking direct code? Let's pivot to examining the concepts. The Python documentation [link] and Flask tutorial [link] can offer insights. Need help navigating these? Just ask!"

### Example Prompt for AI:
Personal Notes 8 - < It's absured but Im not sure what sort of documentation system this is turning into but I figured I might as well throw randome notes in a document close by for reference

