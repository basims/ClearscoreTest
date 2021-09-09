# ClearscoreTest


### Project Architecture:

* I have used Kotlin as the development language and MVVM as an architecture so that there won't be any tight coupling between components and we can unit test the code easily
* Given API is used as backend
* Hilt is used for Dependency Injection to inject all the required modules
* The app is designed as a single Activity architecture
* A Repository class which act as a bridge between View model and API
* Room is used to cache data locally, so that even if there is no network, offline data will be displayed
* RemoteDataSource class to communicate with API and provide results to Repository class
* A Resource class is used to wrap API response and to handle the response with LiveData
* View binding and databinding is used
* Memory leaks are handled properly
* KTX library is used for avoiding lots of boiler plate codes

### UI Design

* A simple UI with custom circular progress bar to display the score
* Loading is animated and used different colors for progress according to the score

### Code Quality

* SOLID and clean code principles are followed
* Lint check is performed and cleared the issues
* Proper Unit tests and Instrumentation tests are added

### Testing Architecture:

* Unit test cases are developed using JUnit
* Viewmodel and Livedata are unit tested using Mockito
* Instrumentation test cases are added for testing Room Database
* UI Automation test cases are added using Espresso and followed Page Object Model
* Counting Idling resource is used to wait for asyn operation when running Espresso tests

### Improvements I have in mind:
* Smooth transition of colors in the progress using object animator


### More Testing Strategy:

* Need to mock the API and add more test cases to test the data displayed in Progressbar
* A unified test coverage report using jacoco
* CI/CD integration using circle CI
