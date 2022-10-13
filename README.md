# NYCPokeRadar Discord Bot
#for personal use only#
<h5>Description</h5>
This discord bot will let you know all pokemon spawn in nyc. This discord bot fetches pokemon spawn data from "https://nycpokemap.com/" and find meta relevent pokemons, after finding all the pokemons it then sends all of them to your discord chat room using discord web hook. 


fetches data from "https://nycpokemap.com/"  ==>> process it ==>> send to discord server using webhook. 

It looks for 3 things,
<ul>
  <li>1st max IV (15,15,15) pokemons,</li>
  <li>2nd pvp IV (eg. GL and UL) pokemons and </li>
  <li>lastly tracks any pokemon that you many not have in your pokedex. </li>
  </ul>
  
<h6>setup and recommendation</h6>
<pre>at 
line 2: const token = "#put your own discord chat room hook here"; </pre> 

<pre>
at
line 101: setInterval(()=>{
line 102   setData()
line 103 },300000)
</pre>
here it is set to run every 5 minutes, you can change it as per you requirement.

also if not necessary then don't use <pre>setIntercal()</pre> insted use a shellscript like:
<pre>
until [true]
do
clear
node index.js
sleep 5m   
done
</pre>
<pre>
at line 67: const msgSend = (m,t,r=0) => {
</pre>
this function is sending every finds individually, you can compose 1 single embed containing upto 15 individual field, but that will not allow every individual pokemon image thumbnail, because embeds can only have 1 Image and 1 Thumbnail

lastly, pvpList.json file is based on "pvpoke.com"s overall rank list for "Greate League" and "Ultra League", and is bound to changes in future, it conrains top 200 pokemons only but it also have all the pokemons that can be evolve into the said pokemon, 
feel free to generate your own list.

