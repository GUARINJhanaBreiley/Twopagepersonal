<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>About Myself!</title>

<style>
body { 
    margin:0; 
    font-family:Arial; 
    background:#b820ff; 
    color:rgb(71, 9, 90); 
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}
.navbar { 
    display:flex; 
    justify-content:space-between; 
    padding:15px; 
    background:rgb(255, 253, 255); 
}
.navbar a { 
    color: rgb(205, 39, 255); 
    text-decoration:none; 
    margin:0 10px; 
}
.section { 
    padding:50px; 
    text-align:center; 
}
.gallery { 
    display:grid; 
    grid-template-columns:repeat(auto-fit, minmax(150px,1fr)); 
    gap:15px; 
}
.gallery img { 
    width:100%; 
    border-radius:10px; 
}
.footer { 
    background:rgb(255, 255, 255); 
    padding: 20px; 
    text-align:center;
    margin-top: auto;
}
</style>
</head>

<body>

<div class="navbar">
  <div>My Website</div>
  <div>
    <a href="page2.html">Hobbies</a>
  </div>
</div>

<div class="section">
  <h1>About Me</h1>
  <p>Hey, Im Jhana and im 16 years old, going to be 17 in june! Im an artist so i do have some art skills but there's some ups and downs when being as an artist so not everything is always enjoyable, haha. I plan to make my own games in the future, which is why i wanted to persue learning coding! I hope in the future life isn't harder than my life right now lol</p>
</div>

<div class="section">
  <h2>My Pictures</h2>

  <div class="gallery">
    <img src="https://cdn.discordapp.com/attachments/1378128071600635976/1488893041204002997/3e74f549-a9d0-42b2-9748-02c07624648f.jpg?ex=69ce6f33&is=69cd1db3&hm=24d95b824b87ec44187952bf898d7e363792a1c52a55ba42af20f14e6ba419ab" alt="My Photo">
    <img src="https://cdn.discordapp.com/attachments/1378128071600635976/1488893066151592077/4ec4d077-e331-498e-b8be-171f84030797.jpg?ex=69ce6f39&is=69cd1db9&hm=a860a979ef5d32b2af8efc264d129321d8d4d2eda95c35af68bf0bc6ca01e386" alt="My Photo">
  </div>

  <div class="gallery" id="gallery1"></div>
</div>

<footer class="footer">© 2026 Know Me!</footer>

<script>
document.addEventListener("DOMContentLoaded", function(){
  const upload = document.getElementById("upload1");
  const gallery = document.getElementById("gallery1");

  upload.addEventListener("change", function(){
    const file = this.files[0];
    if(file){
      const reader = new FileReader();
      reader.onload = function(e){
        const img = document.createElement("img");
        img.src = e.target.result;
        gallery.appendChild(img);
      }
      reader.readAsDataURL(file);
    }
  });
});
</script>

</body>
</html>
