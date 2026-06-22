<!-- ═══════════════════════════════════════════════════════════════════
     3-D ANIMATED HERO — pure SVG, no external service required
     ═══════════════════════════════════════════════════════════════════ -->
<div align="center">

<svg viewBox="0 0 900 340" xmlns="http://www.w3.org/2000/svg" width="100%">
  <defs>
    <!-- deep-space background gradient -->
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%"   stop-color="#020817"/>
      <stop offset="50%"  stop-color="#0d1117"/>
      <stop offset="100%" stop-color="#0a0f1e"/>
    </linearGradient>

    <!-- purple-to-blue glow gradient for name -->
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#a78bfa"/>
      <stop offset="50%"  stop-color="#70a5fd"/>
      <stop offset="100%" stop-color="#38bdae"/>
    </linearGradient>

    <!-- shimmer gradient for top edge -->
    <linearGradient id="shimmer" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#a78bfa" stop-opacity="0"/>
      <stop offset="30%"  stop-color="#70a5fd" stop-opacity="1"/>
      <stop offset="70%"  stop-color="#38bdae" stop-opacity="1"/>
      <stop offset="100%" stop-color="#a78bfa" stop-opacity="0"/>
    </linearGradient>

    <!-- glow filter for name 3-D effect -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>

    <!-- soft drop-shadow for tagline -->
    <filter id="softShadow">
      <feDropShadow dx="0" dy="2" stdDeviation="3" flood-color="#70a5fd" flood-opacity="0.4"/>
    </filter>

    <!-- orbiting particle motion paths -->
    <path id="orbit1" d="M450,170 m-130,0 a130,40 0 1,1 260,0 a130,40 0 1,1 -260,0" fill="none"/>
    <path id="orbit2" d="M450,170 m-90,0 a90,90 0 1,1 180,0 a90,90 0 1,1 -180,0" fill="none"/>
    <path id="orbit3" d="M450,170 m-160,0 a160,55 0 1,0 320,0 a160,55 0 1,0 -320,0" fill="none"/>
  </defs>

  <!-- ── Background ── -->
  <rect width="900" height="340" fill="url(#bg)" rx="0"/>

  <!-- ── Star field ── -->
  <g opacity="0.6">
    <circle cx="45"  cy="25"  r="1.2" fill="#fff"><animate attributeName="opacity" values="0.3;1;0.3" dur="2.1s" repeatCount="indefinite"/></circle>
    <circle cx="120" cy="60"  r="0.8" fill="#a78bfa"><animate attributeName="opacity" values="0.5;1;0.5" dur="3.3s" repeatCount="indefinite"/></circle>
    <circle cx="200" cy="20"  r="1.0" fill="#70a5fd"><animate attributeName="opacity" values="0.2;1;0.2" dur="1.8s" repeatCount="indefinite"/></circle>
    <circle cx="300" cy="45"  r="0.7" fill="#fff"><animate attributeName="opacity" values="0.4;1;0.4" dur="2.6s" repeatCount="indefinite"/></circle>
    <circle cx="380" cy="15"  r="1.1" fill="#38bdae"><animate attributeName="opacity" values="0.3;1;0.3" dur="3.0s" repeatCount="indefinite"/></circle>
    <circle cx="520" cy="30"  r="0.9" fill="#fff"><animate attributeName="opacity" values="0.6;1;0.6" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="620" cy="55"  r="1.3" fill="#a78bfa"><animate attributeName="opacity" values="0.2;1;0.2" dur="1.6s" repeatCount="indefinite"/></circle>
    <circle cx="720" cy="18"  r="0.8" fill="#70a5fd"><animate attributeName="opacity" values="0.5;1;0.5" dur="2.9s" repeatCount="indefinite"/></circle>
    <circle cx="820" cy="40"  r="1.0" fill="#38bdae"><animate attributeName="opacity" values="0.3;1;0.3" dur="3.5s" repeatCount="indefinite"/></circle>
    <circle cx="870" cy="22"  r="0.7" fill="#fff"><animate attributeName="opacity" values="0.4;1;0.4" dur="2.2s" repeatCount="indefinite"/></circle>
    <circle cx="55"  cy="300" r="1.0" fill="#a78bfa"><animate attributeName="opacity" values="0.3;1;0.3" dur="2.7s" repeatCount="indefinite"/></circle>
    <circle cx="160" cy="320" r="0.8" fill="#fff"><animate attributeName="opacity" values="0.5;1;0.5" dur="3.1s" repeatCount="indefinite"/></circle>
    <circle cx="750" cy="310" r="1.1" fill="#70a5fd"><animate attributeName="opacity" values="0.2;1;0.2" dur="2.0s" repeatCount="indefinite"/></circle>
    <circle cx="850" cy="290" r="0.9" fill="#38bdae"><animate attributeName="opacity" values="0.4;1;0.4" dur="1.9s" repeatCount="indefinite"/></circle>
  </g>

  <!-- ── Top shimmer bar ── -->
  <rect x="0" y="0" width="900" height="3" fill="url(#shimmer)" rx="2">
    <animate attributeName="opacity" values="0.5;1;0.5" dur="3s" repeatCount="indefinite"/>
  </rect>

  <!-- ── GitHub Octocat 3-D sphere (left side) ── -->
  <!-- sphere base glow -->
  <circle cx="155" cy="170" r="85" fill="#0d1a2e" opacity="0.9"/>
  <circle cx="155" cy="170" r="83" fill="none" stroke="#70a5fd" stroke-width="1.5" opacity="0.6">
    <animate attributeName="r" values="83;87;83" dur="3s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.6;1;0.6" dur="3s" repeatCount="indefinite"/>
  </circle>
  <!-- inner purple glow -->
  <circle cx="155" cy="170" r="68" fill="none" stroke="#a78bfa" stroke-width="0.8" opacity="0.3"/>
  <!-- GitHub mark (simplified Octocat head + body in SVG path) -->
  <g transform="translate(155,170)" filter="url(#glow)">
    <!-- head -->
    <circle cx="0" cy="-12" r="28" fill="#c9d1d9"/>
    <!-- ear-fins -->
    <ellipse cx="-19" cy="-26" rx="8" ry="11" fill="#c9d1d9" transform="rotate(-30,-19,-26)"/>
    <ellipse cx="19"  cy="-26" rx="8" ry="11" fill="#c9d1d9" transform="rotate(30,19,-26)"/>
    <!-- face shadow -->
    <circle cx="0" cy="-12" r="22" fill="#0d1117"/>
    <!-- eyes -->
    <circle cx="-8" cy="-16" r="3.5" fill="#c9d1d9"/>
    <circle cx="8"  cy="-16" r="3.5" fill="#c9d1d9"/>
    <!-- body / tentacles -->
    <rect x="-18" y="16" width="36" height="24" rx="10" fill="#c9d1d9"/>
    <rect x="-18" y="16" width="36" height="18" rx="8"  fill="#0d1117"/>
    <!-- tentacle lines -->
    <line x1="-12" y1="32" x2="-18" y2="50" stroke="#c9d1d9" stroke-width="5" stroke-linecap="round"/>
    <line x1="0"   y1="34" x2="0"   y2="52" stroke="#c9d1d9" stroke-width="5" stroke-linecap="round"/>
    <line x1="12"  y1="32" x2="18"  y2="50" stroke="#c9d1d9" stroke-width="5" stroke-linecap="round"/>
    <animate attributeName="transform" values="translate(0,0);translate(0,-5);translate(0,0)" dur="4s" repeatCount="indefinite" additive="sum"/>
  </g>

  <!-- ── Orbiting code particles ── -->
  <!-- orbit ring 1 (tilted ellipse) -->
  <ellipse cx="155" cy="170" rx="100" ry="30" fill="none" stroke="#70a5fd" stroke-width="0.6" opacity="0.25" transform="rotate(-20,155,170)"/>
  <!-- orbit ring 2 -->
  <ellipse cx="155" cy="170" rx="108" ry="38" fill="none" stroke="#a78bfa" stroke-width="0.6" opacity="0.2" transform="rotate(15,155,170)"/>

  <!-- orbiting dot 1 -->
  <circle r="5" fill="#70a5fd" filter="url(#glow)">
    <animateMotion dur="5s" repeatCount="indefinite" rotate="auto">
      <mpath href="#orbit1"/>
    </animateMotion>
  </circle>
  <!-- orbiting dot 2 (counter) -->
  <circle r="4" fill="#a78bfa" filter="url(#glow)">
    <animateMotion dur="7s" repeatCount="indefinite" rotate="auto" keyPoints="1;0" keyTimes="0;1" calcMode="linear">
      <mpath href="#orbit2"/>
    </animateMotion>
  </circle>
  <!-- orbiting dot 3 -->
  <circle r="3.5" fill="#38bdae" filter="url(#glow)">
    <animateMotion dur="6s" repeatCount="indefinite" rotate="auto" begin="2s">
      <mpath href="#orbit3"/>
    </animateMotion>
  </circle>

  <!-- ── NAME — 3-D layered text ── -->
  <!-- shadow layer (offset, dark) -->
  <text x="532" y="133" text-anchor="middle" font-family="'Segoe UI',Arial,sans-serif" font-weight="900" font-size="58" fill="#0a0f1e" letter-spacing="3" opacity="0.8">INBARASAN J P</text>
  <!-- mid-tone layer -->
  <text x="530" y="131" text-anchor="middle" font-family="'Segoe UI',Arial,sans-serif" font-weight="900" font-size="58" fill="#1e3a5f" letter-spacing="3" opacity="0.9">INBARASAN J P</text>
  <!-- main gradient layer -->
  <text x="529" y="129" text-anchor="middle" font-family="'Segoe UI',Arial,sans-serif" font-weight="900" font-size="58" fill="url(#nameGrad)" letter-spacing="3" filter="url(#glow)">
    INBARASAN J P
    <animate attributeName="opacity" values="0.85;1;0.85" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- ── TAGLINE ── -->
  <text x="529" y="163" text-anchor="middle" font-family="'Courier New',monospace" font-size="13.5" fill="#8b949e" letter-spacing="4" font-weight="600">
    ASPIRING SOFTWARE ENGINEER  ·  FULL STACK DEVELOPER  ·  AI &amp; DATA ENTHUSIAST
  </text>

  <!-- ── Animated underline beneath tagline ── -->
  <line x1="290" y1="172" x2="290" y2="172" stroke="url(#shimmer)" stroke-width="1.5">
    <animate attributeName="x2" values="290;768;290" dur="2.5s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.2,1;0.4,0,0.2,1"/>
    <animate attributeName="opacity" values="0;1;0" dur="2.5s" repeatCount="indefinite"/>
  </line>

  <!-- ── TYPING role cards ── -->
  <!-- card 1 -->
  <g>
    <rect x="308" y="190" width="150" height="34" rx="8" fill="#0d1a2e" stroke="#70a5fd" stroke-width="0.8" opacity="0.85"/>
    <text x="383" y="212" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#70a5fd" font-weight="700">☕ Java Developer</text>
    <animate attributeName="opacity" values="0;1;1;0" dur="6s" begin="0s" repeatCount="indefinite"/>
  </g>
  <!-- card 2 -->
  <g opacity="0">
    <rect x="308" y="190" width="150" height="34" rx="8" fill="#0d1a2e" stroke="#a78bfa" stroke-width="0.8" opacity="0.85"/>
    <text x="383" y="212" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#a78bfa" font-weight="700">⚛️ React · Node.js</text>
    <animate attributeName="opacity" values="0;0;1;1;0" dur="6s" begin="2s" repeatCount="indefinite"/>
  </g>
  <!-- card 3 -->
  <g opacity="0">
    <rect x="308" y="190" width="150" height="34" rx="8" fill="#0d1a2e" stroke="#38bdae" stroke-width="0.8" opacity="0.85"/>
    <text x="383" y="212" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#38bdae" font-weight="700">🤖 AI · ML · Data</text>
    <animate attributeName="opacity" values="0;0;1;1;0" dur="6s" begin="4s" repeatCount="indefinite"/>
  </g>

  <!-- stat pills -->
  <rect x="478" y="190" width="118" height="34" rx="8" fill="#0d1a2e" stroke="#bf91f3" stroke-width="0.8" opacity="0.85"/>
  <text x="537" y="208" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="10" fill="#8b949e">LeetCode Rating</text>
  <text x="537" y="220" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#bf91f3" font-weight="700">⚡ 1429 Max</text>

  <rect x="608" y="190" width="118" height="34" rx="8" fill="#0d1a2e" stroke="#38bdae" stroke-width="0.8" opacity="0.85"/>
  <text x="667" y="208" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="10" fill="#8b949e">Problems Solved</text>
  <text x="667" y="220" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#38bdae" font-weight="700">✅ 170+ DSA</text>

  <rect x="738" y="190" width="118" height="34" rx="8" fill="#0d1a2e" stroke="#70a5fd" stroke-width="0.8" opacity="0.85"/>
  <text x="797" y="208" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="10" fill="#8b949e">Certifications</text>
  <text x="797" y="220" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#70a5fd" font-weight="700">🏅 10+ Certs</text>

  <!-- ── Tech stack floating chips ── -->
  <g font-family="'Courier New',monospace" font-size="10.5" font-weight="600">
    <rect x="308" y="240" width="64" height="20" rx="5" fill="#1c2b1c" stroke="#4ade80" stroke-width="0.7"/>
    <text x="340" y="254" text-anchor="middle" fill="#4ade80">Python</text>

    <rect x="382" y="240" width="52" height="20" rx="5" fill="#1a1c2e" stroke="#70a5fd" stroke-width="0.7"/>
    <text x="408" y="254" text-anchor="middle" fill="#70a5fd">React</text>

    <rect x="444" y="240" width="48" height="20" rx="5" fill="#1c1a14" stroke="#f59e0b" stroke-width="0.7"/>
    <text x="468" y="254" text-anchor="middle" fill="#f59e0b">Java</text>

    <rect x="502" y="240" width="66" height="20" rx="5" fill="#131e13" stroke="#4ade80" stroke-width="0.7"/>
    <text x="535" y="254" text-anchor="middle" fill="#4ade80">Node.js</text>

    <rect x="578" y="240" width="48" height="20" rx="5" fill="#1a1c2e" stroke="#60a5fa" stroke-width="0.7"/>
    <text x="602" y="254" text-anchor="middle" fill="#60a5fa">AWS</text>

    <rect x="636" y="240" width="76" height="20" rx="5" fill="#1e1320" stroke="#a78bfa" stroke-width="0.7"/>
    <text x="674" y="254" text-anchor="middle" fill="#a78bfa">PostgreSQL</text>

    <rect x="722" y="240" width="74" height="20" rx="5" fill="#122020" stroke="#38bdae" stroke-width="0.7"/>
    <text x="759" y="254" text-anchor="middle" fill="#38bdae">MongoDB</text>

    <rect x="806" y="240" width="50" height="20" rx="5" fill="#1a1c2e" stroke="#f472b6" stroke-width="0.7"/>
    <text x="831" y="254" text-anchor="middle" fill="#f472b6">ML/AI</text>
  </g>

  <!-- ── Bottom shimmer bar ── -->
  <rect x="0" y="337" width="900" height="3" fill="url(#shimmer)" rx="2">
    <animate attributeName="opacity" values="0.5;1;0.5" dur="3s" begin="1.5s" repeatCount="indefinite"/>
  </rect>
</svg>

</div>

<!-- ═══════════════════════════ TYPING SVG ═══════════════════════════ -->
<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=22&duration=2800&pause=900&color=70A5FD&center=true&vCenter=true&width=780&lines=Full+Stack+Developer+%7C+Java+Enthusiast+%E2%98%95;AI+%2B+ML+Explorer+%F0%9F%A4%96;Deloitte+%7C+Tata+GenAI+%7C+PwC+Certified+%F0%9F%8F%85;Building+scalable+solutions+one+commit+at+a+time+%F0%9F%9A%80)](https://git.io/typing-svg)

</div>

<!-- ════════════════════════ SOCIAL BADGES ════════════════════════ -->
<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/inbarasan-jp)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:inbarasan0809@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/inbarasanjpcse2023-stack)

![Profile Views](https://komarev.com/ghpvc/?username=inbarasanjpcse2023-stack&color=70a5fd&style=for-the-badge&label=Profile+Views)

</div>

<!-- ════════════════════════ SNAKE ANIMATION DIVIDER ════════════════ -->
<div align="center">
  <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake animation" width="100%"/>
</div>

---

## 🧑‍💻 About Me

<img align="right" width="380" src="https://raw.githubusercontent.com/abhisheknaiidu/abhisheknaiidu/master/code.gif"/>

```java
public class Inbarasan {

    String name        = "Inbarasan J P";
    String location    = "Coimbatore, Tamil Nadu, India";
    String degree      = "B.E. Computer Science & Engineering (2023–2027)";
    String college     = "SNS College of Technology";
    float  cgpa        = 7.89f;

    String[] stack = {
        "Java", "Python", "React.js", "Node.js",
        "Express.js", "PostgreSQL", "MongoDB", "AWS"
    };

    String[] currentlyLearning = {
        "System Design", "Spring Boot",
        "Advanced DSA", "n8n Workflow Automation"
    };

    String funFact = "I solved 170+ LeetCode problems and still debug at 2 AM.";

    String motto() {
        return "Build. Break. Learn. Repeat. 🚀";
    }
}
```

<br clear="right"/>

📫 **Reach me:** [inbarasan0809@gmail.com](mailto:inbarasan0809@gmail.com) &nbsp;|&nbsp; [LinkedIn](https://linkedin.com/in/inbarasan-jp) &nbsp;|&nbsp; [LeetCode](https://leetcode.com)

---

## 🛠️ Tech Stack

**Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![React](https://img.shields.io/badge/React.js-61DAFB?style=flat-square&logo=react&logoColor=black)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**Cloud & DevOps**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

**Libraries & Tools**

![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)

---

## 📊 GitHub Stats

<div align="center">
  <a href="https://github.com/inbarasanjpcse2023-stack">
    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=inbarasanjpcse2023-stack&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&bg_color=0d1117&title_color=70a5fd&icon_color=bf91f3&text_color=c9d1d9&border_radius=10"/>
  </a>
  <a href="https://github.com/inbarasanjpcse2023-stack">
    <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=inbarasanjpcse2023-stack&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=70a5fd&text_color=c9d1d9&langs_count=8&border_radius=10"/>
  </a>
</div>

---

## 🔥 Streak Stats

<div align="center">
  <img src="https://streak-stats.demolab.com?user=inbarasanjpcse2023-stack&theme=tokyonight-duo&hide_border=true&background=0D1117&ring=70A5FD&fire=BF91F3&currStreakLabel=70A5FD&sideLabels=38BDAE&dates=8B949E&currStreakNum=C9D1D9&sideNums=C9D1D9&stroke=0D1117&border_radius=10" alt="GitHub Streak"/>
</div>

---

## 📈 Activity Graph

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=inbarasanjpcse2023-stack&theme=tokyo-night&bg_color=0d1117&color=70a5fd&line=bf91f3&point=38bdae&area=true&hide_border=true" width="100%"/>
</div>

---

## 🏆 Trophy Wall

<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=inbarasanjpcse2023-stack&theme=tokyonight&no-frame=true&no-bg=true&row=1&column=7&margin-w=4"/>
</div>

---

## 💼 Work Experience

<details>
<summary>🌐 <strong>Web Development Intern</strong> — InternPe &nbsp;|&nbsp; June 2026 &nbsp;|&nbsp; Remote</summary>

<br/>

> ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

- Developed responsive, user-friendly web applications using HTML, CSS, JavaScript, and React, focusing on performance and UX best practices.
- Integrated RESTful APIs and built reusable UI components to enhance application functionality and maintainability.
- Improved website performance and user experience through code optimization and adherence to industry best practices.
- Collaborated effectively using Git and Agile workflows to consistently deliver high-quality solutions on schedule.

</details>

<details>
<summary>☕ <strong>Java Programming Intern</strong> — Synovers &nbsp;|&nbsp; Dec 2025 – Jan 2026 &nbsp;|&nbsp; Coimbatore</summary>

<br/>

> ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

- Applied core Java concepts including OOPs, Collections Framework, Exception Handling, and Multithreading to build robust modules.
- Developed and tested Java modules with a focus on debugging, code optimization, and clean architecture.
- Followed Agile practices and used Git for version control, enabling efficient team collaboration.
- Built maintainable and scalable Java applications that adhered to industry coding standards.

</details>

<details>
<summary>📊 <strong>Data Science Intern</strong> — Ether Infotech &nbsp;|&nbsp; May 2025 – June 2025 &nbsp;|&nbsp; Coimbatore</summary>

<br/>

> ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)

- Performed end-to-end data workflows: cleaning, preprocessing, exploratory data analysis, and predictive modeling on real-world datasets.
- Built machine learning models using Python, Pandas, NumPy, and Scikit-learn to extract actionable insights.
- Created visualizations and comprehensive reports that directly supported data-driven business decision-making.
- Enhanced data quality pipelines, improving overall model reliability and reporting accuracy.

</details>

<details>
<summary>🤖 <strong>Machine Learning Intern</strong> — Postulates Info Technology &nbsp;|&nbsp; July 2024 – August 2024 &nbsp;|&nbsp; Coimbatore</summary>

<br/>

> ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)

- Implemented supervised learning algorithms on real-world datasets, from data ingestion through model deployment.
- Performed feature engineering, data preprocessing, and rigorous model evaluation to optimize prediction accuracy.
- Analyzed model performance metrics and iteratively improved results through hyperparameter tuning and cross-validation.
- Gained hands-on exposure to end-to-end AI/ML workflows applicable to production environments.

</details>

---

## 🚀 Featured Projects

<div align="center">

| Project | Stack | Highlights |
|:-------:|:-----:|:----------:|
| [**🗂️ Smart Task Management System**](https://github.com/inbarasanjpcse2023-stack) | React.js · Node.js · Express.js · PostgreSQL · AWS · Render | Full-stack platform with role-based auth, REST APIs, CRUD operations, AWS cloud storage, real-time task tracking & status updates |
| [**💰 AI Finance Tracker**](https://github.com/inbarasanjpcse2023-stack) | Python · NLP · Pandas · Streamlit · SQLite | AI-powered finance tracker with NLP transaction categorization, interactive dashboards, budget recommendations & spending insights |
| [**🌾 Agri Predict**](https://github.com/inbarasanjpcse2023-stack) | Python · Pandas · Scikit-learn · Streamlit · SQL | ML crop recommendation system analyzing soil & environmental parameters; Streamlit UI delivering real-time crop predictions to farmers |
| [**🏥 Medical Insurance Cost Predictor**](https://github.com/inbarasanjpcse2023-stack) | Python · Pandas · NumPy · Scikit-learn | Regression model for insurance cost prediction with EDA, feature engineering, and visual insights for data-driven decisions |
| [**🔧 Mechanic Mate**](https://github.com/inbarasanjpcse2023-stack) | HTML · CSS · JavaScript · MongoDB | Platform connecting vehicle owners with mechanics; includes booking management, mechanic profiles & responsive UI across devices |

</div>

---

## 📜 Certifications

<div align="center">

### 🏢 Industry Simulations & Professional Certifications

<table>
<tr>
<td align="center" width="33%">

**🔵 Deloitte**

[![Deloitte](https://img.shields.io/badge/Deloitte-86BC25?style=for-the-badge&logo=deloitte&logoColor=white)](https://www.theforage.com)

**Data Analytics**
*Job Simulation · Forage*

Data cleaning · EDA · Dashboarding
Statistical analysis · Business insights

</td>
<td align="center" width="33%">

**🟣 Tata Group**

[![Tata](https://img.shields.io/badge/Tata%20Consultancy-0052CC?style=for-the-badge&logo=tata&logoColor=white)](https://www.theforage.com)

**Generative AI + Data Analytics**
*Job Simulation · Forage*

GenAI fundamentals · LLM applications
Data-driven storytelling · AI tools

</td>
<td align="center" width="33%">

**🔴 PwC Switzerland**

[![PwC](https://img.shields.io/badge/PwC-D04A02?style=for-the-badge&logo=pwc&logoColor=white)](https://www.theforage.com)

**Cybersecurity**
*Job Simulation · Forage*

Risk assessment · Threat analysis
Security frameworks · Incident response

</td>
</tr>
</table>

### 🎓 Technical Certifications

| Badge | Certification | Issuer | Domain |
|:-----:|:-------------|:------:|:------:|
| ☁️ | **Azure AI Fundamentals (DP-900)** | Microsoft | AI / Cloud |
| 🤖 | **Generative AI** | Databricks | AI / LLMs |
| 💾 | **Database Management System & SQL** | Infosys Springboard | Backend / DB |
| 🖥️ | **Human Computer Interaction** | NPTEL | UX / Design |
| 📊 | **Business Intelligence** | NPTEL | Analytics |
| 💻 | **C Programming** | PrepInsta | Programming |
| 🧮 | **Data Structures & Algorithms** | PrepInsta | DSA |

</div>

---

## 🏅 Achievements

<div align="center">

| 🏆 | Achievement | Details |
|:--:|:-----------:|:-------:|
| 💻 | **LeetCode Problem Solver** | Solved **170+** DSA problems on LeetCode |
| 🥇 | **LeetCode Contest Rating** | Maximum contest rating of **1429** |
| ⚙️ | **Workflow Automation Builder** | Built **3** workflow automation projects using **n8n** |
| 🧠 | **DSA Expertise** | Proficient in Arrays, Strings, Linked Lists, Trees, Graphs, DP & Recursion |
| ☁️ | **Microsoft Certified** | Azure AI Fundamentals **(DP-900)** |
| 🤖 | **Databricks Certified** | Generative AI certification |
| 🎓 | **NPTEL Certified** | Human Computer Interaction & Business Intelligence |
| 🏛️ | **Infosys Springboard** | Database Management System & SQL |

</div>

---

## 🎓 Education

<div align="center">

| Degree | Institution | Year | Score |
|:------:|:-----------:|:----:|:-----:|
| 🎓 B.E. Computer Science & Engineering | SNS College of Technology, Coimbatore | 2023 – 2027 | CGPA: **7.89** |
| 📘 Higher Secondary Certificate (HSC) | The Suburban Higher Secondary School | 2021 – 2023 | — |
| 📗 SSLC | Elsie Matriculation Higher Secondary School | 2020 – 2021 | — |

</div>

---

## 🌱 Currently Learning

```
🏗️  System Design        →  Scalability, Load Balancing, Caching, Microservices
☕  Spring Boot          →  REST APIs, Spring Security, JPA/Hibernate
🧮  Advanced DSA         →  Segment Trees, Tries, Bit Manipulation, Graph Algorithms
⚙️  n8n Automation       →  Complex Workflow Pipelines, API Integrations, AI Nodes
☁️  Cloud Architecture   →  AWS EC2, S3, Lambda, RDS
```

---

<div align="center">
  <em>"Passionate about learning new technologies and building impactful software solutions."</em>
  <br/><br/>
  <strong>⭐ If you find my work helpful, consider giving a star to my repositories!</strong>
</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&animation=twinkling" width="100%"/>
