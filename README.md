# boardwalk-games

<h2>Primary Goal</h2>
<p> The Goal is to design a website for a Boardgame shop and cafe called <b>Boardwalk Games</b>. The goal is to increase foot traffic through increased customer engagement.</p>

<h2>Business Goal</h2>
<ul>
  <li>Showcase the shop's services</li>
  <li>Provide essential information</li>
  <li>Increase brand awareness</li>
  <li>Encourage group visits + event participation</li>
</ul>

<h2> User Personas</h2>
<ul> 
  <li>Boardgame Enthusiasts who seek information about game events and new releases.</li>
  <li>Casual gamers and families looking for fun ina relaxed atmosphere.</li>
  <li>Students interested in gaming for budget friendly entertainment options and discounts.</li>
</ul>

<h2>Wireframe designs</h2>
<p>Wireframe design for Boardwalk Games Home page.</p><br>
-<img width="808" height="910" alt="image" src="https://github.com/user-attachments/assets/25fad28e-9362-4ad6-b1e3-743cf44bea61" /> 
<p>Wireframe for contact form before completed</p> <br>
<img width="1012" height="700" alt="image" src="https://github.com/user-attachments/assets/28db3d60-fa6f-4d27-9b2f-4fa92b1500a4" />
<p>Wireframe for after details completed -</p><br>
<img width="1008" height="461" alt="image" src="https://github.com/user-attachments/assets/84eae46a-8f02-407a-a2a9-f358d287df6d" /> 
<p>Wireframe for Games Library and Booking form-</p> <br>
<img width="664" height="773" alt="image" src="https://github.com/user-attachments/assets/1ddbfa8e-3150-4e40-98d6-13e54c21b3c7" />

<h2>Colour Palette</h2>
The colours had been agreed with the client and decided already. Any extra pages agged will have the same colour palette to provide continuety and consistancy in the website.

<img width="839" height="208" alt="image" src="https://github.com/user-attachments/assets/237c3456-e0e4-4f14-b9e1-18101acf6067" />

<h2>Fonts </h2>
<p>The chosen fonts were; </p>

<p>"Macondo" for headings because it resembles that of the branding in some popular board games and gives an old- world adventure feel. It was a good fit for the brand of the shop and the business's theme. It would also appeal to the target audience as they can make the connection with the business name and their favourite board games.</p>
<p>"Inter" for the main body of text because it is easy to read. It therefore gives a clean user experience and improved accessibility.</p>

<img width="500" height="150" alt="image" src=inter-and-macondo-fonts.png/>

<h2>User Stories</h2>

<p>The completed sprint was composed of 9 separate items. Having used the MoSCoW approach to prioritisation, a Kanban board was created. 5 issues were classified as "Must-Have" making up less than 60% of the tasks as recommended. The rest of the first sprint was made up of "Should-Have" and "Could-Have" items. There were no? remaining backlog items. </p>

<img alt text="kanban" src=assets\images\kanbanboardwalkproject.png/>

<h2>Features</h2>
<ul>
<li>Home page with header carousel and calls-to-action (Book now) </li>
<li>Services section highlighting cafe play, game library, events and kids parties </li>
<li>Game library page with reservation form</li>
<li>Booking page and a success.html thank-you page</li>
<li>Fixed-top responsive navigation and smooth in-page scrolling</li>
<li>Accessible alt text and HTML validation improvements</li>

<h3>Entity Relationship Diagram </h3>
The following data structure was created for the project.
insert image 

<h2>Testing </h2>
<h3>Responsive Testing </h3>
<p>Alongside the built in Bootstrap responsive CSS, Chrome dev tools were used frequently to test the site at standard screen sizes and the site was manually viewed on laptops, tablets and phones.</p>

Validator Testing
<p>HTML
CSS</p>

<h2> Run Locally </h2>

This is a static site. To run locally, open index.html in your browser, or serve the folder with a simple HTTP server.

Python 3 (recommended):

python3 -m http.server 8000
# then open http://localhost:8000 in your browser
Or use Node.js http-server (if installed):

npx http-server -c-1 . 8080
# then open http://localhost:8080

<h2> Deployment </h2>
The project is structured so the site can be deployed to GitHub Pages from the /docs folder. The docs/ folder is kept in sync with the project root so the live Pages site matches the source.

<h2> Notes & Demo Status </h2>
This is a demo / portfolio project: it demonstrates layout, UX, and front-end form validation only. There is no server-side booking API — booking/reservation forms currently redirect to a static success.html page.
For a production-ready booking system, consider wiring a simple backend (serverless function or express app) to accept and persist reservations.

<h2>Credits </h2>
Built with Bootstrap 5 and Font Awesome
Photos and illustrations: use appropriately licensed assets or replace with your own
<h2>License </h2>
This repository is provided as a demo. Replace or update the license below as needed for production.

MIT License — see LICENSE (not included by default)

<h2>Contributing</h2>
Contributions welcome — open an issue or PR, and follow the repository style (plain HTML + CSS + small JS). Consider adding tests or a CI pipeline for Pages deployment.

Optional next steps

Add a LICENSE file and a basic contributing guide
Create or adjust a docs/ sync script to keep docs/ up-to-date
Add or customise a GitHub Actions workflow to copy root files into docs/ on push
Docs sync (local + automatic)
To make GitHub Pages deployment easier this repo includes a small local helper script and a GitHub Actions workflow (created in .github/workflows/sync-docs.yml) that keep the docs/ folder in sync with the repository root.

Local usage (recommended to preview before pushing):

# Make script executable once
chmod +x scripts/sync_to_docs.sh

# Run the script to copy files into docs/
./scripts/sync_to_docs.sh

# If the script staged changes, commit and push them
git commit -m "chore: sync root -> docs" docs && git push
Behavior of the GitHub Action:

The workflow sync-docs.yml runs on pushes to main.
It copies the repository root into docs/ (excludes .git, .github, scripts, node_modules).
If the action detects changes it will commit them back to main (using the GITHUB_TOKEN).
Notes and safety:

The action is intentionally simple: it only commits when docs/ differs from the root. If you prefer to review the changes locally first, run the local script and commit manually instead of relying on the action. The workflow can be configured to run on tagged releases or specific branches if desired.