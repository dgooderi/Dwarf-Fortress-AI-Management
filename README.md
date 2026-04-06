# Dwarf Fortress AI Management
A framework for managing and assigning dwarves using the actual attributes from the dwarves (Dwarf Therapist). Having AI assign positions using specific rules ensuring Dwarves have the correct, Job, Noble Position, or Military position. It also preserves the mental health of your dwarves.

Remember that some AI systems limit the number of files you can upload and they may not keep the file in memory.
AI does, and will make mistakes. I tried to spoon feed it like a baby but it can be forgetfull.
The example results below were created with Gemini

## Requirnments

1. Dwarf Therapist <https://github.com/dwarf-therapist/dwarf-therapist>
2. DF Hack (steam version)
3. Dwarf Fortress (steam version)
4. Dwarves assigned nicknames

## Setup

1. Install Dwarf Therapist
2. Install DF Hack via steam
3. Assign Nicknames to every Dwarf
   a. Open Dwarf Fortress and load your game
   b. Open DF Hack
   c. Run 'autonick all'    (assigns nicknames to all dwarves who do not already have nickname)
                            (should be re-run with every migration)
4. Create a new Dwarf Therapist memory profile
   a. Open DF Hack
   b. run 'devel/export-dt-ini' (created a therapist.ini file in the root of DF Hack.
   c. Move the Therapist.ini file to Dwarf Therapist install folder/data.
      for example DwarfTherapist-v42.1.6-win64\data\memory_layouts\windows
   d. run Dwarf Therapist. If everything worked you should have a list of dwarves.

5. Configure Dwarf Therapist
   a. Open File Options
   b. Check Don't Display Children or Babies
   c. Check Don't Display Visitors/Guests
   d. Uncheck Show Full Unit Names
   e. Uncheck Show generic Unit Names
   f. ensure these grid views are visible (select add on the main screen)
      - Labors Full
      - Military
      - Other Skills
      - Attributes
      - Roles
      - health
      - Needs
      - Traits
      - Weapons
   
## Data Extraction
1. Select each Grid View.
2. Select File - Export Current Grid View as CSV

##Put AI to work
1. * Paste this prompt file into your favorite AI and add all of the files you exported earlier.

2. You should get a result which you can print and apply to Dwarf Fortress.

## Example Output



   
