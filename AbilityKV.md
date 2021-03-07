DOTA2数据驱动文件字段: https://developer.valvesoftware.com/wiki/Dota_2_Workshop_Tools:zh-cn/Scripting:zh-cn/Abilities_Data_Driven:zh-cn
1. BaseClass : `https://moddota.com/abilities/ability-keyvalues#baseclass`
2. AbilityBehavior 
- DOTA_ABILITY_BEHAVIOR - 技能行为实现(目标,范围,被动,开关等等)
- - 这个行为列表有的行为是提示行为`https://moddota.com/abilities/ability-keyvalues#behavior-tooltips`
3. AbilityType 技能类型,默认值为`DOTA_ABILITY_TYPE_BASIC`
- DOTA_ABILITY_TYPE - 技能类型
4. MaxLevel 技能最大等级
5. RequiredLevel : `https://moddota.com/abilities/ability-keyvalues#requiredlevel`
6. LevelsBetweenUpgrades : `https://moddota.com/abilities/ability-keyvalues#levelsbetweenupgrades`
7. AbilityTextureName - 技能图标 size : 128 x 128
- https://github.com/yika-aixi/DotaModNotes#4-%E6%8A%80%E8%83%BD%E5%9B%BE%E6%A0%87
8. CastFilterRejectCaster : https://moddota.com/abilities/ability-keyvalues#reject-self-cast
9. IsCastableWhileHidden : https://moddota.com/abilities/ability-keyvalues#cast-while-hidden
10. Target块: https://moddota.com/abilities/ability-keyvalues#targeting
- Center
- Radius
- Teams - 类型为 `DOTA_UNIT_TARGET_TEAM` : https://moddota.com/abilities/ability-keyvalues#team
- Types - 类型为 `DOTA_UNIT_TARGET` : https://moddota.com/abilities/ability-keyvalues#type
- ExcludeTypes - 排除指定类型,类型为 `DOTA_UNIT_TARGET`
- Flags - 类型为 `DOTA_UNIT_TARGET_FLAG` : https://moddota.com/abilities/ability-keyvalues#flags
- ExcludeFlags - 排除Flag,类型为 `DOTA_UNIT_TARGET_FLAG`
- ScriptSelectPoints 块,用脚本选择 : https://moddota.com/abilities/ability-keyvalues#scriptselectpoints
- - ScriptFile - lua脚本路径(带后缀)
- - Function - 方法名
- - Count - 啥数量? 
- - Radius - 不知道是不是因为版本问题,并没有在这个块中有提示
11. Line : https://moddota.com/abilities/ability-keyvalues#line
- Length - 长度
- Thickness - 宽度
12. MaxTargets - 最大目标数量 : https://moddota.com/abilities/ability-keyvalues#limiting-the-amount-of-targets
13. Random - 最大单位指定后多选择几个随机单位,结合MaxTargets使用 : https://moddota.com/abilities/ability-keyvalues#limiting-the-amount-of-targets
14. AbilityUnitDamageType - 伤害类型,类型为 `DAMAGE_TYPE`


