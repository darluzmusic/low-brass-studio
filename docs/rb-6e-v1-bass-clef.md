  <style>
    img {
      height: auto;
      width: 100%;
      display: inline-block;
      margin-bottom: 0.5rem;
    }
    select {
      color: white;
      background-color: gray;
      font-family: arial;
      font-size: 2rem;
      border-radius: 0.5rem;
      height: 4.5rem;
      text-align: left;
      margin: 0.1rem;
    }
    #top {
      margin-bottom: 0.5rem;
      font-family: arial;
      font-size: 3rem;
      color: #75ab9a;
    }
    #tunes {
      display:flex;
      flex-wrap: wrap;
      align-items: center;
      font-family: arial;
      font-size: 3rem;
    }
    #transport {
      display: flex;
      align-items:center;
      flex-wrap: wrap;
    }
    #audioControl {
      display: flex;
      align-items:center;
      margin-right:3rem;
    }
    #nav {
      display: flex;
    }
    .navButton {
      cursor: pointer;
      font-size: 2rem;
      border-radius: 0.5rem;
      background-color: #75ab9a;
      color: white;
      padding: 1rem;
      margin: 0.1rem;
      text-decoration: none;
    }
    .navButton:hover {
      text-decoration:none;
    }
    #pad {
      height: 1440px;
    }
  </style>
<body onload="selectFunction()" style="background-color:white">
      <div id='tunes' >
      <select style="width: 18rem;" id="tuneSelect" onchange="selectFunction()">
<option value="10-10-241" selected>10 African Flower Petite Fleur Africaine</option>
<option value="11-11-241">11 Afro Blue</option>
<option value="12-12-241">12 Afternoon In Paris</option>
<option value="13-13-3">13 Airegin🎵</option>
<option value="14-15-2">14 Água De Beber Water To Drink🎵</option>
<option value="16-16-241">16 Alfie</option>
<option value="17-17-4">17 Alice In Wonderland🎵</option>
<option value="18-18-241">18 All Blues</option>
<option value="19-19-241">19 All By Myself</option>
<option value="20-20-6">20 All Of Me🎵</option>
<option value="21-21-7">21 All Of You🎵</option>
<option value="22-22-8">22 All The Things You Are🎵</option>
<option value="23-23-241">23 Always</option>
<option value="24-25-9">24 Alright Okay You Win🎵</option>
<option value="26-27-241">26 Ana Maria</option>
<option value="28-28-10">28 Angel Eyes🎵</option>
<option value="29-29-11">29 Anthropology🎵</option>
<option value="30-31-241">30 Apple Honey</option>
<option value="32-32-12">32 April In Paris🎵</option>
<option value="33-33-241">33 April Joy</option>
<option value="34-35-241">34 Arise Her Eyes</option>
<option value="36-36-241">36 Armageddon</option>
<option value="37-37-13">37 Au Privave🎵</option>
<option value="38-38-14">38 Autumn In New York🎵</option>
<option value="39-39-15">39 Autumn Leaves🎵</option>
<option value="40-40-241">40 Beautiful Love</option>
<option value="41-41-241">41 Beauty And The Beast</option>
<option value="42-42-16">42 Bessies Blues🎵</option>
<option value="43-43-17">43 Bewitched🎵</option>
<option value="44-44-241">44 Big Nick</option>
<option value="45-45-18">45 Black Coffee🎵</option>
<option value="46-46-241">46 Black Diamond</option>
<option value="47-47-241">47 Black Narcissus</option>
<option value="48-48-241">48 Black Nile</option>
<option value="49-49-19">49 Black Orpheus🎵</option>
<option value="50-50-241">50 Blue Bossa</option>
<option value="51-51-20">51 Blue In Green🎵</option>
<option value="52-52-241">52 Blue Monk</option>
<option value="53-53-21">53 The Blue Room🎵</option>
<option value="54-54-22">54 Blue Train Blue Trane🎵</option>
<option value="55-55-23">55 Blues For Alice🎵</option>
<option value="56-56-24">56 Bluesette🎵</option>
<option value="57-57-25">57 Body And Soul🎵</option>
<option value="58-58-26">58 Boplicity Be Bop Lives🎵</option>
<option value="59-59-27">59 Bright Size Life🎵</option>
<option value="60-60-241">60 Broad Way Blues</option>
<option value="61-61-28">61 Broadway🎵</option>
<option value="62-62-29">62 But Beautiful🎵</option>
<option value="63-63-241">63 Butterfly</option>
<option value="64-64-241">64 Byrd Like</option>
<option value="65-65-241">65 Cest Si Bon</option>
<option value="66-66-31">66 Call Me🎵</option>
<option value="67-67-30">67 Call Me Irresponsible🎵</option>
<option value="68-68-32">68 Cant Help Lovin Dat Man🎵</option>
<option value="69-69-241">69 Central Park West</option>
<option value="70-71-33">70 Captain Marvel🎵</option>
<option value="72-72-34">72 Ceora🎵</option>
<option value="73-73-241">73 Chelsea Bells</option>
<option value="74-75-35">74 Chega De Saudade No More Blues🎵</option>
<option value="76-76-36">76 Chelsea Bridge🎵</option>
<option value="77-77-37">77 Cherokee Indian Love Song🎵</option>
<option value="78-78-38">78 Cherry Pink And Apple Blossom White🎵</option>
<option value="79-79-39">79 A Child Is Born🎵</option>
<option value="80-80-241">80 Chippie</option>
<option value="81-81-40">81 Chitlins Con Carne🎵</option>
<option value="82-82-41">82 Come Sunday🎵</option>
<option value="83-83-241">83 Como En Vietnam</option>
<option value="84-85-42">84 Con Alma🎵</option>
<option value="86-86-43">86 Conception🎵</option>
<option value="87-87-44">87 Confirmation🎵</option>
<option value="88-88-241">88 Contemplation</option>
<option value="89-89-241">89 Coral</option>
<option value="90-90-45">90 Cotton Tail🎵</option>
<option value="91-91-241">91 Could It Be You</option>
<option value="92-92-46">92 Countdown🎵</option>
<option value="93-93-241">93 Crescent</option>
<option value="94-94-241">94 Crystal Silence</option>
<option value="95-95-47">95 D Natural Blues🎵</option>
<option value="96-97-241">96 Daahoud</option>
<option value="98-98-49">98 Dancing On The Ceiling🎵</option>
<option value="99-99-50">99 Darn That Dream🎵</option>
<option value="100-100-241">100 Day Waves</option>
<option value="101-101-241">101 Days And Nights Waiting</option>
<option value="102-102-51">102 Dear Old Stockholm🎵</option>
<option value="103-103-52">103 Dearly Beloved🎵</option>
<option value="104-104-241">104 Dedicated To You</option>
<option value="105-105-54">105 Detour Ahead🎵</option>
<option value="106-107-241">106 Deluge</option>
<option value="108-109-53">108 Desafinado🎵</option>
<option value="110-111-241">110 Desert Air</option>
<option value="112-112-55">112 Dexterity🎵</option>
<option value="113-113-56">113 Dizzy Atmosphere🎵</option>
<option value="114-115-48">114 Django🎵</option>
<option value="116-117-241">116 Doin The Pig</option>
<option value="118-118-241">118 Dolores</option>
<option value="119-119-57">119 Dolphin Dance🎵</option>
<option value="120-120-241">120 Domino Biscuit</option>
<option value="121-121-58">121 Dont Blame Me🎵</option>
<option value="122-122-59">122 Dont Get Around Much Anymore🎵</option>
<option value="123-123-60">123 Donna Lee🎵</option>
<option value="124-124-241">124 Dream A Little Dream Of Me</option>
<option value="125-125-61">125 Dreamsville🎵</option>
<option value="126-126-63">126 Easter Parade🎵</option>
<option value="127-127-64">127 Easy Living🎵</option>
<option value="128-128-65">128 Easy To Love Youd Be So Easy To Love🎵</option>
<option value="129-129-241">129 Ecclusiastics</option>
<option value="130-130-241">130 Eighty One</option>
<option value="131-131-241">131 El Gaucho</option>
<option value="132-132-66">132 Epistrophy🎵</option>
<option value="133-133-67">133 Equinox🎵</option>
<option value="134-134-241">134 Equipoise</option>
<option value="135-135-62">135 E.S.P.🎵</option>
<option value="136-136-241">136 Fall</option>
<option value="137-137-241">137 Falling Grace</option>
<option value="138-138-68">138 Falling In Love With Love🎵</option>
<option value="139-139-241">139 Fee-Fi-Fo-Fum</option>
<option value="140-140-69">140 A Fine Romance🎵</option>
<option value="141-141-1">141 500 Miles High🎵</option>
<option value="142-142-241">142 502 Blues</option>
<option value="143-143-241">143 Follow Your Heart</option>
<option value="144-144-70">144 Footprints🎵</option>
<option value="145-145-71">145 For All We Know🎵</option>
<option value="146-146-72">146 For Heavens Sake🎵</option>
<option value="147-147-73">147 I Love You For Sentimental Reasons🎵</option>
<option value="148-148-241">148 Forest Flower</option>
<option value="149-149-75">149 Four🎵</option>
<option value="150-150-74">150 Four On Six🎵</option>
<option value="151-151-76">151 Freddie Freeloader🎵</option>
<option value="152-152-241">152 Freedom Jazz Dance</option>
<option value="153-153-78">153 Gee Baby Aint I Good To You🎵</option>
<option value="154-155-77">154 Full House🎵</option>
<option value="156-156-241">156 Gemini</option>
<option value="157-157-79">157 Giant Steps🎵</option>
<option value="158-158-80">158 The Girl From Ipanema Garôta De Ipanema🎵</option>
<option value="159-159-241">159 Glorias Step</option>
<option value="160-160-81">160 God Bless The Child🎵</option>
<option value="161-161-241">161 Golden Lady</option>
<option value="162-163-241">162 Good Evening Mr. And Mrs. America</option>
<option value="164-164-241">164 Grand Central</option>
<option value="165-165-241">165 The Green Mountains</option>
<option value="166-166-82">166 Groovin High🎵</option>
<option value="167-167-241">167 Grow Your Own</option>
<option value="168-168-83">168 Guilty🎵</option>
<option value="169-169-84">169 Gypsy In My Soul🎵</option>
<option value="170-171-85">170 Half Nelson🎵</option>
<option value="172-172-86">172 Have You Met Miss Jones🎵</option>
<option value="173-173-241">173 Heaven</option>
<option value="174-174-241">174 Heebie Jeebies</option>
<option value="175-175-88">175 Heres That Rainy Day🎵</option>
<option value="176-177-87">176 Hello Young Lovers🎵</option>
<option value="178-178-89">178 Hot Toddy🎵</option>
<option value="179-179-241">179 House Of Jade</option>
<option value="180-180-90">180 How High The Moon🎵</option>
<option value="181-181-91">181 How Insensitive Insensatez🎵</option>
<option value="182-182-241">182 How My Heart Sings</option>
<option value="183-183-241">183 Hullo Bolinas</option>
<option value="184-184-92">184 I Cant Get Started🎵</option>
<option value="185-185-93">185 I Cant Give You Anything But Love🎵</option>
<option value="186-186-94">186 I Could Write A Book🎵</option>
<option value="187-187-95">187 I Got It Bad And That Aint Good🎵</option>
<option value="188-188-96">188 I Let A Song Go Out Of My Heart🎵</option>
<option value="189-189-97">189 I Love Paris🎵</option>
<option value="190-190-98">190 I Love You🎵</option>
<option value="191-191-99">191 I Mean You🎵</option>
<option value="192-193-100">192 I Remember Clifford🎵</option>
<option value="194-194-241">194 I Should Care</option>
<option value="195-195-241">195 I Wish I Knew How It Would Feel To Be Free</option>
<option value="196-196-101">196 Ill Never Smile Again🎵</option>
<option value="197-197-102">197 Ill Remember April🎵</option>
<option value="198-199-241">198 Im All Smiles</option>
<option value="200-200-103">200 Im Beginning To See The Light🎵</option>
<option value="201-201-241">201 Im Your Pal</option>
<option value="202-203-241">202 Icarus</option>
<option value="204-204-241">204 If You Never Come To Me Inutil Paisagem</option>
<option value="205-205-104">205 Impressions🎵</option>
<option value="206-206-105">206 In A Mellow Tone🎵</option>
<option value="207-207-106">207 In A Sentimental Mood🎵</option>
<option value="208-209-107">208 In The Mood🎵</option>
<option value="210-210-108">210 In The Wee Small Hours Of The Morning🎵</option>
<option value="211-211-241">211 In Your Quiet Place</option>
<option value="212-212-109">212 The Inch Worm🎵</option>
<option value="213-213-241">213 Indian Lady</option>
<option value="214-214-241">214 Inner Urge</option>
<option value="215-215-241">215 Interplay</option>
<option value="216-216-241">216 The Intrepid Fox</option>
<option value="217-217-110">217 Invitation🎵</option>
<option value="218-218-241">218 Iris</option>
<option value="219-219-112">219 Isnt It Romantic🎵</option>
<option value="220-221-111">220 Is You Is Or Is You Aint Ma Baby🎵</option>
<option value="222-222-241">222 Isotope</option>
<option value="223-223-113">223 Israel🎵</option>
<option value="224-224-114">224 It Dont Mean A Thing If It Aint Got That Swing🎵</option>
<option value="225-225-115">225 Its Easy To Remember🎵</option>
<option value="226-226-241">226 Jelly Roll</option>
<option value="227-227-116">227 Jordu🎵</option>
<option value="228-228-241">228 Journey To Recife</option>
<option value="229-229-241">229 Joy Spring</option>
<option value="230-230-117">230 Juju🎵</option>
<option value="231-231-118">231 June In January🎵</option>
<option value="232-233-241">232 Jump Monk</option>
<option value="234-234-119">234 Just One More Chance🎵</option>
<option value="235-235-120">235 Lady Bird🎵</option>
<option value="236-237-241">236 Kelo</option>
<option value="238-238-121">238 Lady Sings The Blues🎵</option>
<option value="239-239-122">239 Lament🎵</option>
<option value="240-240-241">240 Las Vegas Tango</option>
<option value="241-241-123">241 Lazy Bird🎵</option>
<option value="242-242-124">242 Lazy River🎵</option>
<option value="243-243-125">243 Like Someone In Love🎵</option>
<option value="244-244-126">244 Limehouse Blues🎵</option>
<option value="245-245-127">245 Little Boat O Barquinho🎵</option>
<option value="246-247-241">246 Lines And Spaces</option>
<option value="248-249-241">248 Litha</option>
<option value="250-250-128">250 Little Waltz🎵</option>
<option value="251-251-129">251 Long Ago And Far Away🎵</option>
<option value="252-252-241">252 Lonnies Lament</option>
<option value="253-253-241">253 Look To The Sky</option>
<option value="254-254-130">254 Love Is The Sweetest Thing🎵</option>
<option value="255-255-131">255 Lucky Southern🎵</option>
<option value="256-256-132">256 Lullaby Of Birdland🎵</option>
<option value="257-257-241">257 The Magician In You</option>
<option value="258-259-133">258 Lush Life🎵</option>
<option value="260-260-134">260 Mahjong🎵</option>
<option value="261-261-135">261 Maiden Voyage🎵</option>
<option value="262-263-136">262 A Man And A Woman🎵</option>
<option value="264-265-241">264 Man In The Green Shirt</option>
<option value="266-266-137">266 Meditation Meditacao🎵</option>
<option value="267-267-241">267 Memories Of Tomorrow</option>
<option value="268-268-241">268 Michelle</option>
<option value="269-269-241">269 Midnight Mood</option>
<option value="270-271-241">270 Midwestern Nights Dream</option>
<option value="272-272-138">272 Milano🎵</option>
<option value="273-273-241">273 Minority</option>
<option value="274-274-241">274 Miss Ann</option>
<option value="275-275-241">275 Missouri Uncompromised</option>
<option value="276-276-143">276 Mr. P.C.🎵</option>
<option value="277-277-139">277 Misty🎵</option>
<option value="278-278-241">278 Miyako</option>
<option value="279-279-141">279 Mood Indigo🎵</option>
<option value="280-281-140">280 Moments Notice🎵</option>
<option value="282-282-241">282 Moonchild</option>
<option value="283-283-142">283 The Most Beautiful Girl In The World🎵</option>
<option value="284-284-241">284 My Buddy</option>
<option value="285-285-144">285 My Favorite Things🎵</option>
<option value="286-286-145">286 My Foolish Heart🎵</option>
<option value="287-287-146">287 My Funny Valentine🎵</option>
<option value="288-288-147">288 My One And Only Love🎵</option>
<option value="289-289-148">289 My Romance🎵</option>
<option value="290-290-149">290 My Shining Hour🎵</option>
<option value="291-291-150">291 My Ship🎵</option>
<option value="292-292-151">292 My Way🎵</option>
<option value="293-293-152">293 Naima Niema🎵</option>
<option value="294-295-241">294 Mysterious Traveller</option>
<option value="296-296-153">296 Nardis🎵</option>
<option value="297-297-154">297 Nefertiti🎵</option>
<option value="298-298-155">298 Never Will I Marry🎵</option>
<option value="299-299-156">299 Nicas Dream🎵</option>
<option value="300-300-157">300 Night Dreamer🎵</option>
<option value="301-301-158">301 The Night Has A Thousand Eyes🎵</option>
<option value="302-302-159">302 A Night In Tunisia🎵</option>
<option value="303-303-241">303 Nobody Knows You When Youre Down And Out</option>
<option value="304-305-160">304 Night Train🎵</option>
<option value="306-306-241">306 Nostalgia In Times Square</option>
<option value="307-307-161">307 Nuages🎵</option>
<option value="308-308-241">308 The Old Man From The Old Country</option>
<option value="309-309-162">309 Oleo🎵</option>
<option value="310-310-241">310 Oliloqui Valley</option>
<option value="311-311-163">311 Once I Loved Amor Em Paz Love In Peace🎵</option>
<option value="312-312-164">312 Once In Love With Amy🎵</option>
<option value="313-313-241">313 One Finger Snap</option>
<option value="314-314-165">314 One Note Samba Samba De Uma Nota So🎵</option>
<option value="315-315-166">315 Only Trust Your Heart🎵</option>
<option value="316-316-241">316 Orbits</option>
<option value="317-317-167">317 Ornithology🎵</option>
<option value="318-318-168">318 Out Of Nowhere🎵</option>
<option value="319-319-169">319 Paper Doll🎵</option>
<option value="320-320-170">320 Passion Dance🎵</option>
<option value="321-321-241">321 Passion Flower</option>
<option value="322-322-171">322 Peace🎵</option>
<option value="323-323-241">323 Peggys Blue Skylight</option>
<option value="324-324-172">324 Pent Up House🎵</option>
<option value="325-325-241">325 Penthouse Serenade</option>
<option value="326-326-173">326 Peris Scope🎵</option>
<option value="327-327-241">327 Pfrancing</option>
<option value="328-328-241">328 Pinocchio</option>
<option value="329-329-241">329 Pithecanthropus Erectus</option>
<option value="330-330-241">330 Portsmouth Figurations</option>
<option value="331-331-174">331 Prelude To A Kiss🎵</option>
<option value="332-332-241">332 Prince Of Darkness</option>
<option value="333-333-241">333 P.S. I Love You</option>
<option value="334-334-241">334 Pussy Cat Dues</option>
<option value="335-335-175">335 Quiet Nights Of Quiet Stars Corcovado🎵</option>
<option value="336-336-241">336 Quiet Now</option>
<option value="337-337-176">337 Recorda Me🎵</option>
<option value="338-339-177">338 Red Clay🎵</option>
<option value="340-340-241">340 Reflections</option>
<option value="341-341-241">341 Ring Dem Bells</option>
<option value="342-343-241">342 Reincarnation Of A Lovebird</option>
<option value="344-344-178">344 Road Song🎵</option>
<option value="345-345-241">345 Round Midnight</option>
<option value="346-347-179">346 Ruby My Dear🎵</option>
<option value="348-348-241">348 The Saga Of Harrison Crabfeathers</option>
<option value="349-349-180">349 Satin Doll🎵</option>
<option value="350-350-241">350 Scotch And Soda</option>
<option value="351-351-181">351 Scrapple From The Apple🎵</option>
<option value="352-353-241">352 Sea Journey</option>
<option value="354-354-182">354 Seven Come Eleven🎵</option>
<option value="355-355-184">355 Sidewinder🎵</option>
<option value="356-357-241">356 Seven Steps To Heaven</option>
<option value="358-358-241">358 Silver Hollow</option>
<option value="359-359-241">359 Sirabhorn</option>
<option value="360-361-241">360 Skating In Central Park</option>
<option value="362-362-185">362 So Nice Summer Samba🎵</option>
<option value="363-363-187">363 Solar🎵</option>
<option value="364-365-186">364 So What🎵</option>
<option value="366-366-188">366 Solitude🎵</option>
<option value="367-367-189">367 Some Day My Prince Will Come🎵</option>
<option value="368-368-190">368 Some Other Spring🎵</option>
<option value="369-369-192">369 Somebody Loves Me🎵</option>
<option value="370-371-191">370 Some Skunk Funk🎵</option>
<option value="372-372-241">372 Sometime Ago</option>
<option value="373-373-193">373 Song For My Father🎵</option>
<option value="374-375-194">374 The Song Is You🎵</option>
<option value="376-376-195">376 Sophisticated Lady🎵</option>
<option value="377-377-196">377 The Sorcerer🎵</option>
<option value="378-378-197">378 Speak No Evil🎵</option>
<option value="379-379-241">379 The Sphinx</option>
<option value="380-380-241">380 Standing On The Corner</option>
<option value="381-381-241">381 The Star-Crossed Lovers</option>
<option value="382-382-198">382 Stella By Starlight🎵</option>
<option value="383-383-241">383 Steps</option>
<option value="384-384-199">384 Stolen Moments🎵</option>
<option value="385-385-200">385 Stompin At The Savoy🎵</option>
<option value="386-386-241">386 Straight No Chaser</option>
<option value="387-387-202">387 Sugar🎵</option>
<option value="388-389-201">388 A String Of Pearls</option>
<option value="390-391-241">390 Stuff</option>
<option value="392-392-203">392 A Sunday Kind Of Love🎵</option>
<option value="393-393-204">393 The Surrey With The Fringe On Top🎵</option>
<option value="394-394-241">394 Swedish Pastry</option>
<option value="395-395-205">395 Sweet Georgia Bright🎵</option>
<option value="396-396-241">396 Sweet Henry</option>
<option value="397-397-206">397 Take Five🎵</option>
<option value="398-398-207">398 Take The “A” Train🎵</option>
<option value="399-399-208">399 Thanks For The Memory🎵</option>
<option value="400-401-241">400 Tame Thy Pen</option>
<option value="402-403-241">402 Tell Me A Bedtime Story</option>
<option value="404-405-241">404 Thats Amore Thats Love</option>
<option value="406-406-209">406 There Is No Greater Love🎵</option>
<option value="407-407-210">407 There Will Never Be Another You🎵</option>
<option value="408-408-241">408 Therell Be Some Changes Made</option>
<option value="409-409-241">409 They Didnt Believe Me</option>
<option value="410-410-211">410 Think On Me🎵</option>
<option value="411-411-212">411 Thou Swell🎵</option>
<option value="412-412-241">412 Three Flowers</option>
<option value="413-413-213">413 Time Remembered🎵</option>
<option value="414-414-214">414 Tones For Joans Bones🎵</option>
<option value="415-415-215">415 Topsy🎵</option>
<option value="416-416-216">416 Tour De Force🎵</option>
<option value="417-417-241">417 Triste</option>
<option value="418-418-217">418 Tune Up🎵</option>
<option value="419-419-218">419 Turn Out The Stars🎵</option>
<option value="420-420-241">420 Twisted Blues</option>
<option value="421-421-241">421 Unquity Road</option>
<option value="422-423-219">422 Unchain My Heart🎵</option>
<option value="424-424-241">424 Unity Village</option>
<option value="425-425-220">425 Up Jumped Spring🎵</option>
<option value="426-426-241">426 Upper Manhattan Medical Group UMMG</option>
<option value="427-427-241">427 Valse Hot</option>
<option value="428-428-221">428 Very Early🎵</option>
<option value="429-429-241">429 Virgo</option>
<option value="430-430-241">430 Wait Till You See Her</option>
<option value="431-431-223">431 Wave🎵</option>
<option value="432-433-222">432 Waltz For Debby🎵</option>
<option value="434-434-241">434 Well Be Together Again</option>
<option value="435-435-224">435 Well You Neednt Its Over Now🎵</option>
<option value="436-436-225">436 West Coast Blues🎵</option>
<option value="437-437-241">437 What Am I Here For</option>
<option value="438-438-241">438 What Was</option>
<option value="439-439-226">439 When I Fall In Love🎵</option>
<option value="440-440-227">440 When Sunny Gets Blue🎵</option>
<option value="441-441-228">441 When You Wish Upon A Star🎵</option>
<option value="442-442-241">442 Whispering</option>
<option value="443-443-229">443 Windows🎵</option>
<option value="444-445-241">444 Wild Flower</option>
<option value="446-446-241">446 Witch Hunt</option>
<option value="447-447-231">447 Woodchoppers Ball🎵</option>
<option value="448-449-230">448 Wives And Lovers Hey Little Girl🎵</option>
<option value="450-450-232">450 Woodyn You🎵</option>
<option value="451-451-241">451 The World Is Waiting For The Sunrise</option>
<option value="452-452-233">452 Yes And No🎵</option>
<option value="453-453-241">453 Yesterday</option>
<option value="454-454-234">454 Yesterdays🎵</option>
<option value="455-455-235">455 You Are Too Beautiful🎵</option>
<option value="456-457-241">456 You Are The Sunshine Of My Life</option>
<option value="458-458-236">458 You Brought A New Kind Of Love To Me🎵</option>
<option value="459-459-237">459 You Dont Know What Love Is🎵</option>
<option value="460-460-238">460 You Took Advantage Of Me🎵</option>
<option value="461-461-240">461 Young At Heart🎵</option>
<option value="462-462-239">462 Youre Nobody til Somebody Loves You🎵</option>
    </select>
    <span class="navButton" onclick="pagePrevious(); selectFunction();">⬅️</span>
    <span class="navButton" onclick="pageNext(); selectFunction();">➡️</span>
    <span class="navButton" id="fs" onclick="fullScreen();">⛶</span>
      <div id="audio"></div>
    </div>
      <div id="music"></div>
    <script>
    //FULLSCREEN//
    var elem = document.documentElement;  
    function fullScreen () {
    if (!document.fullscreenElement) {
      if (elem.requestFullscreen) {
      elem.requestFullscreen();
      } else if (elem.webkitRequestFullscreen) { /* Safari */
      elem.webkitRequestFullscreen();
      } else if (elem.msRequestFullscreen) { /* IE11 */
      elem.msRequestFullscreen();
      }
      return;
      }
      if (document.exitFullscreen) {
      document.exitFullscreen();
      } else if (document.webkitExitFullscreen) { /* Safari */
      document.webkitExitFullscreen();
      } else if (document.msExitFullscreen) { /* IE11 */
      document.msExitFullscreen();
      }
      }
    //BUTTONS//
    function pagePrevious() {
      var x = 
      document.getElementById("tuneSelect").selectedIndex;
      if (x > 0) {
        document.getElementById("tuneSelect").selectedIndex = x - 1;
      }
      }
    function pageNext() {
      var x = 
      document.getElementById("tuneSelect").selectedIndex;
      var s = 
      document.getElementById("tuneSelect").length;
      if (x < s - 1) {
        document.getElementById("tuneSelect").selectedIndex = x + 1;
      }
      }
    //PLAY//
    function audioPlay(id) {
      var z = document.getElementById(id);
      if (z.paused || z.ended) {
        z.play();
        document.getElementById("transport" + id).innerHTML = "⏸️";
      } else {
        z.pause();
        document.getElementById("transport" + id).innerHTML = "▶️";
      }
      z.onended = function() {
        document.getElementById("transport" + id).innerHTML = "▶️";
      }
      }
    //RESTART//
    function audioRestart(id) {
      var y = document.getElementById(id);   
      y.currentTime=0;
      y.pause();
      document.getElementById("transport" + id).innerHTML = "▶️";
      }
    //PLAYBACKRATE//
    //Needed '' in function call to read as id//
    function audioRate(l,m) {
      var r = document.getElementById(l);
      var v = document.getElementById(m).value;
      r.playbackRate = v;
    }
    //LOOP//
    const dir = "https://rb-6e-v1.s3.us-west-1.amazonaws.com/";
    const img = "bass-clef_Page_";
    const dir_img = `${dir}${img}`;
    function selectFunction() {
      let text_1 = "";
      let text_2 = "";
      var x = document.getElementById("tuneSelect").value;
      const myArray = x.split("-");
      var i = myArray[0];
      var num = myArray[1];
      var lim = myArray[2]
      for (j = myArray[2]; j <= lim; j++)
      {
        if (j < 10) {
        zero = "00";
      } else if (j < 100) {
        zero = "0";
      } else {
        zero = "";
      }
        var rate = "<select id=pbr" + j + " onchange=audioRate(" + j + ",'pbr" + j + "')><option value='0.5' >x0.5</option><option value='0.625' >x0.63</option><option value='0.75'>x0.75</option><option value='0.875'>x0.88</option><option value='1' selected>x1</option></select>";
        var aud = "<audio id=" + j + " preload='none'><source src=" +  dir + zero + j + ".mp3></audio><span class=navButton onclick=audioRestart(" + j + ")>🔃</span>";
        var play = "<span class=navButton id=transport" + j + " onclick=audioPlay(" + j + ")>▶️</span>"
        text_1 += "<div id=transport><div id=audioControl>" + play + aud + rate + "</div><div id=nav>" + "</div></div>";
      }
      for (; i <= num; i++) 
      {
        if (i < 10) {
        zero = "00";
      } else if (i < 100) {
        zero = "0";
      } else {
        zero = "";
      }
      var img = "<img id=tune" + i + " src=" + dir_img + zero + i + ".png>";
        text_2 += "<a href=#tune" + (i - -1) + ">" + img + "</a>";
      }
      document.getElementById("audio").innerHTML = text_1;
      document.getElementById("music").innerHTML = text_2;
    }
    </script>