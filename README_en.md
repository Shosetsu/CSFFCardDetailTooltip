# Card Detail Tooltip - Card Survival Fantasy Forest

[![zh](https://img.shields.io/badge/lang-zh-red.svg)](https://github.com/Shosetsu/CSFFCardDetailTooltip/blob/master/README.md)
[![en](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/Shosetsu/CSFFCardDetailTooltip/blob/master/README_en.md)

This mod shows card status and progress related details in tooltip.

![Preview](pic/screenshot1.png)

# Usage

## Install BepInEx

This mod works as a plug-in of BepInEx 5 framework.

See <https://docs.bepinex.dev/v5.4.21/articles/user_guide/installation/index.html>

## Mod Setup

- Download latest release from <https://github.com/Shosetsu/CSFFCardDetailTooltip/releases>.
- Extract `CSFFDetailedCardProgress.dll` to `BepInEx/plugins folder`.

## Settings (Optional)

The configuration file can be found at `/BepInEx/config/CSFFCardDetailTooltip.cfg`

| Name                          | Default      | Description                                                                                                                    |
| ----------------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| Enabled                       | true         | If set to true, will show the details tooltips                                                                                 |
| HotKey                        | F2           | The key to enable and disable the tool tips                                                                                    |
| WeatherCardInspectable        | true         | If true, the weather card on the left side of the clock can be clicked to inspect. True is required for showing tooltip on it. |
| RecipesShowTargetDuration     | false        | If true, cookers like traps will show exact cooking duration instead of a range.                                               |
| HideImpossibleDropSet         | true         | If true, impossible drop sets will be hidden.                                                                                  |
| TooltipNextPageHotKey         | RightBracket | The key to show next page of the tool tip.                                                                                     |
| TooltipPreviousPageHotKey     | LeftBracket  | The key to show previous page of the tool tip.                                                                                 |
| AdditionalEncounterLogMessage | false        | If true, shows additional tips in the message log of combat encounter.                                                         |
| ForceInspectStatInfos         | false        | If true, stats like Bacteria Fever are forced to be inspectable.                                                               |

**Toggle Note**: When using the hotkey to enable/disable the detailed tooltips, the tooltips will not be updated until the user moves the mouse off of a card.

# Known Issues

- Weather card will not show details even if `WeatherCardInspectable` is set to true.
- Not fully adapted to the new CSFF combat system.
- May be some typographical issues.

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
