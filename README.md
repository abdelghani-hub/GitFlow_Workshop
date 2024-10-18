# GitFlow Workshop

GitFlow Workshop: Hands-on practice with branching strategies and collaborative development. Learn to manage features, releases, and hotfixes using GitFlow in a simulated team environment. Ideal for students and developers looking to enhance their Git skills.

## Workshop Outline

### 1. Setup

- Form teams of 4-5 members
- Choose a Scrum Master (leader) for each team
- Clone the repository:
  ```
  git clone https://github.com/abdelghani-hub/GitFlow_Workshop.git
  cd GitFlow_Workshop
  ```

### 2. Introduction

- Overview of GitFlow
![GitFlow Diagram](https://drive.google.com/file/d/1PllEy_XNqmhsiMUZOFkgplylMFDTfvkI/view?usp=sharing)

### 3. Initial Branching

#### Team Leaders:
1. Create and switch to the 'develop' branch:
   ```
   git checkout -b develop
   ```
2. Push the develop branch to remote:
   ```
   git push -u origin develop
   ```

#### Team Members:
1. Pull the latest changes:
   ```
   git pull origin develop
   ```
2. Switch to the develop branch:
   ```
   git checkout develop
   ```

### 4. Feature Assignment

Team leaders assign features to members:
1. Home page
2. About page
3. Contact page
4. Login page
5. Sign up page

### 5. Feature Development

For each team member:
1. Create a feature branch:
   ```
   git checkout -b feature/feat_[featureName]
   ```
2. Work on the assigned feature
3. Commit changes regularly:
   ```
   git add .
   git commit -m "Add feature: [featureName]"
   ```
4. Push the feature branch to remote:
   ```
   git push -u origin feature/feat_[featureName]
   ```

### 6. Pull Requests

#### Team Members:
1. Create a new pull request from your feature branch to 'develop'
2. Add a description of your changes
3. Assign your team leader as the reviewer

#### Team Leaders:
1. Review the pull requests
2. Provide feedback or approve changes
3. Merge approved pull requests into 'develop'

### 7. Release Process

#### Team Leaders:
1. Create release/v0.1.0 (home, login, signup pages):
   ```
   git checkout -b release/v0.1.0 develop
   # Make any necessary adjustments
   git commit -am "Prepare release v0.1.0"
   ```
2. Finish the release:
   ```
   git checkout main
   git merge --no-ff release/v0.1.0
   git tag -a v0.1.0 -m "Version 0.1.0"
   git checkout develop
   git merge --no-ff release/v0.1.0
   git branch -d release/v0.1.0
   ```
3. Repeat the process for release/v0.2.0 (about, contact pages)

### 8. Wrap-up and Q&A

- Discuss challenges faced during the workshop
- Q&A session
- Recap of GitFlow benefits in collaborative development

## Project Structure

Your project should include the following pages:

1. Home page (src/ index.html)
2. About page (src/ pages/ about.html)
3. Contact page (src/ pages/ contact.html)
4. Login page (src/ pages/ login.html)
5. Sign up page (src/ pages/ signup.html)

## Guidelines

- Commit often with clear, concise commit messages
- Follow GitFlow principles throughout the workshop
- Communicate with your team members
- Ask questions if you're unsure about any step

Good luck, and enjoy learning GitFlow!😊😁
