<template>
  <div>
    <h1 v-show="show">
      Hello Akash
      <span class="smiley" @click="gitAkash()"
        ><i class="fa fa-github" style="font-size: 36px"></i
      ></span>
      <span class="smiley" @click="instaAkash()"
        ><i class="fa fa-instagram" style="font-size: 36px"></i
      ></span>
    </h1>
    <h3 v-show="show" @click="click1()">Software Developer</h3>
    <h1 v-show="!show">
      Hello Krishnan<span class="smiley" @click="gitHari()"
        ><i class="fa fa-github" style="font-size: 36px"></i
      ></span>
      <span class="smiley" @click="instaHari()"
        ><i class="fa fa-instagram" style="font-size: 36px"></i
      ></span>
    </h1>
    <h3 v-show="!show" @click="click2()">Software Destroyer</h3>
    <button @click="display">Change name</button>
    <button @click="toggleTable">
      <span v-show="!table">show table</span>
      <span v-show="table">Hide table</span>
    </button>
    <table v-show="table" class="dataTable">
      <tr>
        <th>ID</th>
        <th>Name</th>
        <th>Role</th>
        <th @click="emailLink()">Email</th>
      </tr>
      <tr v-for="user in users" :key="user.id">
        <td>{{ user.id }}</td>
        <td>{{ user.name }}</td>
        <td>{{ user.role }}</td>
        <td @click="emailLink()">{{ user.email }}</td>
      </tr>
    </table>
    <img
      src="https://gowithcode.com/wp-content/uploads/2021/04/top-programming-languages.jpg"
      usemap="#workmap"
      height="300"
      width="600"
      alt="Workplace"
    />
    <map name="workmap">
      <area
        target=""
        alt="python"
        title="python"
        href="https://www.python.org/"
        coords="24,13,161,45"
        shape="rect"
      />
      <area
        target=""
        alt="ruby"
        title="ruby"
        href="https://www.ruby-lang.org/en/"
        coords="189,7,256,78"
        shape="rect"
      />
      <area
        target=""
        alt="mongodb"
        title="mongodb"
        href="https://www.mongodb.com/"
        coords="282,3,341,95"
        shape="rect"
      />
      <area
        target=""
        alt="css"
        title="css"
        href="https://developer.mozilla.org/en-US/docs/Web/CSS"
        coords="358,10,425,106"
        shape="rect"
      />
      <area
        target=""
        alt="commandline"
        title="commandline"
        href=""
        coords="437,76,450,25,508,26,498,77"
        shape="poly"
      />
      <area
        target=""
        alt="C++"
        title="C++"
        href="https://www.w3schools.com/cpp/"
        coords="521,34,558,12,596,33,596,75,559,99,522,76"
        shape="poly"
      />
      <area
        target=""
        alt="typescript"
        title="typescript"
        href="https://www.typescriptlang.org/"
        coords="6,66,83,140"
        shape="rect"
      />
      <area
        target=""
        alt="html"
        title="html"
        href="https://www.w3schools.com/html/"
        coords="272,194,273,214,278,280,309,288,336,279,341,214,340,193"
        shape="poly"
      />
      <area
        target=""
        alt="javascript"
        title="javascript"
        href="https://www.w3schools.com/js/"
        coords="365,205,368,280,400,290,433,280,437,204"
        shape="poly"
      />
      <area
        target=""
        alt="php"
        title="php"
        href="https://www.php.net/"
        coords="541,235,576,233,495,228,515,210,590,219,599,237,581,258,542,266,500,254,66,227,111,224,136,233,218,233,219,267,131,268,113,273,63,275,244,268"
        shape="poly"
      />
      <area
        target=""
        alt="swift"
        title="swift"
        href="https://developer.apple.com/swift/"
        coords="29,249,73,249,178,259,180,284,77,292,29,293"
        shape="poly"
      />
      <area
        target=""
        alt="csharp"
        title="csharp"
        href="https://www.w3schools.com/cs/index.php"
        coords="11,173,44,153,75,173,78,207,45,229,11,210"
        shape="poly"
      />
      <area
        target=""
        alt="java"
        title="java"
        href="https://www.java.com/en/"
        coords="103,236,108,176,137,135,161,174,157,231,155,231,107,238"
        shape="poly"
      />
      <area
        target=""
        alt="c"
        title="c"
        href="https://www.tutorialspoint.com/cprogramming/index.htm"
        coords="276,126,315,104,345,125,344,161,312,182,276,163"
        shape="poly"
      />
      <area
        target=""
        alt="perl"
        title="perl"
        href="https://www.perl.org/"
        coords="447,178,482,158,557,162,564,168,565,201,461,202,446,192"
        shape="poly"
      />
      <area
        target=""
        alt="R"
        title="R"
        href="https://www.r-project.org/about.html"
        coords="96,79,136,61,173,80,169,114,124,122,98,101"
        shape="poly"
      />
    </map>
  </div>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default {
  name: "Home_1",
  data() {
    return {
      show: true,
      table: true,
      users: [
        {
          id: 1,
          name: "Akash",
          role: "Software Developer",
          email: "wohligakash@gmail.com",
        },
        {
          id: 2,
          name: "krishnan",
          role: "Software Destroyer",
          email: "wohligkrishnan@gmail.com",
        },
      ],
    };
  },
  methods: {
    display() {
      this.show = !this.show;
    },
    toggleTable() {
      this.table = !this.table;
    },
    click() {
      console.log("You have clicked on software developer");
      location.href =
        "https://www.google.com/search?client=firefox-b-d&q=software+developer";
    },
    click2() {
      console.log("You have clicked on software destroyer");
      location.href =
        "https://www.google.com/search?client=firefox-b-d&q=software+destroyer";
    },
    emailLink() {
      console.log("You have clicked on email");
      location.href =
        "https://accounts.google.com/signin/v2/identifier?continue=https%3A%2F%2Fmail.google.com%2Fmail%2F&service=mail&sacu=1&rip=1&flowName=GlifWebSignIn&flowEntry=ServiceLogin";
    },
    gitAkash() {
      console.log("You have clicked on gitAkash");
      location.href = "https://github.com/Akashpawar11";
    },
    gitHari() {
      console.log("You have clicked on gitHari");
      location.href = "https://github.com/harinaidu7";
    },
    instaAkash() {
      console.log("You have clicked on instaAkash");
      location.href = "https://www.instagram.com/akash.k.pawar";
    },
    instaHari() {
      console.log("You have clicked on instaHari");
      location.href = "https://www.instagram.com/hari.naidu77/";
    },
  },
};
</script>
