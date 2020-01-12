# Homebridge-Rituals
a cup of tea! v1 is functional release

<img src="https://img.shields.io/badge/stage-stable-green"> <img src="https://img.shields.io/badge/completion-90%25-yellow"> <img src="https://img.shields.io/badge/license-MIT-green"> <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=4YXRZVGSVNAEE&item_name=Just+for+a+coffe&currency_code=EUR&source=url"><img src="https://img.shields.io/static/v1?label=Buy%20me%20a%20coffe&message=using%20paypal&color=green"></a>

<img src="https://user-images.githubusercontent.com/19808920/58770949-bd9c7900-857f-11e9-8558-5dfaffddffda.png" height="100"> <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRoyOlRgCEZSyCrf2Ika_luW6N9ridvyC1Genb49xCQyLbc5eMG&s" height="90" align="right"> <img src="https://www.rituals.com/dw/image/v2/BBKL_PRD/on/demandware.static/-/Sites-rituals-products/default/dw7656c020/images/zoom/1106834_WirelessperfumeDiffuserPROAPrimary.png?sw=500&sh=500&sm=fit&q=100" height="100" align="right">

Homebridge Rituals is a homebridge-plugin to manage a Rituals Genie over homebridge infraestructure.
Homebridge is a lightweight NodeJS server you can run on your home network that emulates the iOS HomeKit API.

Since Siri supports devices added through HomeKit, this means that with Homebridge you can ask Siri to control devices that don't have any support for HomeKit at all. For instance, using just some of the available plugins, you can say:

With this plugin you can do

 * _Siri, turn on the Genie._ 
 * _Siri, turn off the Genie._


#### Before begin, (assumptions)
* Your genie has been registered using Rituals App.
* Your genie is working fine.
* Your <a href="https://github.com/nfarina/homebridge">homebridge</a> is working fine and has been added to your home app as bridge. If not, please take a look to <a href="#considerations">considerations section</a>.
Find more about on <a href="https://www.rituals.com/es-es/faqs.html?catid=faq-perfume-genie&qid=fag-what-is-the-perfume-genie-and-what-can-it-do">Official Rituals Site</a>

## 01.Installation
With npm -i or if you are using manual plugin module installation.
```sh
npm -i homebridge-rituals
```
Otherwise you can use throught Homebridge UI-X the plugin search engine and just write : "homebridge-rituals or rituals" and click INSTALL

## <a name="considerations"></a>02.Considerations
0. This plugin is under development, (**Unstable installation 0.0.x**) (stable installation 1.0.0 or greather..)
1. **Node v4.3.2 or greater is required.** Check by running: `node --version`. The plugins you use may require newer versions.
2. **On Linux only:** Install the libavahi-compat-libdnssd-dev package: `sudo apt-get install libavahi-compat-libdnssd-dev`
3. Install Homebridge using: `npm install -g homebridge` _or_ `sudo npm install -g --unsafe-perm homebridge` (see below)
4. Install the plugins using: `npm install -g <plugin-name>`
5. Create the `config.json` file.

## 03.Configuration
One installed, you must modify your config.json file and add the following data:
1. Accessory = "Rituals"
2. Account = "xxxx@xxx.com" < that is the mail you are using in Rituals App Registration.
3. Password = "yyyyyyyy" < that is the password you are using in Rituals App
SAVE your config.json file and RESTART homebridge.

    "accessories": [
        {
            "accessory": "Rituals",
            "name": "My Genie",
            "account": "xxx@xxx.com",
            "password": "yyyyyyy"
        }
    ],

## 04.Limitations
* It will appears in you home app like a Fan Accessory.
* You can control start/stop and fan speed.
* You can't see other properties like in the app, maybe later.
* The most important limitation, with this very first version you can only manage only 1 genie under the rituals account.

## 05.Following Features Implementation (Nice to have in the future)
01. Allow to show battery level information
02. Allow to show the fragance name
03. Allow to show the fragance quantity remains inside genie
04. Allow to manage more than one genie if you can more than one in the same rituals account.

Yeah, many work .. but you can helpme with a coffe .. <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=4YXRZVGSVNAEE&item_name=Just+for+a+coffe&currency_code=EUR&source=url"><img src="https://img.shields.io/static/v1?label=Buy%20me%20a%20coffe&message=using%20paypal&color=green"></a>

## 06.Credits && Trademarks
Rituals & Genie are registered trademarks of Rituals Cosmetics Enterprise B.V.
