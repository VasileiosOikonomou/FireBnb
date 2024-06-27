# Room Rental Management System

## Description
This application was developed as a university project for the "Distributed Systems" course. The application is a room rental management system that allows users to perform manager and tenant operations. The system uses the MapReduce framework for processing large volumes of data and consists of a backend implemented in Java and a mobile application in Android.

## Project Requirements
### Manager Functions:
- Add accommodations.
- Add available dates for rental for these accommodations.
- Display bookings for the accommodations they own.
- Manage these functions via a console application.

### Tenant Functions:
- Filter accommodations based on:
  - Area of interest.
  - Desired dates.
  - Number of people.
  - Price.
  - Rating (stars).
- Book an accommodation.
- Rate the accommodation (1-5 stars).
- Perform these actions via an Android UI.
  - A `search()` function sends the filter to the Master asynchronously and displays the search results.
  - A `book()` function allows the user to book an accommodation from the search results.

### System Requirements:
- The system should run distributed across multiple machines.
- Use MapReduce for processing data.
- Implement Master and Worker nodes communication using TCP sockets.
- Ensure thread synchronization using `synchronized`, `wait`, and `notify`.
- Data should be stored in memory (except for photos).

### Backend Implementation Requirements:
- The Master must be a multi-threaded TCP Server implemented in Java.
- Workers should also be multi-threaded to handle multiple requests from the Master.
- Workers should be dynamically specified during the Master initialization.
- Implement active replication to ensure data redundancy and fault tolerance.
- Synchronize data across multiple nodes to prevent data loss if a worker node fails.

### Frontend Implementation Requirements:
- Develop an Android application for the user interface.
- Communication between the Application and Master must use TCP sockets.
- Implement asynchronous communication to keep the application interactive.

## How to Run the Application

### Backend Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/room-rental-management-system.git](https://github.com/PanagiotisEvaggelou/FireBnb.git
    ```
2. Navigate to the .java files directory:
    ```bash
    cd \app\src\main\java\com\example\firebnb
    ```
3. Compile the Java files:
    ```bash
    javac *.java
    ```
4. Run the Master server:
    ```bash
    java Master
    ```
6. In separate terminals, run the Worker servers, the Reducer and the BackupWorker server in this exact sequence:
    ```bash
    java Worker1
    java Worker2
    etc..
    ```

### Frontend Setup (Android Application)
1. Open Android Studio.
2. Import the project by selecting the root directory of the cloned repository.
3. Build and run the application on an emulator or a physical device.

### Usage
- **Manager Console Application**: Use the console application to add accommodations, set available dates, and view bookings.
- **Tenant Android Application**: Use the Android app to filter and book accommodations, as well as to rate them.

## Setting Up on Windows Environment

1. Install Android Studio if necessary (version 2.1.13 or newer is recommended). If you have a version older than 2.3.0, you will need an internet connection because Android Studio will automatically download the required software.

2. Set up the environment variable <code>ANDROID_HOME</code> by running the command line instruction <code>setx ANDROID_HOME C:\\Users\\%username%\\AppData\\Local\\Android\\sdk</code>. If you have installed the Android SDK in another folder, enter that one instead and make sure it exists. If it's missing during step 6 execution, an error message indicating the absence of the <code>ANDROID_HOME</code> environment variable will appear.

3. Install the Java JDK if necessary. If it's missing during step 6 execution, an error message indicating the absence of the <code>JAVA_HOME</code> environment variable will appear.

4. Accept the Android SDK licenses by running the command line instruction <code>"%ANDROID_HOME%/tools/bin/sdkmanager" --licenses</code> and pressing <code>y</code> on everything. If you haven't accepted them, executing step 6 will show an error message about "accepting the Android licenses".

5. Download the application code from GitHub and place it in a folder, extracting it if necessary.


Alternatively, from the initial screen of Android Studio, select "Open an existing Android Studio project" and open the project. Once the scripts running upon opening the project from the top menu are completed, we choose "Build -> Make Project". This compiles the code and runs automatic checks but does not produce reports or signed executables.


## Screenshots
![Image Description](img/Screenshot1.png)

![Image Description](img/Screenshot2.png)

![Image Description](img/Screenshot3.png)

![Image Description](img/Screenshot4.png)

![Image Description](img/Screenshot5.png)

![Image Description](img/Screenshot6.png)

