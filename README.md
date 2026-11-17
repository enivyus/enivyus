Hi ![](https://user-images.githubusercontent.com/18350557/176309783-0785949b-9127-417c-8b55-ab5a4333674e.gif) My name is Chalanthorn Srinaunchan
================================================================================================================================================

Software Engineering student at Thammasat University

* 🌍  I'm based in Bangkok , Thailand
* ✉️  You can contact me via [Email](mailto:tonlism02548@gmail.com)

<p align="left">
<a href="https://www.python.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/python-colored.svg" alt="Python" title="Python" width="36" height="36" /></a><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/javascript-colored.svg" alt="JavaScript" title="JavaScript" width="36" height="36" /></a><a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/typescript-colored.svg" alt="TypeScript" title="TypeScript" width="36" height="36" /></a><a href="https://code.visualstudio.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/visualstudiocode-colored.svg" alt="VS Code" title="VS Code" width="36" height="36" /></a><a href="https://developer.mozilla.org/en-US/docs/Glossary/HTML5" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/html5-colored.svg" alt="HTML5" title="HTML5" width="36" height="36" /></a><a href="https://reactjs.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/react-colored.svg" alt="React" title="React" width="36" height="36" /></a><a href="https://nextjs.org/docs" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/nextjs-colored-dark.svg" alt="NextJs" title="NextJs" width="36" height="36" /></a><a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/tailwindcss-colored.svg" alt="TailwindCSS" title="TailwindCSS" width="36" height="36" /></a><a href="https://vitejs.dev/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/vite-colored.svg" alt="Vite" title="Vite" width="36" height="36" /></a><a href="https://nodejs.org/en/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/nodejs-colored.svg" alt="NodeJS" title="NodeJS" width="36" height="36" /></a><a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mongodb-colored.svg" alt="MongoDB" title="MongoDB" width="36" height="36" /></a><a href="https://www.mysql.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mysql-colored.svg" alt="MySQL" title="MySQL" width="36" height="36" /></a><a href="https://www.postgresql.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/postgresql-colored.svg" alt="PostgreSQL" title="PostgreSQL" width="36" height="36" /></a><a href="https://firebase.google.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/firebase-colored.svg" alt="Firebase" title="Firebase" width="36" height="36" /></a><a href="https://www.figma.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/figma-colored.svg" alt="Figma" title="Figma" width="36" height="36" /></a><a href="https://www.docker.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/docker-colored.svg" alt="Docker" title="Docker" width="36" height="36" /></a><a href="https://flutter.dev/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/flutter-colored.svg" alt="Flutter" title="Flutter" width="36" height="36" /></a>
</p>


## My Works

### [Mule Account Detector](https://github.com/enivyus/mule-detector)
**A mini core bank plus a system that catches mule accounts: accounts that receive scam victims' money and pass it on within minutes.**

Built end to end: the bank, a streaming detector, a graph analysis step, auto-freeze, and an investigator dashboard. All data is synthetic.

- **Core banking that keeps its books straight:** Spring Boot + PostgreSQL, double-entry ledger, row locks taken in a fixed order, idempotency keys. 1,000 concurrent transfers still balance to the satang.
- **Real-time detection:** every completed transfer is published to Redpanda (Kafka API). A rule engine scores accounts as money moves and freezes them automatically when 3+ rules fire.
- **Follow the money:** Neo4j graph analysis spreads suspicion along the money trail and groups rings with Louvain community detection.
- **Measured honestly:** thresholds were tuned on one seed and scored once on a seed never seen before.

| | Precision | Recall |
|---|---|---|
| Simple rules (baseline) | 32% | 100% |
| **Rules + graph** | **87%** | **100%** |
| **Auto-freeze tier** | **100%** (0 genuine accounts frozen) | 59% |

- **Live demo result:** 23 accounts frozen (all mules), **89% of the rings' cash-out withdrawals refused**.
- **Secure by role:** Spring Security roles (channel, investigator, rule engine). Every freeze and unfreeze is written to an audit log with who did it and why.
- **Investigator dashboard:** React + Cytoscape.js, Thai/English, light/dark. A "survey map" design: risk drawn as contour rings, stolen money traced as a route across accounts.

`Java 21` `Spring Boot` `PostgreSQL` `Kafka / Redpanda` `Neo4j` `React` `Cytoscape.js` `Python` `Docker`
