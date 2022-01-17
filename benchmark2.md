## Minecraft load time benchmark


---

<p align="center" style="font-size:160%;">
MC total load time:<br>
585.35 sec
<br>
<sup><sub>(
9:45 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[394.07]},%20{label:%20'FML%20stuff:',%20data:%20[191.28]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%203e76ba%2039.61s%20Just%20Enough%20Items;%20386AA7%2019.34s%20Just%20Enough%20Items%20(Plugins);%20386AA7%2034.75s%20Just%20Enough%20Items%20(Ingredient%20Filter);%20518ba8%2028.77s%20Charset;%20516fa8%2020.96s%20Ender%20IO;%20214d9e%2020.11s%20Minecraft%20Forge;%208f304e%2016.01s%20Astral%20Sorcery;%20438f30%2014.06s%20The%20Betweenlands;%20813e81%2010.49s%20OpenComputers;%208c2ccd%207.98s%20Immersive%20Engineering;%208f3087%207.16s%20Forge%20Mod%20Loader;%209d2ccd%206.85s%20Immersive%20Intelligence;%207c813e%206.56s%20Thaumcraft;%206e176a%205.30s%20Unlimited%20Chisel%20Works;%208f6c30%204.71s%20Dynamic%20Surroundings;%205162a8%204.53s%20Applied%20Energistics%202;%20cd922c%204.34s%20NuclearCraft;%206e175e%203.99s%20Recurrent%20Complex;%20306e8f%203.87s%20Custom%20Loading%20Screen;%202c9e21%203.78s%20GregTech;%205161a8%203.64s%20CraftTweaker2;%208f308f%203.38s%20JourneyMap;%20444444%2064.99s%2036%20Other%20mods;%20333333%2057.97s%20206%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%200.93s%2022%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20Charset%20|%200.02|%200.01|%200.78|%200.18|%200.00|%2027.75|%200.02|%200.00;%20Ender%20IO%20|%207.87|%200.02|%202.85|%200.50|%204.03|%204.43|%200.02|%201.24;%20Astral%20Sorcery%20|%200.25|%200.02|%207.58|%202.70|%200.00|%205.44|%200.02|%200.00;%20The%20Betweenlands%20|%200.66|%200.04|%2010.99|%201.87|%200.00|%200.47|%200.02|%200.00;%20OpenComputers%20|%200.26|%200.03|%205.96|%202.44|%201.76|%200.02|%200.02|%200.00;%20Immersive%20Engineering%20|%201.01|%200.01|%201.01|%200.94|%200.00|%204.99|%200.02|%200.00;%20Immersive%20Intelligence%20|%201.17|%200.02|%202.04|%200.88|%200.00|%202.72|%200.02|%200.00;%20Thaumcraft%20|%200.84|%200.01|%200.35|%200.43|%200.01|%204.90|%200.02|%200.00;%20Unlimited%20Chisel%20Works%20|%200.05|%200.00|%205.16|%200.05|%200.00|%200.02|%200.02|%200.00;%20Dynamic%20Surroundings%20|%200.21|%200.01|%200.21|%200.14|%200.00|%201.22|%202.93|%200.00;%20Applied%20Energistics%202%20|%200.30|%200.02|%203.10|%200.32|%200.18|%200.59|%200.02|%200.00;%20NuclearCraft%20|%200.20|%200.02|%202.34|%200.43|%200.00|%201.26|%200.02|%200.07%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%204.22:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%202.63:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%202.33:%20cofh.thermalexpansion.plugins.jei.JEIPluginTE;%201.84:%20gregtech.integration.jei.GTJeiPlugin;%201.71:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%201.17:%20mezz.jei.plugins.vanilla.VanillaPlugin;%200.70:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%200.64:%20thebetweenlands.compat.jei.BetweenlandsJEIPlugin;%200.42:%20nc.integration.jei.NCJEI;%200.41:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.33:%20com.codetaylor.mc.athenaeum.integration.jei.PluginDelegate;%200.32:%20epicsquid.roots.integration.jei.JEIRootsPlugin;%200.25:%20mcjty.rftools.compat.jei.RFToolsJeiPlugin;%200.17:%20zmaster587.advancedRocketry.integration.jei.ARPlugin;%200.16:%20teamroots.embers.compat.jei.EmbersJEIPlugin;%202.07:%20Other%2064%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[191.28,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%202.58s%20Loading%20sounds;%20994400%202.66s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2015.06s%20ModelLoader:%20blocks;%20995900%204.35s%20ModelLoader:%20items;%20996300%2013.42s%20ModelLoader:%20baking;%20996D00%2034.65s%20Indexing%20ingredients;%20444444%20118.57s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
