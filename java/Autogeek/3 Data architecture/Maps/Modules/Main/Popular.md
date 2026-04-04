A window with list of popular cars.

Principles:
- Represents a [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]]: [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model|model]] and [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Generation|generations]];
- Priority of region selection settings:
	1. Specified by the user;
	2. Taken from personal [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Account|accounts]] information;
	3. Location of IP-address.
- The list can be sorted by the following criteria:
	- Number of successful transactions;
	- Number of entity views;
	- Number of new ads.
- Popularity metrics are calculated over the last three months.

Wired with:
- On site:
	- [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Main menu|Main menu]];
- In telegram bot:
	- Command "/top"