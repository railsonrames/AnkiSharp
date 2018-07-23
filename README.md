# AnkiSharp

:tada: It's finally here! You can create automatically anki cards from your C# application. :tada:

![ankisharp](https://github.com/Clement-Jean/AnkiSharp/blob/master/Readme/Anki-icon.svg.png)

### Basic use
``` csharp
AnkiSharp.Anki test = new AnkiSharp.Anki(_PATH_FOR_TEMP_FILES_, _NAME_OF_ANKI_PACKAGE_);

test.AddItem("Hello", "Bonjour");
test.AddItem("How are you ?", "Comment ca va ?");
test.AddItem("Flower", "fleur");
test.AddItem("House", "Maison");

test.CreateApkgFile(_PATH_FOR_ANKI_FILE_);
```

### SetFields
``` csharp
AnkiSharp.Anki test = new AnkiSharp.Anki(_PATH_FOR_TEMP_FILES_, _NAME_OF_ANKI_PACKAGE_);

//Permits to set more than two fields 
test.SetFields("English", "Spanish", "French");

test.AddItem("Hello", "Hola", "Bonjour");
test.AddItem("How are you ?", "Como estas?", "Comment ca va ?");
test.AddItem("Flower", "flor", "fleur");
test.AddItem("House", "Casa", "Maison");

test.CreateApkgFile(_PATH_FOR_ANKI_FILE_);
```

### SetCss
``` csharp
AnkiSharp.Anki test = new AnkiSharp.Anki(_PATH_FOR_TEMP_FILES_, _NAME_OF_ANKI_PACKAGE_);

//Permits to change the css of your cards by providing it Css file path
test.SetCss(_PATH_OF_CSS_FILE_);

test.AddItem("Hello", "Bonjour");
test.AddItem("How are you ?", "Comment ca va ?");
test.AddItem("Flower", "fleur");
test.AddItem("House", "Maison");

test.CreateApkgFile(_PATH_FOR_ANKI_FILE_);
```
### SetFormat
``` csharp
AnkiSharp.Anki test = new AnkiSharp.Anki(_PATH_FOR_TEMP_FILES_, _NAME_OF_ANKI_PACKAGE_);

test.SetFields("English", "Spanish", "French");

//Everything before '<br>' is the front of the card, everything after is the behind
test.SetFormat("{0} - {1} \\n<br>\\n {2}");

test.AddItem("Hello", "Hola", "Bonjour");
test.AddItem("How are you ?", "Como estas?",  "Comment ca va ?");
test.AddItem("Flower", "Flor", "fleur");
test.AddItem("House", "Casa", "Maison");

test.CreateApkgFile(_PATH_FOR_ANKI_FILE_);
```

## TO-DO

:ok_hand: = Done

:zzz: = Waiting for you to be developed

- Add more fields to the cards :ok_hand:
- Possibility to change the card's CSS :ok_hand:
- Being able to show what's on the front and on the back of the card :ok_hand:
- Generate audio with synthetizer or other tools? (Need to be careful about different languages) :zzz:

## Resources

- [Anki APKG format documentation](http://decks.wikia.com/wiki/Anki_APKG_format_documentation)
- [Database Structure](https://github.com/ankidroid/Anki-Android/wiki/Database-Structure)