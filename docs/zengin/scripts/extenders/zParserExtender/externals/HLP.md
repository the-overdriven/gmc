# HLP - help functions
Helper functions generally used for safety checks, to get specific information from the engine or to interface with the configuration `.ini` files.

## Hlp_HasFocusVob
Returns `TRUE`, if a specified NPC has a Vob in focus

```dae
func int Hlp_HasFocusVob( var C_NPC npc ) {};
```

- `npc` - NPC
- `return` - `TRUE` if npc has a focus Vob, `FALSE` if it does not

## Hlp_GetFocusVob
Returns NPC's focus Vob

```dae
func instance Hlp_GetFocusVob( var C_NPC npc ) {};
```

- `npc` - NPC
- `return` - focus vob

## Hlp_GetFocusVobName
Returns the name of NPC's focus vob

```dae
func string Hlp_GetFocusVobName( var C_NPC npc ) {};
```

- `npc` - NPC
- `return` - focus vob name

## Hlp_GetStringLength
Returns the lenght of a specified string

```dae
func int Hlp_GetStringLength( var string str ) {};
```

- `return` - length of `str`

## IsNAN
Checks wheter floating point number is valid

```dae
func int IsNAN( var float value ) {};
```

- `return` - `TRUE` if `value` is NaN, `FALSE` if `value` is a valid floating point number

## Hlp_KeyToggled
Checks wheter `key` is toggled

```dae
func int Hlp_KeyToggled( var int key ) {};
```

- `key` - key code
- `return` - `TRUE` if key is toggled, `FALSE` if key is not toggled

## Hlp_KeyPressed
Checks wheter `key` is pressed

```dae
func int Hlp_KeyPressed( var int key ) {};
```

- `key` - key code
- `return` - `TRUE` if key is pressed, `FALSE` if key is not pressed

## Hlp_LogicalKeyToggled
Checks wheter logical `key` is toggled

```dae
func int Hlp_LogicalKeyToggled( var int key ) {};
```

- `key` - key code
- `return` - `TRUE` if key is toggled, `FALSE` if key is not toggled

## Hlp_GameOnPause()
Checks wheter the game is paused

```dae
func int Hlp_GameOnPause() {};
```

- `return` - `TRUE` if the game is paused, `FALSE` if the game is not paused

## Hlp_MessageBox
Opens a message box with a specified message

```dae
func void Hlp_MessageBox( var string message ) {};
```

- `message` - message to be printed

## Hlp_PrintConsole
Prints a message to the Union debug console

```dae
func void Hlp_PrintConsole(var string message) {};
```

- `message` - message to be printed

## Hlp_OptionIsExists
Checks wheter the `entry` in `section` in `.ini` file `optName` exists

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func int Hlp_OptionIsExists(var string optName, var string section, var string entry) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[GAME]`
- `entry` - one setting entry like `playLogoVideos`
- `return` - `TRUE` if the option exists, `FALSE` if the option does not exist

## Hlp_ReadOptionInt
Read an integer value from spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func int Hlp_ReadOptionInt(var string optName, var string section, var string entry, var int default) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[GAME]`
- `entry` - one setting entry like `playLogoVideos`
- `default` - default value - if the value is empty
- `return` - the option value

## Hlp_ReadOptionFloat
Read a floating point value from spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func float Hlp_ReadOptionFloat(var string optName, var string section, var string entry, var float default) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[INTERFACE]`
- `entry` - one setting entry like `scale`
- `default` - default value - if the value is empty
- `return` - the option value

## Hlp_ReadOptionString
Read a string value from spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func string Hlp_ReadOptionString(var string optName, var string section, var string entry, var string default) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[GAME]`
- `entry` - one setting entry like `invCatOrder`
- `default` - default value - if the value is empty
- `return` - the option value

## Hlp_WriteOptionInt
Writes an integer value to spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func void Hlp_WriteOptionInt(var string optName, var string section, var string entry, var int value) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[INTERFACE]`
- `entry` - one setting entry like `scale`
- `value` - value to be written

## Hlp_WriteOptionFloat
Writes a floating point value to spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func void Hlp_WriteOptionFloat(var string optName, var string section, var string entry, var float value) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[INTERFACE]`
- `entry` - one setting entry like `scale`
- `value` - value to be written

## Hlp_WriteOptionString
Writes a string value to spicified `.ini` file, section and entry.

`optName` values
- `Gothic`
- `Mod`
- `SystemPack`

```dae
func void Hlp_WriteOptionString(var string optName, var string section, var string entry, var string value) {};
```

- `optName` - the `.ini` file
- `section` - settings section like `[GAME]`
- `entry` - one setting entry like `invCatOrder`
- `value` - value to be written

## Hlp_GetSteamPersonalName
Returns the name of the current Steam user
Returns empty string when not run with Steam

```dae
func string Hlp_GetSteamPersonalName() {};
```

- `return` - string containing the Steam username, or an empty string

## Externals with docu comments

```dae
/// Returns `TRUE`, if a specified NPC has a Vob in focus
///
/// @param npc NPC
/// @return `TRUE` if npc has a focus Vob, `FALSE` if it does not
func int Hlp_HasFocusVob( var C_NPC npc ) {};

/// Returns NPC's focus Vob
///
/// @param npc NPC
/// @return focus vob
func instance Hlp_GetFocusVob( var C_NPC npc ) {};

/// Returns the name of NPC's focus vob
///
/// @param npc NPC
/// @return focus vob name
func string Hlp_GetFocusVobName( var C_NPC npc ) {};

/// Returns the lenght of a specified string
///
/// @return str input string
/// @return length of `str`
func int Hlp_GetStringLength( var string str ) {};

/// Checks wheter floating point number is valid
///
/// @return `TRUE` if `value` is NaN, `FALSE` if `value` is a valid floating point number
func int IsNAN( var float value ) {};

/// Checks wheter `key` is toggled
///
/// @param key key code
/// @return `TRUE` if key is toggled, `FALSE` if key is not toggled
func int Hlp_KeyToggled( var int key ) {};

/// Checks wheter `key` is pressed
///
/// @param key key code
/// @return `TRUE` if key is pressed, `FALSE` if key is not pressed
func int Hlp_KeyPressed( var int key ) {};

/// Checks wheter logical `key` is toggled
///
/// @param key key code
/// @return `TRUE` if key is toggled, `FALSE` if key is not toggled
func int Hlp_LogicalKeyToggled( var int key ) {};

/// Checks wheter the game is paused
///
/// @return `TRUE` if the game is paused, `FALSE` if the game is not paused
func int Hlp_GameOnPause() {};

/// Opens a message box with a specified message
///
/// @param message message to be printed
func void Hlp_MessageBox( var string message ) {};

/// Prints a message to the Union debug console
///
/// @param message message to be printed
func void Hlp_PrintConsole(var string message) {};

/// Checks wheter the `entry` in `section` in `.ini` file `optName` exists
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[GAME]`
/// @param entry one setting entry like `playLogoVideos`
/// @return `TRUE` if the option exists, `FALSE` if the option does not exist
func int Hlp_OptionIsExists(var string optName, var string section, var string entry) {};

/// Read an integer value from spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[GAME]`
/// @param entry one setting entry like `playLogoVideos`
/// @param default default value - if the value is empty
/// @return the option value
func int Hlp_ReadOptionInt(var string optName, var string section, var string entry, var int default) {};

/// Read a floating point value from spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[INTERFACE]`
/// @param entry one setting entry like `scale`
/// @param default default value - if the value is empty
/// @return the option value
func float Hlp_ReadOptionFloat(var string optName, var string section, var string entry, var float default) {};

/// Read a string value from spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[INTERFACE]`
/// @param entry one setting entry like `scale`
/// @param default default value - if the value is empty
/// @return the option value
func string Hlp_ReadOptionString(var string optName, var string section, var string entry, var string default) {};

/// Writes an integer value to spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[INTERFACE]`
/// @param entry one setting entry like `scale`
/// @param value value to be written
func void Hlp_WriteOptionInt(var string optName, var string section, var string entry, var int value) {};

/// Writes a floating point value to spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[INTERFACE]`
/// @param entry one setting entry like `scale`
/// @param value value to be written
func void Hlp_WriteOptionFloat(var string optName, var string section, var string entry, var float value) {};

/// Writes a string value to spicified `.ini` file, section and entry.
///
/// `optName` values
/// - `Gothic`
/// - `Mod`
/// - `SystemPack`
///
/// @param optName the `.ini` file
/// @param section settings section like `[INTERFACE]`
/// @param entry one setting entry like `scale`
/// @param value value to be written
func void Hlp_WriteOptionString(var string optName, var string section, var string entry, var string value) {};

/// Returns the name of the current Steam user
/// Returns empty string when not run with Steam
///
/// @return string containing the Steam username, or an empty string
func string Hlp_GetSteamPersonalName() {};

```