# Requirements

Last update: 29.07.2024

## A. CORE

1. A timer mechanism that we can hook up functions to

## B. TASKS

### a. Performance and power consumption

1. Set CPU governor to powersave when the network is down
2. Set CPU governor to performance when a tasksched spike is observed
3. Set CPU governor to performance when a user logs in
4. Set CPU governor to powersave when no users are present for `T` amount of time

#### 1. system temperature

1. Check CPU core temperature
2. Check HDD temperature (via smartctl)
3. Run the fan (via rpi-fan-control) if temperature reaches upper threshold OR a tasksched spike is observed
5. Stop the fan if temperature reaches lower threshold OR (a tasksched plateau is observed AND temperature is not above upper threshold) 

### b. Security and logging

1. Send an email when a user logs in
2. Keep a trace file to log hard shutdowns
