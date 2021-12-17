# General

`mission.gen.ownerid` - creator name
`mission.gen.dec` - array of strings for the description
`mission.gen.nm` - mission name
`mission.gen.num` - max players
`mission.gen.start` - trigger pos

`mission.gen.todhr` - time of day (h)
`mission.gen.todmn` - time of day (m)
`mission.rule.weth` - weather:

`mission.prop` - objects
  `model` - model hash as int
  `loc` - location as obj, with x, y, z
  `vRot` - rotation as obj, with x, y, z
  `head` - heading
  `prpclr` / `prpclc` - prop colour index
  `prplod` - lod distance
  `prpsba` - speed amount for boostpads

`mission.dprop` - dynamic objects
  `model` - model hash as int
  `loc` - location as obj, with x, y, z
  `vRot` - rotation as obj, with x, y, z
  `head` - heading
  `prpdclr` / `prpdclc` - prop colour index
  `prplod` - lod distance
  `prpsba` - speed amount for boostpads

`mission.dhprop` - "fixture removal" - prop hiding, use `CreateModelHideExcludingScriptObjects` to hide
  `mn` - model hash as int
  `pos` - location as obj, with x, y, z

list of props they deem "big" and use radius of 8.0 with:
`"prop_gate_airport_01" , "prop_gate_military_01", "prop_dock_bouy_1", -1761409654,  1836331637, "prop_dock_bouy_2", -1964610140,  2027407751, "prop_dock_bouy_3", -1498457916, "prop_dock_bouy_5", "h4_prop_office_desk_01"`
(dont ask about the mix of numbers and strings, theyre copied from the scripts so blame r*)
note that this doesnt actually remove *all* things that are hidden in gtao, this is due to some extra native they use which removes these things that isnt usable in fivem.

`mission.unit` handles vehicle/ped placement for street races, possibly more (headache to document+research, if you want to try have a go at parsing it, look at decomp scripts)