## Runeterra Dart
This project is a dart library for decoding and encoding decks in Legend of Runeterra.
It is based on [RiotGames/LoRDeckCodes](https://github.com/RiotGames/LoRDeckCodes)

## Install
Installation is in [lor_deck_codes_dart](https://pub.dev/packages/lor_deck_codes_dart) in Installing section

## How to use
You can create deck like I showed down below.
This deck is [Budget Elites (New Players)](https://lor.mobalytics.gg/decks/bojrj0dp0i9p574edqug) 
from [lor.mobalytics.gg](https://lor.mobalytics.gg).

### Decode
```dart
List<CardCodeAndCount> deck = LoRDeckEncoder.GetDeckFromCode(
      'CEAQQAIAAECAMFBCEQTTMAQCAEBASGQFAEAAGCYSDUXQCAQBAADQY');  
      /* 
        3:01DE001
        3:01DE004
        3:01DE006
        3:01DE020
        3:01DE034
        3:01DE036
        3:01DE039
        3:01DE054
        2:01IO009
        2:01IO026
        2:01DE003
        2:01DE011
        2:01DE018
        2:01DE029
        2:01DE047
        1:01DE007
        1:01DE012
      */
      deck[0].CardCode //01DE001
      deck[0].Count //3
```
### Encode
```dart
  String code = LoRDeckEncoder.GetCodeFromDeck(deck);
  //CEAQQAIAAECAMFBCEQTTMAQCAEBASGQFAEAAGCYSDUXQCAQBAADQY
```
## Notes
This package is using [fixnum](https://pub.dev/packages/fixnum) package for creating a fixed-width 32-bit integer in dart
