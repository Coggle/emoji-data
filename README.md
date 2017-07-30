This is a fork of iamcal/emoji-data intended to host an up-to-date version of
the emoji-data JSON files, for consumption by other modules which don't need
the hundreds of MB of images included in the upstream module.

## Using the data

The file you want is `emoji.json`. It contains an array of entries for emoji that 
look like this:

	[
		{
			"name": "WHITE UP POINTING INDEX",
			"unified": "261D",
			"variations": [
				"261D-FE0F"
			],
			"docomo": null,
			"au": "E4F6",
			"softbank": "E00F",
			"google": "FEB98",
			"image": "261d.png",
			"sheet_x": 1,
			"sheet_y": 2,
			"short_name": "point_up",
			"short_names": [
				"point_up"
			],
			"text": null,
			"texts": null,
			"category": "People",
			"sort_order": 116,
			"added_in": "1.4",
			"has_img_apple": true,
			"has_img_google": true,
			"has_img_twitter": true,
			"has_img_emojione": false,
			"has_img_facebook": false,
			"has_img_messenger": false,
			"skin_variations": {
				"1F3FB": {
					"unified": "261D-1F3FB",
					"image": "261d-1f3fb.png",
					"sheet_x": 1,
					"sheet_y": 3,
					"added_in": "6.0",
					"has_img_apple": true,
					"has_img_google": false,
					"has_img_twitter": false,
					"has_img_emojione": false
					"has_img_facebook": false
					"has_img_messenger": false
				},
				...
			},
			"obsoletes": "ABCD-1234",
			"obsoleted_by": "5678-90EF"
		},
		...
	]

An explanation of the various fields is in order:

* `name` - The offical Unicode name, in SHOUTY UPPERCASE.
* `unified` - The Unicode codepoint, as 4-5 hex digits. Where an emoji
   needs 2 or more codepoints, they are specified like `1F1EA-1F1F8`.
* `variations` - An array of commonly used codepoint variations.
* `docomo`, `au`, `softbank`, `google` - The Unicode codepoints used
   by various mobile vendors.
* `image` - The name of the image file.
* `sheet_x` & `sheet_y` - The position of the image in the spritesheets.
* `short_name` - The commonly-agreed upon short name for the image, as
   supported in campfire, github etc via the :colon-syntax:
* `short_names` - An array of all the known short names.
* `text` - An ASCII version of the emoji (e.g. `:)`), or null where
   none exists.
* `texts` - An array of ASCII emoji that should convert into this emoji.
   Each ASCII emoji will only appear against a single emoji entry.
* `has_img_*` - A flag for whether the given image set has an image (named by the `image` prop) available.
* `added_id` - Unicode versions in which this codepoint/sequence was added.
* `skin_variations` - For skin-varying emoji, a list of alternative glyphs, keyed by the skin tone.
* `obsoletes` / `obsoleted_by` - Emoji that are no longer used, in preference of gendered versions.


## Version history

See [CHANGES.md](CHANGES.md)



