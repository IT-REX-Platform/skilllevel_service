# SkillLevel Service

The Skill Level Service, a pivotal component of the "intelligent tutor" system, plays a central role in comprehensively analyzing and enhancing students' learning experiences. This service leverages the renowned "Bloom's Taxonomy" framework to assess and categorize students' cognitive abilities across various dimensions, including their capacity to remember, understand, apply, and analyze course material. These distinct cognitive skills, referred to as "skills" within the system, are evaluated independently for each chapter of a course.

The calculated skill level, expressed as a score ranging from 0 to 100, represents a dynamic measure of a student's proficiency and competence. It is not a static assessment but rather a continuously evolving reflection of a student's learning journey within the platform.[SkillLevel Service Scoring System and Bloom's Taxonomy](https://gits-enpro.readthedocs.io/en/latest/dev-manuals/gamification/Scoring%20System.html)

The Skill Level Service adeptly harnesses data from various sources, including solved quizzes, content revisitation, engagement with flashcards, and other platform activities, to precisely compute the skill level of each student. By assimilating this multifaceted data, it generates a comprehensive profile that reflects a student's cognitive growth and aptitude within the course.

Extending its reach beyond the boundaries of the platform, this service provides an Application Programming Interface (API) that external services can utilize to contribute to a student's skill level within IT-REX. For instance, when a student successfully completes an exercise on an external platform, this accomplishment seamlessly integrates into the skill level system of IT-REX, providing a holistic view of the student's abilities.

Moreover, the system offers a human touch by allowing lecturers and tutors to manually input skill level data, particularly relevant for physical exercises and assignments that may not be automatically tracked. This input ensures that all facets of a student's learning journey are accurately captured and analyzed.

The Skill Level Service functions as a sophisticated analyzer, meticulously dissecting and understanding each student's individual learning path. Based on a student's skill level score and progress within the course, the service provides tailored recommendations for the next steps in their educational journey, suggesting both content to continue with and areas to focus on for improvement.

In summary, the Skill Level Service combines data-driven analysis with human input, aligning with Bloom's Taxonomy to provide a comprehensive understanding of student proficiency. It empowers both students and educators with valuable insights, fostering a personalized and effective learning experience within IT-REX.

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