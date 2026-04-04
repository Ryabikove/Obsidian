A window with [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]] of [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Offer|offers]], which user has added to the app.

Principles:
- It is intendes as module which allows to add [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Variation|variations]] of car for selling;
- There can be only [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Offer|offers]] in list;
- You cannot add an entity to the module if the account is [[Autogeek/3 Data architecture/Maps/Modules/Main/Autorization and Registration|not verified]].

Wired with:
- On site:
	- [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Assistant menu|Assistant menu]] - available only if user has been autorized;
	- [[Autogeek/3 Data architecture/Maps/Modules/Main/About profile|About profile]];
- In telegram bot:
	- Command "/in_sale" - available only if user has been autorized;
	- [[Autogeek/3 Data architecture/Maps/Modules/Main/About profile|About profile]].