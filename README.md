# eve-companion/

```txtnpx swagger-typescript-api \
  -p ./esi.json \
  -o ./src/api/esi \
  -n index.ts \
  --axios \
  --modular \
  --union-enums

root/
├── docs/               # GENERATED Documentation
├── img/                # Images and assets
├── src/
│   ├── api/
│   │   └── esi/        # GENERATED Swagger API client
│   │       ├── apis/
│   │       ├── models/
│   │       └── index.ts
│   └── main/           # Electron main process code
│   └── renderer/       # Renderer UI and logic
├── style-guide/        # Design docs, style references
├── package.json
├── esi.json            # (optional) local Swagger spec
```

```mermaid
mindmap
  root((Companion App))
    Main
      APIRequests
        ESI
          RequestUniverseTypes
          RequestCategories
          RequestRegions
          RequestSystems
          RequestBlueprints
          RequestMarketData
        ZKillboard
          RequestKillmails
          FetchShipLosses
          FetchCorporationStats
        APIIntegrations
          IntegrateWithCustomAPIs
          HandleGeneralAPIRequests
      ErrorHandling
        ImplementGlobalErrorLog
        HandleFailedRequests
      DataManagement
        ParseAPIResponses
        OrganizeFetchedData
        StoreDataInDB
        UpdateData
    Renderer
      UIUX
        MainWindow
          RenderPrimaryDashboard
          DisplayRealTimeUpdates
        Sidebar
          ProvideQuickNavigation
        InteractiveDataDisplay
          RenderDynamicGraphs
          DisplayTables
      DataHandling
        IndexedDB
          StoreTypes
          StoreCategories
          StoreRegions
          StoreBlueprintData
          StoreMarketData
          StoreCorporationData
        DataPersistence
          ManageDataUpdates
          EnsureDataConsistency
      UserInteractions
        HandleButtonClicks
        HandleInputFields
        UpdateUIBasedOnData
    WebWorker
      RequestQueueManagement
        ManageAPIRequestQueue
        OptimizeRequestIntervals
      DataCollation
        FormatRawData
        MergeDataForUI
      BackgroundTasks
        PerformHeavyCalculations
        FetchDataInParallel
    Preload
      Authentication
        OAuth2Integration
          AuthenticateWithESI
          ManageTokensAndRefresh
      OfflineFunctionality
        AllowOfflineUsage
        DisplayLastKnownData
      DataBridge
        FetchDataFromMain
        PassDataToRenderer
      Security
        SecureDataExchangeBetweenProcesses
        ValidateUserInput

```

## Other Files
1. [GenerateReadmes.js](./GenerateReadmes.js)
2. [jsdoc.json](./jsdoc.json)
3. [package-lock.json](./package-lock.json)
4. [package.json](./package.json)

## Subfolders
- [docs/](./docs/README.md)
- [img/](./img/README.md)
- [src/](./src/README.md)
- [style-guide/](./style-guide/README.md)
