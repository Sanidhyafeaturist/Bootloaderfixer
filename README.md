# Bootloader Fixer

Broken a Bootloader and need a fix within arduino uno? well you are in the right place!
This bootloader fixer fixes your bootloader within arduino uno.

## ⚠️ Caution

**Caution:** 

- Using this project if your data loses then I AM NOT RESPONSIBLE!
- If you want to avoid risk then simply us a vm machine like virtualbox. Note - This is for test purposes only.
- You need an arduino uno and a supporting usb cable and ensure latest version of windows is installed.

## 📜 Disclaimer

**Disclaimer:**

- It is for test purposes only. If you try to be oversmart and destroy your bootloader then you are responsible.


## 🚀 Getting Started


- Locate Hex File:
After the compilation process is complete, navigate to the temporary directory where Arduino stores the compiled hex files. The location can vary depending on your operating system:

On Windows: C:\Users\<YourUsername>\AppData\Local\Temp\build<SomeRandomNumber>\
On macOS: /var/folders/<SomeRandomCharacters>/T/arduino_build_<SomeRandomNumber>/
On Linux: /tmp/arduino_build_<SomeRandomNumber>/
Inside the above directory, you'll find a .hex file with a name matching your sketch.

Open Arduino ISP Example:
In the Arduino IDE, go to File > Examples > 11.ArduinoISP > ArduinoISP and open the example sketch.

Select Board and Port:
In the Arduino IDE, go to Tools > Board and select the appropriate board (Arduino Uno) and processor.

Burn Bootloader (Optional):
If you're uploading to a blank or new ATmega328P microcontroller, you might need to burn the bootloader first. This can be done using the Arduino IDE. Go to Tools > Burn Bootloader.

Upload Using Programmer:
In the ArduinoISP example sketch, click the right-arrow icon (Upload Using Programmer) to upload the sketch to the Arduino Uno. This sketch essentially turns your Uno into a programmer.

Upload Hex File:
Now that your Arduino Uno is acting as a programmer, go to Sketch > Upload Using Programmer in the original sketch you opened. This will upload the hex file you generated earlier to the target microcontroller.

Verify Upload:
The Arduino IDE will show you the progress and status of the upload process. Once complete, you should see a success message.

That's it! Your hex file should now be uploaded to your Arduino Uno. Remember that the steps might vary slightly based on the version of the Arduino IDE you're using and any specific configurations you have.


## 📝 License

This project is licensed under the Apache Licence.

---


