# ISAT Registry


**Official Site:** [isat.college](https://isat.college)

This repository serves as the centralized database for student profiles displayed on [isat.college](https://isat.college). It contains JSON files representing individual student portfolios.

## Directory Structure

```
isat-registry/
├── students/
│   ├── <username>.json
│   └── ...
└── README.md
```

## How to Add Your Profile

1.  **Fork this repository.**
2.  **Create a new file** in the `students/` directory.
    *   The filename must be your desired username (e.g., `johndoe.json`).
    *   **Rules:**
        *   Must be lowercase.
        *   Must contain only letters, numbers, and hyphens.
        *   Must NOT be a reserved word (e.g., `admin`, `root`, brand names, university names).
3.  **Add your profile data** following the schema below.
4.  **Submit a Pull Request.**

## Profile Schema

Copy the following template and fill in your details.

```json
{
  "version": "1.0",
  "type": "portfolio",
  "config": {
    "theme": "modern-dark",
    "accentColor": "#6366f1"
  },
  "profile": {
    "name": "Your Name",
    "tagline": "A short professional tagline",
    "avatar": "https://github.com/yourusername.png",
    "location": "City, Country",
    "email": "you@example.com"
  },
  "socials": [
    {
      "platform": "github",
      "url": "https://github.com/yourusername"
    },
    {
      "platform": "linkedin",
      "url": "https://linkedin.com/in/yourusername"
    }
  ],
  "education": [
    {
      "institution": "ISAT College",
      "degree": "B.Tech in Computer Science",
      "year": "2023-2027"
    }
  ],
  "skills": [
    {
      "category": "Frontend",
      "items": ["React", "TypeScript", "Tailwind CSS"]
    },
    {
      "category": "Backend",
      "items": ["Node.js", "Python"]
    }
  ],
  "projects": [
    {
      "name": "Project Name",
      "description": "Brief description of the project.",
      "url": "https://project-url.com",
      "techStack": ["React", "Node.js"]
    }
  ]
}
```

### Configuration Options

*   **theme**: Currently supports `modern-dark` or `light-minimal`.
*   **accentColor**: Hex code for your preferred accent color.

## Validation

An automated bot will check your Pull Request to ensure:
1.  **Valid Username:** The filename is not on the banned list (e.g., brands, institutions, system terms).
2.  **Valid JSON:** The file contains valid JSON syntax.
3.  **Correct Schema:** The structure matches the required profile format.

If the bot detects a banned username or invalid format, your PR will be automatically marked with a ❌.
