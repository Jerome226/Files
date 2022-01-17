## Minecraft load time benchmark


---

<p align="center" style="font-size:160%;">
MC total load time:<br>
921.46 sec
<br>
<sup><sub>(
15:21 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[642.63]},%20{label:%20'FML%20stuff:',%20data:%20[278.83]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%203e76ba%20176.06s%20Just%20Enough%20Items;%20386AA7%2033.25s%20Just%20Enough%20Items%20(Plugins);%20518ba8%2034.50s%20Charset;%20438f30%2025.36s%20The%20Betweenlands;%208c2ccd%2021.74s%20Immersive%20Engineering;%20516fa8%2019.89s%20Ender%20IO;%205161a8%2019.23s%20CraftTweaker2;%20214d9e%2018.36s%20Minecraft%20Forge;%208f304e%2018.19s%20Astral%20Sorcery;%205a352c%2016.34s%20Shadowfacts'%20Forgelin;%20306e8f%2012.66s%20Custom%20Loading%20Screen;%209d2ccd%2012.56s%20Immersive%20Intelligence;%207c813e%208.64s%20Thaumcraft;%205162a8%208.06s%20Applied%20Energistics%202;%206e176a%207.51s%20Unlimited%20Chisel%20Works;%20813e81%206.63s%20OpenComputers;%203e8160%206.54s%20The%20Twilight%20Forest;%208f3087%206.31s%20Forge%20Mod%20Loader;%20cd922c%205.92s%20NuclearCraft;%206e175e%205.89s%20Recurrent%20Complex;%20308f7e%205.31s%20Quark:%20RotN%20Edition;%20444444%20110.75s%2047%20Other%20mods;%20333333%2062.29s%20199%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%200.64s%2018%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20Charset%20|%200.03|%200.01|%202.92|%200.34|%200.00|%2031.18|%200.02|%200.00;%20The%20Betweenlands%20|%201.04|%200.08|%2020.68|%201.78|%200.00|%201.76|%200.02|%200.00;%20Immersive%20Engineering%20|%202.82|%200.03|%2011.40|%201.35|%200.00|%206.12|%200.03|%200.00;%20Ender%20IO%20|%203.02|%200.03|%204.23|%200.74|%204.37|%205.55|%200.02|%201.93;%20CraftTweaker2%20|%203.71|%200.01|%2015.24|%200.03|%200.00|%200.23|%200.02|%200.00;%20Astral%20Sorcery%20|%200.42|%200.02|%2015.03|%201.97|%200.00|%200.73|%200.02|%200.00;%20Shadowfacts'%20Forgelin%20|%2016.21|%200.03|%200.04|%200.02|%200.00|%200.02|%200.02|%200.00;%20Custom%20Loading%20Screen%20|%2012.58|%200.01|%200.02|%200.02|%200.00|%200.02|%200.02|%200.00;%20Immersive%20Intelligence%20|%201.46|%200.04|%206.40|%201.20|%200.00|%203.44|%200.02|%200.00;%20Thaumcraft%20|%201.24|%200.02|%200.89|%200.58|%200.01|%205.87|%200.02|%200.00;%20Applied%20Energistics%202%20|%200.27|%200.03|%204.03|%201.21|%200.16|%202.33|%200.02|%200.00;%20Unlimited%20Chisel%20Works%20|%200.08|%200.00|%207.34|%200.05|%200.00|%200.02|%200.02|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%206.06:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%203.99:%20cofh.thermalexpansion.plugins.jei.JEIPluginTE;%202.93:%20com.buuz135.thaumicjei.ThaumcraftJEIPlugin;%202.75:%20crazypants.enderio.machines.integration.jei.MachinesPlugin;%202.61:%20com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;%202.43:%20nc.integration.jei.NCJEI;%202.29:%20gregtech.integration.jei.GTJeiPlugin;%201.85:%20hellfirepvp.astralsorcery.common.integrations.ModIntegrationJEI;%201.42:%20mezz.jei.plugins.vanilla.VanillaPlugin;%201.01:%20pl.pabilo8.immersiveintelligence.common.compat.jei.JEIHelper;%200.80:%20com.codetaylor.mc.athenaeum.integration.jei.PluginDelegate;%200.48:%20crazypants.enderio.base.integration.jei.JeiPlugin;%200.41:%20thebetweenlands.compat.jei.BetweenlandsJEIPlugin;%200.40:%20mcjty.rftools.compat.jei.RFToolsJeiPlugin;%200.37:%20epicsquid.roots.integration.jei.JEIRootsPlugin;%203.45:%20Other%2064%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[278.83,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%202.69s%20Loading%20sounds;%20994400%202.78s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2020.06s%20ModelLoader:%20blocks;%20995900%2013.78s%20ModelLoader:%20items;%20996300%2013.35s%20ModelLoader:%20baking;%20996D00%20152.33s%20Indexing%20ingredients;%20444444%2073.85s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
