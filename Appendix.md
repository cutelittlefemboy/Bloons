## Main properties

- _Damage_ (**d**) is the amount of health a single hit of an attack removes.
    
    Some attacks do additional damage to certain types of bloon, such as:
    
    - _Boss damage_ (**bd**)
        
    - _MOAB-class damage_ (**md**)
        
    - _Ceramic damage_ (**cd**)
        
    - _Fortified damage_ (**fd**)
        
    - _Lead damage_, or _flead damage_
        
    - _Camo damage_
        
    
    Excess damage to blimps does not usually affect the children; exceptions will be indicated with "_penetrates blimps_". Excess damage to bloons usually does carry over to the children, so exceptions are indicated with "_single-layer_".
    
    "Layers" is sometimes used in in-game descriptions to mean damage. This is somewhat misleading, because for example a ceramic has 1 more layer than a rainbow, but it requires 10 damage to remove this layer.
    
- _Projectile count_ (**j**) is the number of projectiles emitted at once. This will be omitted if there is only 1.
    
    The spread of multiple projectiles will be indicated after the projectile count. For example, "8j/360°" means 8 projectiles spread out over 360 degrees.
    
- _Pierce_ (**p**) is the number of different targets a single projectile can hit.
    
    It is possible for pierce to not be an integer, if certain buffs are in effect (call to arms or shinobi tactics). In this case, the largest integer less than it is used, and the fractional part is carried over to the next projectile. For example, with 1.6 pierce, the first projectile would have 1 pierce with 0.6 left over, then 0.6+1.6 = 2.2, so the second projectile would have 2 pierce with 0.2 left over, and so on.
    
    "Popping power" is often used by in-game descriptions to mean pierce. We avoid the term because it is vague.
    
- _Impact_ is similar to pierce, but not affected by a "pierce buff". There is also usually a short cooldown after each impact where the projectile cannot collide with anything.
    
- _Range_ (**r**) is the radius of the targetable area, given in "units". May be a "_blast_" or a "_zone_", which both mean that the attack immediately affects anything in range up to the pierce limit, instead of emitting a projectile.
    
- _Reload time_ (**s**) is the number of seconds between attacks. This is **not** "attack speed", though they are closely linked: _speed = 1 / reload_ and _reload = 1 / speed_.
    
    May be qualified with _passive_, which means that the attack will be used automatically, instead of only when a valid target is in range.
    
    Reload times greater than 0.1s are only accurate to the nearest frame (1/60th of a second). Times less than 0.1s are accurate on average — towers will release multiple projectiles on the same frame as necessary to maintain this average, similar to fractional pierce.
    
    Note that in-game descriptions and patch notes usually use the word "speed" even when they in fact refer to reload time.
    
- Each attack has a [damage type](https://www.reddit.com/aqv9qy), determining which bloons take damage from the attack. Lead popping ability and camo detection can additionally be granted, indicated simply with the words "lead" or "camo". Here is a summary of which bloons can be damaged by which type:
    
    |Type|Black|White|Purple|Lead|Frozen|
    |---|---|---|---|---|---|
    |Normal|✅|✅|✅|✅|✅|
    |Acid|✅|✅|✅|✅|✅|
    |Sharp|✅|✅|✅|||
    |Explosion||✅|✅|✅|✅|
    |Cold|✅||✅|||
    |Glacier|✅||✅||✅|
    |Shatter|✅|✅|✅||✅|
    |Energy|✅|✅|||✅|
    |Plasma|✅|✅||✅|✅|
    |Fire|✅|✅||✅|✅|
    
- Attacks can have special effects other than dealing damage, which may be triggered in one of several ways:
    
    - hitting but not necessarily damaging a target ("on contact")
        
    - damaging a target ("on damage")
        
    - delivering the final hit on a target ("on pop")
        
    - the projectile simply expiring ("on expire")
        
    
    Some common effects:
    
    - removing camo status ("decamo")
        
    - removing regrow status ("degrow")
        
    - removing fortified status ("defort") — this halves (or quarters for lead) the health of a fortified target, rounding down
        
    - creating explosions
        
    - emitting more projectiles
        
    - applying a status (such as glue or burn) to the target
        
- Some attacks can only target certain types of bloon — the most obvious example is not targeting camo bloons, but also some attacks can only see blimps, or cannot see blimps, or all blimps except BAD, etc.
    
- A tower can have any number of attacks, with completely independent values for all of the above stats.
    
- This is not enough to fully describe all attacks! There are many special cases that simply need more words.
    

## Upgrades

Stat modifications from a tower's upgrades are combined and applied to the base stats in the following sequence:

- Multiplicative upgrades are applied first. These are written with a multiplcation symbol: eg "0.8×s" means that the reload time is 80% of what it was at the previous upgrade.
    
- Then, percentage buffs are summed and applied together as a single modifier. For example, if one upgrade says "+10%r" and another says "+15%r", then the overall result is "+25%r", ie the range will be multiplied by 1.25.
    
- Finally additive bonuses are applied. These are indicated with "+", such as "+1p" for 1 extra pierce.
    

These upgrades will additionally all be followed by the new value in brackets, eg "+1d (2d)".

Some tower upgrades reset a stat to a specific value instead of applying any of the above bonuses. In this case, buffs from upgrades earlier in the same path are ignored, while those from crosspaths continue to apply.

In many cases, crosspaths may apply improved or different buffs. These are listed in their own section, on the path with the higher tier.

## Buffs

Towers are also able to receive "buffs" from a variety of sources. Often from other towers, but some towers also affect themselves with their own buff, some monkey knowledges act as buffs rather than upgrades, and some maps have buff effects. Most — but not all — can be identified in-game by an icon displayed above a selected tower.

Unless explicitly stated, buffs from the same "source" (the same upgrade on a different tower), do not stack.

Buffs follow the same application order as upgrades: multiplicative, percentage, additive. However, they apply separately, after all upgrades, instead of being combined with them. For example, a +10% upgrade and a +10% buff means an overall multiplier of 1.1 * 1.1 = 1.21, not 1 + 0.1 + 0.1 = 1.2 as it would be if they were both upgrades or both buffs.

Additional notes:

- If an attack creates any extra effects, they are also affected by damage and pierce buffs that applied to the attack that created them.
    
- If an attack explicitly says 0d, this **can** be buffed. If an attack does not mention damage, it cannot gain any from buffs.