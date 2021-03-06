# Tealium Mobile Library for iOS Version 5.0.4

This mobile library leverages the power of Tealium's [TIQ™ Tag Management](http://tealium.com/products/tealium-iq-tag-management-system/), [AudienceStream™](http://tealium.com/products/audiencestream/) and [Data Access™](http://tealium.com/products/tealium-dataaccess/) products, or any combination of, making them natively available to iOS applications. Please contact your Account Manager first to verify your agreement(s) for licensed products.

## What does Tealium do?

Tealium provides the platform for crafting a modern, scalable and flexible marketing technology stack so you can easily connect and integrate all of your best-in-class solutions.

### What is Tag Management ?

Tealium iQ™ powers more web experiences than any other enterprise tag management provider.  

As the foundation of Tealium’s real-time customer data platform, the Tealium iQ tag management solution enables marketing organizations to unify disparate data sources and drive more consistent visitor interactions. Equipped with an ecosystem of hundreds of turnkey vendor integrations, you can easily deploy and manage vendor tags, test new technologies, and finally take control of your marketing technology stack.

### What is Audience Stream ?

Tealium AudienceStream is the leading omnichannel customer segmentation and action engine, combining robust audience management and profile enrichment capabilities with the ability to take immediate, relevant action.

AudienceStream allows you to create a unified view of your customers, correlating data across every customer touchpoint, and then leverage that comprehensive customer profile across your entire digital marketing stack.

### What is Data Access ?

Tealium DataAccess™ is a suite of rich data services built from the ground up to break down the barriers between the marketing data set and data available across an entire organization. DataAccess offers the richest source of clean omnichannel, event, and audience data collected across web and mobile touch points, and makes that data available for real-time action.

## How To Get Started

* Check out the [Getting Started](https://community.tealiumiq.com/t5/6-Mobile-Documentation/Mobile-120-Getting-Started-with-iOS-5-x/ta-p/10374) guide for a step by step walkthough of adding Tealium to an extisting project.  
* The public API can viewed online [here](http://tealium.github.io/tealium-ios/), it is also provided in the Documentation directory of this repo as html and docset for Xcode and Dash integration.
* There are many other useful articles on our [community site](https://community.tealiumiq.com).

## Contact Us

* If you have **code questions** or have experienced **errors** please post an issue in the [issues page](../../issues)
* If you have **general questions** or want to network with other users please visit the [Tealium Learning Community](https://community.tealiumiq.com)
* If you have **account specific questions** please contact your Tealium account manager

## Change Log

- 5.0.4
    - First track event now waits for webview ready when Tag Management option enabled
    - Lifecycle module first launch auto detection now fires when autotrack lifecycle enabled
    - SetOverrideCollectDispatchURL fix
    - Volatile and Persistent data is now processed at track call time, instead of dispatch time
    - Lifecycle module has additional manual lifecycle calls that take optional data sources
    - Devices only builds added to repo (no simulator support frameworks)
    - DSYMs provided with each framework
    - Tealium universal data sources added for all dispatches:
        - event_name (previously link_id)
        - tealium_account
        - tealium_environment
        - tealium_library_name
        - tealium_library_version
        - tealium_profile
        - tealium_random (different 16 digit long number for each track event)
        - tealium_session_id
        - tealium_timestamp_epoch (previously timestamp_unix)
        - tealium_visitor_id (previously tealium_vid)

- 5.0.3 Bug Fixes
    - Protections added to the collectDispatchURL that may have caused crashes at launch time
    - Lifecycle module update fixing errant isFirstLaunch data source with subsequent events
    - Simulator stripping run script added to Sample Apps

- 5.0.2 Lifecycle Module & Sample App Added
    - TealiumIOSLifecycle.framework and sample app added to Support folder
    - Initial queue size init after first launch for default -1 setting fixed
    - CaptureTimeDataSources now safely adds additional data for certain launch edge cases
    - DestroyInstanceForKey: method now properly clears persistent data
    - Additional Data Source Keys to support lifecycle module added
    - Offline TagBridge feature enabled

- 5.0.1 Bug fixes
    - Remote disable fix
    - Reachability check fix
    - @import TealiumIOS module name fix
    - Minutes between refresh now displays correct time remaining 
    - Dispatch logs updated with a QA verbosity option
    - Minor documentation update
    - Nullability specifiers for inits corrected for cleaner swift implementation
    - OverrideS2SLegacyDispatchURL can now accept base addresses without trailing '?'
    - TEALDispatch stringForDispatchStatusType class method made public
    - Track calls forced to stay on main thread until data capture complete, then to background queue
    - Blank sample app updated with proper method signatures

- 5.0.0 Initial Release
    - Multiton support
    - Collect Dispatch support
    - S2S Dispatch support
    - Tag Managment Dispatch support
    - TIQ Mobile Publish Settings v5 support

## License

Use of this software is subject to the terms and conditions of the license agreement contained in the file titled "LICENSE.txt".  Please read the license before downloading or using any of the files contained in this repository. By downloading or using any of these files, you are agreeing to be bound by and comply with the license agreement.


---
Copyright (C) 2012-2016, Tealium Inc.
