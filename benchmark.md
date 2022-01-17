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
<img src="https://quickchart.io/chart?w=400&h=30&c={
  type: 'horizontalBar',
  data: {
    datasets: [
      {label:      'MODS:', data: [642.63]},
      {label: 'FML stuff:', data: [278.83]}
    ]
  },
  options: {
    scales: {
      xAxes: [{display: false,stacked: true}],
      yAxes: [{display: false,stacked: true}],
    },
    elements: {rectangle: {borderWidth: 2}},
    legend: {display: false,},
    plugins: {datalabels: {color: 'white',formatter: (value, context) =>
      [context.dataset.label, value].join(' ')
    }}
  }
}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={
  type: 'outlabeledPie',
  options: {
    cutoutPercentage: 25,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v,i)=>[
          v.labels[v.dataIndex],' ',
          (v.percent*1000|0)/10,
          String.fromCharCode(37)].join('')
      }
    }
  },
  data: {...
`
3e76ba 176.06s Just Enough Items;
386AA7  33.25s Just Enough Items (Plugins);
518ba8  34.50s Charset;
438f30  25.36s The Betweenlands;
8c2ccd  21.74s Immersive Engineering;
516fa8  19.89s Ender IO;
5161a8  19.23s CraftTweaker2;
214d9e  18.36s Minecraft Forge;
8f304e  18.19s Astral Sorcery;
5a352c  16.34s Shadowfacts' Forgelin;
306e8f  12.66s Custom Loading Screen;
9d2ccd  12.56s Immersive Intelligence;
7c813e   8.64s Thaumcraft;
5162a8   8.06s Applied Energistics 2;
6e176a   7.51s Unlimited Chisel Works;
813e81   6.63s OpenComputers;
3e8160   6.54s The Twilight Forest;
8f3087   6.31s Forge Mod Loader;
cd922c   5.92s NuclearCraft;
6e175e   5.89s Recurrent Complex;
308f7e   5.31s Quark: RotN Edition;
444444 110.75s 47 Other mods;
333333  62.29s 199 'Fast' mods (load 1.0s - 0.1s);
222222   0.64s 18 'Instant' mods (load %3C 0.1s)
`
    .split(';').reduce((a, l) => {
      l.match(/(\w{6}) *(\d*\.\d*)s (.*)/)
      .slice(1).map((a, i) => [[String.fromCharCode(35),a].join(''), parseFloat(a), a][i])
      .forEach((s, i) => 
        [a.datasets[0].backgroundColor, a.datasets[0].data, a.labels][i].push(s)
      );
      return a
    }, {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 1
      }]
    })
  }
}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={
  options: {
    scales: {
      xAxes: [{stacked: true}],
      yAxes: [{stacked: true}],
    },
    plugins: {
      datalabels: {
        anchor: 'end',
        align: 'top',
        color: 'white',
        backgroundColor: 'rgba(46, 140, 171, 0.6)',
        borderColor: 'rgba(41, 168, 194, 1.0)',
        borderWidth: 0.5,
        borderRadius: 3,
        padding: 0,
        font: {size:10},
        formatter: (v,ctx) => 
          ctx.datasetIndex!=ctx.chart.data.datasets.length-1 ? null
            : [((ctx.chart.data.datasets.reduce((a,b)=>a- -b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')
      },
      colorschemes: {
        scheme: 'office.Damask6'
      }
    }
  },
  type: 'bar',
  data: {...(() => {
    let a = { labels: [], datasets: [] };
`
1: Construction;
2: Loading Resources;
3: PreInitialization;
4: Initialization;
5: InterModComms$IMC;
6: PostInitialization;
7: LoadComplete;
8: ModIdMapping
`
    .split(';')
      .map(l => l.match(/\d: (.*)/).slice(1))
      .forEach(([name]) => a.datasets.push({ label: name, data: [] }));
`
                           1      2      3      4      5      6      7      8  ;
Charset                |  0.03|  0.01|  2.92|  0.34|  0.00| 31.18|  0.02|  0.00;
The Betweenlands       |  1.04|  0.08| 20.68|  1.78|  0.00|  1.76|  0.02|  0.00;
Immersive Engineering  |  2.82|  0.03| 11.40|  1.35|  0.00|  6.12|  0.03|  0.00;
Ender IO               |  3.02|  0.03|  4.23|  0.74|  4.37|  5.55|  0.02|  1.93;
CraftTweaker2          |  3.71|  0.01| 15.24|  0.03|  0.00|  0.23|  0.02|  0.00;
Astral Sorcery         |  0.42|  0.02| 15.03|  1.97|  0.00|  0.73|  0.02|  0.00;
Shadowfacts' Forgelin  | 16.21|  0.03|  0.04|  0.02|  0.00|  0.02|  0.02|  0.00;
Custom Loading Screen  | 12.58|  0.01|  0.02|  0.02|  0.00|  0.02|  0.02|  0.00;
Immersive Intelligence |  1.46|  0.04|  6.40|  1.20|  0.00|  3.44|  0.02|  0.00;
Thaumcraft             |  1.24|  0.02|  0.89|  0.58|  0.01|  5.87|  0.02|  0.00;
Applied Energistics 2  |  0.27|  0.03|  4.03|  1.21|  0.16|  2.33|  0.02|  0.00;
Unlimited Chisel Works |  0.08|  0.00|  7.34|  0.05|  0.00|  0.02|  0.02|  0.00
`
    .split(';').slice(1)
      .map(l => l.split('|').map(s => s.trim()))
      .forEach(([name, ...arr], i) => {
        a.labels.push(name);
        arr.forEach((v, j) => a.datasets[j].data[i] = v)
      }); return a
  })()}
}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={
  options: {
    elements: { rectangle: { borderWidth: 1 } },
    legend: false
  },
  type: 'horizontalBar',
    data: {...(() => {
      let a = {
        labels: [], datasets: [{
          backgroundColor: 'rgba(0, 99, 132, 0.5)',
          borderColor: 'rgb(0, 99, 132)',
          data: []
        }]
      };
`
  6.06: li.cil.oc.integration.jei.ModPluginOpenComputers;
  3.99: cofh.thermalexpansion.plugins.jei.JEIPluginTE;
  2.93: com.buuz135.thaumicjei.ThaumcraftJEIPlugin;
  2.75: crazypants.enderio.machines.integration.jei.MachinesPlugin;
  2.61: com.rwtema.extrautils2.crafting.jei.XUJEIPlugin;
  2.43: nc.integration.jei.NCJEI;
  2.29: gregtech.integration.jei.GTJeiPlugin;
  1.85: hellfirepvp.astralsorcery.common.integrations.ModIntegrationJEI;
  1.42: mezz.jei.plugins.vanilla.VanillaPlugin;
  1.01: pl.pabilo8.immersiveintelligence.common.compat.jei.JEIHelper;
  0.80: com.codetaylor.mc.athenaeum.integration.jei.PluginDelegate;
  0.48: crazypants.enderio.base.integration.jei.JeiPlugin;
  0.41: thebetweenlands.compat.jei.BetweenlandsJEIPlugin;
  0.40: mcjty.rftools.compat.jei.RFToolsJeiPlugin;
  0.37: epicsquid.roots.integration.jei.JEIRootsPlugin;
  3.45: Other 64 Plugins
`
        .split(';')
        .map(l => l.split(':'))
        .forEach(([time, name]) => {
          a.labels.push(name);
          a.datasets[0].data.push(time)
        })
        ; return a
    })()
  }
}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={
  options: {
    rotation: Math.PI,
    cutoutPercentage: 55,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v)=>v.labels
      },
      doughnutlabel: {
        labels: [
          {
            text: 'FML stuff:',
            color: 'rgba(128, 128, 128, 0.5)',
            font: {size: 18}
          },
          {
            text: [278.83,'s'].join(''),
            color: 'rgba(128, 128, 128, 1)',
            font: {size: 22}
          }
        ]
      },
    }
  },
  type: 'outlabeledPie',
  data: {...(() => {
    let a = {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 2
      }]
    };
`
993A00   2.69s Loading sounds;
994400   2.78s Loading Resource - SoundHandler;
994F00  20.06s ModelLoader: blocks;
995900  13.78s ModelLoader: items;
996300  13.35s ModelLoader: baking;
996D00 152.33s Indexing ingredients;
444444  73.85s Other
`
    .split(';')
      .map(l => l.match(/(\w{6}) *(\d*\.\d*)s (.*)/))
      .forEach(([, col, time, name]) => {
        a.labels.push([name, ' ', time, 's'].join(''));
        a.datasets[0].data.push(parseFloat(time));
        a.datasets[0].backgroundColor.push([String.fromCharCode(35), col].join(''))
      })
      ; return a
  })()}
}"/>
</p>

<br>
