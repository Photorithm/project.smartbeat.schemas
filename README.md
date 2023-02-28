# project.smartbeat.schemes
Nanobebe internal and external schemes

## Internals
NOTE: make sure the repository you generate for is in the same directory as this one.

Internals schema first used with quicktype generation
install:
```
npm install -g quicktype
```

### generate connetivity_api for connectivity service (wifi-tools)
From root directory type:
```
quicktype --src internals/connectivity-schema.json --src-lang schema --lang typescript --top-level ConnectivityAPI --converters all-objects --out ../project.smartbeat.hotspot/src/modules/ipc_agent/connectivity_ipc_api.ts
```

### generate connetivity_api for monitor service (used by wifi-manager)
From root directory type:
```
quicktype --src internals/connectivity-schema.json --src-lang schema --lang typescript --top-level ConnectivityAPI --converters all-objects --out ../project.smartbeat.monitor/Modules/Node/business/api/connectivity_ipc_api.ts
```