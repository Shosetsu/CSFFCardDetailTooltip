# Card Detail Tooltip - Card Survival Fantasy Forest

[![zh](https://img.shields.io/badge/lang-zh-red.svg)](README_zh.md)
[![en](https://img.shields.io/badge/lang-en-blue.svg)](README.md)

This mod shows card status and progress related details in tooltip.

[Preview](pic/screenshot1.png)

# Usage

## Install BepInEx

This mod works as a plug-in of BepInEx 5 framework.

See <https://docs.bepinex.dev/v5.4.21/articles/user_guide/installation/index.html>

## Mod Setup

- Download latest release from <https://github.com/Shosetsu/CSFFCardDetailTooltip/releases>.
- Extract `CSFFDetailedCardProgress.dll` to `BepInEx/plugins folder`.

## Settings (Optional)

The configuration file can be found at `/BepInEx/config/CSFFCardDetailTooltip.cfg`

| Name                          | Default      | Description                                                                      |
| ----------------------------- | ------------ | -------------------------------------------------------------------------------- |
| Enabled                       | true         | If set to true, will show the details tooltips                                   |
| HotKey                        | F2           | The key to enable and disable the tool tips                                      |
| RecipesShowTargetDuration     | false        | If true, cookers like traps will show exact cooking duration instead of a range. |
| HideImpossibleDropSet         | true         | If true, impossible drop sets will be hidden.                                    |
| TooltipNextPageHotKey         | RightBracket | The key to show next page of the tool tip.                                       |
| TooltipPreviousPageHotKey     | LeftBracket  | The key to show previous page of the tool tip.                                   |
| AdditionalEncounterLogMessage | false        | If true, shows additional tips in the message log of combat encounter.           |
| ForceInspectStatInfos         | false        | If true, stats like Bacteria Fever are forced to be inspectable.                 |

**Toggle Note**: When using the hotkey to enable/disable the detailed tooltips, the tooltips will not be updated until the user moves the mouse off of a card.

# Change Log

## 1.0.0

- Updated for CSFF.

## 1.0.1

- Fixed incorrect chance reporting in fishing events.

## 1.0.2

- Added support for CSFF's overhauled trap system.

## 1.0.3 ~ 1.0.5

- Improved Stat handling logic, significantly boosting performance (especially in late game).

## 1.0.6

- Fixed incorrect type definition in Encounter.cs.

## 1.0.7

- Fixed missing SpoilageRateModifier handling in liquid container details.

## 1.0.8 ~ 1.0.8.1

- Removed handling for unsupported `WeatherCardInspectable`.
- Disabled Weight display in `EquipmentButton` tooltip when [WikiMod](https://csff-db.uuppi.com/_WikiMod) v1.0.6 or higher is loaded; full encumbrance info is available there.

## 1.0.9

- Refined the display logic for the Time Cost Modifiers to improve clarity and readability.
- Removed the novelty countdown timer from permanently decaying stats, as these modifier do not actually expire—eliminating potential user confusion.

## 1.0.10

- Added support for displaying Multiply Modifiers.
