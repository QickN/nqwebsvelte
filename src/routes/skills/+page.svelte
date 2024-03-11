<script>
   import { goto } from "$app/navigation";
   import nick from "$lib/images/nick.png";
</script>

<svelte:head>
   <title>About</title>
   <meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
   <div class="glass-effect">
       <div class="block">
           <div class="content">
               <img src="{nick}" alt='synapse-logo' class="nickimg"/>
               <h3><strong>Im Nick</strong></h3>
               <p>Computer Science BS | GPA 3.52<br/></p>

               <!-- Skills list -->
               <h3>Skills</h3>
               <p>✅ Python<br/>
                  ✅ Java<br/>
                  ✅ C++<br/>
                  ✅ JavaScript<br/>
                  ✅ HTML/CSS<br/>
                  ✅ C#<br/>
                  ✅ C<br/>
                  ✅ Swift<br/>
               </p>

               <!-- Related Coursework -->
               <h3>Related Coursework</h3>
               <p>✅ MAT 243 - Discrete Math Structures<br/>
                  ✅ MAT 265 - Calculus for Engineers I<br/>
                  ✅ MAT 266 - Calculus for Engineers II<br/>
                  ✅ MAT 267 - Calculus for Engineers III<br/>
                  ✅ MAT 343 - Applied Linear Algebra<br/>
                  ✅ CSE 120 - Digital Design Fundamentals<br/>
                  ✅ CSE 230 - Computer Org/Assembly Language Programming<br/>
                  ✅ CSE 240 - Intro to Programming Languages<br/>
                  ✅ CSE 310 - Data Structures and Algorithms<br/>
                  ✅ CSE 330 - Operating Systems<br/>
                  ✅ CSE 340 - Principles of Programming Lang<br/>
                  ✅ CSE 355 - Intro Theoretical Computer Science<br/>
                  ✅ CSE 445 - Distributed Software Development<br/>
                  ✅ IEE 380 - Probability & Stats Engineering Problem Solving<br/>
               </p>
           </div>
       </div>
   </div>
</div>

<style>
.text-column {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
  align-items: start;
  justify-content: center;
  text-align: center;
}


.glass-effect {
  position: relative;
  
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 20px;
  padding: 30px;
  animation: floatAnimation 10s infinite;
  transform-style: preserve-3d;
  transform: translateZ(0);
  box-shadow: 0 2px 30px 10px rgba(0, 0, 0, 0.3);
  margin: 1rem;

  
}

button {
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.6em 1.2em;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  background-color: rgb(53, 118, 248);
  cursor: pointer;
  transition: border-color 0.25s;
  color: white;
}
button:hover {
  border-color: #ffffff;
}
button:focus,
button:focus-visible {
  outline: 4px auto -webkit-focus-ring-color;
}

.nickimg{
   width: 200px;
}
</style>
