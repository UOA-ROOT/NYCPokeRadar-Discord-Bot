# NYCPokeRadar
#for personal use only#

fetches data from "https://nycpokemap.com/"  ==>> process it ==>> send to discord server using webhook. 

It looks for 3 things,
<ul>
  <li>1st max IV (15,15,15) pokemons,</li>
  <li>2nd pvp IV (eg. GL and UL) pokemons and </li>
  <li>lastly tracks any pokemon that you many not have in your pokedex. </li>
  </ul>
  
<h6>setup and recommendation</h6>
<pre>at 
line 2: const token = "<your_discord_hook_url>"; #put your own discord chat room hook</pre> 

<pre>
at
line 101: setInterval(()=>{
line 102   setData()
line 103 },300000)
</pre>
here it is set to run every 5 minutes, you can change it as per you requirement.

also if not necessary the dont use <pre>setIntercal()</pre> insted use a shellscript like:
<pre>
until [true]
do
clear
node index.js
sleep 5m   
done
</pre>
