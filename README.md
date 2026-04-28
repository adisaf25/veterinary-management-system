# veterinary-management-system
This project, developed as part of our training program, is a command-line interface (CLI) application built in Python for the complete management of a veterinary clinic. It aims to modernize patient tracking by replacing paper processes with an efficient, robust, and easy-to-use digital solution.
Here is the clean English translation of your README file, with no icons, no code blocks, and a simple layout.

---


Repository Structure

The file structure of this project:

.
├── README.md
├── assets/
│   ├── architecture.png
│   ├── class_diagram.png
│   └── sequence_diagram.png
├── code/
│   ├── main.py
│   ├── clinique.py
│   ├── models.py
│   ├── persistence.py
│   ├── analyse.py
│   └── data.json
└── documents/
    ├── rapport_projet.docx
    ├── presentation_projet.pptx
    └── notebook_documentation.ipynb

assets/ : Contains all UML diagrams (Architecture, Classes, Sequence) used for the project design.

code/ : Contains all the Python source code of the application.

documents/ : Groups the documentation deliverables: the detailed project report, the PowerPoint presentation, and the explanatory Jupyter Notebook.

---

 Software Architecture

The application is built on a modular architecture that promotes separation of concerns. This approach makes the code more readable, maintainable, and scalable.

main.py (Presentation Layer) : This is the entry point that manages the command-line interface (CLI). It is responsible for displaying menus, capturing user input, and orchestrating calls to the business layer.

clinique.py (Business Layer / Controller) : The logical core of the application. The Clinique class centralizes all business operations (adding an owner, recording a consultation, etc.) and manipulates model objects.

models.py (Data Layer / Model) : Defines the "blueprints" of our data through Python classes (Owner, Animal, Consultation). It encapsulates the attributes and basic behaviors of the domain entities.

persistence.py (Persistence Layer) : Manages saving and loading the application state. It converts Python objects to JSON format for storage on disk and performs the reverse operation at startup.

analyse.py (Analysis Module) : A module specialized in data processing for report generation. It uses Pandas and Matplotlib libraries to create statistics and visualizations.

---

 Main Features

Entity Management : Complete CRUD (Create, Read, Update, Delete) for owners and animals (Dog, Cat).

Medical Records : Detailed recording of each consultation (reason, diagnosis, cost) and viewing of complete history by animal.

Reliable Persistence : Automatic saving of all data to a data.json file after each modification.

Advanced Search : Keyword search function within consultation diagnoses.

Analysis and Reports : Generation of activity reports including monthly revenue, most frequent consultation reasons, and a histogram of animal age distribution.

Input Validation : Robust checks are in place to ensure that user-entered data (numbers, non-empty text) is valid.

---

 Installation and Usage

To run the project on your local machine, follow these steps:

1. Clone the repository

git clone https://github.com/Laamouri144/Final_project
cd your-repo

2. Install dependencies

The project requires pandas and matplotlib for report generation.

pip install pandas matplotlib

3. Run the application

Execute the main.py module from the code/ folder.

python code/main.py

The application will launch in your terminal, and a data.json file will be created in the code/ folder to store the data.
