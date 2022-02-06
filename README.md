# Utility scripts for Perseus app
Brief description of scripts to use the Perseus results app without the web interface (these scripts need to be run from the host machine)

## admin.rb
Provides options to:
* Set the active competition. All displays & results inputs screens read/write data for this competition.
* Purge the Event Stream (e.g. of results from a previous round).

**Run**

```bash
./admin.rb -w <competition_id> # sets the active competition
./admin.rb -p                  # purges the broadcast stream
```

## registration.rb
Read a CSV file containing climber information and update the LAN database to include these climbers

**Run**

```bash
./registration.rb -f <filename>	
# reads <filename> and adds any new climbers into the database
```

The required file format is a comma-delimited CSV file with headers as follow:

```bash
per_id,lastname,firstname,club,nation,birthyear,gender
2000104,Abbey,Sam,,,,M
2000347,Acereda Ortiz,Carla,,,1998,F
```

