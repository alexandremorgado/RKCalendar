
### In addition to the original code
- Compatibility with xCode 11 beta 6
- Added multiple dates selection: *selectedDates: [Date] to RKManager*
- Added a new mode=3 for the selectedDates
- Added disabled dates option: *disabledDates: [Date] to RKManager*
- Moved the mode variable to the RKManager to allow for dynamic setting.
- Start and End dates selections (mode=1 and 2) are set automaticaly upon tapping. So start in mode=1. Note start date must be greater than the end date.

***
<br>

# RKCalendar
SwiftUI Simple Calendar / Date Picker for iOS

### Light Mode
<img src="https://github.com/RaffiKian/RKCalendar/blob/master/RKCalendar/Images/demo-app-light-mode-1.png" alt="demo app first screenshot" width="260"/> <img src="https://github.com/RaffiKian/RKCalendar/blob/master/RKCalendar/Images/demo-app-light-mode-2.png" alt="demo app first screenshot" width="260"/> 
### Dark Mode
<img src="https://github.com/RaffiKian/RKCalendar/blob/master/RKCalendar/Images/demo-app-dark-mode-1.png" alt="demo app first screenshot" width="260"/> <img src="https://github.com/RaffiKian/RKCalendar/blob/master/RKCalendar/Images/demo-app-dark-mode-2.png" alt="demo app first screenshot" width="260"/> 

**⚠️ WARNING ⚠️** This is an early version of this library that requires Swift 5.1 and Xcode 11 that are currently still in beta.

# Requirements
- iOS 13.0+
- Xcode 11+
- Swift 5.1+

# Installation
You can integrate RKCalendar into your project manually.

# Usage 

//Provide Calendar, minimum and maximum date that can be selected

RKManager(calendar: Calendar.current, minimumDate: Date(), maximumDate: Date().addingTimeInterval(60*60*24*365)

## Single Date Selection

//Pass mode 0 to select a single date

PresentationLink(destination: RKViewController(rkManager : self.exampleOne, mode: 0), label:{
    Text(getTextFromDate(date: self.exampleOne.selectedDate, mode: 0))
    }
)

## Start and End Date Selection

//Pass mode 1 to select start date

PresentationLink(destination: RKViewController(rkManager : self.exampleTwo, mode: 1), label:{
    Text(getTextFromDate(date: self.exampleTwo.startDate, mode: 1))
    }
)

//Pass mode 2 to select end date

PresentationLink(destination: RKViewController(rkManager : self.exampleTwo, mode: 2), label:{
    Text(getTextFromDate(date: self.exampleTwo.endDate, mode: 2))
    }
)

# License
RKCalendar is available under the MIT license. See the LICENSE file for more info.
