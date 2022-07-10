# Pathfdiner Inventory Management

## Authentication
Want every user to be able to access only their own "inventory sheets".

Future work may involve sharing "party" sheets.

## Backups
As this would be available publicly (eventually) backing up user data is essential such that any mistakes developers / users make or bugs that appear do not permanently delete a massive amount of character inventory data.

## Functionality
Inventory "sheets" similar in style to an excel spreadsheet. 
Containing additional functionality to make managing inventory simpler than using spreadsheets directly.

This functionality would include at minimum:
- Ability to add/remove gold from inventory by simply stating how much gold to remove or add (instead of calculating the difference by hand)
  - Ability to additionally place a "note" of what the gold is being used for. With the app maintaining a "gold log" for future reference
- Ability to add items to the inventory, including name, cost, weight, "notes", quantity.
  - Potential for autofilling item details by drawing from the global list of item names, a sort of fuzzy search. This has privacy concerns though. Might be better to build a list of names from the open rpg data. (see Foundry)
- Allowing simpler management of consumable items, provide an easy to use interface for ticking "down" or "up" consumables such as wands. This could go as far to calculate remaining value of such items based on initial / current charges left.
  - Note this could be easily adapted to managing class feature consumables such as rage rounds or burn. Might be out of scope for MVP however.
- Streamline buying and selling large amounts of loot (item categories?)
  - Input item worth (is treasure or not)
  - Intuitive UI for mass selling / undoing 
  - Intuitive method for splitting funds by n (i.e. split by 5 to all party members)
- Handle encumbrance in a way that is fun and easy to use. By utilizing bags and other containers. (HARD)

## Design

### Front End
Probably suits a single page application well.
So React would be a decent choice, if not a bit over-kill for the current feature set.

Have some experience writing React and will allow for more sophistication later on.

Constant addition / deletion and updating of state also suits Reacts paradigms well.

I don't care it it looks trash, has to be functional

### Back End
Rust solely because I need to practice using it

Good for ensuring correctness if a document store db is used?

Fast?

Experience using it.

### Database