## 3.2.0

- Support selecting the `inputMethod`, with possible values: `either` (default), `drag`, or `clickTwoSquares`.

## 3.1.1

- Allow shapes to be drawn on a non-interactable board.
- Fix a bug where the board would be stuck after transitioning from a
  non-interactable board to an interactable one.
- Selecting a piece will now clear all shapes on the board.
- Add the `scale` property to all `Shape` classes. Use a 0.8 scale for the
  shapes being drawn on the board to distinguish them from the already drawn
  ones.

## 3.1.0

- Add an optional `scale` parameter to arrows (default is `scale: 1.0`, matching the previous behavior).
- Implement `BoardData.copyWith` method to allow updating the board data
- Implement `BoardData` equality and hashcode operators
- Implement `BoardSettings` equality and hashcode operators

## 3.0.0

Improve board interaction and add support for drawing shapes while playing.

### Playing:
- pieces are now moved with pointer down events, instead of a tap events
  (pointer down followed by a pointer up event): this allows to move a piece
  faster
- premoves are not anymore cleared when selecting another piece: this matches lichess website behaviour and allow to prepare another move along with the premove that is currently set

### Drawing shapes (experimental)
- drawing shapes is now possible while keeping the normal board play interaction (before it was either one or another mode)
- one can draw a shape by holding a finger to an empty square while using a second finger to draw a shape anywhere in the board
- a double tap on an empty square will clear all shapes at once
- to clear a single shape is still supported: draw the same shape again

## 2.6.4

- Fix coordinates and board display on devices with RightToLeft Directionality.

## 2.6.3

- Improve coordinates display on the board.

## 2.6.2

- Fix `borderRadius` settings not being applied to the board highlights.

## 2.6.1

- Fix BoardSettings `copyWith` method.

## 2.6.0

- Add 2 new settings: `borderRadius` and `boxShadow`.

## 2.5.0

- Add a new shape type: piece (useful to show promotion hints).

## 2.4.1

- Don't clip board: fix annotations display on edge.

## 2.4.0

- Deprecate `BoardTheme` and export `Background`.

## 2.3.0

- Remove handling of android gestures exclusion.

## 2.2.1

- Upgrade fast_immutable_collections to version 10.0.0.

## 2.2.0

- Improve quality of PNG files, fix wrong rendering of some piece set like
  "Cardinal". More info: https://github.com/lichess-org/flutter-chessground/pull/28.
- Piece cache size is now rounded to the nearest integer above the actual value.

## 2.1.0

- `BoardData.sideToMove` is now optional with no default value, as well as
`BoardData.isCheck` and constructor assertion will guarantee they are set when
needed.

## 2.0.0

- `BoardData.sideToMove` is now a required parameter.

## 1.6.1

- Fix missing blindfoldMode to BoardSettings.copyWith

## 1.6.0

- Add blindfold mode

## 1.5.3

- Don't run premove timer if premove is not set

## 1.5.2

- Don't try to execute a premove if it is not allowed.

## 1.5.1

- Use an immediate timer to execute premove, instead of a post frame callback.

## 1.5.0

- `premove` is not anymore a local state, so it can be controlled by the parent

## 1.4.1

- Change the `autoQueenPromotionOnPremove` default setting to true

## 1.4.0

- Add a drawing shapes option
- Add the `autoQueenPromotionOnPremove` setting

## 1.3.1

- Improve check highlight appearance and fix rendering with Impeller.

## 1.3.0

- Remove opacity on origin piece when dragging because of performance issue with
  impeller engine.

## 1.2.0

- Add `isDrop` meta info to `onMove` callback.

## 1.1.0

- Add Caliente, Kiwen-Suwi and MPChess piece sets
- Fix promotion menu still showing when going back in moves history

## 1.0.4

- tapping one's piece now cancels premove.

## 1.0.3

- `showValidMoves` board setting now applies to premoves.

## 1.0.2

- When premoving, tapping same piece will now deselect it (to be consistent with
normal moves).

## 1.0.1

- Ensure premove square highlight takes precedence over last move.

## 1.0.0

Initial release.
