Welcome to the CSN-150-Midterm project!

Project name: Sending Messages Through WhatsApp

Purpose: Using a ESP32 to send myself messages to WhatsApp

Equipment:

ESP32CAM USB Micro Data Cable Link to documentation followed: https://randomnerdtutorials.com/esp32-send-messages-whatsapp/

Steps I followed:

1. I went into my WhatsApp app and added this number to my contact list: +34 621 331 709
2. I sent the following message to the number to receive an API key: "I allow callmebot to send me messages"
3. I received the API key and went to this website replacing anything inside [ ] with my information I got from the bot and a custom message saying "Hi" to send myself via message on WhatsApp and test to see if it works: https://api.callmebot.com/whatsapp.php?phone=[phone_number]&text=[message]&apikey=[your_apikey]
4. After testing and was successful, I went into my Arduino and went to Sketch > Include Library > Manage Libraries to search for URLEncode library by Masayuki Sugahara and process to download the sketch
5. I created a new sketch with the newly URLEncode and copy and paste an example code that was given by Masayuki on the site and edited by putting for example my ssid for my hotspot on my cell phone
6. Once done finishing editing the code I on to compiling the sketch onto the ESP32 and got an error
7. I once again tried to compile the sketch and it fully uploaded to the ESP32. The ESP32 sent a message to my WhatsApp saying "Hello from ESP32!" I did it again to make sure and got the same message again.
8. I changed the message I get from the code for shits and giggles to "You are number one!" Uploaded again and got the message.

Problems:

1. I uploaded the sketch and got an "redefinition void setup ()" error and went back into the code, saw that it was define twice also the void loop was define twice, so I deleted the extra definitions and anything in the {}.
