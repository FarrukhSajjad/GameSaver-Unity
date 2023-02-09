# GameSaver-Unity

# About

GameSaver is a package to simplify saving game data in Unity.

# How to use
* Create a class that holds your save data states.
* Populate your object with data.

## Save Data Class Example:
```c#
public class SaveData
{
    public int level;
    public string levelNumberString;
    public Dictionary<string, int> numberOfEnemies = new Dictionary<string, int>();
    public List<string> playerSkins = new List<string>();
}
```

## Create an instance of your save data class:
```c#
var saveDataObject = new SaveObject
{
    level = 5,
    levelNumberString = "69",
    numberOfEnemies = new Dictionary<string, int>{{"L1Enemy", 5}, {"L2Enemy", 2}},
    playerSkins = new List<string>{"skin1", "skin2"}
};
```
## Saving:
Use the following snipped to create a save file called "save1"
```c#
SaveManager.Save<SaveData>("SaveDataFile", saveDataObject);
```

## Loading:
Use the following snipped to load a save file called "save1"
```c#
var loadObject = Load<SaveData>("SaveDataFile");
```

## Document revision history

|Date|Version|
|---|---|
|February 9th, 2023|Version 0.0.2|
