<h1 align="left">Oh God, It's Jason Warren</h1>

<pre align="center">Neurodivergent • Anarchosocialist • Mouthy Little Gremlin</pre>

<h2 align="center">Dev Profile API</h2>

<details align="left">
  <summary alight="left"><h3>./src/index.ts</h3></summary>
  
  ```ts
  import { desc } from "./utils/getProfile";
  import type { User } from "$lib/types"

  const jason: User = { name: "Jason" };

  desc(jason);
  ```
  <hr/>
</details>

<details align="right">
  <summary align="right"><h3>./src/utils/getProfile.ts</h3></summary>

  ```ts
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
  ```
  <hr/>
</details>

<details align="left">
  <summary align="left"><h3>./src/lib/types.d.ts</h3></summary>
  
  ```ts
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
  ```
  <hr/>
</details>

<details align="right">
  <summary align="right"><h3>./db/facts.ts</h3></summary>
    
  ```ts
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
  ```
  <hr/>
</details>

---

<h2 align="center">The Debris Left in My Wake</h2>

<details align="left">
  <summary align="left"><h3>Current Hyperfoci</h3></summary>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | ☑️ | ***Name TBD*** | turn static accessibility surveys into dynamic evolving conversations | [repo](github.com/foundersandcoders/Lift02) |
  | 🏛 | **Those Who Came Before** | procedurally generate artefacts from extinct fictional cultures & then make players deal with how they interpreted them | [repo](github.com/JasonWarrenUK/those-who-came-before) |
  <hr/>
</details>

<details align="right">
  <summary align="right"><h3>Dormant Ambitions</h3></summary>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | 🧵 | **Beacons** | store free text journals as actionable conversation graphs | [client](github.com/foundersandcoders/lift-frontend) / [server](github.com/foundersandcoders/lift-backend) |
  <hr/>
</details>

<details>
  <summary align="left" align="left"><h3>Seed Vault</h3></summary>

  <h4 align="center">Apps</h4>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | ⏳ | **Grand Chronicle** | taking someone who witnessed a historical event & see what else they lived through | [repo](github.com/JasonWarrenUK/grand-chronicle) |
  | 🔮 | **Sparker** | a note-taking app that supports SEN groups | [repo](github.com/JasonWarrenUK/sparker) |
  | 🗑 | **Pretty Vacancies** | (1) ridiculous amount of work now (2) small convenience later | [repo](github.com/JasonWarrenUK/pretty-vacancies) |

  <h4 align="center">Games</h4>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | ✒️ | **The Work** | write a thesis in one night whilst staving off existential angst | [repo](github.com/JasonWarrenUK/the-work) |
  |   | **Flyt** | defeat the village's champion boaster by using a changing world as inspiration | [repo](github.com/JasonWarrenUK/flyt) |
  <hr/>
</details>

<details align="right">
  <summary align="right"><h3>Whimsies</h3></summary>

  | Name | Links | Year |
  | ---- | ----- | ---- |
  | **Nihilistic Onboarder** | [repo](github.com/JasonWarrenUK/nihilistic-onboarder) | 2025 |
  | **Hat Recommender** | [repo](github.com/JasonWarrenUK/telebrain) | 2025 |
  | **Petulant God** | [repo](github.com/JasonWarrenUK/petulant-god) | 2023 |
  | **Melonhead** | [itch](neurosocialist.itch.io/melonhead) | 2022 |
  | **Prisms** | [itch](neurosocialist.itch.io/prisms)/[repo](github.com/JasonWarrenUK/prisms) | 2021 |
  | **My Brothers, Counting** | [itch](neurosocialist.itch.io/brothers-trying-to-count) | 2020 |
  <hr/>
</details>

<details align="left">
  <summary align="left"><h3>Idea Graveyard</h3></summary>

  | Name | Links |
  | ---- | ----- |
  | **Got My Back** | [Repo](github.com/JasonWarrenUK/got-my-back) |
  | **Knowledge Kata** | [Repo](github.com/JasonWarrenUK/knowledge-kata) |
  <hr/>
</details>

---

<!-- ====== SOCIALS ====== -->
<h2 align="center">Hit Me Up</h2>

<p align="center">
  <a align="center" href="https://twitter.com/neurosocialist" target="blank">
    <img align="center" alt="@neurosocialist on Twitter"
      src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg"
      height="30"
      width="40"
    />
  </a>
  
  <a align="center" href="https://linkedin.com/in/jasonwarrenuk" target="blank">
    <img align="center" alt="jasonwarrenuk on LinkedIn"
      src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg"
      height="30"
      width="40"
    />
  </a>
  
  <a align="center" href="https://instagram.com/neurosocialist" target="blank">
    <img align="center" alt="neurosocialist"
      src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg"
      height="30"
      width="40"
    />
  </a>
</p>

<hr/>

<h2 align="center">Field Guide to Jason</h2>

<details align="left">
  <summary align="left"><h3>What Is It Doing?</h3></summary>

  I’m currently seriously learning about...
  
  - **Svelte**
  - **neo4j**
  - **MCP servers**
  
  I'm also dabbling with...
  
  - **ink** (*CLI Building Framework*)
  
  <hr/>
</details>

<details align="right">
  <summary align="right"><h3>How Does It Behave?</h3></summary>
  
  <h4 align="right"><s>I Need Help</s>Collaboration Opportunities</h4>
  
  - I’m looking to collaborate on **useless-yet-interesting linguistics utilities & neurodivergent revolutionary digital infrastructure**
  - I’m looking for help with **basic life skills**
  
  <h4 align="right">Past Lives</h4>
  
  - Also I started by bimbling about with [ink stories](neurosocialist.itch.io/)
  - I wroted a book: [here it is](amazon.co.uk/Creating-Worlds-Immersive-Theatre-Making/dp/1848424450)
  
  <h4 align="right">Trivia</h4>
  
  - Ask me about **arts pedagogy & interactive narrative**
  - How to reach me: **~~gently, and with a kind smile~~ jason@foundersandcoders.com**
  - Fun Fact: **There is no ethical consumption under late-stage capitalism**
</details>

<hr/>

<div align="center">
  <!-- ====== SKILL BRAG BULLSHIT ====== -->
  <div id="skills" align="center">
    <h2 align="center">is rl dev, look</h2>
    <p/>
    <!-- ====== BADGES ====== -->
    <div id="badges" align="center">
      <h3 align="center">meny langs duz it spk</h3>
      <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer">
        <img alt="css3"
          src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg"
          width="40"
          height="40"
        />
      </a>
      <a href="https://git-scm.com/" target="_blank" rel="noreferrer">
        <img alt="git"
          src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg"
          width="40"
          height="40"
        />
      </a>
      <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer">
        <img alt="html5"
          src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg"
          width="40"
          height="40"
        />
      </a>
      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer">
        <img alt="javascript"
          src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"
          width="40"
          height="40"
        />
      </a>
    </div>
    <p/>
    <!-- ====== TOP LANGUAGES ====== -->
    <div id="languages" align="center">
      <img alt="jasonwarrenuk"
        src="https://github-readme-stats.vercel.app/api/top-langs?username=jasonwarrenuk&show_icons=true&locale=en&layout=compact"
      />
    </div>
  </div>
  
  <!-- ====== SHINY BRAG BULLSHIT ====== -->
  <div align="center">
    <!-- ====== TROPHY RACK ====== -->
    <div id="trophies" align="center">
      <a href="https://github.com/ryo-ma/github-profile-trophy">
        <img alt="JasonWarrenUK's GitHub Trophy Rack, courtesy of ryo-ma's incredible work"
          src="https://github-profile-trophy.vercel.app/?username=jasonwarrenuk&theme=gruvbox&no-frame=false&no-bg=false&rank=-C,-?&row=3&column=3&margin-h=15&margin-w=15"
        />
      </a>
    </div>
    <!-- ====== CODEWARS ====== -->
    <div id="codewars" align="center">
      <a href="https://www.codewars.com/users/JasonWarrenUK" target="blank">
        <img alt="JasonWarrenUK's neglected codewars account"
          src="https://www.codewars.com/users/JasonWarrenUK/badges/large?theme=light"
        />
      </a>
    </div>
  </div>
</div>
