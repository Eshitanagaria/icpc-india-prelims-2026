# ICPC India Prelims 2026 Ranklist

A filterable dashboard for the tentative ICPC India Prelims 2026 ranklist (4,055 teams, 375 colleges), with registration lists for the Mathura and Chennai regionals.

**Live site:** https://eshitanagaria.github.io/icpc-india-prelims-2026/


## Features
 
- **Tabs:** Final list, Mathura, Chennai, Not in final list, Missing by college and My notes. A tab can be linked directly, for example `/#mathura`.
- **Ranklist:** search by team, college or username; filter by problems solved, college, institute type (IIT, NIT, IIIT, Other), rank range, penalty, individual problems and region
- **Submission links:** every filled square in a team's row opens that team's accepted submissions for that problem on CodeChef, in a new tab
- **Region tags:** teams registered for Mathura and/or Chennai are tagged, and can be filtered
- **Institute topper tag**, a college rank for every other team, and a "top N from each college" filter
- **Regional tabs:** every registered team for that regional, with a vertical filter sidebar (search, "in or not in the prelims ranklist", "also in the other regional", institute type and college). Teams on the ranklist show their prelims rank, which links to the ranklist, plus the institute topper tag or their college rank.
- **Not in final list:** the 1,727 teams in the master list of all registered teams (5,610) that are not in the final selection list. The master list has only a username and problems solved, so that is all the tab shows. The files give no reason, so the tab makes no claim about why.
- **Missing by college:** a partial leaderboard of colleges with teams missing from the final list, with the number of teams not in the final list and the number of teams in the final list. A college is known only for the 286 of the 1,727 missing teams that were on the earlier tentative ranklist, so the counts are minimums and the order could change with full data.
- **My notes:** press "+ Note" next to any team to add a private note. The My notes tab lists them all, with search, edit, delete, and a copy and restore backup. There is also a "Teams with my notes" filter.
- Sort options, light and dark mode, works on phones
## How it works
 
Everything is in one static file, `index.html`. The data is embedded in the page, so there is no build step and no server.
 
Notes are saved in the visitor's own browser (local storage) and are keyed by the team's username. They are not sent anywhere, so they are not shared between people or devices, and clearing site data erases them. Sharing notes between visitors would need a server or database, which a GitHub Pages site does not have.
 
## Notes
 
- This is an unofficial dashboard built from the final selection list released by ICPC India. Check the official ICPC India site for final results.
- Submission links follow the pattern `https://www.codechef.com/ICPCOL2026/status/<problem code>?usernames=<team username>`, taken from the submission-linked ranklist. They go to CodeChef, so what a visitor sees there depends on CodeChef.
- Tied teams share a rank. College rank is the number of better-ranked teams from the same college, plus one.
- On the regional tabs, the institute topper tag and college rank are the team's values on the prelims ranklist. The college rank counts every ranklist team from that college, not only those registered for the regional. Teams that are not on the ranklist have neither.
- Regional tags match on team name and college (ignoring capitals, spaces and punctuation). A few college names spelled differently in the two sources were matched by hand (for example KIIT University and Kalinga Institute of Industrial Technology); others may be missed. Two teams with the same name at one college are both tagged.
- College names that differed only in spelling or capitalisation were merged, and the organizers' own renames (for example the Amrita and KIIT names) are treated as the same college on the regional tabs. Institute type is read from the college name.
 
