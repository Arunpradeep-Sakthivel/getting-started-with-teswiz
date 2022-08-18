# getting-started-with-teswiz
Sample project to get started with teswiz - https://github.com/znsio/teswiz

Simply download the repo as a zip file, or clone it, and run the command:

    ./gradlew clean run

# Getting started

Refer to prerequisites mentioned here https://github.com/znsio/teswiz#prerequisites

# Running the sample tests

## Android tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @single-user" PLATFORM=android ./gradlew run 

## Web tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @single-user" PLATFORM=web ./gradlew run 

## Multiuser Android-web tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @multiuser-android-web" ./gradlew run

## Multiuser Android tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @multiuser-android and @single-app" ./gradlew run

## Multiuser-Multiapp Android tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @multiuser-android and @multi-app" ./gradlew run

## Multiuser-Multiapp Android-web tests
    CONFIG=./configs/jiomeet_config.properties TAG="@jiomeet and @multiuser-android-web and @multi-app" ./gradlew run

# Rich Reports using cucumber-reporting
teswiz creates rich reports for offline consuption using cucumber-reporting (https://github.com/damianszczepanik/cucumber-reporting)

These reports will be available in the following directory:

`LOG_DIR/mm-dd-yyyy/hh-mm-ss/reports/richReports/cucumber-html-reports/overview-features.html`

Example:

`~/teswiz/target/08-17-2022/17-36-02/reports/richReports/cucumber-html-reports/overview-features.html`

## Feature coverage
cucumber-reports has the ability to show tag statistics. This is very helpful to understand feature coverage from your automated tests.

Read more about this feature here: https://github.com/damianszczepanik/cucumber-reporting/blob/master/.README/tag-overview.png

You can find that report here:

`~/teswiz/target/08-17-2022/17-36-02/reports/richReports/cucumber-html-reports/overview-tags.html`

To exclude any tag(s) to be added in the rich reports, add the following line in your RunTestCukes.java

`System.setProperty(TEST_CONTEXT.TAGS_TO_EXCLUDE_FROM_CUCUMBER_REPORT, "@web,@android");`