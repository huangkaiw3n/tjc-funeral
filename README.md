TJC Streams
======================
Just a static site built with Jekyll to show available TJC livestreams

Define a stream under _data/streams.yml

# Some initial data model ideas

## Simple version
Minimal data parsing version

Streams
- display_name (eg. TJC Adam Singapore Livestream)
- url (string)
- languages ([string]) eg. “English”, “Chinese”
- when_description (string) eg. “Sat 10am and 2pm (UTC +8, SGT)”


## Complicated version
With fine grained data and proper iso time data for parsing to enable features like search and filtering.

To enable search and filter like:
1. Know viewer’s time zones and filter streams that are airing now
2. Filter country
3. Filter languages

Streams
- church_name (string) eg. Adam
- country (string) eg. Singapore
- timeslots ([Timeslot])
- url (string)
- language ([string]) eg. “English”, “Chinese”


Timeslot
- day of week (ISO day of week) 1...7 eg. 6 for Saturday
- start_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 14:00
- end_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 16:00
- timezone (Z) Offset from UTC as +-HH:mm eg. +08:00

