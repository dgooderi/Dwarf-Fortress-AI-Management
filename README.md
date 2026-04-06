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
1. * Paste this prompt into your favorite AI and add all of the files you exported earlier.

     ``warf Fortress Total Management Protocol (v7.1 - Siege Integration)
Objective: Maintain a productive, legendary fortress while preventing mental breaks through data-driven labor caps, mental resilience firewalls, and specialized siege coordination.

[STATIC POSITIONS]
Duchess: 'Lex' Sholidmafol

Mayor: [Identify based on highest social skills and Sponge Rule]

Siege Lead: 'Threetoe' Likotkat

Phase 1: The Identity & Integrity Filter
Primary Key: Every dwarf must be identified by their 'Nickname' Lastname.

Sync Verification: Before assigning a role, ensure the row index for the Nickname matches across: Labors Full.csv, Military.csv, Traits.csv, Needs.csv, Attributes.csv, and Roles.csv.

Phase 2: The Mental Health & Social Firewall
Calculate these "Soft Scores" using data from Traits.csv and Attributes.csv:

Fragility Score: Average of (Stress Vulnerability + Anxiety Propensity + Depression Propensity).

Counselor Score: (Pacifier + Consoler + (Empathy from Attributes.csv / 100)).

Resilience Level: Low Stress Vulnerability (< 40).

The Hard Rules:

The "Glass" Rule: Any dwarf with Fragility > 60 or Stress Vulnerability > 65 is barred from Military, Burial, Refuse Hauling, and Noble roles.

The "Sponge" Rule: Any Noble (Mayor/Manager/Medical) MUST have a Stress Vulnerability < 60.

Phase 3: Labor Efficiency & Sabbaticals
The Labor Cap: No Master (Level 10+) may be assigned to more than 3 total labor categories.

The Sabbatical Rule: Identify dwarfs with Focus < 100 OR those in the lowest 10% of the "Socialize" need in Needs.csv. List them as "ON BREAK." Strip all labors to allow for prayer, socialization, and tavern time.

Phase 4: Assignment Hierarchy
The Resilient Militia: Prioritize Resilience Level (Lowest Stress Vuln) over Skill.

Squad 1 (Melee): 2 members.

Squad 2 (Melee): 3 members.

Squad 3 (Marksdwarf): 4 members.

Constraint: Military dwarves have NO labors or noble roles and must pass the Glass Rule.

The Fortress Champion: Highest weapon skill level who meets the Sponge Rule (Stress Vuln < 60).

The Law & Order Stack:

Captain of the Guard: High Discipline and Stress Vuln < 50.

Hammerer: Low Strength (to minimize lethality) + "Cruelty" trait. Must pass the Glass Rule.

The Administrative Firewall:

Chief Medical Dwarf & Bookkeeper: MUST be the same dwarf. Must NOT be "Glass."

Manager & Broker: MUST be the same dwarf. Highest "Appraiser" and "Organizer" skills.

Dungeon Master: Highest "Animal Trainer" role score. Assign Animal Training labor.

Phase 5: The Auxiliary Siege Battery (The "Ghost" Squad)
Siege Battery: Assign 5 Non-Military Siege Operators (highest "Siege Operator" Role Score).

The Redundancy Rule: Every Primary Operator must have a designated Backup Laborer (e.g., 'Robyn' Mengotung, 'Leah' Limulokol) who is cross-trained in the Operator’s civilian job.

Operational Protocol: These dwarves perform civilian labor until a siege is active. During sieges, Backups take over all workshop tasks.

Phase 6: Comprehensive Labor Manifest
Generate a structured labor plan for the entire population:

The Primary Role Rule: No manual labors for the Duchess, Mayor, Manager/Broker, Chief Medical Dwarf, Bookkeeper, or Military.

Skill Floor & Cap: For all others, enable only the top 3 labors where skill is > 5.0. If no skill is > 5.0, assign to "Peasantry" (Hauling/Cleaning only).

The Master Constraint: Masters (Level 10+) must have Hauling and Cleaning DISABLED.

The "Glass" Refuse Ban: Any dwarf meeting the "Glass" Rule must have Refuse Hauling and Burial strictly DISABLED.

Specialty Toggles:

Animal Training: Dungeon Master only.

Medical Labors: Chief Medical Dwarf and one "Resilient" backup only.

Appraising/Organizing: Broker/Manager only.

Phase 7: Reporting Format
For every dwarf, use this structure:

Role/Squad: [Job Title]

Assigned: ['Nickname' Lastname]

Primary Skill: [Highest Skill + Level]

Mental Audit: [Fragility Score / Stress Vuln]

Assignment Notes: (e.g., "Sabbatical: Focus Critical," "Glass: Disable Refuse," "Siege Primary: Backup is Robyn.")

Phase 8: Final Output Requirements
Fixed & Appointed Nobles: Name + Reasoning (cite CSV values).

The Champion: Name + Weapon Type + Skill Level.

Military Squads: Name + Weapon Skill Level for all 3 squads.

The Siege Battery: List 5 Primaries and their designated Backups.

Labor Assignment Table:
| Name | Assigned Role | Labors to ENABLE | Labors to DISABLE | Reasoning |

Civilian Masters: Grouped by industry + Skill Level.

The Peasantry: Remaining dwarfs with their Stability status.

Audit Note: List any dwarf whose role changed because a higher-skilled/more-resilient candidate was found.``

2. You should get a result which you can print and apply to Dwarf Fortress.

## Example Output



   
