TJC Streams
======================

# Data model ideas

## Simple version
Minimal data to enable displaying list of data

Streams
- display_name (eg. TJC Adam Singapore Livestream)
- stream_url (string)
- description (string) eg. “English and Chinese stream at every Sat 10am and 2pm Singapore Time”


## Complicated version
With fine grained data to enable features like search and filtering. Such as displaying times in viewer’s time zones, search and filter streams that are airing now.

Streams
- church_name (string) eg. Adam
- country (string) eg. Singapore
- timeslots ([Timeslot])
- stream_url (string)
- language ([string]) eg. “English”, “Chinese”


Timeslot
- day of week (ISO day of week) 1...7 eg. 6 for Saturday
- start_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 14:00
- end_time (HH:mm) 0...23 Hours 0…59 Minutes eg. 16:00
- timezone (Z) Offset from UTC as +-HH:mm eg. +08:00

