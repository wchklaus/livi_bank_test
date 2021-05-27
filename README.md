# livi_bank_test

Simple Flutter project.
  - DataBase - [Hive](https://pub.dev/packages/hive) (NO SQL DataBase)
  - Stage Management - [Provider](https://pub.dev/packages/provider), StatefulBuilder, setState
  - Does not connect with any API

## This Project Used to show the Ideas behind of Behavior Driven Development (BDD)

Take a look of the file called [phone_notifier.dart](https://github.com/Klaus-Wong/livi_bank_test/blob/master/lib/home/util/phone_notifier.dart)

// Go Through the function call changePhoneNum(), which used to asynchronously update the change of the phone number in the TextField Widget

#### Background: 
  - Given that "the Country_Code, Country_Name and the Corresponding Phone_Prefix in the corresponding country are valid"

#### Action:
  - Verify the User Input Mobile Phone Number whether valid or not through matching the user input value comparison with a valid pattern of the mobile phone with the corresponding length of the mobile phone

#### Assetion:
  - If the length of the input values matching with the length of the phone, it would consider that it is a phone structure. However, we wanna verify whether this is a valid phone mobile that why we need to consider the corresponding country mobile pattern in their phone structure.

#### Consider the HK as an example:
  - We knew that HK phone number at least is 8 digital, only the number exactly equal to 8 digital we would assume it is an HK phone number, and the country prefix starting with +852. If you wanna verify is it a mobile phone number we would check with the first digital phone number. If the first number is equal to one of the below set it is a valid mobile phone 
  set  = {'4', '5', '6', '7', '8', '9'};

About the details implementation please refer to the function called changePhoneNum(), which from inside [phone_notifier.dart](https://github.com/Klaus-Wong/livi_bank_test/blob/master/lib/home/util/phone_notifier.dart)
