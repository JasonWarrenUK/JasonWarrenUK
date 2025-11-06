<h1 align="left">Oh God, It's Jason Warren</h1>

<pre align="center">Neurodivergent • Anarchosocialist • Mouthy Little Gremlin</pre>

<h2 align="center">Dev Profile API</h2>

<details>
  <summary alight="left"><h3>./src/index.ts</h3></summary>
  
  ```ts
  import { desc } from "./utils/getProfile";
  import type { User } from "$lib/types"

  const jason: User = { name: "Jason" };

  desc(jason);
  ```

</details>

<details>
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

</details>

<details>
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

</details>

<details>
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

</details>

---

<h2 align="center">The Debris Left in My Wake</h2>

<details><summary align="left"><h3>Current Hyperfoci</h3></summary>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | ☑️ | ***Name TBD*** | turn static accessibility surveys into dynamic evolving conversations | [repo](github.com/foundersandcoders/Lift02) |
  | 🏛 | **Those Who Came Before** | procedurally generate artefacts from extinct fictional cultures & then make players deal with how they interpreted them | [repo](github.com/JasonWarrenUK/those-who-came-before) |

</details>

<details><summary align="right"><h3>Dormant Ambitions</h3></summary>

  |   | Name | Description | Links |
  | - | ---- | ----------- | ----- |
  | 🧵 | **Beacons** | store free text journals as actionable conversation graphs | [client](github.com/foundersandcoders/lift-frontend) / [server](github.com/foundersandcoders/lift-backend) |

</details>

<details><summary align="left"><h3>Seed Vault</h3></summary>

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

  </details>

<details><summary align="right"><h3>Whimsies</h3></summary>

  | Name | Links | Year |
  | ---- | ----- | ---- |
  | **Nihilistic Onboarder** | [repo](github.com/JasonWarrenUK/nihilistic-onboarder) | 2025 |
  | **Hat Recommender** | [repo](github.com/JasonWarrenUK/telebrain) | 2025 |
  | **Petulant God** | [repo](github.com/JasonWarrenUK/petulant-god) | 2023 |
  | **Melonhead** | [itch](neurosocialist.itch.io/melonhead) | 2022 |
  | **Prisms** | [itch](neurosocialist.itch.io/prisms)/[repo](github.com/JasonWarrenUK/prisms) | 2021 |
  | **My Brothers, Counting** | [itch](neurosocialist.itch.io/brothers-trying-to-count) | 2020 |

</details>

<details><summary align="left"><h3>Idea Graveyard</h3></summary>

  | Name | Links |
  | ---- | ----- |
  | **Got My Back** | [Repo](github.com/JasonWarrenUK/got-my-back) |
  | **Knowledge Kata** | [Repo](github.com/JasonWarrenUK/knowledge-kata) |

</details>

---

<h2 align="center">Field Guide to Jason</h2>

<details><summary align="left"><h3>What Is It Doing?</h3></summary>

  🌱 I’m currently seriously learning about...
  
  - **Svelte**
  - **neo4j**
  - **MCP servers**
  
  I'm also dabbling with...
  
  - **ink** (*CLI Building Framework*)

</details>

<details><summary align="right"><h3>How Does It Behave?</h3></summary>

  - 👯 I’m looking to collaborate on **useless-yet-interesting linguistics utilities & neurodivergent revolutionary digital infrastructure**
  - 🤝 I’m looking for help with **basic life skills**
  - 👨‍💻 Also I started by bimbling about with [ink stories](neurosocialist.itch.io/)
  - 📝 I wroted a book: [here it is](amazon.co.uk/Creating-Worlds-Immersive-Theatre-Making/dp/1848424450)
  - 💬 Ask me about **arts pedagogy & interactive narrative**
  - 📫 How to reach me: **~~gently, and with a kind smile~~ jason@foundersandcoders.com**
  - ⚡ Fun Fact: **There is no ethical consumption under late-stage capitalism**

</details>

---

<h2 align="center">Hit Me Up</h2>

<p align="center">
  <a href="https://twitter.com/neurosocialist" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="neurosocialist" height="30" width="40" />
  </a>
  
  <a href="https://linkedin.com/in/jasonwarrenuk" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="jasonwarrenuk" height="30" width="40" />
  </a>
  
  <a href="https://instagram.com/neurosocialist" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="neurosocialist" height="30" width="40" />
  </a>
</p>

---

<h2 align="center">is rl dev, look</h2>

<p></p>

<div align="center">
  <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/>
  </a>
  
  <a href="https://git-scm.com/" target="_blank" rel="noreferrer">
    <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/>
  </a>
  
  <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/>
  </a>
  
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/>
  </a>
</div>

<p></p>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=jasonwarrenuk&show_icons=true&locale=en&layout=compact" alt="jasonwarrenuk" />
</div>

<p></p>

<p align="center">
  <a href="https://github.com/ryo-ma/github-profile-trophy">
    <img src="https://github-profile-trophy.vercel.app/?username=jasonwarrenuk&theme=gruvbox" alt="jasonwarrenuk" />
  </a>
</p>

<div align="center">
  <a href="https://www.codewars.com/users/JasonWarrenUK" target="blank">
    <img src="https://www.codewars.com/users/JasonWarrenUK/badges/large?theme=light" alt="codewars" />
  </a>
</div>
