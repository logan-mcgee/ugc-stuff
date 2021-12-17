# race stuff (`mission.race`)

- `mission.race.ch*` - a lot of the checkpoint stuff is pretty well known, check out jaymo/smallo's racing stuff
- `mission.race.cpbs1` - handles the round/vs regular checkpoint types, by using the 1st and second(?) bit, to determine if or not it is round
^ and maybe 2? still not super certain, needs to be further looked into but seems 99% accurate


## vehicle usage handling

these are for class 0-20 (in race format, the list has them laid out like that also), each one of these has 21 values in an array which need to be read then used to determine the vehicles allowed

each bit of a number represents a vehicle being permitted if its set(1) otherwise it is not permitted

- `mission.race.aveh`
- `mission.race.adlc` 
- `mission.race.adlc2`
- `mission.race.adlc3`

see my [vehicle list in Lua](https://gist.github.com/sadboilogan/c40beda3a1af1141c752a97efa92615f) for the data needed to handle this

- `mission.race.rdis` - race distance in meters
- `mission.race.lap` - amount of laps (0 being ptp)
- `mission.race.type` - used to determine how to treat the race, goes like:
```
27      - Street Race
26      - Pursuit Race
24 + 25 - Open Wheel Race
4 + 5   - Air Race
2 + 3   - Sea Race
12 + 13 - Bike Race
18 + 19 - Target Assault Race
6 + 7   - Stunt Race
10 + 11 - On Foot Race
0 + 1   - Land Race
else    - Race
```