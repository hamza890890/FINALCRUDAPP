# READ THIS TOP SECTION BEFORE ATTEMPTING TO DO ANYTHING PLEASE
## CRUD MVC App using JPA/Hibernate, MySQL, and ThymeLeaf.
## Instructions: (Below are a set of detailed instructions (made by me) telling the user what they should have installed and what they should do from start to finish in a very detailed explanation, BUT if you just want to run the program, follow the instructions in the very next paragraph (which is right below this text).) 
## FOLLOW THESE INSTRUCTIONS IF YOU JUST WANT TO RUN IT: (CLONE IT by selecting Get from VCS, pasting the link (the HTTPS LINK under the green Code button on the repository), and select a destination (an empty folder, you will have to create one if you haven't already done so), after attempting to download the file from this repository and unzipping it multiple times so that it runs smoothly on your end, I find that this method works better for running the program), and right click the top most folder (on the left side of the screen) and select reload from disk. After this, click main menu on the top left of intelliJ and select: run->Edit Configurations->Add New Configuration (Left side of the window)->Application->Name it->Select the deafult main class (there should be only the one)->Apply->Ok->And you should be able to run it (Even if it gives a red x, run it and click continue anyway) and perform the tests on the http://localhost:8080 as usual. IF NONE OF THIS WORKS, PLEASE USE THE PREVIOUS SUBMISSION (It was a forked repository) instead, that has worked perfectly. 

## My Instructions for running the program (This took roughly 8 hours in total to complete, the entire assignment I mean. Starting the Friday of Memorial day Weekend and Continuing up until the day before it was due)

### Step 1: Fork and Clone the Repository

1. **Fork the Repository:**
  - Go to the provided demo repository: [su24-jpa-demo](https://github.com/uncg-csc340/su24-jpa-demo).
  - Click on the "Fork" button in the top-right corner to create a copy of the repository under your GitHub account.

2. **Clone the Repository:**
  - Open your terminal or command prompt.
  - Clone your forked repository using the following command:
    ```bash
    git clone https://github.com/your-username/su24-jpa-demo.git
    ```
  - Navigate into the cloned repository:
    ```bash
    cd su24-jpa-demo
    ```

### Step 2: View Dependencies and Set Up MySQL

1. **Dependencies:**
  - Open the `pom.xml` file in your project directory to check the project's dependencies. Ensure it includes Spring Boot, JPA, MySQL, and Thymeleaf.

2. **Set Up MySQL:**
  - **Install XAMPP:** If you haven't installed XAMPP, download and install it from [XAMPP official site](https://www.apachefriends.org/index.html).
  - **Start XAMPP:**
    - Open the XAMPP Control Panel.
    - Start the Apache and MySQL services.
  - **Create Database:**
    - Open the MySQL command line or phpMyAdmin.
    - Create a database named `task_manager_db`:
      ```sql
      CREATE DATABASE task_manager_db;
      ```

3. **Configure Application Properties:**
  - Open the `src/main/resources/application.properties` file and configure the database connection:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/task_manager_db
    spring.datasource.username=root
    spring.datasource.password=yourpassword
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    ```

### Step 3: Run the Program

1. **Run the Spring Boot Application:**
  - In your terminal, navigate to the root directory of your project.
  - Use Maven to run the Spring Boot application:
    ```bash
    ./mvnw spring-boot:run
    ```

### Step 4: Access the Application on Localhost

1. **Access the Application:**
  - Open your web browser and go to `http://localhost:8080/students/all`, `http://localhost:8080/goals/all`, 
   `http://localhost:8080/task/all`. Depending on what you want to access first.
  - You should see the home page of your Task Manager application.

### Final Step: Commit and Push Changes

1. **Commit Your Changes:**
  - After implementing new features or making changes, you need to commit these changes.
  - Stage the changes:
    ```bash
    git add .
    ```
  - Commit the changes with a meaningful message:
    ```bash
    git commit -m "Implemented task and goal management features"
    ```

2. **Push Changes to GitHub:**
  - Push your committed changes to your GitHub repository:
    ```bash
    git push origin main
    ```

### Submission

1. **Update README.md:**
  - Include detailed instructions on how to run your application, including setting up the database and accessing the application on localhost. An example:
    ```markdown
    ## Task Manager Application

    ### How to Run

    1. **Clone the Repository:**
       ```bash
       git clone https://github.com/your-username/su24-jpa-demo.git
       cd su24-jpa-demo
       ```

    2. **Set Up MySQL:**
      - Install XAMPP and start MySQL.
      - Create a database named `task_manager_db`.

    3. **Configure the Application:**
      - Update `src/main/resources/application.properties` with your MySQL credentials.

    4. **Run the Application:**
       ```bash
       ./mvnw spring-boot:run
       ```

    5. **Access the Application:**
      - Open your browser and go to `http://localhost:8080`.

    ### Database Schema

    - Include a `.sql` file for the database schema, if necessary.
    

2. **Submit the GitHub Repository Link:**
  - Copy the URL of your GitHub repository and submit it as required.
