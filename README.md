<!-- |========| Xxx |========| -->
<!-- \--------\ Xxx \--------\ -->
<h1 align="left">Oh God, It's Jason Warren</h1>

<pre align="center">Neurodivergent • Anarchosocialist • Mouthy Little Gremlin</pre>

---

<!-- |========| Xxx |========| -->
<!-- \--------\ Xxx \--------\ -->
<div id="dev-profile-api">
<h2 align="center">Dev Profile API</h2>

<div id="src/index.ts">
<details align="left">
<summary><strong>./src/index.ts</strong></summary>

<code align="left"><pre>
import { describe } from "./utils/getProfile";

const jason = { name: "Jason" } as const;
const profile = describe(jason);

console.log(profile.species);  // "goblin"
console.log(profile.desc);     // "neurodivergent anarchosocialist goblin"
</pre></code>
</details>
</div>

<div id="src/utils/getProfile.ts">
<details align="right">
<summary><strong>./src/utils/getProfile.ts</strong></summary>

<code align="right"><pre>
import { roles } from "../../db/facts";
import type { Profile } from "../lib/types";

function isJason(name: string): name is "Jason" {
  return name === "Jason";
}

export function describe(user: { name: "Jason" }): Profile&lt;"goblin"&gt;;
export function describe(user: { name: string }): Profile&lt;"human"&gt;;
export function describe(user: { name: string }): Profile {
  if (isJason(user.name)) {
    return {
      name: user.name,
      species: "goblin",
      desc: "neurodivergent anarchosocialist goblin",
      roles: roles.jason,
    };
  }

  return {
    name: user.name,
    species: "human",
    desc: ["pro", "fullstack", "dev"].join(" "),
    roles: roles.default,
  };
}
</pre></code>
</details>
</div>

<div id="src/lib/types.d.ts">
<details align="left">
<summary><strong>./src/lib/types.d.ts</strong></summary>

<code align="left"><pre>
type Species = "human" | "goblin";

type Adjective = "pro" | "fullstack" | "neurodivergent" | "anarchosocialist";
type Noun = "dev" | "goblin";
type Tag = `${Adjective} ${Noun}`;

interface Role {
  readonly org: string;
  readonly role: string;
  readonly level?: string;
  readonly from: string;
  readonly to?: string;
}

interface Profile&lt;S extends Species = "human"&gt; {
  readonly name: string;
  readonly species: S;
  readonly desc: S extends "goblin"
    ? "neurodivergent anarchosocialist goblin"
    : string;
  readonly roles: readonly Role[];
}
</pre></code>
</details>
</div>

<div id="db/facts.ts">
<details align="right">
<summary><strong>./db/facts.ts</strong></summary>

<code align="right"><pre>
export const stack = [
  "svelte", "deno", "claude", "ink",
] as const satisfies readonly string[];

export const roles = {
  default: [
    { org: "@techStartUp", role: "innovation engineer" },
  ],
  jason: [
    { org: "@foundersandcoders", role: "apprentice dev", level: "mid/senior (shhh)", from: "2025" },
    { org: "@foundersandcoders", role: "L6 AI apprenticeship mentor", from: "2025" },
    { org: "@FAC-31", role: "facilitator", from: "2025-02", to: "2025-07" },
    { org: "@foundersandcoders", role: "dev", from: "2024-09", to: "2025" },
    { org: "@fac30", role: "grad", from: "2024-09", to: "2024-12" },
    { org: "@FAC29A", role: "grad", from: "2023-09", to: "2023-11" },
  ],
} as const;
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
<td>🏗️</td>
<td><strong>FAC Internal Platform</strong></td>
<td>monorepo platform: GraphQL API, Next.js & Vite apps, K8s deployment — with <a href="https://github.com/Jaz-spec">@Jaz-spec</a>, Izaak & Dan</td>
<td></td>
</tr>
<tr>
<td>✒️</td>
<td><strong>The Work</strong></td>
<td>write a thesis in one night whilst staving off existential angst</td>
<td><a href="https://github.com/JasonWarrenUK/the-work">repo</a></td>
</tr>
<tr>
<td>👹</td>
<td><strong>Goblin Mode</strong></td>
<td>commands, skills, hooks, agents & output styles for Claude Code</td>
<td><a href="https://github.com/JasonWarrenUK/goblin-mode">repo</a></td>
</tr>
<tr>
<td>🏛️</td>
<td><strong>Those Who Came Before</strong></td>
<td>try to understand a vanished culture by interpreting procedurally generated artefacts</td>
<td><a href="https://github.com/JasonWarrenUK/those-who-came-before">repo</a></td>
</tr>
</table>
</details>

<details align="right" id="completed">
<summary><h3>Completed</h3></summary>

<table align="right">
<tr>
<th>Name</th>
<th>Description</th>
<th>Team</th>
<th>Year</th>
<th>Links</th>
</tr>
<tr>
<td><strong>Iris</strong></td>
<td>ILR toolkit for apprenticeship data submission — TUI, desktop & CLI</td>
<td><a href="https://github.com/Jaz-spec">@Jaz-spec</a>, Izaak & Dan</td>
<td>2026</td>
<td><a href="https://github.com/foundersandcoders/iris">repo</a></td>
</tr>
<tr>
<td><strong>Workwise</strong></td>
<td>document workplace accessibility needs & share them on your own terms</td>
<td><a href="https://github.com/AlexVOiceover">@AlexVOiceover</a></td>
<td>2025</td>
<td><a href="https://github.com/foundersandcoders/workwise">repo</a></td>
</tr>
<tr>
<td><strong>Things We Do</strong></td>
<td></td>
<td><a href="https://github.com/jackcasstlesjones">@jackcasstlesjones</a>, <a href="https://github.com/maxitect">@maxitect</a> & <a href="https://github.com/gurtatiLND">@gurtatiLND</a></td>
<td>2024</td>
<td><a href="https://github.com/fac30/things-we-do">repo</a></td>
</tr>
<tr>
<td><strong>Sakura</strong></td>
<td></td>
<td><a href="https://github.com/jackcasstlesjones">@jackcasstlesjones</a> & <a href="https://github.com/JoshCodedit">@JoshCodedit</a></td>
<td>2024</td>
<td><a href="https://github.com/fac30/sakura-api">server</a> / <a href="https://github.com/fac30/sakura-front">client</a></td>
</tr>
</table>
</details>

<details align="left" id="seed-vault">
<summary><h3>Seed Vault</h3></summary>

<table align="left">
<tr>
<th></th>
<th>Name</th>
<th>Description</th>
<th>Links</th>
</tr>
<tr>
<td>🍞</td>
<td><strong>Bag of Bread</strong></td>
<td>crumbs and nuggets for the Hovis-inclined</td>
<td><a href="https://github.com/JasonWarrenUK/Bag-of-Bread">repo</a></td>
</tr>
<tr>
<td>🔮</td>
<td><strong>Sparker</strong></td>
<td>a note-taking app that supports SEN groups</td>
<td><a href="https://github.com/JasonWarrenUK/sparker">repo</a></td>
</tr>
<tr>
<td>⏳</td>
<td><strong>Grand Chronicle</strong></td>
<td>taking someone who witnessed a historical event & see what else they lived through</td>
<td><a href="https://github.com/JasonWarrenUK/grand-chronicle">repo</a></td>
</tr>
<tr>
<td>🗑️</td>
<td><strong>Pretty Vacancies</strong></td>
<td>(1) ridiculous amount of work now (2) small convenience later</td>
<td><a href="https://github.com/JasonWarrenUK/pretty-vacancies">repo</a></td>
</tr>
<tr>
<td>🔬</td>
<td><strong>Prism</strong></td>
<td>visualise educational networks & deliver personalised learning through AI-curated paths</td>
<td><a href="https://github.com/foundersandcoders/prism">repo</a></td>
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
<td>🤖</td>
<td><strong>Rhea</strong></td>
<td>an LLM-powered assistant for democratic/peer-led learning cohorts</td>
<td><a href="https://github.com/foundersandcoders/rhea">repo</a></td>
</tr>
<tr>
<td>💭</td>
<td><strong>Inconsequential Thinking</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/inconsequential-thinking">repo</a></td>
</tr>
<tr>
<td>🧵</td>
<td><strong>Beacons</strong></td>
<td>store free text journals as actionable conversation graphs</td>
<td><a href="https://github.com/foundersandcoders/beacons-backend">server</a> / <a href="https://github.com/foundersandcoders/beacons-frontend-v2">client</a></td>
</tr>
</table>
</details>

<details align="left" id="whimsies">
<summary><h3>Whimsies</h3></summary>

<table align="left">
<tr>
<th>Name</th>
<th>Team</th>
<th>Links</th>
<th>Year</th>
</tr>
<tr>
<td><strong>Rimewarden</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/rimewarden">repo</a></td>
<td>2026</td>
</tr>
<tr>
<td><strong>Sith Maker</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/sith-maker">repo</a></td>
<td>2026</td>
</tr>
<tr>
<td><strong>Nihilistic Onboarder</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/nihilistic-onboarder">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Hat Recommender</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/telebrain">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Psyche</strong></td>
<td><a href="https://github.com/Jaz-spec">@Jaz-spec</a></td>
<td><a href="https://github.com/fac-31/psyche">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Commons Traybake</strong></td>
<td><a href="https://github.com/Jaz-spec">@Jaz-spec</a>, <a href="https://github.com/nchua3012">@nchua3012</a> & <a href="https://github.com/JosephPotashnik">@JosephPotashnik</a></td>
<td><a href="https://github.com/fac-31/commons-traybake">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>ReDoT</strong></td>
<td><a href="https://github.com/JosephPotashnik">@JosephPotashnik</a> & <a href="https://github.com/FortyTwoFortyTwo">@FortyTwoFortyTwo</a></td>
<td><a href="https://github.com/fac-31/ReDoT">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>The Forgotten One</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/the-forgotten-one">repo</a></td>
<td>2025</td>
</tr>
<tr>
<td><strong>Petulant God</strong></td>
<td></td>
<td><a href="https://github.com/JasonWarrenUK/petulant-god">repo</a></td>
<td>2023</td>
</tr>
<tr>
<td><strong>Melonhead</strong></td>
<td></td>
<td><a href="https://neurosocialist.itch.io/melonhead">itch.io</a></td>
<td>2022</td>
</tr>
<tr>
<td><strong>Prisms</strong></td>
<td></td>
<td><a href="https://neurosocialist.itch.io/prisms">itch.io</a> / <a href="https://github.com/JasonWarrenUK/prism">repo</a></td>
<td>2021</td>
</tr>
<tr>
<td><strong>My Brothers, Counting</strong></td>
<td></td>
<td><a href="https://neurosocialist.itch.io/brothers-trying-to-count">itch.io</a></td>
<td>2020</td>
</tr>
</table>
</details>

<details align="right" id="idea-graveyard">
<summary><h3>Idea Graveyard</h3></summary>

<table align="right">
<tr>
<th>Name</th>
<th>Links</th>
</tr>
<tr>
<td><strong>Got My Back</strong></td>
<td><a href="https://github.com/JasonWarrenUK/got-my-back">repo</a></td>
</tr>
<tr>
<td><strong>Knowledge Kata</strong></td>
<td><a href="https://github.com/JasonWarrenUK/knowledge-kata">repo</a></td>
</tr>
</table>
</details>
</div>

---

<div id="hit-me-up">
<h2 align="center">Hit Me Up</h2>

<p align="center">
<a href="https://bsky.app/profile/neurosocialist.bsky.social" target="blank">
<img alt="neurosocialist on Bluesky"
src="https://img.shields.io/badge/Bluesky-neurosocialist-0285FF?style=flat-square&logo=bluesky&logoColor=white"
/>
</a>
&nbsp;
<a href="https://neurosocialist.itch.io" target="blank">
<img alt="neurosocialist on itch.io"
src="https://img.shields.io/badge/itch.io-neurosocialist-FA5C5C?style=flat-square&logo=itchdotio&logoColor=white"
/>
</a>
&nbsp;
<a href="https://linkedin.com/in/jasonwarrenuk" target="blank">
<img alt="jasonwarrenuk on LinkedIn"
src="https://img.shields.io/badge/LinkedIn-jasonwarrenuk-0A66C2?style=flat-square&logo=linkedin&logoColor=white"
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
<li>I'm looking to collaborate on <strong>useless-yet-interesting linguistics utilities & neurodivergent revolutionary digital infrastructure</strong></li>
<li>I'm looking for help with <strong>basic life skills</strong></li>
</ul>
</div>

<div align="right" id="past-lives">
<h4 align="right">Past Lives</h4>

<ul>
<li>Also I started by bimbling about with <a href="https://neurosocialist.itch.io/">ink stories</a></li>
<li>I wroted a book: <a href="https://amazon.co.uk/Creating-Worlds-Immersive-Theatre-Making/dp/1848424450">here it is</a></li>
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

<p>I'm currently seriously learning about...</p>

<ul>
<li><strong>Claude Code</strong> (<em>deep customisation & power-user workflows: hooks, skills, agents, output styles</em>)</li>
<li><strong>Shell scripting</strong> & <strong>terminal customisation</strong></li>
<li><strong>Tauri</strong></li>
<li><strong>PostgreSQL</strong></li>
<li><strong>Bun</strong></li>
</ul>

<p>I'm also dabbling with...</p>

<ul>
<li><strong>OpenTUI</strong></li>
<li><strong>D3</strong></li>
<li><strong>Docker</strong> & <strong>Kubernetes</strong></li>
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
src="https://github-readme-stats.vercel.app/api/top-langs?username=jasonwarrenuk&show_icons=true&locale=en&layout=compact&theme=gruvbox"
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
