Cisco-Meraki CMX API Sample Data
==================================

At Cisco-Meraki, we developed an API that lets network admins characterize the flow of foot traffic through their network's physical space.
We do this by observing wireless devices' probe requests, as seen by Meraki APs, using each wireless device to represent a human network user.
How often do people revisit a site? Where in the site do they tend to hang out?
Are Androids more popular than iPhones in one particular area?
Github uses the Meraki API to help employees find each other around the office, while Peet’s uses it to see how busy their coffee shops are.

---------------------------------

Here’s an example of how Cisco-Meraki uses our API to monitor foot traffic
(or skateboard, or unicycle, or smart-canine---traffic is pretty multimodal at Meraki HQ)
of celebrities through our San Francisco office. (OK, these are actually engineers pretending to be celebrities).
This is what a single API result looks like:

```
AP 00:18:0a:91:b6:50 on ["5th Floor"]: {
"location":{"lat":37.77007744703792,"lng":-122.38730154826811,"unc":4.350499857899908,"x":[46.879278792949194],"y":[16.069850942124226]},
"manufacturer":"Apple","ipv4":"/10.96.1.225","seenTime":"2014-09-10T20:14:53Z","seenEpoch":1410380093,"clientName":"Diane von Furstenburg",
"ipv6":null,"ssid":"Unconfigured SSID 3","os":"Mac OS X","rssi":31
}
```

At the bottom of this readme, we link to a data set taken over 5 days on our office's 5th floor. Such data reveal what types of devices
were probing the nearest wireless access point for network availability in precise longitudes/latitudes at specific points in time.
We invite you to see what visualizations you can build with these data—whether a time-series animation of people as they come and go,
relative distribution of traffic density between yurts, or diurnal cycles of coffee bar use. [Here’s](example.png) a basic example, showing
where these celebrities were standing at 3:00 p.m., plotted on a Google Map. What other cool visualizations can you build using Meraki's CMX API?

A note on using the data: The x-y locations show where each celebrity is on Meraki's [5th floor](floor-plan.png).
The measurements are in meters from the lower-left corner of the building (the image is 46 pixels per meter).

The full 175 MB data set is [here](https://qstewart.egnyte.com/dl/HYwXLgPoFl).


