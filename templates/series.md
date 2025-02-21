<%*
const date = await tp.system.prompt("Enter the date (YYYY-MM-DD)", tp.date.now("YYYY-MM-DD"));
let team1 = await tp.system.prompt("Team 1?");
let team2 = await tp.system.prompt("Team 2?");
let isScrimm = await tp.system.prompt("Is this a scrimm? (y/n)", "n");
team1 = team1.toUpperCase();
team2 = team2.toUpperCase();
isScrimm = team1.toLowerCase();
const title = await tp.system.prompt("Title", `${team1} vs ${team2} | ${date}`);
const filename = `${date}-${team1}-vs-${team2}`.toLowerCase();
await tp.file.rename(filename);
%>---
title: <% title %>
aliases: <% title %>
date: <% date %>
tags:
  - <% team1 %>
  - <% team2 %>
  - <% isScrimm === "y" ? 'scrimm' : '' %>
---



# 📝 Pre-Game Prep  
- **Strategy:**  
- **Enemy Weaknesses:**  
- **Win Condition:**  

---

# 📊 Post-Game Review  
- **Outcome:**  
- **What Worked:**  
- **What Needs Improvement:**  
