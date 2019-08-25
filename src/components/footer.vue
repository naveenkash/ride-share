<template>
  <div class="f-h pad-m footer">
    <div class="container">
      <div class="footer-wrapper">
        <div class="lang">
          <h3>Language</h3>
          <div class="sel-lang">
            <div class="sel-arr">
              <span>English</span>
              <span @click="showLang" id="arrowd">&darr;</span>
            </div>
            <div v-if="showLangOption" class="lang-opt">
              <ul>
                <li>English</li>
                <li>French</li>
                <li>Hindi</li>
              </ul>
            </div>
          </div>
          <h3>Download The App</h3>
        </div>
        <div class="about-us">
          <h3>About Us</h3>
          <ul>
            <li>
              <a href>Support Center</a>
            </li>
            <li>
              <a href>Customer Support</a>
            </li>
            <li>
              <a href>About Us</a>
            </li>
            <li>
              <a href>Copyright</a>
            </li>
            <li>
              <a href>Popular Campaign</a>
            </li>
          </ul>
        </div>
        <div class="our-info">
          <h3>Our Information</h3>
          <ul>
            <li>
              <a href>Return Policy</a>
            </li>
            <li>
              <a href>Privacy Policy</a>
            </li>
            <li>
              <a href>Terms & Conditions</a>
            </li>
            <li>
              <a href>Site Map</a>
            </li>
            <li>
              <a href>Store Hours</a>
            </li>
          </ul>
        </div>
        <div class="my-acc">
          <h3>My Account</h3>
          <ul>
            <li>
              <a href>Press inquiries</a>
            </li>
            <li>
              <a href>Social media directories</a>
            </li>
            <li>
              <a href>Images & B-roll</a>
            </li>
            <li>
              <a href>Permissions</a>
            </li>
            <li>
              <a href>Speaker requests</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="copyright">
        <div class="copy-text">
          <span>Copyright 2018 @Godrive Corporation.</span>
        </div>
        <div class="social">
          <div class="social-link">
            <a href>
              <svg
                fill="currentColor"
                style="display:inline-block;vertical-align:middle"
                height="18"
                width="18"
                viewBox="0 0 512 512"
              >
                <path
                  d="M492,109.5c-17.4,7.7-36,12.9-55.6,15.3c20-12,35.4-31,42.6-53.6c-18.7,11.1-39.4,19.2-61.5,23.5
	C399.8,75.8,374.6,64,346.8,64c-53.5,0-96.8,43.4-96.8,96.9c0,7.6,0.8,15,2.5,22.1c-80.5-4-151.9-42.6-199.6-101.3
	c-8.3,14.3-13.1,31-13.1,48.7c0,33.6,17.2,63.3,43.2,80.7C67,210.7,52,206.3,39,199c0,0.4,0,0.8,0,1.2c0,47,33.4,86.1,77.7,95
	c-8.1,2.2-16.7,3.4-25.5,3.4c-6.2,0-12.3-0.6-18.2-1.8c12.3,38.5,48.1,66.5,90.5,67.3c-33.1,26-74.9,41.5-120.3,41.5
	c-7.8,0-15.5-0.5-23.1-1.4C62.8,432,113.7,448,168.3,448C346.6,448,444,300.3,444,172.2c0-4.2-0.1-8.4-0.3-12.5
	C462.6,146,479,129,492,109.5z"
                />
              </svg>
            </a>
          </div>
          <div class="social-link">
            <a href>
              <svg
                fill="currentColor"
                style="display:inline-block;vertical-align:middle"
                height="18"
                width="18"
                viewBox="0 0 512 512"
              >
                <path
                  d="M288,192v-38.1c0-17.2,3.8-25.9,30.5-25.9H352V64h-55.9c-68.5,0-91.1,31.4-91.1,85.3V192h-45v64h45v192h83V256h56.4l7.6-64
	H288z"
                />
              </svg>
            </a>
          </div>
          <div class="social-link">
            <a href>
              <svg
                fill="currentColor"
                style="display:inline-block;vertical-align:middle"
                height="18"
                width="18"
                viewBox="0 0 512 512"
              >
                <path
                  d="M256,64C150,64,64,150,64,256c0,106.1,86,192,192,192s192-85.9,192-192C448,150,362,64,256,64z M377.9,152.5
	c21.6,25.4,35.3,57.6,37.7,92.9c-34.6-1.8-76-1.8-109.2,1.3c-4.2-10.6-8.5-21-13.2-31C331.5,199.1,361,177.3,377.9,152.5z M256,96
	c38.8,0,74.4,13.8,102.1,36.8c-17.4,22-44.7,41.1-78.7,55.6c-18.6-34.4-40-64-62.8-87.3C229.3,97.9,242.4,96,256,96z M183.6,113.5
	c23.1,23,44.8,52.3,63.8,86.6c-36.1,11-77.5,17.3-121.7,17.3c-8.4,0-16.6-0.3-24.7-0.8C112.5,171.5,143,134.1,183.6,113.5z
	 M96.3,248.4c9.1,0.4,18.3,0.6,27.6,0.5c50.4-0.6,97.3-8.5,137.6-21.4c3.8,7.9,7.4,16,10.8,24.3c-5.5,1.3-10.4,2.7-14.3,4.3
	c-55.1,23.1-98.5,60.4-122,105.5c-24.8-28.2-40-65.1-40-105.6C96,253.4,96.1,250.9,96.3,248.4z M256,416c-37,0-71-12.6-98.1-33.7
	c21.3-42.2,59.3-77.1,107.2-98.8c4.5-2.1,10.5-3.8,17.4-5.3c5.7,15.8,10.8,32.2,15.3,49.2c6.9,26.5,11.8,52.7,14.8,78.1
	C295,412.2,276,416,256,416z M342.5,390.5c-3-25.7-7.9-52.1-14.9-78.9c-3.4-13-7.3-25.6-11.5-37.9c31.4-2.6,69-2.2,98.9,0
	C409.6,322.8,382,365,342.5,390.5z"
                />
              </svg>
            </a>
          </div>
          <div class="social-link">
            <a href>
              <svg
                fill="currentColor"
                style="display:inline-block;vertical-align:middle"
                height="18"
                width="18"
                viewBox="0 0 512 512"
              >
                <path
                  d="M256,32C132.3,32,32,134.9,32,261.7c0,101.5,64.2,187.5,153.2,217.9c1.4,0.3,2.6,0.4,3.8,0.4c8.3,0,11.5-6.1,11.5-11.4
	c0-5.5-0.2-19.9-0.3-39.1c-8.4,1.9-15.9,2.7-22.6,2.7c-43.1,0-52.9-33.5-52.9-33.5c-10.2-26.5-24.9-33.6-24.9-33.6
	c-19.5-13.7-0.1-14.1,1.4-14.1c0.1,0,0.1,0,0.1,0c22.5,2,34.3,23.8,34.3,23.8c11.2,19.6,26.2,25.1,39.6,25.1c10.5,0,20-3.4,25.6-6
	c2-14.8,7.8-24.9,14.2-30.7c-49.7-5.8-102-25.5-102-113.5c0-25.1,8.7-45.6,23-61.6c-2.3-5.8-10-29.2,2.2-60.8c0,0,1.6-0.5,5-0.5
	c8.1,0,26.4,3.1,56.6,24.1c17.9-5.1,37-7.6,56.1-7.7c19,0.1,38.2,2.6,56.1,7.7c30.2-21,48.5-24.1,56.6-24.1c3.4,0,5,0.5,5,0.5
	c12.2,31.6,4.5,55,2.2,60.8c14.3,16.1,23,36.6,23,61.6c0,88.2-52.4,107.6-102.3,113.3c8,7.1,15.2,21.1,15.2,42.5
	c0,30.7-0.3,55.5-0.3,63c0,5.4,3.1,11.5,11.4,11.5c1.2,0,2.6-0.1,4-0.4C415.9,449.2,480,363.1,480,261.7C480,134.9,379.7,32,256,32z
	"
                />
              </svg>
            </a>
          </div>
          <div class="social-link">
            <a href>
              <svg
                fill="currentColor"
                style="display:inline-block;vertical-align:middle"
                height="18"
                width="18"
                viewBox="0 0 512 512"
              >
                <g>
                  <path
                    d="M223.5,82.1c11.8,9.6,36.4,29.7,36.4,68c0,37.3-21.5,54.9-43.1,71.5c-6.7,6.6-14.4,13.6-14.4,24.7
		c0,11.1,7.7,17.2,13.3,21.7l18.5,14.1c22.6,18.6,43.1,35.8,43.1,70.6c0,47.4-46.7,95.2-135,95.2C67.9,448,32,413.2,32,375.9
		c0-18.1,9.2-43.8,39.5-61.5c31.8-19.1,75-21.7,98-23.2c-7.2-9.1-15.4-18.7-15.4-34.3c0-8.6,2.6-13.6,5.1-19.7
		c-5.6,0.5-11.3,1-16.4,1c-54.4,0-85.2-39.8-85.2-79.1c0-23.2,10.8-48.9,32.9-67.5C119.8,68,154.7,64,182.4,64h105.7l-32.8,18.1
		H223.5z M187,305.9c-4.1-0.5-6.7-0.5-11.8-0.5c-4.6,0-32.3,1-53.9,8c-11.3,4-44.1,16.1-44.1,51.9c0,35.8,35.4,61.5,90.3,61.5
		c49.3,0,75.4-23.2,75.4-54.4C242.9,346.7,226,333.1,187,305.9 M201.9,210.1c11.8-11.6,12.8-27.7,12.8-36.8
		c0-36.3-22.1-92.7-64.7-92.7c-13.3,0-27.7,6.5-35.9,16.6c-8.7,10.6-11.3,24.2-11.3,37.3c0,33.8,20,89.7,64.2,89.7
		C179.8,224.3,193.6,218.2,201.9,210.1"
                  >
                    <path
                      d="M223.5,82.1c11.8,9.6,36.4,29.7,36.4,68c0,37.3-21.5,54.9-43.1,71.5c-6.7,6.6-14.4,13.6-14.4,24.7
		c0,11.1,7.7,17.2,13.3,21.7l18.5,14.1c22.6,18.6,43.1,35.8,43.1,70.6c0,47.4-46.7,95.2-135,95.2C67.9,448,32,413.2,32,375.9
		c0-18.1,9.2-43.8,39.5-61.5c31.8-19.1,75-21.7,98-23.2c-7.2-9.1-15.4-18.7-15.4-34.3c0-8.6,2.6-13.6,5.1-19.7
		c-5.6,0.5-11.3,1-16.4,1c-54.4,0-85.2-39.8-85.2-79.1c0-23.2,10.8-48.9,32.9-67.5C119.8,68,154.7,64,182.4,64h105.7l-32.8,18.1
		H223.5z M187,305.9c-4.1-0.5-6.7-0.5-11.8-0.5c-4.6,0-32.3,1-53.9,8c-11.3,4-44.1,16.1-44.1,51.9c0,35.8,35.4,61.5,90.3,61.5
		c49.3,0,75.4-23.2,75.4-54.4C242.9,346.7,226,333.1,187,305.9 M201.9,210.1c11.8-11.6,12.8-27.7,12.8-36.8
		c0-36.3-22.1-92.7-64.7-92.7c-13.3,0-27.7,6.5-35.9,16.6c-8.7,10.6-11.3,24.2-11.3,37.3c0,33.8,20,89.7,64.2,89.7
		C179.8,224.3,193.6,218.2,201.9,210.1"
                    />
                  </path>
                  <polygon
                    points="480,142.3 401.7,142.3 401.7,64.1 384,64.1 384,142.3 304.3,142.3 304.3,160.1 384,160.1 384,241 401.7,241 
		401.7,160.1 480,160.1 	"
                  >
                    <polygon
                      points="480,142.3 401.7,142.3 401.7,64.1 384,64.1 384,142.3 304.3,142.3 304.3,160.1 384,160.1 384,241 401.7,241 
		401.7,160.1 480,160.1 	"
                    />
                  </polygon>
                </g>
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showLangOption: false
    };
  },
  methods: {
    showLang() {
      this.showLangOption = !this.showLangOption;
    }
  }
};
</script>
<style scoped>
.footer {
  background: #232244;
  background-image: url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI1NTQuNjY0IiBoZWlnaHQ9IjYxOSI+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4Mj0iMSIgeTI9IjEiIGdyYWRpZW50VW5pdHM9Im9iamVjdEJvdW5kaW5nQm94Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiMyMTIxNDEiLz48c3RvcCBvZmZzZXQ9Ii4xODQiIHN0b3AtY29sb3I9IiMyMTIxNDEiLz48c3RvcCBvZmZzZXQ9Ii40OTEiIHN0b3AtY29sb3I9IiM4NjczZDYiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNmZmYiLz48L2xpbmVhckdyYWRpZW50PjwvZGVmcz48ZyBkYXRhLW5hbWU9ImxvZ28iPjxnIGRhdGEtbmFtZT0iTGF5ZXIgMSI+PHBhdGggZGF0YS1uYW1lPSImbHQ7UGF0aCZndDsiIGQ9Ik01NTQuNjY0IDI3Ni44MjFWNjE5SDIzMi40YTMxNC41ODMgMzE0LjU4MyAwIDAgMCAyNjQuNy0xNDQuMzA1Yy4yNjEtLjQuNTIyLS43NTUuNzU1LTEuMTM5YTMwMC42NTkgMzAwLjY1OSAwIDAgMCA1MC0xNjYuMDczYzAtOC43NDMtLjM1Ny0xNy4zOS0xLjEzOS0yNS45NHYtLjFxLS4xNTEtMi4zMDYtLjQtNC42MTJjLS4zMjktMy4yOC0uNzE0LTYuNTg4LTEuMjA4LTkuODI3YTE0NC42MSAxNDQuNjEgMCAwIDAtLjUyMi0zLjc2MUgyOTAuOTc1VjM1NC41SDQzNS4wOWEyMTkuMTQ5IDIxOS4xNDkgMCAwIDEtMjAuMyA0NS43NzMgMTkxLjg3OCAxOTEuODc4IDAgMCAxLTMwLjQ4NCA0MC45MjhxLTUuNjU1IDUuODQ3LTExLjc5IDExLjEzMWwtLjI2MS4xOTJhMjIyLjg4NiAyMjIuODg2IDAgMCAxLTY2LjExNCA0MS43MjQgMjE4LjEyMiAyMTguMTIyIDAgMCAxLTQwLjQwNyAxMi4wNzggMjIzLjM3NyAyMjMuMzc3IDAgMCAxLTQzLjEzOCA0LjI0MWMtMy4wMDYgMC02LS4xLTguOTc2LS4yMzNDOTQuMjYxIDUwNS41MjItLjAxNiA0MDcuMzUxIDAgMjg3LjlhMjI4LjgxNiAyMjguODE2IDAgMCAxIDEuMzczLTI0LjI2NkEyNzYuOTYxIDI3Ni45NjEgMCAwIDEgMzMyLjI2MSA1LjM2NmMxMjYuODYyIDI1LjI4MiAyMjIuNDAzIDEzNy4yMSAyMjIuNDAzIDI3MS40NTV6IiBmaWxsPSJ1cmwoI2EpIiBvcGFjaXR5PSIuMDQiLz48L2c+PC9nPjwvc3ZnPg==");
  background-repeat: no-repeat;
  background-position: 100% center;
  border-top: 1px solid rgb(112, 112, 112);
  overflow: hidden;
}
.footer-wrapper {
  width: 100%;
  height: auto;
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr 1fr;
  padding-bottom: 100px;

  color: white;
}
.footer-wrapper h3 {
  font-size: 18px;
  margin-bottom: 35px;
}
/* .lang h3:nth-child(1){
    margin-bottom: 35px;
} */
.footer-wrapper ul {
  padding: 0;
  margin: 0;
}
.footer-wrapper ul li {
  list-style: none;
  line-height: 35px;
}
.footer-wrapper ul li a {
  text-decoration: none;
  color: white;
  font-size: 13px;
}
.lang span {
  font-size: 15px;
}
.copyright {
  width: 100%;
  height: auto;
  display: flex;
  align-items: center;
}
.copy-text {
  margin-right: auto;
  color: white;
}
.social {
  margin-left: auto;
  display: flex;
  align-items: center;
  padding-right: 100px;
}
.social-link {
  margin-right: 15px;
}
.social-link a {
  text-decoration: none;
  color: white;
  font-size: 10px;
}
.sel-lang {
  margin-bottom: 30px;
  position: relative;
  width: 130px;
  margin-bottom: 70px;
}
.lang-opt {
  position: absolute;
  bottom: -135px;
  left: 0;
  width: 100%;
  background: white;
  color: #232244;
  border-radius: 6px;
  /* padding: 5px; */
}
.lang-opt ul {
  /* padding-left: 10px; */
  border-radius: 6px;
}
.lang-opt ul li:nth-child(1) {
  border-top-left-radius: 6px;
  border-top-right-radius: 6px;
}

.lang-opt ul li:nth-child(3) {
  border-bottom-left-radius: 6px;
  border-bottom-right-radius: 6px;
}
.lang-opt ul li {
  padding: 1px 0;
  padding-left: 10px;
  /* background: #615ceb; */
  /* border-radius: 5px; */
  transition: 0.1s;
}
.lang-opt ul li:hover {
  background: rgb(238, 234, 250);
}
.sel-arr {
  display: flex;
  align-items: center;
}
#arrowd {
  margin-left: 45px;
  /* background: yellow; */
  width: 23px;
  height: 23px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
@media screen and (max-width:900px){
  .social{
    padding-right: 70px;
  }
}
@media screen and (max-width:800px){
  .footer-wrapper{
    grid-column-gap: 10px;
  }
  .footer-wrapper h3{
    font-size: 15px;
  }
}
@media screen and (max-width:650px){
  .social{
    padding-right: 40px;
  }
  .footer-wrapper{
    grid-template-columns: 1fr;
  }
}
</style>
