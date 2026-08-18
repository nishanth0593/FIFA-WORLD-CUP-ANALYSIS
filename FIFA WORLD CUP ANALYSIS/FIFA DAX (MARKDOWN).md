### FIFA WORLD CUP ANALYSIS DAX :

### 

### 1.SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### 2.SEASON\_WINNER =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR WinnerTeam =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 1))

### &#x20;

### RETURN

### WinnerTeam

### 

### 3.SEASON\_WINNER\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR WinnerTeam =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 1))

### &#x20;

### RETURN

### LOOKUPVALUE(TEAM\[IMAGE\_URL],

### &#x20;           TEAM\[TEAM\_NAME],

### &#x20;           WinnerTeam)

### 

### 4.SEASON\_RUNNERUP =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR RUNNERUP\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 2))

### &#x20;

### RETURN

### RUNNERUP\_Team

### 

### 5.SEASON\_RUNNERUP\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR RUNNERUP\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 2))

### &#x20;

### RETURN

### LOOKUPVALUE(TEAM\[IMAGE\_URL],

### &#x20;           TEAM\[TEAM\_NAME],

### &#x20;           RUNNERUP\_Team)

### 

### 6.WINNER\_MANAGER =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR MANAGER\_NAME = CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[MANAGER\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 1))

### &#x20;

### RETURN

### MANAGER\_NAME

### 

### 7.RUNNERUP\_MANAGER =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR MANAGER\_NAME = CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[MANAGER\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 2))

### &#x20;

### RETURN

### MANAGER\_NAME

### 

### 8.SEASON\_3rd\_PLACE =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR Third\_PLACE\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 3))

### &#x20;

### RETURN

### Third\_PLACE\_Team

### 

### 

### 9.3rd\_PLACE\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR Third\_PLACE\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 3))

### &#x20;

### RETURN

### 

### LOOKUPVALUE(TEAM\[IMAGE\_URL],

### &#x20;           TEAM\[TEAM\_NAME],

### &#x20;           Third\_PLACE\_Team)

### 

### 10.3rd\_MANAGER =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR MANAGER\_NAME = CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[MANAGER\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 3))

### &#x20;

### RETURN

### MANAGER\_NAME

### 

### 

### 11.SEASON\_4th\_PLACE =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR FORTH\_PLACE\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 4))

### &#x20;

### RETURN

### FORTH\_PLACE\_Team

### 

### 

### 12.4th\_PLACE\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR FORTH\_PLACE\_Team =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[TEAM\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 4))

### &#x20;

### RETURN

### 

### LOOKUPVALUE(TEAM\[IMAGE\_URL],

### &#x20;           TEAM\[TEAM\_NAME],

### &#x20;           FORTH\_PLACE\_Team)

### 

### 

### 13.4th\_MANAGER =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR MANAGER\_NAME = CALCULATE(

### &#x20;       SELECTEDVALUE(WINNER\[MANAGER\_NAME]),

### &#x20;       FILTER(WINNER, WINNER\[YEAR] = SelectedSeason \&\& WINNER\[POSITION] = 4))

### &#x20;

### RETURN

### MANAGER\_NAME

### 

### 

### 14.MAN\_OF\_THE\_MATCH =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### VAR FinalMOTM =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;       FILTER(

### &#x20;           MOTM,

### &#x20;           MOTM\[Year] = SelectedSeason \&\&

### &#x20;           MOTM\[MATCH] = "FINAL'S"

### &#x20;       )

### &#x20;   )

### RETURN

### IF(

### &#x20;   ISBLANK(FinalMOTM),

### &#x20;   "Not Introduced In This Season",

### &#x20;   FinalMOTM

### )

### 

### 

### 15.MAN\_OF\_THE\_MATCH\_2 =

### 

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR FinalMOTM =

### &#x20;   CALCULATE(SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;                   FILTER(

### &#x20;                   MOTM,

### &#x20;                   MOTM\[Year] = SelectedSeason \&\&

### &#x20;                   MOTM\[MATCH] = "THIRD PLACE MATCH"))

### 

### RETURN

### IF(

### &#x20;   ISBLANK(FinalMOTM),

### &#x20;   "Not Introduced In This Season",

### &#x20;   FinalMOTM

### )

### 

### 

### 16.MOTM\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### VAR FinalMOTM =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;       FILTER(

### &#x20;           MOTM,

### &#x20;           MOTM\[Year] = SelectedSeason \&\&

### &#x20;           MOTM\[MATCH] = "FINAL'S"

### &#x20;       )

### &#x20;   )

### RETURN

### LOOKUPVALUE(Player\_ID\[PLAYERS\_IMAGE\_URL],

### Player\_ID\[PLAYER\_NAME],

### IF(

### &#x20;   ISBLANK(FinalMOTM),

### &#x20;   "Not Introduced In This Season",

### &#x20;   FinalMOTM

### ))

### 

### 

### 15.MOTM2\_LOGO =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### VAR FinalMOTM =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;       FILTER(

### &#x20;           MOTM,

### &#x20;           MOTM\[Year] = SelectedSeason \&\&

### &#x20;           MOTM\[MATCH] = "THIRD PLACE MATCH"

### &#x20;       )

### &#x20;   )

### RETURN

### LOOKUPVALUE(Player\_ID\[PLAYERS\_IMAGE\_URL],

### Player\_ID\[PLAYER\_NAME],

### IF(

### &#x20;   ISBLANK(FinalMOTM),

### &#x20;   "Not Introduced In This Season",

### &#x20;   FinalMOTM

### ))

### 

### 

### 16.MOTM\_TMN =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### VAR FinalMOTM =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;       FILTER(

### &#x20;           MOTM,

### &#x20;           MOTM\[Year] = SelectedSeason \&\&

### &#x20;           MOTM\[MATCH] = "FINAL'S"

### &#x20;       )

### &#x20;   )

### 

### VAR TEAM\_NAME = CALCULATE(SELECTEDVALUE(MOTM\[Team]),

### MOTM\[PLAYER NAME ] = FinalMOTM)

### 

### RETURN

### IF(

### &#x20;   ISBLANK(TEAM\_NAME),

### &#x20;   "Not Introduced In This Season",

### &#x20;   TEAM\_NAME

### )

### 

### 

### 17.MOTM2\_TMN =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### VAR FinalMOTM =

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(MOTM\[PLAYER NAME ]),

### &#x20;       FILTER(

### &#x20;           MOTM,

### &#x20;           MOTM\[Year] = SelectedSeason \&\&

### &#x20;           MOTM\[MATCH] = "THIRD PLACE MATCH"

### &#x20;       )

### &#x20;   )

### 

### VAR TEAM\_NAME = CALCULATE(SELECTEDVALUE(MOTM\[Team]),

### MOTM\[PLAYER NAME ] = FinalMOTM)

### 

### RETURN

### IF(

### &#x20;   ISBLANK(TEAM\_NAME),

### &#x20;   "Not Introduced In This Season",

### &#x20;   TEAM\_NAME

### )

### 

### 

### 18.AWARD\_WINNER\_PLAYERS =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_AWARD = SELECTEDVALUE(AWARDS\[AWARD\_NAME])

### 

### VAR PLAYERS = CALCULATE(SELECTEDVALUE(AWARDS\[PLAYER\_NAME]),

### &#x20;               FILTER(AWARDS,AWARDS\[YEAR] = SELECTED\_SEASON),

### &#x20;               FILTER(AWARDS,AWARDS\[AWARD\_NAME] = SELECTED\_AWARD))

### 

### RETURN PLAYERS

### 

### 

### 19.FAIRPLAY =

### VAR SS = SELECTEDVALUE(host\_countries\[YEAR])

### VAR MinCards =

### &#x20;   CALCULATE(

### &#x20;       MINX(FILTER(CARDS, CARDS\[YEAR] = SS), CARDS\[TOTAL CARD])

### &#x20;   )

### VAR TeamWithMinCards =

### &#x20;   CALCULATE(

### &#x20;       MAXX(

### &#x20;           FILTER(CARDS, CARDS\[YEAR] = SS \&\& CARDS\[TOTAL CARD] = MinCards),

### &#x20;           CARDS\[TEAM NAME]

### &#x20;       )

### &#x20;   )

### RETURN

### IF(

### &#x20;   ISBLANK(TeamWithMinCards),

### &#x20;   "N/I",

### &#x20;   TeamWithMinCards

### )

### 

### 

### 

### 

### 20.pts\_logo =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[TEAM NAME]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### 

### LOOKUPVALUE(TEAM\[IMAGE\_URL],TEAM\[TEAM\_NAME],

### TEAM)

### 

### 

### 21.W =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[WIN]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 22.L =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[LOSS]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 23.D =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[DRAW]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 

### 24.G\_F =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[GF]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 25.G\_A =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[GA]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 26.G\_D =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[GD]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 27.PTS =

### 

### VAR SELECTED\_SEASON = SELECTEDVALUE(host\_countries\[YEAR])

### 

### VAR SELECTED\_GROUP = SELECTEDVALUE('POINTS TABLE'\[GROUP],"SELECT GROUP")

### 

### VAR TEAM = CALCULATE(

### &#x20;               SELECTEDVALUE('POINTS TABLE'\[POINTS]),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[YEAR]=SELECTED\_SEASON),

### &#x20;               FILTER('POINTS TABLE','POINTS TABLE'\[GROUP] = SELECTED\_GROUP))

### RETURN

### TEAM

### 

### 

### 28.HATRICK\_PLAYERS =

### VAR SelectedSeason = SELECTEDVALUE(host\_countries\[YEAR])

### RETURN

### CONCATENATEX (

### &#x20;   FILTER (

### &#x20;       'HATRICK GOALS',

### &#x20;       'HATRICK GOALS'\[YEAR] = SelectedSeason \&\&

### &#x20;       'HATRICK GOALS'\[GOALS] >= 3

### &#x20;   ),

### &#x20;   'HATRICK GOALS'\[PLAYERS],

### &#x20;   ", "

### )

### 



### 29\. ParticipatedCountries =

### VAR SelectedSeason = SELECTEDVALUE('POINTS TABLE'\[YEAR])

### RETURN

### IF(

### &#x20;   ISBLANK(SelectedSeason),

### &#x20;   "NOT SELECTED",

### &#x20;   COUNTROWS(

### &#x20;       FILTER(

### &#x20;           'POINTS TABLE',

### &#x20;           'POINTS TABLE'\[YEAR] = SelectedSeason

### &#x20;       )

### &#x20;   )

### )



### 

### 30\. EDITIONS = COUNTROWS(ALL(host\_countries\[YEAR]))





### 31\. EDITIONS\_No =

### VAR SS = SELECTEDVALUE('POINTS TABLE'\[YEAR])

### RETURN

### IF(

### &#x20;   ISBLANK(SS),

### &#x20;   "NOT SELECTED",

### &#x20;   CALCULATE(

### &#x20;       SELECTEDVALUE(host\_countries\[EDITIONSYEAR]),

### &#x20;       host\_countries\[YEAR] = SS

### &#x20;   )

### )





### 

### 32\. SELECTED\_YEAR = SELECTEDVALUE('POINTS TABLE'\[YEAR],"N/S")

### 

### 33\. TITLE YEAR = "PARTCIPATED COUNTRIES IN " \& \[SELECTED\_YEAR]

### 

### 

# SUMMARY:

### 

### 📊 FIFA World Cup Analysis – Notes

### 

### \- \*\*Dashboard Pages Created\*\*

### &#x20; 1. \*\*Winners \& Managers\*\* – Season‑wise champions, runner‑ups, managers, and logos.

### &#x20; 2. \*\*Points Table\*\* – Dynamic calculations for wins, losses, draws, goals, and points.

### &#x20; 3. \*\*Participated Countries Map\*\* – Visual coverage of all nations with highlights.

### 

### \- \*\*DAX Measures Implemented\*\*

### &#x20; - SELECTEDVALUE, HASONEVALUE for dynamic titles.

### &#x20; - Calculations for \*\*Goals, Points, Yellow Cards, Hat‑tricks, Fair Play, Awards\*\*.

### &#x20; - Man of the Match and other player‑level insights.

### 

### \- \*\*Key Features\*\*

### &#x20; - Interactive visuals with KPIs.

### &#x20; - Clean storytelling using Power BI visuals.

### &#x20; - Professional layout across three pages.

### 

### \- \*\*Tools Used\*\*

### &#x20; - Power BI, DAX, SQL, Excel.

### 

### \------------------------------------------------------------------------------------------------------------------

### 

### 🏆 FIFA World Cup Analysis – DAX Notes

### 

### 🎯 Season \& Team Insights

### \- \*\*SELECTED\_SEASON\*\* → Dynamic season selection.

### \- \*\*SEASON\_WINNER / RUNNERUP / 3rd / 4th Place\*\* → Retrieves team names based on position.

### \- \*\*LOGO Measures\*\* → Uses `LOOKUPVALUE` to fetch team logos for winner, runner‑up, 3rd, and 4th place.

### \- \*\*MANAGER Measures\*\* → Pulls manager names for each position.

### 

### 👤 Player Highlights

### \- \*\*MAN\_OF\_THE\_MATCH (Final \& 3rd Place)\*\* → Displays MOTM player names, with fallback text if not introduced.

### \- \*\*MOTM\_LOGO / MOTM2\_LOGO\*\* → Fetches player images.

### \- \*\*MOTM\_TMN / MOTM2\_TMN\*\* → Retrieves MOTM team names.

### \- \*\*AWARD\_WINNER\_PLAYERS\*\* → Dynamic award‑wise player selection.

### \- \*\*HATRICK\_PLAYERS\*\* → Lists players scoring 3+ goals in a season.

### 

### ⚖️ Fair Play \& Discipline

### \- \*\*FAIRPLAY\*\* → Identifies team with minimum cards in a season.

### 

### 📊 Points Table Metrics

### \- \*\*pts\_logo\*\* → Displays team logo in points table.

### \- \*\*W, L, D\*\* → Wins, losses, draws.

### \- \*\*G\_F, G\_A, G\_D\*\* → Goals for, against, and difference.

### \- \*\*PTS\*\* → Total points calculation.

### 

### \------------------------------------------------------------------------------------------------------------------





### 📊 FIFA World Cup Analysis – Project Notes

### 

### \### 🔹 Dashboard Pages

### 1\. \*\*Winners \& Managers\*\*

### &#x20;  - Season‑wise champions, runner‑ups, 3rd \& 4th place teams.

### &#x20;  - Dynamic display of team logos and manager names.

### 

### 2\. \*\*Points Table\*\*

### &#x20;  - Interactive group‑wise stats: Wins, Losses, Draws, Goals For/Against, Goal Difference, Points.

### &#x20;  - Team logos integrated for clarity.

### 

### 3\. \*\*Participated Countries Map\*\*

### &#x20;  - Visual representation of all nations that played.

### &#x20;  - Clean geographic storytelling of tournament participation.

### 

### \---

### 

### \### 🔹 DAX Measures (28 created)

### \- \*\*Season Context\*\*: `SELECTED\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_SEASON` for dynamic year selection.

### \- \*\*Team Insights\*\*: Winner, Runner‑up, 3rd \& 4th place teams with logos and managers.

### \- \*\*Player Highlights\*\*:

### &#x20; - Man of the Match (Final \& 3rd Place) with player names, logos, and team names.

### &#x20; - Award winners by category.

### &#x20; - Hat‑trick players listed dynamically.

### \- \*\*Fair Play\*\*: Identifies team with minimum cards in each season.

### \- \*\*Points Table Metrics\*\*: Wins, Losses, Draws, Goals For/Against, Goal Difference, Points.

### 

### \---

### 

### \### 🔹 Technical Strengths

### \- Strong use of \*\*SELECTEDVALUE, CALCULATE, FILTER, LOOKUPVALUE, CONCATENATEX\*\*.

### \- Measures designed for \*\*dynamic, interactive dashboards\*\*.

### \- Covers \*\*teams, managers, players, awards, fair play, and performance metrics\*\*.

### 

### \---

### 

### \### 🔹 Project Impact

### \- Provides \*\*season‑wise insights\*\* into winners, managers, and player achievements.

### \- Enables \*\*quick analysis of team performance trends\*\* across tournaments.

### \- Delivers a \*\*professional, multi‑page Power BI dashboard\*\* with storytelling visuals.

### 

### 

### \------------------------------------------------------------------------------------------------------------------

### 

### 🎤 Mentor Presentation – Talking Points

### 

### \*\*Opening\*\*

### \- “I’ve completed a Power BI project called \*FIFA World Cup Analysis\*. The aim was to build an interactive dashboard that gives season‑wise insights into winners, managers, players, and team performance.”

### 

### \*\*Dashboard Pages\*\*

### \- “The project has three main pages:

### &#x20; 1. \*\*Winners \& Managers\*\* – shows champions, runner‑ups, 3rd and 4th place teams, with logos and manager names.

### &#x20; 2. \*\*Points Table\*\* – interactive stats for wins, losses, draws, goals, and points.

### &#x20; 3. \*\*Participated Countries Map\*\* – highlights all nations that played in each season.”

### 

### \*\*Technical Work (DAX)\*\*

### \- “I created \*\*28 custom DAX measures\*\*. These include:

### &#x20; - Dynamic season selection.

### &#x20; - Winner, runner‑up, 3rd \& 4th place teams with logos and managers.

### &#x20; - Man of the Match for finals and 3rd place matches, with player images and team names.

### &#x20; - Award winners, fair play team, and hat‑trick players.

### &#x20; - Complete points table metrics: Wins, Losses, Draws, Goals For/Against, Goal Difference, and Points.”

### 

### \*\*Impact\*\*

### \- “This project enables quick analysis of team performance and historical trends. It combines storytelling visuals with technical DAX to make the dashboard interactive and professional.”

### 

### \*\*Closing\*\*

### \- “Overall, this project demonstrates my ability to use Power BI and DAX to build a structured, insightful sports analytics dashboard.”

### 

### \------------------------------------------------------------------------------------------------------------------

### 

