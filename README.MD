					[ COMBAT MANAGER ]
	Combat Manager simplifies the tracking of creatures in combat to speed up combat.  The 
manager tracks the hp and initiative of creatures.  Creatures are listed in order of highest 
initiative to lowest.  Some commands require either a target, a dice roll, or both.  Targets 
are selected via the battle box on the left while dice rolls are decided by what is written 
in the "Dice" text box in the middle.

					  [ DICE SYNTAX ]
	The text in the "Dice" box is read using the syntax [Number of Rolls]d[Dice Size]+[Modifier] 
(Just like in the source books).  [Number of Rolls] decides how many times to roll the dice,
[Dice Size] decides the size of the dice, and modifier is an integer to be added after all the dice
are rolled.  Note, [Number of Rolls] and [Modifier] are optional parameters.  If you have rolled a
physical dice and want to input that number (or have decided a number arbitraily because you want to 
kill off all the PCs), you can use an integer instead of a dice value.  Finally, whenever a single d20 
is rolled, the log will inform you if the roll was a natural one or a natural 20 before the modifier is
applied.  

	Examples of Valid Dice Rolls:
		d20:	Rolls a standard twenty-sided die with no modifiers.
		8d6:	Rolls eight six-sided die, the damage Fireball cast at 3rd level.
		d20+3:	Rolls a twenty-dided die and adds three to the result.  A typical ability check.
		10d6+40:Rolls a six-sided die ten times then adds fourty for when you cast Disintigrate.
		7d1:	Rolls seven mobius strips.  Will always result in a seven.
		7:	Returns seven.  Saves the program the trouble of finding all of it's modius strips.

					   [ ACTIONS ]

"New Combatant": Creates a new creature with the specified amount of hp and an optional initiative modifier 
	[init mod] You cannot make multiple creatures with the same name.  Putting a "@" in front of the 
	initiative modifier changes it from a modifier to a set value, that is, it's initiative will always 
	be that number.  If you are adding monsters it is recomended you number them to make them eassily 
	searchable.  See "Search" for details on how to do this.
"Remove Combatant": Removes the selected creature from the combat.
"Search Combatant": Searches roll20.net for the name of the combatant in your webbrowser.  If you will have 
	multiple of the same type of monster it is recomended that you name your them with the syntax 
	[Monster Type]#[Identifier].  "Search Combatant" ignores anything after a number sign.  For example,
	"Zombie", "Zombie#8", and "Zombie#Bill" all search for "Zombie".  
"Damage": Rolls the "Dice" and deals that amount of damage to the selected creature.  Notifies you of massive 
	damage (phb page 197) if occurs.
"Heal": Rolls the "Dice" and heals the selected creature for that amount.  Will not exceed the creatures 
	maximum hp.
"Roll Initiative": Rolls 1d20+[init mod] for all creatures and ranks them by initiative.  A creature's 
	[init mod] must be specified when it is created with "New Combatant".
"Roll Dice": Rolls the "Dice" with no side effects.  The result is printed to the log.
