<script src="https://code.jquery.com/jquery-3.5.1.min.js" integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" crossorigin="anonymous"></script>

<h2 style="text-align:center">Our Team</h2>
<div class="row">
  <div class="column">
    <div class="card">
      <img class="about-img"  src="assets/images/team/merlijn.png" alt="Merlijn Vermeer" style="width:100%">
      <div class="container">
        <h2>Merlijn Vermeer</h2>
        <p class="title">Project Leader</p>
        <p class="quote"></p>
        <p><a href="mailto:merlijn.vermeer@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/marc.jpg" alt="Marc van Bommel" style="width:100%">
      <div class="container">
        <h2>Marc van Bommel</h2>
        <p class="title">Security engineer</p>
        <p class="quote"></p>
        <p><a href="mailto:marc.vanbommel@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>

  <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/rick.png" alt="Rick Theeuwes" style="width:100%">
      <div class="container">
        <h2>Rick Theeuwes</h2>
        <p class="title">Ethical Hacker</p>
        <p class="quote"></p>
        <p><a href="mailto:r.theeuwes@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>
  <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/thomas.png" alt="Thomas van Heel" style="width:100%">
      <div class="container">
        <h2>Thomas van Heel</h2>
        <p class="title">Ethical Hacker</p>
        <p><a href="mailto:t.vanheel@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>
</div>
<div class="row">
    <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/joel.png" alt="Joel Adams" style="width:100%">
      <div class="container">
        <h2>Joël Adams</h2>
        <p class="title">Ethical Hacker</p>
        <p class="quote"></p>
        <p><a href="mailto:j.adams@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>
  <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/hristo.png" alt="Hristo Slavchev" style="width:100%">
      <div class="container">
        <h2>Hristo Slavchev</h2>
        <p class="title">Security engineer</p>
        <p class="quote"></p>
        <p><a href="mailto:h.slavchev@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>
  <div class="column">
    <div class="card">
      <img class="about-img" src="assets/images/team/anouk.png" alt="Anouk Brondijk" style="width:100%">
      <div class="container">
        <h2>Anouk Brondijk</h2>
        <p class="title">Ethical hacker</p>
        <p class="quote"></p>
        <p><a href="mailto:anouk.brondijk@student.fontys.nl" class="button">Contact</a></p>
      </div>
    </div>
  </div>
</div>


<script type="text/javascript">

    function generateRandomPosts()
    {
        $.getJSON("/assets/json/search.json", function(data) {
            console.log("[search.json loaded for random posts]");

            var postsCount = data.length;
            var posts = data;

            var randomIndexUsed = [];
            var counter = 0;
            var numberOfPosts = 7;

            var divRandomPosts = $(".quote");

            while (counter < numberOfPosts)
            {
                var randomIndex = Math.floor(Math.random() * postsCount);

                if (randomIndexUsed.indexOf(randomIndex) == "-1")
                {
                    var postAuthor = posts[randomIndex].author;
                    var postText = posts[randomIndex].text;

                    divRandomPosts.append(postText + " - " + postAuthor);

                    randomIndexUsed.push(randomIndex);

                    counter++;
                }
            }
        });
    }

    $(document).ready(function() {
        generateRandomPosts();
    });

</script>