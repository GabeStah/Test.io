# Top 10 Mobile Testing Challenges

Unlike desktop applications, mobile application testing requires a particular set of considerations that are unique to the mobile environment; everything from screen size and assorted OS versions to power consumption and device settings.

While properly testing everything that a mobile device can throw your way can be challenging, in this article we go through the top 10 most common mobile testing challenges, detailing each and offering a bit of advice on how to account for and handle each particular trial.  Let's get to it!

## Screen Sizes

If there's one thing that's always changing in the realm of mobile devices, it's the actual pixel density that goes into the wide range of products released year after year.  Just glancing through the list of common mobile devices [`provided by Google's Material.io site`](https://material.io/devices/), we can already see there are well over a dozen different screen sizes across popular mobile phones to date.  Add in tablets and even the advent of smartwatches, and the difficulty for developers to properly design pixel perfect interfaces is largely a thing of the past.

Not only do developers and designers need to create application using dynamic elements and layouts, but this vast array of screen sizes also requires testers to run the gamut of all possible screen sizes and aspect ratios.

## Connection Types

Testing all the various connection types available to modern mobile devices can be yet another challenge for the QA team.  Mobile data connection types typically fall into three well-known categories of `2G`, `3G`, and `4G`, each incrementally providing generational increases to speed and better transmission technology.  While [`90% of the world's population`](http://www.ericsson.com/res/docs/2012/ericsson-mobility-report-november-2012.pdf) is expected to have access to at least `2G` coverage sometime in 2017, the varying speeds and connection qualities across these generations makes testing a challenge.  Even WiFi connectivity can range from as good as a hard-line broadband connection to barely better than a mobile data connection.

For these reasons, it's critical that testing accounts for the wide range of speeds and qualities of connectivity the application may experience.  Moreover, testing should also acknowledge and measure the bandwidth usage of the application, since many carriers and service plans do not allow for unlimited data usage.

## OS Version Fragmentation

New iOS version adoption rates are quite high, with roughly [`93% of all iOS devices`](https://david-smith.org/iosversionstats/) currently utilizing either version `9.X` or `10.X` of the software.  By comparison, Android users are typically much slower to adopt newer OS versions, with large percentages of users still [`sticking with versions`](https://www.statista.com/statistics/271774/share-of-android-platforms-on-mobile-devices-with-android-os/) more than two generations old.

For this reason, it is critical that testing accounts for the wide variety of potential (or, at least, likely) operating system versions that users may have installed.

## Browser Fragmentation

While there are certainly fewer popular browsers in use today on mobile devices than in the past, just as with the fragmentation of operating systems, it's critical to account for the various browsers (and their respective capabilities) when performing testing.

At present, roughly [`80% of all mobile devices`](https://www.netmarketshare.com/browser-market-share.aspx?qprid=1&qpcustomb=1) are utilizing either Chrome or Safari browsers, yet there are four particularly popular browsers and a variety of lesser-used ones to take into account during testing.

## Power Consumption/Battery Life

While the industry-wide trend is that battery life is on the [`rise over the past few years`](http://www.phonearena.com/news/Smartphone-battery-life-over-the-years-A-surprising-study_id82315), the jump is not as dramatic as most people might expect or hope for.  As the growth in battery life increases at a fairly slow pace, the trend in power consumption from ever-more-demanding applications is trouncing battery growth quite handily.  As apps trend towards more demanding needs -- such as higher quality video or more urgent calculations -- the mobile hardware must chug along to keep up and battery power is drained that much faster.

Obviously, this means that testing procedures should account for power consumption whenever possible, particularly for highly demanding tasks the application might be capable of.

## Usability

One of the most critical components to any well-designed and well-tested application is the ability (or inability, as the case may be) for users to easily and accurately interact with the application.  This is particularly critical for apps running on mobile devices, which present a fairly small and thus limited amount of screen real estate in which to properly display not only all relevant information, but provide an easily accessible interface by which the user interacts with the application.

When performing testing for applications on mobile devices, it's critical to examine the size and dimensions of interactive elements, and to ensure proper legibility of both text and graphical elements the user may need to examine.

## Internationalization

Internationalization, or `I18N` for short, is a development practice that allows the application to be utilized across various languages and cultures.  Ideally, proper `I18N` accounts for not only differences in actual written translations throughout the app, but will also focus on different regional traits, such as locale, timezones, and even canonical equivalences.

Proper `I18N` testing should evaluate not only proper written translations, but also check for spacing and layouts that need to properly adjust for languages written from left-to-right, right-to-left, and top-to-bottom.

## Device Settings

Most modern mobile devices allow access to dozens of device-specific settings: Everything from network connectivity method and airplane mode to screen rotation and location awareness to notification and locale.  If you've never taken the time, just open up your phone's settings screen right now and count how many unique device settings are available -- you might be surprised at the sheer quantity, most of which you probably never use.

The challenge for testers, however, is that any or all of these device settings can (and will) be changed at any time when your particular application is in use, whether it's being launched, closed, or otherwise manipulated in some way.

## Location-Dependence

Another challenge for proper mobile application development is recognizing and handling the location-based information your application might need to utilize, depending on where the user is currently located.  GPS systems are the most frequent user of such modern mobile features, but a wide range of applications now utilize location-dependent algorithms to provide real-time information about the user's surroundings, or provide alerts to other users of the same app that may be nearby.

Testers should ensure that any location-dependent functionality is properly tested, either through simulation tools that emulate changes in location on the device itself, or by physically taking a device to different locations and testing the results.

## Legacy Devices

While it may come as no surprise that Android and iOS devices have become the excessively dominant force in the war for mobile users, at [`roughly 96% combined`](http://www.idc.com/promo/smartphone-market-share/os), other legacy devices are still in use by a good chunk of mobile users, and these devices cannot be ignored by developers nor testers alike.

BlackBerry, Windows Phone, and Symbian OS (powering legacy Nokia devices) all still remain active by a small, but die-hard percentage of the mobile market.  Testing procedures must, therefore, take into account the existence of such devices, particularly when the application in question could feasibly be accessed and run on these legacy devices.

---

__META DESCRIPTION__

A detailed examination of the top 10 most challenging aspects of mobile device and mobile application testing.

---

__SOURCES__

- http://blog.testlio.com/post/6-key-challenges-of-mobile-app-testing
- https://material.io/devices/
- https://en.wikipedia.org/wiki/Mobile_broadband
- https://www.statista.com/statistics/271774/share-of-android-platforms-on-mobile-devices-with-android-os/
- https://david-smith.org/iosversionstats/
- https://www.netmarketshare.com/browser-market-share.aspx?qprid=1&qpcustomb=1
- http://www.phonearena.com/news/Smartphone-battery-life-over-the-years-A-surprising-study_id82315
- http://www.idc.com/promo/smartphone-market-share/os
