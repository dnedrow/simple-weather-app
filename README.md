# iOS Coding Assignment

This is a coding challenge for iOS developers.  

# Prerequisites
## All candidates
Candidate **must** have git installed on their machine.
## Candidate on pre-Tahoe macOS
Candidate must have Xcode 15.4+, and at least one iOS 15+ model iPhone emulator
## Candidate with Tahoe (macOS 26+)
Candidate must have Xcode 26+, and at least one iOS 26+ model iPhone emulator

# Relax
- We're more concerned with your thought process and how you approach the
  problem than the final product.
- Don't worry about the time. We are looking for a working app, not a
  polished one.

# Step 1
**Fork** this repository on GitHub and **clone** it.

Open the **WeatherPlus** project in Xcode.
 * For the UI, you will use SwiftUI
 * Use the [Model-View-ViewModel](https://en.wikipedia.org/wiki/Model–view–viewmodel) 
   (MVVM) pattern. Bonus points for also using the Coordinator pattern.

# Step 2

Use the [Open Weather API](https://openweathermap.org/api) to fetch weather
details. Here is an example call requesting the hourly temperature and rainfall
for the lat/long of New York City, NY. Below is an example query you will use. You must
update the latitude and longitude values in the URL to match the listed cities.

`https://api.open-meteo.com/v1/forecast?latitude=40.71&longitude=-74.01&hourly=temperature_2m,rain`

Note: You can use the above query's response to create your data model.

Please use the latitude and longitude of the following cities to fetch
temperature and rainfall conditions for every hour of the day. A day is
considered to run from 00:00:00 through 23:59:59. Hours should be displayed in
the app according to the device's time display option.

| City | Lat  | Long |
| ------- | --- | --- |
| New York | 40.71 | -74.01 |
| Dallas | 32.78 | -96.81 |
| Miami | 25.77 | -80.19 |

Use the images included in the `assets` folder (in the root directory of your
local clone) for a visual indicator of the weather conditions. There are three
images for each asset. Talk us through why you choose a particular type.

| Precipitation | Weather Condition | Image |
| ------------- | ----------------- | ----- |
| 0.0 | Sunny | ![sunny](assets/sunny.png) |
| 0.0 < x < 1.0 | Light Rain | ![light rain](assets/light-rain.png) |
| x >= 1.0 | Heavy Rain | ![heavy rain](assets/heavy-rain.png) |

Here is a rough design for the sample app...

![weather app drawio](https://user-images.githubusercontent.com/1957407/206615131-5afcbb18-1d7e-4b38-b9f1-7f4b1333defd.png)


# Expected funtionality in descending order of importance
1. Fetch the current temperature for the three cities and list their current
   temperature, along with a rain or sun symbol as appropriate. 
1. Clicking on a city row will display the full weather report of that city
   for each hour of the day
1. A control at the top of the main screen that switches between 
   Celsius and Fahrenheit. This control can be any type you choose.
1. The temperature system selected in view 1 should be carried to view 2.


# Evaluation
- Clean, readable code
- Knowledge of MVVM, delegation, UI and navigation, fetching and parsing JSON
  data, git.

# Acknowledgements
Weather image assets <a href="http://www.freepik.com">designed by
Anindyanfitri / Freepik</a>.
