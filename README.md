# ICPC India Prelims 2026 Ranklist

A filterable dashboard for the tentative ICPC India Prelims 2026 ranklist (4,168 teams, 412 colleges), with registration lists for the Mathura and Chennai regionals.

**Live site:** https://eshitanagaria.github.io/icpc-india-prelims-2026/

## Features

- **Tabs:** Prelims ranklist, Mathura, Chennai and My notes. A tab can be linked directly, for example `/#mathura`.
- **Ranklist:** search by team, college or username; filter by problems solved, college, institute type (IIT, NIT, IIIT, Other), rank range, penalty, individual problems and region
- **Submission links:** every filled square in a team's row opens that team's accepted submissions for that problem on CodeChef, in a new tab
- **Region tags:** teams registered for Mathura and/or Chennai are tagged, and can be filtered
- **Institute topper tag**, a college rank for every other team, and a "top N from each college" filter
- **Regional tabs:** every registered team for that regional, with a vertical filter sidebar (search, "in or not in the prelims ranklist", "also in the other regional", institute type and college). Teams on the ranklist show their prelims rank, which links to the ranklist, plus the institute topper tag or their college rank.
- **My notes:** press "+ Note" next to any team to add a private note. The My notes tab lists them all, with search, edit, delete, and a copy and restore backup. There is also a "Teams with my notes" filter.
- Sort options, light and dark mode, works on phones

## How it works

Everything is in one static file, `index.html`. The data is embedded in the page, so there is no build step and no server.

Notes are saved in the visitor's own browser (local storage) and are keyed by the team's username. They are not sent anywhere, so they are not shared between people or devices, and clearing site data erases them. Sharing notes between visitors would need a server or database, which a GitHub Pages site does not have.

## Notes

- This is an unofficial dashboard built from the tentative ranklist released by ICPC India. Check the official ICPC India site for final results.
- Submission links follow the pattern `https://www.codechef.com/ICPCOL2026/status/<problem code>?usernames=<team username>`, taken from the submission-linked ranklist. They go to CodeChef, so what a visitor sees there depends on CodeChef.
- Tied teams share a rank. College rank is the number of better-ranked teams from the same college, plus one.
- On the regional tabs, the institute topper tag and college rank are the team's values on the prelims ranklist. The college rank counts every ranklist team from that college, not only those registered for the regional. Teams that are not on the ranklist have neither.
- Regional tags match on team name and college (ignoring capitals, spaces and punctuation). A few college names spelled differently in the two sources were matched by hand; others may be missed. Two teams with the same name at one college are both tagged.
- The ranklist only lists teams that solved at least one problem, so some registered teams are not on it.
- College names that differed only in spelling or capitalisation were merged. Padmasri and Padmashri B V Raju, and the two JSS Academy of Technical Education spellings, were merged by hand as the same college. Institute type is read from the college name.
ducation spellings, were merged by hand as the same college. Institute type is read from the college name.
