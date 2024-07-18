# Scratch-Checkout
A self checkout coded entirely in scratch with functionality for NFC tags instead of barcodes.
To use NFC you must run the project on an android device running Google Chrome. On startup select standalone if you want to use this on only one device.

## Multiple Devices
Use one device (like a tablet) with a touchscreen as the display. This will be where customers interact with the machine. It is also responsible for calculating prices and such.
Set the other device (Must be android running Google chrome) into scanner mode. The devices will communicate with each other and send scanned data. Place this device under the surface ar which customers will scan items.
## NFC Tag data
NFC formats for items.

**Purchasable items:** `ITEM NAME - $0.00` (Change the $0.00 to the price of the item, add `18+ | ` to age restrict the item to require an attendant to verify the user's age.)

**Employee cards:** `ADMIN`

**Payment cards:** `1234|VISA/MASTERCARD|PIN|LIMIT` (Replace 1234 with the last 4 digits of the card, visa and Mastercard you can choose one or use a different card type, PIN gets replaced with the pin of the card, these can be as long as needed, and LIMIT is the spending limit of the card)

## IF YOUR CARD KEEPS DECLINING
**You might be out of money**, scan the admin chip *or press get help on non NFC capable devices* then type 5 to select `Add $$$`, enter the last 4 digits of the card and then the amount of money you want to add. (Or put a negative `-` to deduct money!)

**You might have exeeded the card limit**, Just rewrite the NFC tag to have a larger limit. Refer to the **NFC Tag data** to learn how to properly format payment cards.
