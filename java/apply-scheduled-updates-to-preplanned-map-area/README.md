# Apply scheduled updates to preplanned map area

Apply scheduled updates to a downloaded preplanned map area.

![Apply scheduled updates to preplanned map area app](apply-scheduled-updates-to-preplanned-map-area.png)

## Use case

With scheduled updates, the author can update the features within the preplanned areas on the service once, and multiple end-users can request these updates to bring their local copies up to date with the most recent state. Importantly, any number of end-users can download the same set of cached updates which means that this workflow is extremely scalable for large operations where you need to minimize load on the server.

This workflow can be used by survey workers operating in remote areas where network connectivity is not available. The workers could download mobile map packages to their individual devices and perform their work normally. Once they regain internet connectivity, the mobile map packages can be updated to show any new features that have been added to the online service.

## How to use the sample

Start the app. It will display an offline map, check for available updates, and show update availability and size. Select 'Apply Updates' to apply the updates to the local offline map and show the results.

## How it works

1. Create an `OfflineMapSyncTask` with your offline map.
2. If desired, get `OfflineMapUpdatesInfo` from the task to check for update availability or update size.
3. Get a set of default `OfflineMapSyncParameters` for the task.
4. Set the parameters to download all available updates.
5. Use the parameters to create an `OfflineMapSyncJob`.
6. Start the job and get the results once it completes successfully.
7. Check if the mobile map package needs to be reopened, and do so if necessary.
8. Finally, display your offline map to see the changes.

## Relevant API

* MobileMapPackage
* OfflineMapSyncJob
* OfflineMapSyncParameters
* OfflineMapSyncResult
* OfflineMapSyncTask
* OfflineMapUpdatesInfo

## Offline Data
1. Download the data from [ArcGIS Online](https://arcgisruntime.maps.arcgis.com/home/item.html?id=740b663bff5e4198b9b6674af93f638a).
2. Extract the contents of the downloaded zip file to disk.
2. Open your command prompt and navigate to the folder where you extracted the contents of the data from step 1.
3. Execute the following command:
`adb push canyonlands/. /sdcard/ArcGIS/Samples/MapPackage/canyonlands`

Link | Local Location
---------|-------|
|[Canyonlands MMPK](https://arcgisruntime.maps.arcgis.com/home/item.html?id=740b663bff5e4198b9b6674af93f638a)| `<sdcard>`/ArcGIS/Samples/MapPackage/canyonlands/|

## About the data

The data in this sample shows the roads and trails in the Canyonlands National Park, Utah. Data by [U.S. National Parks Service](https://public-nps.opendata.arcgis.com/). No claim to original U.S. Government works.

## Additional information

**Note:** preplanned areas using the Scheduled Updates workflow are read-only. For preplanned areas that can be edited on the end-user device, see [Take a map offline - preplanned](https://developers.arcgis.com/java/latest/guide/take-map-offline-preplanned.htm).

#### Tags
Edit and Manage Data
offline, preplanned
pre-planned
synchronize
update
