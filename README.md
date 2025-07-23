<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Straw Hat Crew Viewer</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #0b0c10;
      color: #fff;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: #FFD700;
    }
    .crew-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 30px;
    }
    .crew-btn {
      background: #1f2833;
      border: 2px solid #66fcf1;
      color: #66fcf1;
      padding: 10px 20px;
      border-radius: 12px;
      cursor: pointer;
      transition: 0.3s;
    }
    .crew-btn:hover {
      background: #45a29e;
      color: #0b0c10;
    }
    .profile {
      margin-top: 30px;
      display: none;
      animation: fadeIn 0.5s;
    }
    .profile img {
      width: 200px;
      border-radius: 12px;
      border: 3px solid #66fcf1;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>

  <h1>☠️ Straw Hat Pirates Profile Viewer</h1>

  <div class="crew-list">
    <button class="crew-btn" onclick="showProfile('luffy')">Luffy</button>
    <button class="crew-btn" onclick="showProfile('zoro')">Zoro</button>
    <button class="crew-btn" onclick="showProfile('nami')">Nami</button>
    <button class="crew-btn" onclick="showProfile('sanji')">Sanji</button>
    <button class="crew-btn" onclick="showProfile('robin')">Robin</button>
  </div>

  <div id="profile" class="profile">
    <h2 id="name"></h2>
    <p id="role"></p>
    <p id="bounty"></p>
    <p id="powers"></p>
    <img id="photo" src="" alt="Crew Photo">
  </div>

  <script>
    const crewData = {
      luffy: {
        name: "Monkey D. Luffy",
        role: "Captain",
        bounty: "₯ 3,000,000,000",
        powers: "Gomu Gomu no Mi (Hito Hito no Mi: Model Nika), Gear 5, Conqueror's Haki",
        photo: "https://static.wikia.nocookie.net/onepiece/images/9/99/Luffy_Gear_5_Anime.png"
      },
      zoro: {
        name: "Roronoa Zoro",
        role: "Swordsman",
        bounty: "₯ 1,111,000,000",
        powers: "Santoryu (Three Sword Style), Advanced Armament Haki",
        photo: "https://static.wikia.nocookie.net/onepiece/images/d/d6/Zoro_Wano_Anime.png"
      },
      nami: {
        name: "Nami",
        role: "Navigator",
        bounty: "₯ 366,000,000",
        powers: "Climatact, Weather Manipulation, Zeus",
        photo: "https://static.wikia.nocookie.net/onepiece/images/f/fd/Nami_Wano_Anime.png"
      },
      sanji: {
        name: "Vinsmoke Sanji",
        role: "Cook",
        bounty: "₯ 1,032,000,000",
        powers: "Black Leg Style, Diable Jambe, Exoskeleton, Sky Walk",
        photo: "https://static.wikia.nocookie.net/onepiece/images/5/59/Sanji_Wano_Anime.png"
      },
      robin: {
        name: "Nico Robin",
        role: "Archaeologist",
        bounty: "₯ 930,000,000",
        powers: "Hana Hana no Mi, Gigantesco Mano, Demonio Fleur",
        photo: "https://static.wikia.nocookie.net/onepiece/images/c/c0/Robin_Post_Wano_Anime.png"
      }
    };

    function showProfile(key) {
      const member = crewData[key];
      document.getElementById("name").textContent = member.name;
      document.getElementById("role").textContent = `Role: ${member.role}`;
      document.getElementById("bounty").textContent = `Bounty: ${member.bounty}`;
      document.getElementById("powers").textContent = `Powers: ${member.powers}`;
      document.getElementById("photo").src = member.photo;
      document.getElementById("profile").style.display = 'block';
    }
  </script>

</body>
</html>
