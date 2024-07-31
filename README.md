## Storage Restrictions Patches

These patches disable the checks done [here](https://android.googlesource.com/platform/frameworks/base/+/refs/heads/android14-qpr3-release/packages/ExternalStorageProvider/src/com/android/externalstorage/ExternalStorageProvider.java#306) and [here](https://android.googlesource.com/platform/frameworks/base/+/refs/heads/android14-qpr3-release/packages/ExternalStorageProvider/src/com/android/externalstorage/ExternalStorageProvider.java#328).  
  
- `FGoogle_frameworks` is the main patch. This adds some checks to the above-linked methods that use [Settings.System](https://developer.android.com/reference/android/provider/Settings.System) to check whether the user has enabled the features.
- `FGoogle_dt` is specific to my device (Poco F2 Pro lmi). I'm using the `XiaomiParts` app to add a new menu in the ROM's system settings that allows the user to enable/disable the features. Two switches will store their state using [Settings.System#putInt](https://developer.android.com/reference/android/provider/Settings.System#putInt(android.content.ContentResolver,%20java.lang.String,%20int))  
  
Needless to say, for these features to work, they need to be integrated in the custom ROM's source code.









<sup><sub>FGoogle = FuckGoogle :)</sub></sup>