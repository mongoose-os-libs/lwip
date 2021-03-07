# cs_lwip

Cesanta-patched LWIP, historically derived from early code drops by Espressif

# sdk_lwip

Imported from [upstream](https://github.com/espressif/ESP8266_NONOS_SDK/tree/158bb7a53f16cfff21b35fb4ec66fa15261f5a4a):

```
rsync -av --delete ESP8266_NONOS_SDK/third_party/include/{arch,lwip*,netif} sdk_lwip/include/
rsync -av --delete ESP8266_NONOS_SDK/third_party/lwip/{api,app,core,netif} sdk_lwip/src/
```

Applied patch to fix build errors with mos compiler settings:

```
patch -p 1 < sdk_lwip.patch
```
