plague_doc(1) -- A filesystem organization specification
========================================================

## NAME

plague_doc is short for Plague Doctor. plague_doc is a specification for organizing filesystems.

## DEFINITIONS

The `/` is considered the filesystem root.

In certain places the notation `[a-z]` may be used. This is used to define a list of folders called 'a', 'b', 'c' and so on. If `[a-z]` is used, it is automatically assumed that its alphabetical notation is for the next folder in the structure.

* `/`:
  The root directory for the filesystem. This is not the computer root (The `/` location), but will be referred to for simplicity for this manpage.

## AUDIO

* `/audio`:
  Generic top directory for audio files.
* `/audio/audiobooks`:
  Directory for audiobooks. Audiobooks are organized by the structure of `[a-z]/<book author>/<book title>/<tracks>`. Formatting of track titles is not enforced by the specification.
* `/audio/music`:
  Directory for music. Music is organized by the structure of `[a-z]/<artist>/<album>/<tracks>`. Formatting of track titles is not enforced by the specification.
* `/audio/podcasts`:
  Directory for podcasts. Podcasts are organized by the structure of `[a-z]/<podcast title>/<tracks>`. Formatting of track titles is not enforced by the specification.
* `/audio/miscellaneous`:
  Directory for misc. files. No direct structure is enforced here. It is not recommended to store audio in this folder.

## VIDEO

* `/video`:
  Generic top directory for video files.
* `/video/tv-shows`:
  Directory for TV Shows. TV Shows are organized by the structure of `[a-z]/<show title>/<season>/<episode files>`. Reference sources such as theTVDB for season structure for extra episodes. For single season TV Shows, the Season folder may be skipped. File naming should be done in such a way Media managers can easily pick up on it and retrieve additional metadata as needed.
* `/video/anime`:
  Directory for anime. Anime is organized by the structure of `[a-z]/<anime title>/<season>/<episode files>`. Reference sources such as theTVDB for season structure for extra episodes. For single season Anime, the Season folder may be skipped. File naming should be done in such a way Media managers can easily pick up on it and retrieve additional metadata as needed.
* `/video/movies`:
  Directory for movies. Movies are organized by the structure of `[a-z]/<movie title>/<movie file>`. Bonus features/bloopers/etcetera may be located in subfolders. File naming should be done in such a way Media managers can easily pick up on it and retrieve additional metadata as needed.

## DOCUMENTS

* `/documents`:
  Generic top directory for documentation.
* `/documents/school`:
  Directory for files related to school. These files should be organized with the structure of `<year>/<course>/<task>/<files>`. For generic course info, a folder called `generic` should be used in the `course` folder. For generic school related information, a folder called `generic` should be used in the `<year>` folder.
* `/documents/work`:
  Directory for files related to work.
* `/documents/private`:
  Directory for private files. These follow no apparent structure.

## SOFTWARE
* `/software`:
  Generic top directory for software.
* `/software/tools`:
  Directory for 'utility' software. This includes file converters, media editors, internet browsers, IDEs and similar utilities. Tools are organized with the following structure: `<platform>/<category>/<program name>/<program.zip>`. Tools should ideally be compressed, if they consist of multiple files. If they consist of a single file, no compression is needed.
* `/software/games`:
  Directory for video games. Games are organized with the following structure: `<platform>/<game name>/<game files>`. This includes games that can be used with emulation software. Cross platform games (those with multiplatform binaries in the same game folder) should be put in a `cross-platform` folder. Virtual Console games for the Nintendo 3DS, Wii or Wii U should be put inside a folder called `VC-<platform>` in the game folder for the original platform and the `VC-<platform>` directory should be symlinked to the platform the Virtual Console is made for.

## OTHER

* `/unsorted`:
  Used as a temporary storage for files that haven't been sorted in the appropriate directories. Should go mostly unused.
* `/websites`:
  Used for archiving websites. Websites should be archived with the structure of `<website name.zip>`. Crawling choice is mostly free, but wget with WARC output is recommended.

## IMAGES

Images are not part of the plague_doc structure. That said, it is recommended to set up a booru using a local webserver. It is entirely possible to point the folder root of this booru to a directory on the filesystem.

* `/images`:
  Optional directory that acts as the booru folder root.

## CREDITS AND LICENSE

plague_doc is licensed under the WTFPL (why should i care how you use this structure anyway). Feel free to expand the specification as needed for your own purposes. 

This implementation was written by Valentijn "ev1l0rd". Do not contact me with requests on how to organize your filesystems. I will ignore those emails.