# ESP32 CAM Data Logging with DHT11 Sensor

- This project utilizes an ESP32 CAM module, a DHT11 sensor, and an SD card to measure and log temperature and humidity data to a text file on the SD card. The project captures sensor data at regular intervals and appends it to a text file for logging purposes
- The reason for using the ESP32 CAM (without the camera sensor obviously) is because it has a built-in SDCARD slot so saved time for SPI wiring

## Hardware Components

- **ESP32 CAM Module**: This microcontroller board acts as the main controller and data logger.
- **DHT11 Sensor**: It's used to measure temperature and humidity.
- **SD Card**: The SD card stores the data in a text file.

## Project Structure

The project contains several parts and utilizes external libraries for the DHT11 sensor and SD card management. The main code structure can be summarized as follows:

- **Initialization**:
  - The project initializes serial communication and sets up the DHT11 sensor and SD card.
- **Main Loop**:
  - The main loop performs the following steps:
    - Reads temperature and humidity data from the DHT11 sensor.
    - Logs the data to a text file on the SD card.
- **DHT11 Sensor Functions**:
  - Functions for initializing the DHT11 sensor and reading temperature and humidity data.
- **Data Logging**:
  - The code appends data to a text file named `datalog.txt` on the SD card.

## Usage

1. Set up the ESP32 CAM module, DHT11 sensor, and SD card.
2. Upload the code to the ESP32 CAM module.
3. The module will read temperature and humidity data and log it to the SD card in the format "temperature,humidity".
4. Data can be retrieved from the SD card by connecting it to a computer or other device with an SD card reader.

## Dependencies

The project depends on the following libraries:

- **DHT.h**: This library manages the DHT11 sensor.
- **SD.h**: It is used for managing the SD card.

## Note

- Ensure the proper wiring and connections of the hardware components.
- Make sure that the SD card is correctly formatted and inserted into the SD card slot.
- Check the availability of the specified text file on the SD card.
- Adjust the data logging interval to suit your requirements.

