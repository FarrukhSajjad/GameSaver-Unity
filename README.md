# GameSaver-Unity

# About

GameSaver is a package to simplify saving game data in Unity.

# How to use
* Create a class that holds your save data.
* Populate your object with data.

## Save Data Class Example:
```c#
public class SaveObject
{
    public int score;
    public string playerName;
    public Dictionary<string, int> numberOfWeapons = new Dictionary<string, int>();
    public List<string> skinsUnlocked = new List<string>();
}
```

## Create an instance of your save data class:
```c#
var saveDataObject = new SaveObject
{
    score = 5,
    playerName = "player",
    numberOfWeapons = new Dictionary<string, int>{{"excalibur", 5}, {"diviner", 2}},
    skinsUnlocked = new List<string>{"skin1", "skin2"}
};
```
## Saving:
Use the following snipped to create a save file called "save1"
```c#
SaveManager.Save<SaveObject>("save1", saveDataObject);
```

## Loading:
Use the following snipped to load a save file called "save1"
```c#
var loadObject = Load<SaveObject>("save1");
```

## Document revision history

|Date|Version|
|---|---|
|April 1st, 2022|Version 0.0.1|
