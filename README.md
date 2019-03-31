# Quality-of-Service-QoS-channel-survey
* Monitor RF noise on all BLE RF channels
* Result may be used to avoid busy channels
  * Set advertiser/scanner/connection channel map
  * Note: Only the BLE Central is allowed to request a change in the channel map. Create a custom BLE service to share results with the central. 
  
  
## Channel survey demo application ##

* Project based on SDK 15.3, with nRF52840 DK (PCA10056)
* Makes 100 channel survey measurements
* Print out the average measured values for all channels



  ```C
     sd_ble_gap_cfg_role_count_t::qos_channel_survey_role_available must be set
     sd_ble_gap_qos_channel_survey_start(interval)
     sd_ble_gap_qos_channel_survey_stop()

