# Astro: Battery optimisation

Battery optimisation on Android is currently a mess, and the Astro is no exception.

If you want an app to be able to run in the background; there are currently 3 places where you need to enable it. All of them are within the settings app.

## Why

Most apps don't give you any benefit from running in the background, while they make a massive difference to your battery usage. Yet there are a few use-cases that are really valuable. Eg:

* Getting instant messages (eg Whatsapp, Messenger or Telegram) in a timely manner. If they are not allowed to run in the background, messages will often be delayed until you open the app, or it gets periodically run to check in.
    * If they are using something like Google's [Firebase Cloud Messaging](https://firebase.google.com/docs/cloud-messaging) (FCM), they come with a significantly lower penalty on the battery. Not all custom ROMs come with FCM.
* Location tracking for navigation (eg Google maps, or GPS Essentials). When they stop running, the navigation or route recording just stops.
* Music plays for a little while after you go to the home screen, or lock the screen.

## DuraSpeed

Go to Settings, and then look for "DuraSpeed" near the bottom of the list:

[[img/duraspeed.png|A screenshot showing DuraSpeed in settings.]]

Find the app that you want to be able to run in the background, and **enable** it.

[[img/duraspeedApps.jpg|A screenshot showing the enabled and disabled apps in DuraSpeed.]]

## Battery manager

Go to Settings, and then look for "Battery" near the top of the list:

[[img/battery.jpg|A screenshot showing where to find the Battery settings.]]

Tap "Battery Manager", then "Restricted apps".

You'll get a list. If the app you want to run in the background is in the list; un-tick it:

[[img/removeRestriction.jpg|A screenshot showing the confirmation dialog box for removing the background restriction on a specific app.]]

Tap "REMOVE" to confirm.

## Battery optimisation

NOTE: This is not simply another view of the "Battery manager".

Go to Settings, and then look for "Apps & notifications" near the top of the list:

[[img/appsAndNotifications.jpg|A screenshot showing where to find the Apps & notifications settings.]]

Tap "Advanced", "Special app access", and then "Battery optimization":

[[img/batteryOptimisation-appList.jpg|A screenshot showing a list of apps to choose battery optimisation or not.]]

Select "All apps" from the dropdown at the top of the screen, and find the app. Tap it:

[[img/dontOptimse.jpg|A screenshot showing the dialog box for choosing whether to optimise a specific app.]]

And choose "Don't optimize".
