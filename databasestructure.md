#MotoXArchive Database Structure Guide

For now this is going to be a very rough guide for the information that we need to have access to. A lot of this will not actually need to be stored within the database because it can be easily calculated from other information that will be in the database. There will also be a lot of information that is going to overlap between categories so it's important that the database is structured properly to eliminate redundancy.

_Italicized items should not need to be stored_

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
    * State/Province(If Applicable)
    * Country
  * Birthdate
* Temporary Identification
  * Number (Only changes at a maximum of once per year. Riders that perform well can earn a career number that won't vary season to season, but the riders who don't are assigned a number based on points from the previous season)
  * Team (Typically will only change every few years, but it is also possible for it to change mid season if things aren't going well)
  * Manufacturer (Almost always tied to the team the rider is riding for. The main exception is for backmarker riders who are paying their own way to the races and don't have sponsor obligations)
  * Current Class (Usually will only change once from 250 to 450. We may want to use MX1 and MX2 identifiers for consistency because the names of the classes have changed multiple times over the years)
* Statistics
  * Championships
    * _Motocross_
    * _Supercross_
    * _Combined
  * Best Season Finish
    * _Motocross_
    * _Supercross_
  * Starts
  * ELO Rating
    * Current Season
      * _Motocross_
      * _Supercross_
    * Career
      * _Motocross_
      * _Supercross_
      * _Combined_
  * Wins
    * Motocross
      * _Raw Number and Percentage_
    * Supercross
      * _Raw Number and Percentage_
    * Combined
      * _Raw Number and Percentage_
  * Podiums
    * Motocross
      * _Raw Number and Percentage_
    * Supercross
      * _Raw Number and Percentage_
    * Combined
      * _Raw Number and Percentage_
  * Average Finishing Position
    * _Motocross_
    * _Supercross_
    * _Combined_
  
##Team
Teams are the organizations that supply bikes and other resources to the riders. It would be nice to be able to track certain statistics such as wins and championships for the team

* Manufacturer
* Riders
  * Current
  * Past riders by year

##Manufacturer
Like with the team it would be nice to be able to track the championships and win statistics for the manufacturer

##Venue
For the most part this will just be a small amount of identifying characteristics of the venue. It may be nice to have to have short description for each venue. This is more important for the motocross venues that have more unique character and history. Supercross takes place in stadiums so there is less uniqueness to them, but certain ones do have more of a history. For example, the Detroit(and before that Pontiac, MI) venues have had a unique feature where the track goes up into the stands.

* Motocross or Supercross
* Location
	* City
	* State/Province
	* Country
* Surface Type
  * Hard-Packed
  * Loamy
  * Sand
  
##Season
* Year

##Series
* Motocross or Supercross

##Race
* Round Number
* Date
* Venue
  * This should link to the venue records

<table width="800px" border="1">
	<tr align="center">
		<td><h2>Year</h2></td>
		<td><h2>Series</h2></td>
		<td><h2>Round</h2></td>
	</tr>
	<tr>
		<td rowspan="6"><b>2016</b></td>
		<td rowspan="4"><b>Supercross</b><br>
		The Supercross series takes place in stadiums around the country between January and May each year. Tracks are created new for each round but are usually composed of very similar elements. There are currently 17 rounds in the series. The 250 class is split into the East and West regions and a rider may only compete in one(They can race the 450 class at round that align with the 250 region they are not competing in.) The season finale is unique in that riders from both regions compete. This could be a hard thing to track as the rules regarding this race and the championship have changed significantly year to year.</td>
		<td><b>Heats</b><br>
		The first races on the night. Each class is split into 2 heat races by best lap times during practice. Heats are shorter races that allow riders to qualify directly to the main event. In the 250 class 9 riders from each heat qualify to the main event. In the 450 class only 4 riders qualify directly.</td>
	</tr>
	<tr>
		<td><b>Semis</b><br>
		For the 450s the next set of races are the Semis. The riders who did not qualify directly to the main from their heat are split into two Semi Final races. The top 5 in each qualify to the main event. The 250 class does not compete in the semi finals.</td>
	</tr>
	<tr>
		<td><b>LCQ</b><br>
		The last chance qualifier is a rider's last chance to make it into the main event. There is 1 LCQ per class consisting of all the riders who have not yet qualified for the main event. 4 riders from each class qualify to the main event.</td>
	</tr>
	<tr>
		<td><b>Main Event</b><br>
		It all comes down to this. This is the race that matters and the only one that counts for the championship and the rider's career statistics that most people car about. Heat wins and maybe how often the rider qualified directly from the heat would be an interesting thing to track however.</td>
	</tr>
	<tr>
		<td rowspan="2"><b>Motocross</b><br>
		The Motocross series takes place at permanent outdoor venues between May and August of each year. The tracks are permanent but do undergo some changes year to year. Many tracks have iconic elements such as Larocco's Leap, a huge step up triple jump, at Red Bud. There are currently 12 rounds in the motocross series. The format is also drastically different from Supercross. Instead of heats, semis, lcq, and main event there are simply 2 motos per class at each round. Each moto scores an equal amount of championship points. However, the overall race winner is the rider with the best combined score from the two motos. Ties are broken with the better placement in the second moto. We should be tracking moto and overall race wins.</td>
		<td><b>Moto 1</b></td>
	</tr>
	<tr>
		<td><b>Moto 2</b></td>
	</tr>
</table>

