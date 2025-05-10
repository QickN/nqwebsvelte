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
  background-color: rgba(0, 0, 0, 0.25);
  border-radius: 24px;
  padding: 2.5rem;
  transform-style: preserve-3d;
  transform: translateZ(0);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  margin: 1rem;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.glass-effect:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

button {
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 0.75em 1.5em;
  font-size: 0.95em;
  font-weight: 500;
  font-family: inherit;
  background-color: var(--color-theme-1);
  cursor: pointer;
  transition: all 0.3s ease;
  color: white;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  margin-top: 1.25rem;
}

button:hover {
  background-color: var(--color-theme-2);
  transform: translateY(-3px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

button:focus,
button:focus-visible {
  outline: 3px solid rgba(255, 255, 255, 0.2);
}

.nickimg {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 50%;
  margin-bottom: 1.5rem;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.25);
  border: 3px solid rgba(255, 255, 255, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.nickimg:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
}

h3 {
  margin-top: 1.75rem;
  margin-bottom: 0.75rem;
  color: var(--color-theme-1);
}
</style>
