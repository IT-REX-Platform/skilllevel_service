# SkillLevel Service



The SkillLevel Service is a vital part of our system that aims to improve students' learning experiences. It assesses and stores the skill levels students achieve through assessments, using a framework called "Bloom's Taxonomy." These skills are measured separately for each part of a course.The SkillLevel Service designed to fulfill the following functions within the platform:

1. **Skill Assessment:** This service calculates and records students' skill levels based on their performance in assessments. These skill levels are represented as scores between 0 and 10, showing how well students are doing. Importantly, these scores change as students learn and progress, so they are always up-to-date.

2. **Data Collection:** The SkillLevel Service gathers data from various activities like quizzes and flashcards to accurately determine each student's skill level.

3. **Integration with GraphQL Service:** It integrates with the GraphQL Service to enhance the learning experience. This integration allows for comprehensive tracking of user progress and assessment data retrieval.

## Purpose

The SkillLevel Service is here to:

1. **Enhance Learning:** By measuring and storing students' skill levels, we aim to improve the learning experience in our system.

2. **Provide Feedback:** The skill level scores offer students valuable feedback on their progress and areas for improvement.

3. **Support Educators:** Teachers can use this data to refine their teaching methods and create more engaging learning environments.


# Usage

A docker-compose file is provided which creates containers for both the service, a postgres database, and a dapr
sidecar.

# Dependencies to Other Services
## Events
The events this service publishes/subscribes to are documented on the wiki:
https://gits-enpro.readthedocs.io/en/latest/dev-manuals/backend/dapr/dapr-topics.html

## GraphQL
This service sends GraphQL queries to the content service to get information about the assessments and users' progress
with them.

**The ENV variable *CONTENT_SERVICE_URL* needs to be set to the URL of the GraphQL endpoint of the content service**