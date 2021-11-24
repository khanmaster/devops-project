# Microservices Architecture with CICD Pipeline.
**Summary**
- The core aim of this API is to provide an environment for an exposed API and an exposed database to be able to practice

Requirements
-	Create a Repo on  Github with main and dev branches for CI
-	Push the zip file's code to the repo
-	Create a Job In Jenkins (Jenkins running on AWS) to trigger job on every commit/push from Dev branch
-	Create a second job in Jenkins to merge the code to main and tigger 3rd job
-	3rd job to build a docker Image of this app and push to your docker hub
-	4rth job to get the latest image from your docker hub and deploy to AWS ec2 instance
-	1 commit/push to your repo should implement complete CICD, the App should be visible on public IP

**Submission**
- Deadline: Friday COB 26/11/2021.
Method: share your GitHub repo, Docker hub image and EC2 public IP).

**Assessment Criteria**
- You will be assessed on:
-	Mark down file README.md created with step by step guide of CICD pipeline
-	4 Jenkins jobs created, one for each step of CICD Pipeline
-	One commit/push to your repo should implement complete CICD on AWS and visible on public IP
-	All endpoints are accessible on public IP
Further Notes

**Hints:**
- You can create docker images on localhost using provided code to check it’s functionality before automating it in Jenkins jobs to create Microservices
You should create 2 docker images, one for flask front end and one for mongo for database
- You can use docker Compose or Kubernetes to deploy it on AWS EC2 instance



### Endpoints
* `localhost:5000/all-movies` Returns all records/movies available
* `localhost:5000/search-movie-title?title-word=batman` -> search Movie title for a specific word in movie titles
  * query param `title-word` as in the example above
  * **NOTE** - must be a full matching word as there is no fuzzy logic search at the moment
* `localhost:5000/search-movie-score/?<lower or great than param>=score` -> Returns all films relating to the IMDB score
  * `localhost:5000/search-movie-score/?score-lt=2` -> return all films with a score lower than 2
  * `localhost:5000/search-movie-score/?score-gt=9` -> return all films with a score greater than 9


**Best of Luck!**

If you need clarification or have any other questions about this project, please contact your trainer as soon as possible.
