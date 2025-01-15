# dnd-data
An open-source library of Dungeons &amp; Dragons data in JSON format, providing easy access to backgrounds, classes, monsters, items, spells and species. Perfect for developers building D&amp;D tools, apps or integrations.

## 📚 Sources

The data in this library has been curated from a variety of official and community-supported resources:

- **Player’s Handbook, 2024 (PHB)**
- **Dungeon Master’s Guide, 2024 (DMG)**
- **Monster Manual (MM)**
- **Xanathar's Guide to Everything (XGtE)**
- **Tasha's Cauldron of Everything (TCoE)**
- **Bigby Presents - Glory of the Giants**
- **Mordenkainen Presents - Monsters of the Multiverse**
- **Curse of Strahd**
- **Princes of the Apocalypse**
- 193 in total

## 📦 Contents

The library provides the following datasets:

| Dataset       | Description                             | Number of Entries |
|---------------|-----------------------------------------|-------------------|
| **Backgrounds** | Background options for characters        | 405               |
| **Classes**    | Character classes and associated details | 134               |
| **Items**      | Magical and mundane items               | 15,749            |
| **Monsters**   | Stat blocks and lore for creatures       | 11,463            |
| **Species**    | Alternate categorization of races       | 383               |
| **Spells**     | Magical spells from various sources     | 5,849             |

## 🛠️ Usage

Install the package via npm:
```bash
npm install dnd-data
```

Pull in the data:

```js
const { spells, monsters, items } = require('dnd-data');

console.log(spells.length); // Outputs: 5849

const { name, description, properties, publisher, book } = monsters[526]

console.log(items[42]) // Outputs
{
	name: 'Abyssal Bane Greataxe',
	description: 'Weapon (any melee), uncommon Component: fiend (demon) bone Fashioned of bone, stone, and demon eyes, abyssal weapons are gestated by unholy bonesmiths within the infernal depths of the Hells. Fortified by magic to prevent the brittle materials from shattering, such weapons are carved with the true name of the demon whose eyes were ‘donated’ to its conception. The power of such a weapon is linked to the number of eyes used to craft it, with each open eye representing one unexpended charge. This weapon has 2 charges and regains all expended charges daily at dawn. Bonerip. As a bonus action when you hit a target with this weapon, you can call the name of the demon to whom the eyes belonged and expend 1 charge. The weapon mobilises, boney teeth and necrotic energy ripping through the target’s defences. The target gains a permanent and cumulative -1 penalty to its AC. Its AC can’t be reduced to less than 10 + its Dexterity modifier. The target can repair its armour with enough rest (for natural armour) or at an appropriate armoursmith’s (for worn armour) at the GM’s discretion.',
	properties: {
		Category: 'Items',
		'Item Type': 'Weapon (greataxe)',
		Properties: 'Heavy, two-handed',
		'Item Rarity': 'uncommon'
	},
	publisher: 'Loot Tavern',
	book: 'L’Arsene’s Ledger of Treasures and Trinkets'
}
```

The `name`, `description`, `publisher` and `book` key, value pairs are consistent across all datasets.

The `properties` value changes depending on the data set you pull in. So for example a spell might have the following value:

```js
{
  Category: 'Spells',
  Save: 'Dexterity',
  Level: 1,
  School: 'evocation',
  Expansion: 29025,
  Components: 'V, S, M',
  'Damage Type': 'acid',
  'Casting Time': '1 action',
  'data-RangeAoe': '60 feet '
}
```

Where an item may have the following value:

```js
{
  Category: 'Items',
  'Item Type': 'Staff',
  'Item Rarity': 'rare',
  'Requires Attunement': 'Requires Attunement'
}
```

Import the datasets in your project:

🤝 Contribution

This library is open source and community-driven. Contributions are welcome! If you’d like to add more data or suggest improvements:
	1.	Fork the repository.
	2.	Make your changes.
	3.	Submit a pull request.

📜 License

This project is licensed under the MIT License. See the LICENSE file for details.
