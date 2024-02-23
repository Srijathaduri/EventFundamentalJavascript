# EventFundamentalJavascript
# HTMLCODE
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous" />
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
  </head>
  <body>
    <div class="dark-background text-center">
      <div>
        <img
          src="https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/bulb-go-on-img.png"
          class="bulb-image"
          id="bulbImage"
        />
      </div>
      <div>
        <img
          src="https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/cat-img.png"
          class="cat-image"
          id="catImage"
        />
      </div>
      <div class="d-flex flex-row justify-content-center pt-5">
        <div class="switch-board">
          <h1 class="switch-status" id="switchStatus">Switched On</h1>
          <button class="off-switch" id="offSwitch" onclick="switchOff()">
            OFF
          </button>
          <button class="on-switch" id="onSwitch" onclick="switchOn()">
            ON
          </button>
        </div>
      </div>
    </div>
  </body>
</html>

# CSSCODE

@import url("https://fonts.googleapis.com/css2?family=Bree+Serif&family=Caveat:wght@400;700&family=Lobster&family=Monoton&family=Open+Sans:ital,wght@0,400;0,700;1,400;1,700&family=Playfair+Display+SC:ital,wght@0,400;0,700;1,700&family=Playfair+Display:ital,wght@0,400;0,700;1,700&family=Roboto:ital,wght@0,400;0,700;1,400;1,700&family=Source+Sans+Pro:ital,wght@0,400;0,700;1,700&family=Work+Sans:ital,wght@0,400;0,700;1,700&display=swap");

.dark-background {
  background-color: #0b0b0b;
}
.bulb-image {
  width: 150px;
}
.cat-image {
  width: 300px;
}
.switch-board {
  background-color: #7b8794;
  width: 294px;
  height: 139px;
  border-radius: 12px;
  padding-left: 16px;
  padding-right: 16px;
  padding-top: 32px;
  padding-bottom: 32px;
  margin: 16px;
}
.switch-status {
  color: #ffffff;
  font-family: "Roboto";
  font-size: 24px;
  font-weight: 500;
  margin-bottom: 24px;
}
.on-switch {
  color: #ffffff;
  background-color: #cbd2d9;
  font-family: "Roboto";
  font-size: 24px;
  font-weight: bold;
  width: 99px;
  height: 44px;
  border-radius: 8px;
  margin-left: 16px;
}
.off-switch {
  color: #ffffff;
  background-color: #e12d39;
  font-family: "Roboto";
  font-size: 24px;
  font-weight: bold;
  width: 99px;
  height: 44px;
  border-radius: 8px;
}

# JavaSCRIPTCODE
function switchOff() {
  document.getElementById("bulbImage").src =
    "https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/bulb-go-off-img.png";
  document.getElementById("catImage").src =
    "https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/cat-eyes-img.png";
  document.getElementById("switchStatus").textContent = "Switched Off";
  document.getElementById("onSwitch").style.backgroundColor = "#22c55e";
  document.getElementById("offSwitch").style.backgroundColor = "#cbd2d9";
}

function switchOn() {
  document.getElementById("bulbImage").src =
    "https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/bulb-go-on-img.png";
  document.getElementById("catImage").src =
    "https://d1tgh8fmlzexmh.cloudfront.net/ccbp-dynamic-webapps/cat-img.png";
  document.getElementById("switchStatus").textContent = "Switched On";
  document.getElementById("offSwitch").style.backgroundColor = "#e12d39";
  document.getElementById("onSwitch").style.backgroundColor = "#cbd2d9";
}
