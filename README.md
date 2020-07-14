# Walking Buddy App
A Swift/SwiftUI application that randomly chooses a place nearby to take a walk/cycle/whatever actually to. You can specify range and presets including names, colors (only iOS 14 for now) and distance. Also wherever you see me typing iOS I also mean iPadOS (thanks Apple lol).

## Requirements
As of now iOS 13 for the app alone, iOS 14 for the color pickers (they've been introduced in iOS 14 and I'm looking for alternatives to use with the iOS 13 version). Probably also iOS 14 for the eventual widgets.

## Screenshots
### iOS

Start Screen               |  Showing route            |  Preset selector          |  Settings modal
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
![](screenshots/Simulator%20Screen%20Shot%20-%20iPhone%2011%20Pro%20Max%20-%202020-07-14%20at%2013.44.52.png)  |  ![](screenshots/Simulator%20Screen%20Shot%20-%20iPhone%2011%20Pro%20Max%20-%202020-07-14%20at%2013.46.21.png)  |  ![](screenshots/Simulator%20Screen%20Shot%20-%20iPhone%2011%20Pro%20Max%20-%202020-07-14%20at%2013.47.04.png)  |  ![](screenshots/Simulator%20Screen%20Shot%20-%20iPhone%2011%20Pro%20Max%20-%202020-07-14%20at%2013.47.12.png)



### iPad

Start Screen               |  Showing route + settings            
:-------------------------:|:-------------------------:
![](screenshots/Simulator%20Screen%20Shot%20-%20iPad%20(7th%20generation)%20-%202020-07-14%20at%2013.47.39.png)  |  ![](screenshots/Simulator%20Screen%20Shot%20-%20iPad%20(7th%20generation)%20-%202020-07-14%20at%2013.47.53.png)

### Mac

Start Screen               |  Showing route + settings            
:-------------------------:|:-------------------------:
![](screenshots/Screenshot%202020-07-14%20at%2013.49.05.png)  |  ![](screenshots/Screenshot%202020-07-14%20at%2013.49.50.png)

## How it works?
A radnom point in the approximate range is calculated. Then a route is plotted on the map. Simple as that. App also supports 2 interfaces, which are similar, but both tailerd to their smaller or bigger screen estate. That's why preset selector is always visible on Mac and iPad, but not iPhone. Also only iPhone versions use modal for settings as the smaller settings pane looked tiny and packed on smaller screens, and bigger modal settings on iPad and Mac obscured whole view and didn't make sense.

## Known issues
- Buttons using SF Symbols, so the selector and settings button, seem to behave differently on iOS 14 than their earlier version counterparts. On iOS 13.2 they have the exact same size, however on these screenshots you can see they're different. Might be an issue with the beta, or Apple just changed this behavior.
- Bridges, rivers and long rail tracks are this application's weaknesses. Sometimes the point will be generated in such place, that the route lenght might be well above the one specified by a user. This is a fault of the way the points are selected, might come back to this issue later.
- Settings and views' backgrounds are messed up on Mac. Instead of `.systemMaterial` the app uses `.systemThinMaterial` (wierd) and the color pickers aren't aligned. Definitely will fix that.

## What's in the store for the future?
Probably a watchOS app and a widget. Too early to tell how they'd work though.
