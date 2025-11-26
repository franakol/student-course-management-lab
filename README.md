# Student Course Management System

A comprehensive Python-based system for managing student information, course offerings, enrollments, and academic records.

## 🎯 Features

- **Student Management**: Create, update, delete, and search student records
- **Course Management**: Manage course catalog with details and instructors
- **Enrollment System**: Track student course enrollments and grades
- **GPA Calculation**: Automatic GPA computation based on grades
- **Data Persistence**: Save and load data using JSON format
- **CLI Interface**: User-friendly command-line menu system

## 📋 Requirements

- Python 3.11 or higher
- Poetry (for dependency management)

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/franakol/student-course-management-lab.git
cd student-course-management-lab

# Install dependencies
poetry install

# Activate virtual environment
poetry shell
```

### Running the Application

```bash
# Run from Poetry
poetry run student-management

# Or within Poetry shell
python -m student_management.main
```

## 📚 Documentation

Comprehensive documentation is available in the [`docs/`](docs/) directory:

- **[README.md](docs/README.md)** - Detailed project overview
- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)** - System architecture and design
- **[DATA_STRUCTURES.md](docs/DATA_STRUCTURES.md)** - Data models and structures
- **[FILE_FORMAT.md](docs/FILE_FORMAT.md)** - Data file format specifications
- **[API_REFERENCE.md](docs/API_REFERENCE.md)** - Complete API documentation
- **[TESTING.md](docs/TESTING.md)** - Testing guide and procedures

## 🏗️ Project Structure

```
student-course-management-lab/
├── docs/                          # Documentation
├── student_management/            # Main application package
│   ├── models/                   # Data models (Student, Course, Enrollment)
│   ├── services/                 # Business logic layer
│   ├── data/                     # File I/O handlers
│   ├── ui/                       # User interface (CLI menu)
│   └── utils/                    # Utility functions
├── data/                         # Data files (JSON)
├── tests/                        # Test suite
├── pyproject.toml               # Poetry configuration
└── README.md                    # This file
```

## 🧪 Testing

```bash
# Run all tests
poetry run pytest

# Run with coverage report
poetry run pytest --cov=student_management --cov-report=html

# View coverage report
open htmlcov/index.html
```

## 🛠️ Development

### Code Quality Tools

```bash
# Format code with Black
poetry run black student_management

# Lint code with Flake8
poetry run flake8 student_management

# Type checking with Mypy
poetry run mypy student_management

# Run all quality checks
poetry run black student_management && poetry run flake8 student_management && poetry run mypy student_management
```

### Development Workflow

1. Create a feature branch from `development`
2. Make changes with clear, focused commits
3. Write or update tests
4. Ensure all tests pass and code quality checks succeed
5. Submit a Pull Request to `development`

## 📊 System Architecture

The system follows a layered architecture:

```
┌─────────────────────────────────┐
│     Presentation Layer (UI)     │
├─────────────────────────────────┤
│   Business Logic (Services)     │
├─────────────────────────────────┤
│      Domain Layer (Models)      │
├─────────────────────────────────┤
│   Data Access Layer (Files)     │
└─────────────────────────────────┘
```

## 💡 Usage Examples

### Student Management

```python
from student_management.services.student_service import StudentService

# Create a student
student = student_service.create_student(
    student_id="S001",
    name="John Doe",
    email="john.doe@example.com",
    program="Computer Science"
)

# Search for students
students = student_service.search_students(program="Computer Science")

# Update student information
updated = student_service.update_student("S001", email="newemail@example.com")
```

### Course Management

```python
from student_management.services.course_service import CourseService

# Create a course
course = course_service.create_course(
    course_code="CSC1234",
    name="Introduction to Programming",
    credits=3,
    instructor="Dr. Smith"
)
```

### Enrollment and Grades

```python
from student_management.services.enrollment_service import EnrollmentService

# Enroll a student in a course
enrollment = enrollment_service.enroll_student("S001", "CSC1234")

# Update grade
enrollment_service.update_grade("S001", "CSC1234", 85.5)

# Calculate GPA
gpa = enrollment_service.calculate_gpa("S001")

# Get transcript
transcript = enrollment_service.get_transcript("S001")
```

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Ensure all tests pass
6. Submit a pull request

## 📝 License

This project is created for educational purposes.

## 🔗 Links

- **Repository**: [https://github.com/franakol/student-course-management-lab](https://github.com/franakol/student-course-management-lab)
- **Issues**: [https://github.com/franakol/student-course-management-lab/issues](https://github.com/franakol/student-course-management-lab/issues)

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

**Built with ❤️ using Python and Poetry**
