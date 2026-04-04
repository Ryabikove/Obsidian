A window with list of recommended cars.

Principles:
- Represents a [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]]: [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model|model]] and [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Generation|generations]];
- If the user is not logged in, it contains information from the [[Autogeek/3 Data architecture/Maps/Modules/Main/Popular|popular]] list;
- Recommendations are prioritized from the following:
	- Favorites;
	- Views (last 3 months).
- The list is automatically sorted and cannot be edited.

Wired with:
- On site:
	- [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Main menu|Main menu]];
- In telegram bot:
	- Command "/recomended"