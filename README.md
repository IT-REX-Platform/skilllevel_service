# SkillLevel Service

The SkillLevel Service is a vital component in our system, dedicated to enhancing students' learning experiences. It assesses and records students' skill levels using "Bloom's Taxonomy" as a framework. These skills are evaluated separately for each chapter of a course.

## Main Functions

1. **Skill Assessment:** The SkillLevel Service calculates and maintains students' skill levels based on their performance in assessments. These skill levels are represented as scores ranging from 0 to 10, reflecting how well students are performing. Importantly, these scores evolve as students learn and progress, ensuring they remain up-to-date.

2. **Data Collection:** This service collects data from various activities, including quizzes and flashcards, to precisely determine each student's skill level.

## Purpose

The SkillLevel Service serves the following purposes:

1. **Enhance Learning:** By measuring and storing students' skill levels, our aim is to enrich the learning experience within our system.

2. **Provide Valuable Feedback:** The skill level scores offer students valuable insights into their progress and areas for improvement.

For more details about the SkillLevel Service Scoring System and Bloom's Taxonomy, please refer to the [documentation](https://gits-enpro.readthedocs.io/en/latest/dev-manuals/gamification/Scoring%20System.html).

# Usage

To deploy the SkillLevel Service, a Docker Compose file is provided, creating containers for the service, a PostgreSQL database, and a Dapr sidecar.

# Dependencies on Other Services

## Events

This service publishes and subscribes to events documented on the [wiki](https://gits-enpro.readthedocs.io/en/latest/dev-manuals/backend/dapr/dapr-topics.html).

## GraphQL

The SkillLevel Service sends GraphQL queries to the Content Service to retrieve information about assessments and users' progress with them.

**Note:** Set the ENV variable *CONTENT_SERVICE_URL* to the URL of the GraphQL endpoint of the Content Service.

The SkillLevel Service is designed to streamline skill assessment and provide valuable feedback to students, contributing to an improved learning experience.
