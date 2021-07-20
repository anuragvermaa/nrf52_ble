# nrf52_ble
### Setup nrf52 BLE folder for development:
- **Create folder for custom services inside directory**
    - custom_services
        - custom_services.h
        - custom_services.c
    
    - **Inside SES IDE**
        - Add above files by creating a folder inside SES "Project items" for custom BLE services
        - Add custom_services.c by right click>>*Add existing files* and navigating
        - Go Project options by right clicking on *Project directory*
        - Change Release to Common, so it's accessible to both 
        - *Preprocessor>>User include directories* and add:
            - Relative path at the bottom for custom_services foder, so that it can find .c & .h files
    
- **Add config files for app config**
    - app_config.h (Create inside project directory, under config folder along with sdk_config)

    - **Inside SES IDE**
    - Add following lines inside app_config
    ```
    #ifndef APP_CONFIG_H
    #define APP_CONFIG_H
     
    #ifndef NRF_SDH_BLE_VS_UUID_COUNT
    #define NRF_SDH_BLE_VS_UUID_COUNT 1             // number of service uuid
    #endif
    ```
    
    - Go Project options by right clicking on *Project directory*
    - Change Release to Common, so it's accessible to both 
    - *Preprocessor>>Preprocessor definitions* and add:
        - USE_APP_CONFIG
        
        

    
    
    
