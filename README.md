# 3DS_EpisodeGenerator_AnimeTemplate
Runs into your browser! Generates an object for you to copy-paste into your Anime Channel catalog. 
This is used with this amazing project from cooolgamer! https://github.com/cooolgamer/Nintendo-Anime-Channel-Revival/
To understand the inputs (what you'll put in the file), you need to read (and understand) the catalog you'll use them for, but here's a brief summary:

The catalog is a JSON file, with 4 sections:
- The "head" object (section), which has basically the main important things that the app needs(?), either way that's supposed to be left intact unless you know what you're doing;

The next 3 sections are in the "body" object, and each of them has a "setNode" object which describes each "component" individually, inside an object, or array of objects. Each "section" is as follows:
- The channels, which must be declared much like a function's prototype, a.k.a. you give them an ID, and each becomes an unique category;
- The episodes, which are all separate "setNode" objects declared one after another, and you complete them according to the section below;
- The channels (again), completed just like the episodes, but some information has to be inserted manually. After "generating" an episode entry, you must also assign the channel they correspond to. In the channel declaration, there's a "children" object that has an array of values, which are the episode assignments. These are given in the generator on the right textbox so you can just copy-paste them into the desired channel. More info on that below;



Each episode is declared with the following info:
- id, which can be set to anything as long as you assign it properly, but it's much easier to use something like "episode:episodename";
- version, which can be set to anything and it shouldn't matter, but the default is a pre-set string just in case;
- type, which has to be set to "episode" so it can be verified as an episode;
- number, the number of the episode in the category, shown in the bottom-right corner of the thumbnail;
- ageRate, which should remain set to 0, unless you want to create an age-restriction of some sort;
- title, self-explained;
- description, self-explained;
- mediaUrls will contain only one language, depending on the setting you'll assign, example:
*"en": "link/to/file.moflex"*;

Additional languages can be added by adding a comma after the string, then inputting the next language with a different (or similar) link to the file;


These languages are shown in-app when changing the audio language, and become available for each video individually, depending on what languages are set in the catalog for each video;
- viewCount, isn't shown in-app;
- imageUrls, just like mediaUrls, assigns an image depending on the "language", but in this app, it's set to "default";
- agePrerollVideo, isn't commonly used, and should remain set to nothing for convenience;

After these are set for each video, after the videos section, each channel/category is defined with the following settings: id, type (which is set to channel), title, eshopLinks and imageUrls; Afterwards, each channel is attributed a "children" object, which has the following values:
- id, which is set to a video defined earlier;
- version, which is set to the version of that earlier video;
Both of these are repeated in their own separate {} object for each video assigned to the channel; Afterwards, one more version tag is added before closing the channel;

This explanation might not be the best, so please check the template from https://github.com/cooolgamer/Nintendo-Anime-Channel-Revival/ before trying to edit on your own;


A live version of this code is available at https://mettlesphee.github.io/3DS_EpisodeGenerator_AnimeTemplate/
