# 3DS_EpisodeGenerator_AnimeTemplate
Runs into your browser! Generates an object for you to copy-paste into your Anime Channel catalog. 
This is used with this amazing project from cooolgamer! https://github.com/cooolgamer/Nintendo-Anime-Channel-Revival/
To understand the inputs, you need to read the catalog you'll use them for, but here's a brief summary:
- The channel categories must be declared much like a function's prototype;
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

Additional languages can be added by adding a comma after the string, then inputting the next language with a different (or similar) link to file;


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
