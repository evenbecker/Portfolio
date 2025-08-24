<template>
    <h4 class = "verdanaH">Experiments</h4>
    <div class="myrow">
      <div class="column20">          
            <img id="potion" src="../assets/pictures/potion-art.jpeg" class="logo" alt="potion logo" />                         
      </div>
      <div class="column80">
        <p class="phrasePaddingBlue">In this section, I present some of my front-end experiments. I have made these little projects to improve my coding skills in various professional use cases.</p>
      </div>  
    </div>
    <div class="spacer"></div>
    <img id="startpage" src="../assets/pictures/startpage-logo.png"></img>
    <button class="would" @click="showInfo = !showInfo" style="font-size:20px"><i class="fa fa-info-circle"></i>&nbsp;Would you like to know more?</button>
    <div id="myInfo" v-show="showInfo">
        <p>This program is written in pure JavaScript, no 3rd party libs. I have used the Startpage theme colors. Startpage provides a search engine and an email service called StartMail. It's a safer way to search and browse online without personal data collection, tracking or targeting. Startpage features an anonymous view proxy to mask your identity while browsing other websites. Local cops cannot access StartMail. </p> 
        <p> Edward Snowden remarked that <q>Arguing that you don't care about the right to privacy because you have nothing to hide is no different than saying you don't care about free speech because you have nothing to say.</q></p>
    </div>
   
    <h2>REGISTRATION FORM</h2>
    <div id="myform">
        <p>
            <label for="name">Name:</label>
            <input type="text" id="name" name="Name" placeholder="Enter your full name" />
            <span id="name-error" class="error-message"></span>
        </p>
        <p>
            <label for="address">Address:</label>
            <input type="text" id="address" name="Address" placeholder="Enter your address" />
            <span id="address-error" class="error-message"></span>
        </p>
        <p>
            <label for="email">E-mail Address:</label>
            <input type="text" id="email" name="EMail" placeholder="Enter your email" />
            <span id="email-error" class="error-message"></span>
        </p>
        <p>
            <label for="password">Password:</label>
            <input type="password" id="password" name="Password" />
            <span id="password-error" class="error-message"></span>
        </p>
        <p>
            <label for="subject">Select your favorite cheese:</label>
            <select id="subject" name="Subject">
                <option value="">Select Cheese</option>
                <option value="g">Gorgonzola</option>
                <option value="e">Emmental</option>
                <option value="m">Mozzarella</option>
                <option value="c">Comt&eacute;</option>
            </select>
            <span id="subject-error" class="error-message"></span>
        </p>
        <p>
            <label for="comment">Explain briefly your interest for privacy:</label>
            <textarea id="comment" name="Comment" ></textarea>
        </p>
        <p>
            <input type="checkbox" id="agree" name="Agree" />
            <label for="agree">&nbsp;I agree with the privacy policy</label>
            <span id="agree-error" class="error-message"></span>
        </p>
        
            <button class="subm" @click="validateForm()">Submit</button>
            <button class="reset" @click="resetErrors">Reset</button>
            
        
    </div>
    <div class="spacer"></div>
</template>

<script>
/* 
Startpage logo

afficher un calendar pour la date de naissance
faire un v-bind:class pour un dark mode 
github readme: 
*/

export default {    
    data() {
        return {
            showInfo: false
            //isValid : false,
            /*
            name: "Even",
            tasks: [],
            hideCompleted: true,
            newItemText: ""*/
        }
    },
      
        methods: {
             validateForm() {
    const name = document.getElementById("name").value;
    const addr = document.getElementById("address").value;
    const email = document.getElementById("email").value;
    const pass = document.getElementById("password").value;
    const sub = document.getElementById("subject").value;
    const agree = document.getElementById("agree").checked;

    const nameErr = document.getElementById("name-error");
    const addrErr = document.getElementById("address-error");
    const emailErr = document.getElementById("email-error");
    const passErr = document.getElementById("password-error");
    const subErr = document.getElementById("subject-error");
    const agreeErr = document.getElementById("agree-error");

    nameErr.textContent = "";
    addrErr.textContent = "";
    emailErr.textContent = "";
    passErr.textContent = "";
    subErr.textContent = "";
    agreeErr.textContent = "";

    let isValid = true;
    
    if (name === "" || /\d/.test(name)) {
        nameErr.textContent = "Please enter your name properly.";
        isValid = false;
    }

    if (addr === "") {
        addrErr.textContent = "Please enter your address.";
        isValid = false;
    }

    if (email === "" || !email.includes("@") || !email.includes(".")) {
        emailErr.textContent = "Please enter a valid email address.";
        isValid = false;
    }

    if (pass === "" || pass.length < 6) {
        passErr.textContent = "Please enter a password with at least 6 characters.";
        isValid = false;
    }

    if (sub === "") {
        subErr.textContent = "Please select your favorite cheese.";
        isValid = false;
    }

    if (!agree) {
        agreeErr.textContent = "Please agree to the above information.";
        isValid = false;
    }

    if (isValid) {
        alert("Form submitted successfully!");
        return true;
    }
    
    else {
        return false;
    }
},

        resetErrors() {
            document.getElementById("name-error").textContent = "";
            document.getElementById("address-error").textContent = "";
            document.getElementById("email-error").textContent = "";
            document.getElementById("password-error").textContent = "";
            document.getElementById("subject-error").textContent = "";
            document.getElementById("agree-error").textContent = "";

            document.getElementById("name").value = "";
            document.getElementById("address").value = "";
            document.getElementById("email").value = "";
            document.getElementById("password").value = "";                        
        }
    }
};
</script>
<style scoped>

button{
  margin-left: 15px;
  margin-right: 15px;
  margin-top: 8px;
  font-size: 16px;
}
button.subm {
  width: 40%;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button.subm:hover {
  background-color: #45a049;
}
button.reset {
  width: 40%;
  padding: 10px;
  background-color: hsl(43, 62%, 52%);
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button.reset:hover {
  background-color: hsl(43, 62%, 45%);
}
button.would {
  /*width: 40%;*/
  padding: 10px;
  margin-bottom: 30px;
  background-color: white;
  color: hsl(235, 100%, 50%);
  border: none;
  border-radius: 8px;
  cursor: pointer;
  border: 1px solid hsl(235, 100%, 65%);
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
}
button.would:hover {
  background-color: whitesmoke;
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24),0 17px 50px 0 rgba(0,0,0,0.19);
}

/*
button:focus,
button:focus-visible {
  outline: 4px auto -webkit-focus-ring-color;
}
*/
.card {
  padding: 2em;
}
#myInfo{
    max-width: 590px;     
  padding: 20px;
}


#myform {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}
input[type="text"],
input[type="password"]
 {
  width: 100%;
  padding: 10px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-sizing: border-box;
  font-size: 16px;
}
input[type=text]:focus,
input[type=password]:focus,
textarea:focus
 {
  outline: 2px solid hsl(235, 100%, 65%);
  outline-offset: -2px;
}
select {
  width: 100%;
  padding: 10px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-sizing: border-box;
  font-size: 16px;
  background-color: #fff;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}
textarea {
  width: 100%;
  padding: 10px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-sizing: border-box;
  font-size: 16px;
  resize: vertical;
}
input[type="submit"],
input[type="reset"],
input[type="checkbox"] {
  background-color: hsl(235, 100%, 65%);

  color: #fff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
}
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="checkbox"]:hover {
  background-color: hsl(235, 100%, 50%);
}
.error-message {
  color: red;
  font-size: 14px;
  margin-top: 5px;
}
h2 {
  font-size: 1.8em;
  /*line-height: 1.1;*/
  margin-top: 1.0rem;
  margin-bottom: 1.0rem;
  text-align: center;
  color: hsl(235, 100%, 60%);
}
#startpage{
    height: 4rem;
   /* width:auto;*/
}
#potion{
    height: 9rem;
   /* width:auto;*/
}
.myrow {
  display: flex;
  max-width: 730px;
  justify-content: center;
  align-items: center;
}
.column80 {
  flex: 80%;
  /*padding: 5px;*/
  
}
.column20 {
  flex: 20%;
  padding-right: 15px;
  padding-left: 45px;
}
.phrasePaddingBlue{
  
  padding-top: 1rem;
padding-right: 2rem;
padding-bottom: 1rem;
padding-left: 0rem;
  
}
</style>                