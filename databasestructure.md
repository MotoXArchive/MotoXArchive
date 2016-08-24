#MotoXArchive Database Structure Guide

For now this is going to be a very rough guide for the information that we need to have access to. A lot of this will not actually need to be stored within the database because it can be easily calculated from other information that will be in the database. There will also be a lot of information that is going to overlap between categories so it's important that the database is structured properly to eliminate redundancy.

##Rider
There is a lot of information that needs to be available for each rider. Some of it is permanent, such as their name, but
other things will change season to season. The temporary things can probably all be linked from other records instead of trying
maintain a large number of separate records that will have to be updated between seasons. The statistics are another thing
that should be done dynamically. I'm probably missing some stats that would be nice to track, but they will be taken from other categories anyway.

* Permanent Identification
  * First Name
  * Last Name
  * Hometown
    * City
    * State(If Applicable)
    * Country
  * Birthdate
* Temporary Identification
  * Number
  * Team
  * Manufacturer
* Statistics
  * Championships
    * Motocross
    * Supercross
    * Combined
  * Best Season Finish
    * Motocross
    * Supercross
  * Starts
  * ELO Rating
    * Current Season
      * Motocross
      * Supercross
    * Career
      * Motocross
      * Supercross
      * Combined
  * Wins
    * Motocross
      * Raw Number and Percentage
    * Supercross
      * Raw Number and Percentage
    * Combined
      * Raw Number and Percentage
  * Podiums
    * Motocross
      * Raw Number and Percentage
    * Supercross
      * Raw Number and Percentage
    * Combined
      * Raw Number and Percentage
  * Average Finishing Position
    * Motocross
    * Supercross
    * Combined
  
##Team
*Manufacturer
*Riders
  *Current
  *Past riders by year

##Manufacturer

##Venue
* Motocross or Supercross?
* Location
* Surface Type
  * Hard-Packed
  * Loamy
  * Sand
  
##Season
* Year

##Series

##Race
* Round Number
* Date
* Venue
  * This should link to the venue records