<h1 align="left">Oh God, It's Jason Warren</h1>

<pre align="center">Neurodivergent • Anarchosocialist • Mouthy Little Gremlin</pre>

---

<div id="dev-profile-api">
<h2 align="center">Dev Profile API</h2>

<div id="src/index.ts">
<details align="left">
<summary><h3>./src/index.ts</h3></summary>

<code align="left"><pre>
import { desc } from "./utils/getProfile";
import type { User } from "$lib/types";

const jason: User = { name: "Jason" };

desc(jason);
</pre></code>
</details>
</div>

<div id="src/utils/getProfile.ts">
<details align="right">
<summary><h3>./src/utils/getProfile.ts</h3></summary>

<code align="right"><pre>
import { roles } from "../../db/facts";
import type { User, Profile } from "$lib/types"

export function desc(user: User): Profile {
const safe = (user.name != "Jason");
const species = safe ? "human" : "goblin";

const tags = [
safe ? "pro" : "neurodivergent",
safe ? "fullstack" : "anarchosocialist",
safe ? "dev" : "goblin"
];

const roles = user.roles
? user.roles
: safe
? roles.default
: roles.jason;

return {
name: user.name,
species: species,
desc: join(tags, " "),
roles: roles
}
}
</pre></code>
</details>
</div>

<div id="src/lib/types.d.ts">
<details align="left">
<summary><h3>./src/lib/types.d.ts</h3></summary>

<code align="left"><pre>
export interface Role {
org: string,
role: string,
from?: string,
to?: string
};

export interface User {
name: string,
roles?: Role[]
};

export interface Profile extends User {
species: string,
desc: string,
};
</pre></code>
</details>
</div>

<div id="db/facts.ts">
<details align="right">
<summary><h3>./db/facts.ts</h3></summary>

<code align="right"><pre>
export const roles = {
default: [
{ org: "@techStartUp", role: "innovation engineer" }
],
jason: [
{ org: "@FAC-31", role: "facilitator", from: date(2025-02), to: date(now()) },
{ org: "@foundersandcoders",  role: "dev", from: date(2024-09), to: date(now()) },
{ org: "@fac30", role: "grad", from: date(2024-09), to: date(2024-12) },
{ org: "@FAC29A", role: "grad", from: date(2023-09), to: date(2023-11) }
]
};
</pre></code>
</details>
</div>
</div>

---

<div id="debris">
<h2 align="center">The Debris Left in My Wake</h2>

<details align="left" id="current-hyperfoci">
<summary><h3>Current Hyperfoci</h3></summary>

<table align="left">
<tr>
<th></th>
<th>Name</th>
<th>Description</th>
<th>Links</th>
</tr>
<tr>
<td>☑️</td>
<td><strong>Name TBD</strong></td>
<td>turn static accessibility surveys into dynamic evolving conversations</td>
<td><a href="github.com/foundersandcoders/Lift02">repo</a></td>
</tr>
<tr>
<td>🏛
<td><strong>Those Who Came Before</strong></td>
<td>procedurally generate artefacts from extinct fictional cultures & then make players deal with how they interpreted them</td>
<td><a href="github.com/JasonWarrenUK/those-who-came-before">repo</a></td>
</tr>
</table>
</details>

<details align="right" id="dormant-ambitions">
<summary><h3>Dormant Ambitions</h3></summary>

<table align="right">
<tr>
<th></th>
<th>Name</th>
<th>Description</th>
<th>Links</th>
</tr>
<tr>
<td>🧵</td>
<td><strong>Beacons</strong></td>
<td>store free text journals as actionable conversation graphs</td>
<td><a href="github.com/foundersandcoders/lift-frontend">client</a> / <a href="github.com/foundersandcoders/lift-backend">server</a></td>
</tr>
</table>
</details>

<details align="left" id="seed-vault">
<summary align="left" align="left"><h3>Seed Vault</h3></summary>

<h4 align="center">Apps</h4>

<table align="left">>
<tr>
<th></th>
<th>Name</th>
<th>Description</th>
<th>Links</th>
</tr>
<tr>
<td>⏳</td>
<td><strong>Grand Chronicle</strong></td>
<td>taking someone who witnessed a historical event & see what else they lived through</td>
<td><a href="github.com/JasonWarrenUK/grand-chronicle">repo</a></td>
</tr>
<tr>
<td>🔮</td>
<td><strong>Sparker</strong></td>
<td>a note-taking app that supports SEN groups</td>
<td><a href="github.com/JasonWarrenUK/sparker">repo</a></td>
</tr>
<tr>
<td>🗑</td>
<td><strong>Pretty Vacancies</strong></td>
<td>(1) ridiculous amount of work now (2) small convenience later</td>
<td><a href="github.com/JasonWarrenUK/pretty-vacancies">repo</a></td>
</tr>
</table>

<h4 align="center">Games</h4>

<table align="left">
<tr>
<th></th>
<th>Name</th>
<th>Description</th>
<th>Links</th>
</tr>
<tr>
<td>✒️</td>
<td><strong>The Work</strong></td>
<td>write a thesis in one night whilst staving off existential angst</td>
<td><a href="github.com/JasonWarrenUK/the-work">repo</a></td>
</tr>
<tr>
<td></td>
<td><strong>Flyt</strong></td>
<td>defeat the village's champion boaster by using a changing world as inspiration</td>
<td><a href="github.com/JasonWarrenUK/flyt">repo</a></td>
</tr>
</table>
</details>

<details align="right" id="whimsies">
<summary align="right"><h3>Whimsies</h3></summary>

<table align="right">
<tr>
<th>Name</th>
<th>Links</th>
<th>Year</th>
</tr>
<tr>
<td><strong>Nihilistic Onboarder</strong></td>
<td><a href="github.com/JasonWarrenUK/nihilistic-onboarder">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Hat Recommender</strong></td>
<td><a href="github.com/JasonWarrenUK/telebrain">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Petulant God</strong></td>
<td><a href="github.com/JasonWarrenUK/petulant-god">repo</a></td>
<td>2023</td>
</tr>
<tr>
<td><strong>Melonhead</strong></td>
<td><a href="neurosocialist.itch.io/melonhead">itch.io</a></td>
<td>2022</td>
</tr>
<tr>
<td><strong>Prisms</strong></td>
<td><a href="neurosocialist.itch.io/prisms">itch.io</a>/<a href="github.com/JasonWarrenUK/prism">repo</a></td>
<td>2021</td>
</tr>
<tr>
<td><strong>My Brothers, Counting</strong></td>
<td><a href="neurosocialist.itch.io/brothers-trying-to-count">repo</a></td>
<td>2020</td>
</tr>
</table>
</details>

<details align="left" id="idea-graveyard">
<summary align="left"><h3>Idea Graveyard</h3></summary>

<table align="left">>
<tr>
<th>Name</th>
<th>Links</th>
</tr>
<tr>
<td><strong>Got My Back</strong></td>
<td><a href="github.com/JasonWarrenUK/got-my-back">Repo</a></td>
</tr>
<tr>
<td><strong>Knowledge Kata</strong></td>
<td><a href="github.com/JasonWarrenUK/knowledge-kata">Repo</a></td>
</tr>
</table>
</details>
</div>

---

<div id="hit-me-up">
<h2 align="center">Hit Me Up</h2>

<p align="center">
<a align="center" href="https://twitter.com/neurosocialist" target="blank">
<img alt="@neurosocialist on Twitter"
align="center"
src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg"
height="30"
width="40"
/>
</a>

<a align="center" href="https://linkedin.com/in/jasonwarrenuk" target="blank">
<img alt="jasonwarrenuk on LinkedIn"
align="center"
src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg"
height="30"
width="40"
/>
</a>

<a align="center" href="https://instagram.com/neurosocialist" target="blank">
<img alt="neurosocialist on insta"
align="center"
src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg"
height="30"
width="40"
/>
</a>
</p>
</div>

---

<div id="field-guide">
<h2 align="center">Field Guide to Jason</h2>

<details align="right" id="how-does-it-behave">
<summary align="right"><h3>How Does It Behave?</h3></summary>

<div align="right" id="collaboration-opportunities">
<h4 align="right"><s>I Need Help</s>Collaboration Opportunities</h4>

<ul>
<li>I’m looking to collaborate on <strong>useless-yet-interesting linguistics utilities & neurodivergent revolutionary digital infrastructure</strong></li>
<li>I’m looking for help with <strong>basic life skills</strong></li>
</ul>
</div>

<div align="right" id="past-lives">
<h4 align="right">Past Lives</h4>

<ul>
<li>Also I started by bimbling about with <a href="neurosocialist.itch.io/">ink stories</a></li>
<li>I wroted a book: <a href="amazon.co.uk/Creating-Worlds-Immersive-Theatre-Making/dp/1848424450">here it is</a></li>
</ul>
</div>

<div align="right" id="trivia">
<h4 align="right">Trivia</h4>

<ul>
<li>Ask me about <strong>arts pedagogy & interactive narrative</strong></li>
<li>How to reach me: <strong><s>gently, and with a kind smile</s> jason@foundersandcoders.com</strong></li>
<li>Fun Fact: <strong>There is no ethical consumption under late-stage capitalism</strong></li>
</ul>
</div>
</details>

<details align="left" id="what-is-it-doing">
<summary align="left"><h3>What Is It Doing?</h3></summary>

<p>I’m currently seriously learning about...</p>

<ul>
<li><strong>Svelte</strong></li>
<li><strong>neo4j</strong></li>
<li><strong>MCP servers</strong></li>
</ul>

<p>I'm also dabbling with...</p>

<ul>
<li><strong>ink</strong> (<em>CLI Building Framework</em>)</li>
</ul>
</details>
</div>

---

<div align="center" id="brag-bullshit">
<h2 align="center">is rl dev, look</h2>

<div align="center" id="like-badges">
<p align="center">
<a href="https://go-skill-icons.vercel.app/">
<img alt="My Stack"
src="https://go-skill-icons.vercel.app/api/icons?i=zed,typescript,deno,svelte,neo4j,langchain,claude,tailwindcss,daisyui,mermaid,n8n"
/>
</a>
</p>
</div>

<div align="center" id="trophy-rack">
<a href="https://github.com/ryo-ma/github-profile-trophy">
<img alt="JasonWarrenUK's GitHub Trophy Rack, courtesy of ryo-ma's incredible work"
src="https://github-profile-trophy.vercel.app/?username=jasonwarrenuk&theme=gruvbox&no-frame=false&no-bg=false&rank=-C,-?&row=3&column=3&margin-h=15&margin-w=15"
/>
</a>
</div>

<div align="center" id="lang-badges">
<p align="center">
<a href="https://go-skill-icons.vercel.app/">
<img alt="Other things what I is knowing"
src="https://go-skill-icons.vercel.app/api/icons?i=html,css,javascript,markdown,json,yaml,regex"
/>
</a>
</p>
</div>

<div align="center" id="languages">
<img alt="jasonwarrenuk"
src="https://github-readme-stats.vercel.app/api/top-langs?username=jasonwarrenuk&show_icons=true&locale=en&layout=compact"
/>
</div>

<div align="center" id="tool-badges">
<p align="center">
<a href="https://go-skill-icons.vercel.app/">
<img alt="Other things what I is knowing"
src="https://go-skill-icons.vercel.app/api/icons?i=nodejs,expressjs,react,nextjs,betterauth,postgresql,sqlite,supabase,mongodb"
/>
</a>
</p>
</div>

<div align="center" id="codewars">
<a href="https://www.codewars.com/users/JasonWarrenUK" target="blank">
<img alt="JasonWarrenUK's neglected codewars account"
src="https://www.codewars.com/users/JasonWarrenUK/badges/large?theme=light"
/>
</a>
</div>
</div>

<footer>
</footer>
