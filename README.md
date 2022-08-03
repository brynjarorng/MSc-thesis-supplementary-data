# Thesis supplementary data
This repo contains supplementary data for the thesis [Reliability via Active Connectivity for the Internet of Robotic Things (IORT)]() by Brynjar Örn Grétarsson.

## ML model
The file `model.h5` is the model which was fully trained on real world RSSI data. This data can be found in the [Real world mobility RSSI dataset](https://github.com/brynjarorng/Rssi-mobility-measurements) repo. The model requires `Keras 2.4` to be imported. It expects the input to be 4 measurements of RSSI values spaced 1 second apart. It then outputs how likely it is that a packet in the signal will drop beneath -87 dB in the next 7 seconds.


## Cooja simulation config
The folder `rssi-contiki47-simulation-config` contains the configuration for the Cooja simulator, firmware files and the script used to move the robots. In order to compile this data, `contiki 2.6` is required since `rime` has been removed from newer versions. The compiled firmware was then run in the Cooja simulator shipped with `contiki 4.7` which was the newest version at the time of testing.