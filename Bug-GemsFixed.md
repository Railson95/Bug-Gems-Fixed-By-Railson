//	Kryszard's PD2 Loot Filter for Season II: ver 1.1.4
//
//	twitch.tv/kryszard
//
//	For Casual and EndGame Players
//
// 	With Bug Gems Fixed by Railson
//Gold
ItemDisplay[GOLD<100 CLVL<18]:
ItemDisplay[GOLD<1000 (CLVL>17 AND CLVL<80)]:
ItemDisplay[GOLD<5000 CLVL>79]:

//Show me that item is ethereal
ItemDisplay[ETH UNI]: %GRAY%[%WHITE%eth%GRAY%] %GOLD%%NAME%%CONTINUE%
ItemDisplay[ETH RARE]: %GRAY%[%WHITE%eth%GRAY%] %YELLOW%%NAME%%CONTINUE%
ItemDisplay[ETH MAG]: %GRAY%[%WHITE%eth%GRAY%] %BLUE%%NAME%%CONTINUE%
ItemDisplay[ETH NMAG]: %GRAY%[%WHITE%eth%GRAY%] %GRAY%%NAME%%CONTINUE%
ItemDisplay[ETH CRAFT]: %GRAY%[%WHITE%eth%GRAY%] %ORANGE%%NAME%%CONTINUE%

//Show me NMAG SOCK=0 items with white color AND NMAG SOCK>0 with gray
ItemDisplay[(ARMOR OR WEAPON) NMAG SOCK=0]: %WHITE%%NAME%%CONTINUE%
ItemDisplay[(ARMOR OR WEAPON) NMAG SOCK>0]: %GRAY%%NAME%%CONTINUE%

//Show me number of sockets of every socketed item
ItemDisplay[SOCK>0]: %NAME% %TAN%[%WHITE%%SOCKETS%%TAN%]%CONTINUE%

//Show me price of every MAG or RARE weapon/armor after ID
ItemDisplay[(ARMOR OR WEAPON) MAG ID]: %NAME% %GRAY%(%TAN%$%WHITE%%PRICE%%GRAY%)%BLUE%%CONTINUE%
ItemDisplay[(ARMOR OR WEAPON) RARE ID]: %NAME% %GRAY%(%TAN%$%WHITE%%PRICE%%GRAY%)%YELLOW%%CONTINUE%

//Health & Mana Potions
ItemDisplay[rvl]: %PURPLE%R %WHITE%Full
ItemDisplay[rvs]: %PURPLE%r %WHITE%35%
ItemDisplay[hp5]: %RED%!%WHITE%Hp
ItemDisplay[mp5]: %BLUE%!%WHITE%Mp
ItemDisplay[hp1 DIFF=0]: %RED%!%WHITE%minor hp
ItemDisplay[hp2 DIFF=0]: %RED%!%WHITE%light hp
ItemDisplay[hp3 DIFF=0]: %RED%!%WHITE%healing
ItemDisplay[hp4 DIFF<2]: %RED%!%WHITE%great hp
ItemDisplay[mp1 DIFF=0]: %BLUE%!%WHITE%minor mp
ItemDisplay[mp2 DIFF=0]: %BLUE%!%WHITE%light mp
ItemDisplay[mp3 DIFF=0]: %BLUE%!%WHITE%mana
ItemDisplay[mp4 DIFF<2]: %BLUE%!%WHITE%great mp
ItemDisplay[(hp1 OR hp2 OR hp3 OR mp1 OR mp2 OR mp3) DIFF>0]:
ItemDisplay[(hp4 OR mp4) DIFF>1]:

//Utilites
ItemDisplay[tsc CLVL<31]: %BLUE%* %GRAY%tp %WHITE%scroll
ItemDisplay[isc CLVL<31]: %RED%* %GRAY%id %WHITE%scroll
ItemDisplay[vps CLVL<31]: %GREEN%!%WHITE%stamina
ItemDisplay[wms CLVL<31]: %GREEN%!%WHITE%thaw
ItemDisplay[(tsc OR isc OR vps OR wms) CLVL>30]:
ItemDisplay[yps]: %GREEN%!%WHITE%ant
ItemDisplay[key]: %GRAY%key%CONTINUE%

//Arrows & Bolts
ItemDisplay[(aqv OR cqv) NMAG CLVL>6]:

//Choking, Exploding, Fulminating, Oil, Rancid, Strangling
ItemDisplay[(gpm OR opm OR opl OR ops OR gps OR gpl) CLVL>23]:

//Gems
//Bug fixed

//Gems Chipped
ItemDisplay[gcv CLVL<21]:chipped amethyst
ItemDisplay[gcw CLVL<21]:chipped diamond
ItemDisplay[gcg CLVL<21]:chipped emerald
ItemDisplay[gcr CLVL<21]:chipped ruby
ItemDisplay[gcb CLVL<21]:chipped sapphire
ItemDisplay[gcy CLVL<21]:chipped topaz
ItemDisplay[skc CLVL<21]:chipped skull
ItemDisplay[gcv CLVL>20]:
ItemDisplay[gcw CLVL>20]:
ItemDisplay[gcg CLVL>20]:
ItemDisplay[gcr CLVL>20]:
ItemDisplay[gcb CLVL>20]:
ItemDisplay[gcy CLVL>20]:
ItemDisplay[skc CLVL>20]:
//Gems Flawed
ItemDisplay[gfv CLVL<30]:flawed amethyst
ItemDisplay[gfw CLVL<30]:flawed diamond
ItemDisplay[gfg CLVL<30]:flawed emerald
ItemDisplay[gfr CLVL<30]:flawed ruby
ItemDisplay[gfb CLVL<30]:flawed sapphire
ItemDisplay[gfy CLVL<30]:flawed topaz
ItemDisplay[skf CLVL<30]:flawed skull
ItemDisplay[gfv CLVL>29]:
ItemDisplay[gfw CLVL>29]:
ItemDisplay[gfg CLVL>29]:
ItemDisplay[gfr CLVL>29]:
ItemDisplay[gfb CLVL>29]:
ItemDisplay[gfy CLVL>29]:
ItemDisplay[skf CLVL>29]:
//Gems Normal
ItemDisplay[gsv CLVL<51]:amethyst
ItemDisplay[gsw CLVL<51]:diamond
ItemDisplay[gsg CLVL<51]:emerald
ItemDisplay[gsr CLVL<51]:ruby
ItemDisplay[gsb CLVL<51]:sapphire
ItemDisplay[gsy CLVL<51]:topaz
ItemDisplay[sku CLVL<51]:skull
ItemDisplay[gsv CLVL>50]:
ItemDisplay[gsw CLVL>50]:
ItemDisplay[gsg CLVL>50]:
ItemDisplay[gsr CLVL>50]:
ItemDisplay[gsb CLVL>50]:
ItemDisplay[gsy CLVL>50]:
ItemDisplay[sku CLVL>50]:
//Gems flawless
ItemDisplay[gzv OR gzvs]:%PURPLE%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[glw OR glws]:%WHITE%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[glg OR glgs]:%GREEN%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[glr OR glrs]:%RED%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[glb OR glbs]:%BLUE%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[gly OR glys]:%YELLOW%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[skl OR skls]:%GRAY%%NAME%%DOT-0C%%BORDER-4B%
//Gems Perfect
ItemDisplay[gpv OR gpvs]:%PURPLE%*%NL%%PURPLE%P Amethyst%NL%%PURPLE%*%WHITE%
ItemDisplay[gpw OR gpws]:%WHITE%*%NL%%PURPLE%P Diamond%NL%%WHITE%*%WHITE%
ItemDisplay[gpg OR gpgs]:%GREEN%*%NL%%PURPLE%P Emerald%NL%%GREEN%*%WHITE%
ItemDisplay[gpr OR gprs]:%RED%*%NL%%PURPLE%P Ruby%NL%%RED%*%WHITE%
ItemDisplay[gpb OR gpbs]:%BLUE%*%NL%%PURPLE%P Sapphire%NL%%BLUE%*%WHITE%
//ItemDisplay[gpy OR gpys]:%YELLOW%*%NL%%PURPLE%P Topaz%NL%%YELLOW%*%WHITE%
ItemDisplay[gpy OR gpys]:%YELLOW%%NAME%%DOT-0C%%BORDER-4B%
ItemDisplay[skz OR skzs]:%GRAY%*%NL%%PURPLE%P Skull%NL%%GRAY%*%WHITE%

//Runes
ItemDisplay[(RUNE<15 OR RUNE=16 OR RUNE=17) (CLVL>1 AND CLVL<80)]: %PX-62%%ORANGE%%RUNENAME% %GRAY%[%TAN%%RUNENUM%%GRAY%]%CONTINUE%
ItemDisplay[(RUNE<15 OR RUNE=16 OR RUNE=17) (CLVL=1 OR CLVL>79)]: %ORANGE%%RUNENAME% %GRAY%[%TAN%%RUNENUM%%GRAY%]%CONTINUE%
ItemDisplay[RUNE=15 OR RUNE=18 OR RUNE=19]: %PX-62%%TAN%*  %ORANGE%%RUNENAME% Rune %GRAY%[%WHITE%%RUNENUM%%GRAY%]%TAN%  *%CONTINUE%
ItemDisplay[RUNE>19 AND RUNE<26]: %DOT-62%%RED%*     %ORANGE%%RUNENAME% Rune %GRAY%[%RED%%RUNENUM%%GRAY%]%RED%     *%CONTINUE%
ItemDisplay[RUNE>25]: %BORDER-62%%NL%%GREEN%*%PURPLE%*%RED%*          %ORANGE%%RUNENAME% Rune %GRAY%[%GREEN%%RUNENUM%%GRAY%]%RED%          *%PURPLE%*%GREEN%*%CONTINUE%

//All Charms
ItemDisplay[cm2 MAG !ID]: %TAN%*%BLUE% %NAME% %TAN%*
ItemDisplay[(cm1 OR cm3) MAG !ID]: %DOT-9B%%PURPLE%*%BLUE%   %NAME%   %PURPLE%*
ItemDisplay[(cm1 OR cm2 OR cm3) UNI !ID]: %PX-68%%NAME%

//Good Charms
ItemDisplay[cm3 (MAXDMG>6 AND LIFE>0)]: %TAN%Max Dmg %RED%Life %BLUE%Grand Charm 
ItemDisplay[cm3 (MAXDMG>6 AND FRW>0)]: %TAN%Max Dmg %ORANGE%frw %BLUE%Grand Charm 
ItemDisplay[cm3 (MAXDMG>6 AND FHR>0)]: %TAN%Max Dmg %ORANGE%FHR %BLUE%Grand Charm 
ItemDisplay[cm2 (MAXDMG>6 AND DEX>0)]: %TAN%Max Dmg %GREEN%dex %BLUE%Grand Charm 
ItemDisplay[cm2 (MAXDMG>6 AND STR>0)]: %TAN%Max Dmg %DARK_GREEN%str %BLUE%Grand Charm 
ItemDisplay[cm3 MAXDMG>8]: %TAN%Max Dmg %BLUE%Grand Charm 
ItemDisplay[cm3 (RES>7 AND LIFE>0)]: %PURPLE%ALL %WHITE%Res %RED%Life %BLUE%Grand Charm 
ItemDisplay[cm3 (RES>7 AND FRW>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%frw %BLUE%Grand Charm 
ItemDisplay[cm3 (RES>7 AND FHR>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%FHR %BLUE%Grand Charm 
ItemDisplay[cm3 RES>9]: %PURPLE%ALL %WHITE%Res %BLUE%Grand Charm 
ItemDisplay[cm2 (MAXDMG>3 AND LIFE>0)]: %TAN%Max Dmg %RED%Life %BLUE%Large Charm 
ItemDisplay[cm2 (MAXDMG>3 AND DEX>0)]: %TAN%Max Dmg %GREEN%dex %BLUE%Large Charm 
ItemDisplay[cm2 (MAXDMG>3 AND STR>0)]: %TAN%Max Dmg %DARK_GREEN%str %BLUE%Large Charm 
ItemDisplay[cm2 (MAXDMG>3 AND FRW>0)]: %TAN%Max Dmg %ORANGE%frw %BLUE%Large Charm 
ItemDisplay[cm2 (MAXDMG>3 AND FHR>0)]: %TAN%Max Dmg %ORANGE%FHR %BLUE%Large Charm 
ItemDisplay[cm2 MAXDMG>4]: %TAN%Max Dmg %BLUE%Large Charm 
ItemDisplay[cm2 !UNI (RES>4 AND FRW>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%frw %BLUE%Large Charm 
ItemDisplay[cm2 !UNI (RES>4 AND FHR>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%FHR %BLUE%Large Charm 
ItemDisplay[cm2 !UNI ((RES>4 AND LIFE>0) OR (RES>0 AND LIFE>29))]: %PURPLE%ALL %WHITE%Res %RED%Life %BLUE%Large Charm 
ItemDisplay[cm2 !UNI RES>6]: %PURPLE%ALL %WHITE%Res %BLUE%Large Charm 
ItemDisplay[cm2 LIFE>33]: %RED%Life %BLUE%Large Charm 
ItemDisplay[cm1 ((MAXDMG>1 AND LIFE>0) OR (MAXDMG>0 AND LIFE>9))]: %TAN%Max Dmg %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 ((MAXDMG>1 AND MFIND>0) OR (MAXDMG>0 AND MFIND>4))]: %TAN%Max Dmg %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 (MAXDMG>1 AND DEX>0)]: %TAN%Max Dmg %GREEN%dex %BLUE%Small Charm 
ItemDisplay[cm1 (MAXDMG>1 AND STR>0)]: %TAN%Max Dmg %DARK_GREEN%str %BLUE%Small Charm 
ItemDisplay[cm1 (MAXDMG>1 AND FRW>0)]: %TAN%Max Dmg %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 (MAXDMG>1 AND FHR>0)]: %TAN%Max Dmg %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 MAXDMG>1]: %TAN%Max Dmg %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (RES>0 AND LIFE>0)]: %PURPLE%ALL %WHITE%Res %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (RES>0 AND FRW>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (RES>0 AND FHR>0)]: %PURPLE%ALL %WHITE%Res %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (RES>0 AND MFIND>0)]: %PURPLE%ALL %WHITE%Res %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 !UNI RES>0]: %PURPLE%ALL %WHITE%Res %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((FRES>9 AND LIFE>0) OR (FRES>4 AND LIFE>10) OR (FRES>0 AND LIFE>16))]: %RED%Fire %WHITE%Res %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((LRES>9 AND LIFE>0) OR (LRES>4 AND LIFE>10) OR (LRES>0 AND LIFE>16))]: %YELLOW%Light %WHITE%Res %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((CRES>9 AND LIFE>0) OR (CRES>4 AND LIFE>10) OR (CRES>0 AND LIFE>16))]: %BLUE%Cold %WHITE%Res %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((PRES>9 AND LIFE>0) OR (PRES>4 AND LIFE>10) OR (PRES>0 AND LIFE>16))]: %GREEN%Psn %WHITE%Res %RED%Life %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (FRES>4 AND FRW>0)]: %RED%Fire %WHITE%Res %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (LRES>4 AND FRW>0)]: %YELLOW%Light %WHITE%Res %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (CRES>4 AND FRW>0)]: %BLUE%Cold %WHITE%Res %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (PRES>4 AND FRW>0)]: %GREEN%Psn %WHITE%Res %ORANGE%frw %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (FRES>4 AND FHR>0)]: %RED%Fire %WHITE%Res %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (LRES>4 AND FHR>0)]: %YELLOW%Light %WHITE%Res %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (CRES>4 AND FHR>0)]: %BLUE%Cold %WHITE%Res %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 !UNI (PRES>4 AND FHR>0)]: %GREEN%Psn %WHITE%Res %ORANGE%FHR %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((FRES>9 AND MFIND>0) OR (FRES>4 AND MFIND>3) OR (FRES>0 AND MFIND>5))]: %RED%Fire %WHITE%Res %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((LRES>9 AND MFIND>0) OR (LRES>4 AND MFIND>3) OR (LRES>0 AND MFIND>5))]: %YELLOW%Light %WHITE%Res %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((CRES>9 AND MFIND>0) OR (CRES>4 AND MFIND>3) OR (CRES>0 AND MFIND>5))]: %BLUE%Cold %WHITE%Res %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 !UNI ((PRES>9 AND MFIND>0) OR (PRES>4 AND MFIND>3) OR (PRES>0 AND MFIND>5))]: %GREEN%Psn %WHITE%Res %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 !UNI FRES>9]: %RED%Fire %WHITE%Res %BLUE%Small Charm 
ItemDisplay[cm1 !UNI LRES>9]: %YELLOW%Light %WHITE%Res %BLUE%Small Charm 
ItemDisplay[cm1 !UNI CRES>9]: %BLUE%Cold %WHITE%Res %BLUE%Small Charm 
ItemDisplay[cm1 !UNI PRES>9]: %GREEN%Psn %WHITE%Res %BLUE%Small Charm 
ItemDisplay[cm1 MFIND>5]: %GREEN%MF %BLUE%Small Charm 
ItemDisplay[cm1 LIFE>16]: %RED%Life %BLUE%Small Charm 

//Skillers
ItemDisplay[cm3 (TABSK0>0 AND FHR>0)]: %PURPLE%Bow and Crossbow %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK2>0 AND FHR>0)]: %PURPLE%Javelin and Spear %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK1>0 AND FHR>0)]: %PURPLE%Passive and Magic %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK8>0 AND FHR>0)]: %PURPLE%Fire Spells %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK9>0 AND FHR>0)]: %PURPLE%Lightning Spells %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK10>0 AND FHR>0)]: %PURPLE%Cold Spells %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK16>0 AND FHR>0)]: %PURPLE%Curses %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK17>0 AND FHR>0)]: %PURPLE%Poison & Bone Spells %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK18>0 AND FHR>0)]: %GRAY%Nec %PURPLE%Summoning Spells %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK24>0 AND FHR>0)]: %GRAY%Pal %PURPLE%Combat %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK25>0 AND FHR>0)]: %PURPLE%Offensive Auras %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK26>0 AND FHR>0)]: %PURPLE%Defensive Auras %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK32>0 AND FHR>0)]: %GRAY%Barb %PURPLE%Combat %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK33>0 AND FHR>0)]: %GRAY%Barb %PURPLE%Masteries %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK34>0 AND FHR>0)]: %PURPLE%Warcries %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK40>0 AND FHR>0)]: %GRAY%Dru %PURPLE%Summoning %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK41>0 AND FHR>0)]: %PURPLE%Shape Shifting %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK42>0 AND FHR>0)]: %PURPLE%Elemental %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK48>0 AND FHR>0)]: %PURPLE%Traps %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK49>0 AND FHR>0)]: %PURPLE%Shadow Disciplines %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK50>0 AND FHR>0)]: %PURPLE%Martial Arts %TAN%Skiller %WHITE%+ %ORANGE%FHR
ItemDisplay[cm3 (TABSK0>0 AND FRW>0)]: %PURPLE%Bow and Crossbow %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK2>0 AND FRW>0)]: %PURPLE%Javelin and Spear %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK1>0 AND FRW>0)]: %PURPLE%Passive and Magic %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK8>0 AND FRW>0)]: %PURPLE%Fire Spells %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK9>0 AND FRW>0)]: %PURPLE%Lightning Spells %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK10>0 AND FRW>0)]: %PURPLE%Cold Spells %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK16>0 AND FRW>0)]: %PURPLE%Curses %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK17>0 AND FRW>0)]: %PURPLE%Poison & Bone Spells %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK18>0 AND FRW>0)]: %GRAY%Nec %PURPLE%Summoning Spells %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK24>0 AND FRW>0)]: %GRAY%Pal %PURPLE%Combat %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK25>0 AND FRW>0)]: %PURPLE%Offensive Auras %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK26>0 AND FRW>0)]: %PURPLE%Defensive Auras %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK32>0 AND FRW>0)]: %GRAY%Barb %PURPLE%Combat %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK33>0 AND FRW>0)]: %GRAY%Barb %PURPLE%Masteries %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK34>0 AND FRW>0)]: %PURPLE%Warcries %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK40>0 AND FRW>0)]: %GRAY%Dru %PURPLE%Summoning %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK41>0 AND FRW>0)]: %PURPLE%Shape Shifting %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK42>0 AND FRW>0)]: %PURPLE%Elemental %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK48>0 AND FRW>0)]: %PURPLE%Traps %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK49>0 AND FRW>0)]: %PURPLE%Shadow Disciplines %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK50>0 AND FRW>0)]: %PURPLE%Martial Arts %TAN%Skiller %WHITE%+ %ORANGE%frw
ItemDisplay[cm3 (TABSK0>0 AND LIFE>0)]: %PURPLE%Bow and Crossbow %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK2>0 AND LIFE>0)]: %PURPLE%Javelin and Spear %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK1>0 AND LIFE>0)]: %PURPLE%Passive and Magic %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK8>0 AND LIFE>0)]: %PURPLE%Fire Spells %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK9>0 AND LIFE>0)]: %PURPLE%Lightning Spells %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK10>0 AND LIFE>0)]: %PURPLE%Cold Spells %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK16>0 AND LIFE>0)]: %PURPLE%Curses %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK17>0 AND LIFE>0)]: %PURPLE%Poison & Bone Spells %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK18>0 AND LIFE>0)]: %GRAY%Nec %PURPLE%Summoning Spells %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK24>0 AND LIFE>0)]: %GRAY%Pal %PURPLE%Combat %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK25>0 AND LIFE>0)]: %PURPLE%Offensive Auras %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK26>0 AND LIFE>0)]: %PURPLE%Defensive Auras %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK32>0 AND LIFE>0)]: %GRAY%Barb %PURPLE%Combat %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK33>0 AND LIFE>0)]: %GRAY%Barb %PURPLE%Masteries %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK34>0 AND LIFE>0)]: %PURPLE%Warcries %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK40>0 AND LIFE>0)]: %GRAY%Dru %PURPLE%Summoning %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK41>0 AND LIFE>0)]: %PURPLE%Shape Shifting %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK42>0 AND LIFE>0)]: %PURPLE%Elemental %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK48>0 AND LIFE>0)]: %PURPLE%Traps %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK49>0 AND LIFE>0)]: %PURPLE%Shadow Disciplines %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 (TABSK50>0 AND LIFE>0)]: %PURPLE%Martial Arts %TAN%Skiller %WHITE%+ %RED%Life
ItemDisplay[cm3 TABSK0>0]: %PURPLE%Bow and Crossbow %TAN%Skiller
ItemDisplay[cm3 TABSK2>0]: %PURPLE%Javelin and Spear %TAN%Skiller
ItemDisplay[cm3 TABSK1>0]: %PURPLE%Passive and Magic %TAN%Skiller
ItemDisplay[cm3 TABSK8>0]: %PURPLE%Fire Spells %TAN%Skiller
ItemDisplay[cm3 TABSK9>0]: %PURPLE%Lightning Spells %TAN%Skiller
ItemDisplay[cm3 TABSK10>0]: %PURPLE%Cold Spells %TAN%Skiller
ItemDisplay[cm3 TABSK16>0]: %PURPLE%Curses %TAN%Skiller
ItemDisplay[cm3 TABSK17>0]: %PURPLE%Poison & Bone Spells %TAN%Skiller
ItemDisplay[cm3 TABSK18>0]: %GRAY%Nec %PURPLE%Summoning Spells %TAN%Skiller
ItemDisplay[cm3 TABSK24>0]: %GRAY%Pal %PURPLE%Combat %TAN%Skiller
ItemDisplay[cm3 TABSK25>0]: %PURPLE%Offensive Auras %TAN%Skiller
ItemDisplay[cm3 TABSK26>0]: %PURPLE%Defensive Auras %TAN%Skiller
ItemDisplay[cm3 TABSK32>0]: %GRAY%Barb %PURPLE%Combat %TAN%Skiller
ItemDisplay[cm3 TABSK33>0]: %GRAY%Barb %PURPLE%Masteries %TAN%Skiller
ItemDisplay[cm3 TABSK34>0]: %PURPLE%Warcries %TAN%Skiller
ItemDisplay[cm3 TABSK40>0]: %GRAY%Dru %PURPLE%Summoning %TAN%Skiller
ItemDisplay[cm3 TABSK41>0]: %PURPLE%Shape Shifting %TAN%Skiller
ItemDisplay[cm3 TABSK42>0]: %PURPLE%Elemental %TAN%Skiller
ItemDisplay[cm3 TABSK48>0]: %PURPLE%Traps %TAN%Skiller
ItemDisplay[cm3 TABSK49>0]: %PURPLE%Shadow Disciplines %TAN%Skiller
ItemDisplay[cm3 TABSK50>0]: %PURPLE%Martial Arts %TAN%Skiller

//Note abut High-LVL Grand Charms
ItemDisplay[cm3 MAG ID ILVL>90]: %NAME%{%WHITE%Cube with 3xPerf Gem%NL%%TAN%Note%WHITE%: ILVL%ORANGE%91+ %BLUE%Grand Charm%WHITE%, to Reroll:}

//Highlight Good Magic items
ItemDisplay[jew MAG !ID]: %DOT-9A%%TAN%*%WHITE%*   %BLUE%%NAME%%WHITE%   *%TAN%*

//Highlight Good Rare items
ItemDisplay[(jew OR rin OR amu OR EQ7) RARE !ID]: %DOT-A8%%TAN%*%WHITE%*   %YELLOW%%NAME%%WHITE%   *%TAN%*

//GG UNIQUES
ItemDisplay[(rin OR amu OR 6ws OR uar OR ulc OR urn OR uap OR ci3 OR xtb OR uit OR 6lw OR 7gw OR 7gd OR obf OR ulm) UNI !ID]: %BORDER-68%%PURPLE%*%RED%*%ORANGE%*%YELLOW%*     %GOLD%%NAME%     %YELLOW%*%ORANGE%*%RED%*%PURPLE%*%NL%%GREEN%pick me up

//OK UNIQUES
//belts
ItemDisplay[(ztb OR zlb OR zvb OR zhb OR umc) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//armors
ItemDisplay[(xea OR uui OR xth OR xhn OR xtp OR xlt OR upl OR uld OR utu) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//gloves
ItemDisplay[(uvg OR uhg OR umg) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//helmets
ItemDisplay[(xh9 OR usk OR ci2 OR baa OR bac OR dra OR dre OR uhm OR uh9 OR xhm OR drd OR bae) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//boots
ItemDisplay[(lbt OR xhb OR uhb OR tbt OR xvb) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//shields
ItemDisplay[(nee OR pa9 OR nea OR uts OR uow OR xsh OR xow OR pae OR nef) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*
//weapons
ItemDisplay[(7cs OR 7ws OR 7fl OR 7kr OR 7cr OR 7gm OR 9tw OR oba OR ama OR obc OR 7lw OR amf OR 7wh) UNI !ID]: %DOT-68%%YELLOW%*%TAN%*%GRAY%*     %GOLD%%NAME%%GRAY%     *%TAN%*%YELLOW%*

//Rainbow Facet
ItemDisplay[jew UNI !ID]: %BORDER-68%%RED%r%ORANGE%a%YELLOW%in%GREEN%b%BLUE%o%PURPLE%w     %GOLD%%NAME%%PURPLE%     r%BLUE%a%GREEN%in%YELLOW%b%ORANGE%o%RED%w%NL%%GREEN%pick me up

//Good SET parts
ItemDisplay[(amu OR rin OR uar OR ci3 OR 7qr OR uth OR paf) SET !ID]: %MAP-84%%PURPLE%*%RED%*%DARK_GREEN%*%GREEN%*     %NAME%     *%DARK_GREEN%*%RED%*%PURPLE%*

//Uniques and Sets worth notifying
//Armors
ItemDisplay[(chn OR uul OR xng OR xui OR spl OR pac OR xmg OR xsk OR xml OR xlb OR xpl OR xap OR xld OR xrs OR gth OR aar OR BELT OR skp OR xhl OR xrn OR vbt OR xmb OR uvb OR umb OR lgl OR vgl OR mgl OR tgl OR hgl OR xlg OR xvg OR xtg OR xhg OR ush OR upk OR uml OR xts OR xrg OR xuc OR tow OR kit OR gts) UNI !ID]: %PX-68%%NAME%
//Weapons
ItemDisplay[((mau OR 7ls OR 9ls OR 7br OR 7sr OR 7p7 OR 9ba OR 7ga OR 7wa OR 7gi OR 7pa OR 8ls OR 72a OR 7o7 OR 9yw OR 9fc OR 7bw OR 9kr OR amb OR 7sc OR 7mp OR 6sw OR 6l7 OR 8hx OR 8rx OR dgr OR 7dg OR 7bl OR 9ma OR 9wh OR 9gm OR 7s8 OR 7wc OR 9ws OR 6cs OR 7b7 OR 7gs OR 9sb) OR (ELT (WP5 OR WP6)) OR 9bw OR ywn OR 7wb OR 7sp) UNI !ID]: %PX-68%%NAME%
//Sets
ItemDisplay[((ARMOR OR WEAPON) (EXC OR ELT OR ci0 OR ba5) !(9vo OR xcl OR xrn)) SET !ID]: %PX-84%%NAME%

//Highlight all Sets and Uniques for low lvl characters
ItemDisplay[UNI !ID CLVL<80]: %PX-68%%NAME%
ItemDisplay[SET !ID CLVL<80]: %PX-84%%NAME%

//Shop Hunting
ItemDisplay[WEAPON !UNI TABSK34>2]: %NAME%%NL%%RED%***   %GREEN%Warcries Weapon%RED%   ***{%RED%***   %GREEN%Warcries Weapon%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[CL5 !UNI ((TABSK49>1 OR CLSK6>1) AND SK278>1)]: %NAME%%NL%%RED%***   %GREEN%Venom Claws%RED%   ***{%RED%***   %GREEN%Venom Claws%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[CL5 !UNI ((TABSK49>1 OR CLSK6>1) AND SK273>1)]: %NAME%%NL%%RED%***   %GREEN%Mind Blast Claws%RED%   ***{%RED%***   %GREEN%Mind Blast Claws%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[CL5 !UNI (TABSK50>2 OR ((TABSK50>1 OR CLSK6>1) AND (SK280>1 OR SK265>1)))]: %NAME%%NL%%RED%***   %GREEN%Martial Arts Claws%RED%   ***{%RED%***   %GREEN%Martial Arts Claws%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[CL5 !UNI (TABSK48>2 OR ((TABSK48>1 OR CLSK6>1) AND (SK366>1 OR SK276>1 OR SK272>1 OR SK271>1 OR SK262>1)))]: %NAME%%NL%%RED%***   %GREEN%Traps Claws%RED%   ***{%RED%***   %GREEN%Traps Claws%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[EQ4 !UNI (TABSK0>2 OR TABSK2>2 OR TABSK50>2) AND IAS>19]: %NAME%%NL%%RED%***   %GREEN%3sk, 20ias Gloves%RED%   ***{%RED%***   %GREEN%3sk, 20ias Gloves%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[WP13 !UNI ((TABSK24>2 AND SK101>1) OR (TABSK24>1 AND SK101>2) OR (CLSK3>1 AND SK101>2))]: %NAME%%NL%%RED%***   %GREEN%Holy Bolt Scepter%RED%   ***{%RED%***   %GREEN%Holy Bolt Scepter%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[WP13 !UNI ((TABSK24>2 AND SK121>1) OR (TABSK24>1 AND SK121>2) OR (CLSK3>1 AND SK121>2))]: %NAME%%NL%%RED%***   %GREEN%FoH Scepter%RED%   ***{%RED%***   %GREEN%FoH Scepter%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[WP13 !UNI ((TABSK25>2 AND SK118>1) OR (TABSK25>1 AND SK118>2) OR (CLSK3>1 AND SK118>2))]: %NAME%%NL%%RED%***   %GREEN%Holy Shock Scepter%RED%   ***{%RED%***   %GREEN%Holy Shock Scepter%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[STAFF !UNI CHSK54>0]: %NAME%%NL%%RED%***   %GREEN%Teleport Charges%RED%   ***{%RED%***   %GREEN%Teleport Charges%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[WAND !UNI CHSK91>0]: %NAME%%NL%%RED%***   %GREEN%Lower Resist Charges%RED%   ***{%RED%***   %GREEN%Lower Resist Charges%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}
ItemDisplay[WAND !UNI CHSK82>0]: %NAME%%NL%%RED%***   %GREEN%Life Tap Charges%RED%   ***{%RED%***   %GREEN%Life Tap Charges%RED%   ***%NL%%TAN%Note%WHITE%: Notice me, That's me:}

//Circlets
ItemDisplay[EQ7 (MAG OR RARE) !ID]: %NAME%
ItemDisplay[ci3 NMAG !ETH SOCK=0]: %NAME% %YELLOW%[%GRAY%imbue%YELLOW%]{%TAN%Note%WHITE%: You can %YELLOW%imbue %WHITE%it using Charsi quest}

//Rare Gloves, Belts and Boots
ItemDisplay[(GLOVES OR BOOTS OR BELT) RARE !ID]: %NAME%

//Rare ETH weapons
ItemDisplay[WEAPON !(hax OR 9ha OR 7ha OR axe OR 9ax OR 7ax OR clb OR 9cl OR 7cl OR spc OR 9sp OR 7sp OR mac OR 9ma OR 7ma OR mst OR 9mt OR 7mt OR ssd OR 9ss OR 7ss OR scm OR 9sm OR 7sm OR sbr OR 9sb OR 7sb OR flc OR 9fc OR 7fc OR wsd OR 9wd OR 7wd OR dgr OR 9dg OR 7dg OR dir OR 9di OR 7di OR bld OR 9bl OR 7bl OR STAFF OR ktr OR wrb OR axf OR ces OR clw OR btl OR skr OR 9ar OR 9wb OR 9xf) RARE ETH !ID]: %NAME%

//Craftables
ItemDisplay[GLOVES ((EXC OR ELT) !(utg OR uhg)) MAG !ETH !ID]: %GRAY%* %BLUE%%NAME% %GRAY%*
ItemDisplay[WEAPON !(hax OR 9ha OR 7ha OR axe OR 9ax OR 7ax OR clb OR 9cl OR 7cl OR spc OR 9sp OR 7sp OR mac OR 9ma OR 7ma OR mst OR 9mt OR 7mt OR ssd OR 9ss OR 7ss OR scm OR 9sm OR 7sm OR sbr OR 9sb OR 7sb OR flc OR 9fc OR 7fc OR wsd OR 9wd OR 7wd OR dgr OR 9dg OR 7dg OR dir OR 9di OR 7di OR bld OR 9bl OR 7bl OR STAFF OR ktr OR wrb OR axf OR ces OR clw OR btl OR skr OR 9ar OR 9wb OR 9xf) MAG ETH !ID]: %NAME%
ItemDisplay[(bhm OR xh9 OR uh9) MAG !ID]: %NAME%
ItemDisplay[(bsh OR xsh OR ush) MAG !ID]: %NAME%
ItemDisplay[(lwb OR 8lw OR 6lw) MAG !ID]: %NAME%
ItemDisplay[CL3 MAG !ID]: %NAME%
ItemDisplay[GLOVES MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Ort %WHITE%| S: Perf %GREEN%O%ORANGE%, Ral%NL%%WHITE%B: Perf %RED%O%ORANGE%, Nef%WHITE% | C: Perf %PURPLE%O%ORANGE%, Ort%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[BOOTS MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Ral %WHITE%| S: Perf %GREEN%O%ORANGE%, Ort%NL%%WHITE%B: Perf %RED%O%ORANGE%, Eth%WHITE% | C: Perf %PURPLE%O%ORANGE%, Thul%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[BELT MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Tal %WHITE%| S: Perf %GREEN%O%ORANGE%, Tal%NL%%WHITE%B: Perf %RED%O%ORANGE%, Tal%WHITE% | C: Perf %PURPLE%O%ORANGE%, Ith%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[SHIELD MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Eth %WHITE%| S: Perf %GREEN%O%ORANGE%, Nef%NL%%WHITE%B: Perf %RED%O%ORANGE%, Ith%WHITE% | C: Perf %PURPLE%O%ORANGE%, Eth%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[HELM MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Ith %WHITE%| S: Perf %GREEN%O%ORANGE%, Ith%NL%%WHITE%B: Perf %RED%O%ORANGE%, Ral%WHITE% | C: Perf %PURPLE%O%ORANGE%, Nef%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[CHEST MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Nef %WHITE%| S: Perf %GREEN%O%ORANGE%, Eth%NL%%WHITE%B: Perf %RED%O%ORANGE%, Thul%WHITE% | C: Perf %PURPLE%O%ORANGE%, Tal%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[WEAPON !(BOW OR XBOW) MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Tir %WHITE%| S: %GRAY%x/Bows only%NL%%WHITE%B: Perf %RED%O%ORANGE%, Ort%WHITE% | C: Perf %PURPLE%O%ORANGE%, Tir%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[(BOW OR XBOW) MAG ID]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Tir %WHITE%| S: Perf %GREEN%O%ORANGE%, Sol%NL%%WHITE%B: Perf %RED%O%ORANGE%, Ort%WHITE% | C: Perf %PURPLE%O%ORANGE%, Tir%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[amu MAG]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Thul %WHITE%| S: Perf %GREEN%O%ORANGE%, Thul%NL%%WHITE%B: Perf %RED%O%ORANGE%, Amn%WHITE% | C: Perf %PURPLE%O%ORANGE%, Ral%NL%Craft Recipes: %BLUE%Jewel,}
ItemDisplay[rin MAG]: %NAME%{%WHITE%HP: Perf %BLUE%O%ORANGE%, Amn %WHITE%| S: Perf %GREEN%O%ORANGE%, Amn%NL%%WHITE%B: Perf %RED%O%ORANGE%, Sol%WHITE% | C: Perf %PURPLE%O%ORANGE%, Amn%NL%Craft Recipes: %BLUE%Jewel,}

//Class items
ItemDisplay[(SOR OR WAND OR SCEPTER OR STAFF OR DRU OR BAR OR NEC OR (SIN !(NORM OR 9ar OR 9wb OR 9xf))) !ETH NMAG]: %NAME% %GRAY%(%TAN%$%WHITE%%PRICE%%GRAY%)%CONTINUE%
ItemDisplay[(SOR OR WAND OR SCEPTER OR STAFF OR DRU OR BAR OR NEC OR (SIN !(NORM OR 9ar OR 9wb OR 9xf))) ETH NMAG]: %NAME%%CONTINUE%
ItemDisplay[(SOR OR WAND OR (wsp OR 9ws OR 7ws) OR (am5 OR ama OR amf) OR (am2 OR am7 OR amc OR am1 OR am6 OR amb) OR DRU OR BAR OR NEC OR (SIN !(NORM OR 9ar OR 9wb OR 9xf))) (MAG OR RARE) !ID]: %NAME%

//Show me exactly +SKILLS values on NMAG items
//Amazon
ItemDisplay[NMAG !RW (TABSK0>0 OR TABSK2>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW TABSK0=1]: %NAME%%NL%+1 Bow and Crossbow Skills%CONTINUE%
ItemDisplay[NMAG !RW TABSK0=2]: %NAME%%NL%+2 Bow and Crossbow Skills%CONTINUE%
ItemDisplay[NMAG !RW TABSK0=3]: %NAME%%NL%+3 Bow and Crossbow Skills%CONTINUE%
ItemDisplay[NMAG !RW TABSK2=1]: %NAME%%NL%+1 Javelin and Spear Skills%CONTINUE%
ItemDisplay[NMAG !RW TABSK2=2]: %NAME%%NL%+2 Javelin and Spear Skills%CONTINUE%
ItemDisplay[NMAG !RW TABSK2=3]: %NAME%%NL%+3 Javelin and Spear Skills%CONTINUE%
//Assasin
ItemDisplay[NMAG !RW (SK261>0 OR SK262>0 OR SK263>0 OR SK264>0 OR SK265>0 OR SK266>0 OR SK267>0 OR SK268>0 OR SK269>0 OR SK270>0 OR SK271>0 OR SK272>0 OR SK273>0 OR SK274>0 OR SK275>0 OR SK276>0 OR SK277>0 OR SK278>0 OR SK279>0 OR SK280>0 OR SK366>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK261=1]: %NAME%%NL%+1 Ch. B. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK261=2]: %NAME%%NL%+2 Ch. B. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK261=3]: %NAME%%NL%+3 Ch. B. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK262=1]: %NAME%%NL%+1 Wake.Fire%CONTINUE%
ItemDisplay[NMAG !RW SK262=2]: %NAME%%NL%+2 Wake.Fire%CONTINUE%
ItemDisplay[NMAG !RW SK262=3]: %NAME%%NL%+3 Wake.Fire%CONTINUE%
ItemDisplay[NMAG !RW SK263=1]: %NAME%%NL%+1 Weapon Block%CONTINUE%
ItemDisplay[NMAG !RW SK263=2]: %NAME%%NL%+2 Weapon Block%CONTINUE%
ItemDisplay[NMAG !RW SK263=3]: %NAME%%NL%+3 Weapon Block%CONTINUE%
ItemDisplay[NMAG !RW SK264=1]: %NAME%%NL%+1 Cloak.Shadow%CONTINUE%
ItemDisplay[NMAG !RW SK264=2]: %NAME%%NL%+2 Cloak.Shadow%CONTINUE%
ItemDisplay[NMAG !RW SK264=3]: %NAME%%NL%+3 Cloak.Shadow%CONTINUE%
ItemDisplay[NMAG !RW SK265=1]: %NAME%%NL%+1 Cobra Strike%CONTINUE%
ItemDisplay[NMAG !RW SK265=2]: %NAME%%NL%+2 Cobra Strike%CONTINUE%
ItemDisplay[NMAG !RW SK265=3]: %NAME%%NL%+3 Cobra Strike%CONTINUE%
ItemDisplay[NMAG !RW SK266=1]: %NAME%%NL%+1 Blade Fury%CONTINUE%
ItemDisplay[NMAG !RW SK266=2]: %NAME%%NL%+2 Blade Fury%CONTINUE%
ItemDisplay[NMAG !RW SK266=3]: %NAME%%NL%+3 Blade Fury%CONTINUE%
ItemDisplay[NMAG !RW SK267=1]: %NAME%%NL%+1 Fade%CONTINUE%
ItemDisplay[NMAG !RW SK267=2]: %NAME%%NL%+2 Fade%CONTINUE%
ItemDisplay[NMAG !RW SK267=3]: %NAME%%NL%+3 Fade%CONTINUE%
ItemDisplay[NMAG !RW SK268=1]: %NAME%%NL%+1 Shadow Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK268=2]: %NAME%%NL%+2 Shadow Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK268=3]: %NAME%%NL%+3 Shadow Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK269=1]: %NAME%%NL%+1 Claws.Thunder%CONTINUE%
ItemDisplay[NMAG !RW SK269=2]: %NAME%%NL%+2 Claws.Thunder%CONTINUE%
ItemDisplay[NMAG !RW SK269=3]: %NAME%%NL%+3 Claws.Thunder%CONTINUE%
ItemDisplay[NMAG !RW SK270=1]: %NAME%%NL%+1 Dragon Tail%CONTINUE%
ItemDisplay[NMAG !RW SK270=2]: %NAME%%NL%+2 Dragon Tail%CONTINUE%
ItemDisplay[NMAG !RW SK270=3]: %NAME%%NL%+3 Dragon Tail%CONTINUE%
ItemDisplay[NMAG !RW SK271=1]: %NAME%%NL%+1 Ch. L. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK271=2]: %NAME%%NL%+2 Ch. L. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK271=3]: %NAME%%NL%+3 Ch. L. Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK272=1]: %NAME%%NL%+1 Wake.Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK272=2]: %NAME%%NL%+2 Wake.Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK272=3]: %NAME%%NL%+3 Wake.Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK273=1]: %NAME%%NL%+1 Mind Blast%CONTINUE%
ItemDisplay[NMAG !RW SK273=2]: %NAME%%NL%+2 Mind Blast%CONTINUE%
ItemDisplay[NMAG !RW SK273=3]: %NAME%%NL%+3 Mind Blast%CONTINUE%
ItemDisplay[NMAG !RW SK274=1]: %NAME%%NL%+1 Blades.Ice%CONTINUE%
ItemDisplay[NMAG !RW SK274=2]: %NAME%%NL%+2 Blades.Ice%CONTINUE%
ItemDisplay[NMAG !RW SK274=3]: %NAME%%NL%+3 Blades.Ice%CONTINUE%
ItemDisplay[NMAG !RW SK275=1]: %NAME%%NL%+1 Dragon Fly%CONTINUE%
ItemDisplay[NMAG !RW SK275=2]: %NAME%%NL%+2 Dragon Fly%CONTINUE%
ItemDisplay[NMAG !RW SK275=3]: %NAME%%NL%+3 Dragon Fly%CONTINUE%
ItemDisplay[NMAG !RW SK276=1]: %NAME%%NL%+1 Death Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK276=2]: %NAME%%NL%+2 Death Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK276=3]: %NAME%%NL%+3 Death Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK277=1]: %NAME%%NL%+1 Blade Shield%CONTINUE%
ItemDisplay[NMAG !RW SK277=2]: %NAME%%NL%+2 Blade Shield%CONTINUE%
ItemDisplay[NMAG !RW SK277=3]: %NAME%%NL%+3 Blade Shield%CONTINUE%
ItemDisplay[NMAG !RW SK278=1]: %NAME%%NL%+1 Venom%CONTINUE%
ItemDisplay[NMAG !RW SK278=2]: %NAME%%NL%+2 Venom%CONTINUE%
ItemDisplay[NMAG !RW SK278=3]: %NAME%%NL%+3 Venom%CONTINUE%
ItemDisplay[NMAG !RW SK279=1]: %NAME%%NL%+1 Shadow Master%CONTINUE%
ItemDisplay[NMAG !RW SK279=2]: %NAME%%NL%+2 Shadow Master%CONTINUE%
ItemDisplay[NMAG !RW SK279=3]: %NAME%%NL%+3 Shadow Master%CONTINUE%
ItemDisplay[NMAG !RW SK280=1]: %NAME%%NL%+1 Phoenix Strike%CONTINUE%
ItemDisplay[NMAG !RW SK280=2]: %NAME%%NL%+2 Phoenix Strike%CONTINUE%
ItemDisplay[NMAG !RW SK280=3]: %NAME%%NL%+3 Phoenix Strike%CONTINUE%
ItemDisplay[NMAG !RW SK366=1]: %NAME%%NL%+1 Light Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK366=2]: %NAME%%NL%+2 Light Sentry%CONTINUE%
ItemDisplay[NMAG !RW SK366=3]: %NAME%%NL%+3 Light Sentry%CONTINUE%
//Barbarian
ItemDisplay[NMAG !RW (SK126>0 OR SK128>0 OR SK130>0 OR SK131>0 OR SK132>0 OR SK133>0 OR SK135>0 OR SK136>0 OR SK137>0 OR SK138>0 OR SK139>0 OR SK140>0 OR SK141>0 OR SK142>0 OR SK143>0 OR SK144>0 OR SK145>0 OR SK146>0 OR SK147>0 OR SK148>0 OR SK149>0 OR SK150>0 OR SK151>0 OR SK152>0 OR SK153>0 OR SK154>0 OR SK155>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK126=1]: %NAME%%NL%+1 Bash%CONTINUE%
ItemDisplay[NMAG !RW SK126=2]: %NAME%%NL%+2 Bash%CONTINUE%
ItemDisplay[NMAG !RW SK126=3]: %NAME%%NL%+3 Bash%CONTINUE%
ItemDisplay[NMAG !RW SK128=1]: %NAME%%NL%+1 General Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK128=2]: %NAME%%NL%+2 General Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK128=3]: %NAME%%NL%+3 General Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK130=1]: %NAME%%NL%+1 Howl%CONTINUE%
ItemDisplay[NMAG !RW SK130=2]: %NAME%%NL%+2 Howl%CONTINUE%
ItemDisplay[NMAG !RW SK130=3]: %NAME%%NL%+3 Howl%CONTINUE%
ItemDisplay[NMAG !RW SK131=1]: %NAME%%NL%+1 Find Potion%CONTINUE%
ItemDisplay[NMAG !RW SK131=2]: %NAME%%NL%+2 Find Potion%CONTINUE%
ItemDisplay[NMAG !RW SK131=3]: %NAME%%NL%+3 Find Potion%CONTINUE%
ItemDisplay[NMAG !RW SK132=1]: %NAME%%NL%+1 Leap%CONTINUE%
ItemDisplay[NMAG !RW SK132=2]: %NAME%%NL%+2 Leap%CONTINUE%
ItemDisplay[NMAG !RW SK132=3]: %NAME%%NL%+3 Leap%CONTINUE%
ItemDisplay[NMAG !RW SK133=1]: %NAME%%NL%+1 Double Swing%CONTINUE%
ItemDisplay[NMAG !RW SK133=2]: %NAME%%NL%+2 Double Swing%CONTINUE%
ItemDisplay[NMAG !RW SK133=3]: %NAME%%NL%+3 Double Swing%CONTINUE%
ItemDisplay[NMAG !RW SK135=1]: %NAME%%NL%+1 Throwing Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK135=2]: %NAME%%NL%+2 Throwing Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK135=3]: %NAME%%NL%+3 Throwing Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK136=1]: %NAME%%NL%+1 P-Spear Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK136=2]: %NAME%%NL%+2 P-Spear Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK136=3]: %NAME%%NL%+3 P-Spear Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK137=1]: %NAME%%NL%+1 Taunt%CONTINUE%
ItemDisplay[NMAG !RW SK137=2]: %NAME%%NL%+2 Taunt%CONTINUE%
ItemDisplay[NMAG !RW SK137=3]: %NAME%%NL%+3 Taunt%CONTINUE%
ItemDisplay[NMAG !RW SK138=1]: %NAME%%NL%+1 Shout%CONTINUE%
ItemDisplay[NMAG !RW SK138=2]: %NAME%%NL%+2 Shout%CONTINUE%
ItemDisplay[NMAG !RW SK138=3]: %NAME%%NL%+3 Shout%CONTINUE%
ItemDisplay[NMAG !RW SK139=1]: %NAME%%NL%+1 Stun%CONTINUE%
ItemDisplay[NMAG !RW SK139=2]: %NAME%%NL%+2 Stun%CONTINUE%
ItemDisplay[NMAG !RW SK139=3]: %NAME%%NL%+3 Stun%CONTINUE%
ItemDisplay[NMAG !RW SK140=1]: %NAME%%NL%+1 Double Throw%CONTINUE%
ItemDisplay[NMAG !RW SK140=2]: %NAME%%NL%+2 Double Throw%CONTINUE%
ItemDisplay[NMAG !RW SK140=3]: %NAME%%NL%+3 Double Throw%CONTINUE%
ItemDisplay[NMAG !RW SK141=1]: %NAME%%NL%+1 Combat Reflex%CONTINUE%
ItemDisplay[NMAG !RW SK141=2]: %NAME%%NL%+2 Combat Reflex%CONTINUE%
ItemDisplay[NMAG !RW SK141=3]: %NAME%%NL%+3 Combat Reflex%CONTINUE%
ItemDisplay[NMAG !RW SK142=1]: %NAME%%NL%+1 Find Item%CONTINUE%
ItemDisplay[NMAG !RW SK142=2]: %NAME%%NL%+2 Find Item%CONTINUE%
ItemDisplay[NMAG !RW SK142=3]: %NAME%%NL%+3 Find Item%CONTINUE%
ItemDisplay[NMAG !RW SK143=1]: %NAME%%NL%+1 Leap Attack%CONTINUE%
ItemDisplay[NMAG !RW SK143=2]: %NAME%%NL%+2 Leap Attack%CONTINUE%
ItemDisplay[NMAG !RW SK143=3]: %NAME%%NL%+3 Leap Attack%CONTINUE%
ItemDisplay[NMAG !RW SK144=1]: %NAME%%NL%+1 Concentrate%CONTINUE%
ItemDisplay[NMAG !RW SK144=2]: %NAME%%NL%+2 Concentrate%CONTINUE%
ItemDisplay[NMAG !RW SK144=3]: %NAME%%NL%+3 Concentrate%CONTINUE%
ItemDisplay[NMAG !RW SK145=1]: %NAME%%NL%+1 Iron Skin%CONTINUE%
ItemDisplay[NMAG !RW SK145=2]: %NAME%%NL%+2 Iron Skin%CONTINUE%
ItemDisplay[NMAG !RW SK145=3]: %NAME%%NL%+3 Iron Skin%CONTINUE%
ItemDisplay[NMAG !RW SK146=1]: %NAME%%NL%+1 Battle Cry%CONTINUE%
ItemDisplay[NMAG !RW SK146=2]: %NAME%%NL%+2 Battle Cry%CONTINUE%
ItemDisplay[NMAG !RW SK146=3]: %NAME%%NL%+3 Battle Cry%CONTINUE%
ItemDisplay[NMAG !RW SK147=1]: %NAME%%NL%+1 Frenzy%CONTINUE%
ItemDisplay[NMAG !RW SK147=2]: %NAME%%NL%+2 Frenzy%CONTINUE%
ItemDisplay[NMAG !RW SK147=3]: %NAME%%NL%+3 Frenzy%CONTINUE%
ItemDisplay[NMAG !RW SK148=1]: %NAME%%NL%+1 Increased Speed%CONTINUE%
ItemDisplay[NMAG !RW SK148=2]: %NAME%%NL%+2 Increased Speed%CONTINUE%
ItemDisplay[NMAG !RW SK148=3]: %NAME%%NL%+3 Increased Speed%CONTINUE%
ItemDisplay[NMAG !RW SK149=1]: %NAME%%NL%+1 Battle Orders%CONTINUE%
ItemDisplay[NMAG !RW SK149=2]: %NAME%%NL%+2 Battle Orders%CONTINUE%
ItemDisplay[NMAG !RW SK149=3]: %NAME%%NL%+3 Battle Orders%CONTINUE%
ItemDisplay[NMAG !RW SK150=1]: %NAME%%NL%+1 Grim Ward%CONTINUE%
ItemDisplay[NMAG !RW SK150=2]: %NAME%%NL%+2 Grim Ward%CONTINUE%
ItemDisplay[NMAG !RW SK150=3]: %NAME%%NL%+3 Grim Ward%CONTINUE%
ItemDisplay[NMAG !RW SK151=1]: %NAME%%NL%+1 Whirlwind%CONTINUE%
ItemDisplay[NMAG !RW SK151=2]: %NAME%%NL%+2 Whirlwind%CONTINUE%
ItemDisplay[NMAG !RW SK151=3]: %NAME%%NL%+3 Whirlwind%CONTINUE%
ItemDisplay[NMAG !RW SK152=1]: %NAME%%NL%+1 Berserk%CONTINUE%
ItemDisplay[NMAG !RW SK152=2]: %NAME%%NL%+2 Berserk%CONTINUE%
ItemDisplay[NMAG !RW SK152=3]: %NAME%%NL%+3 Berserk%CONTINUE%
ItemDisplay[NMAG !RW SK153=1]: %NAME%%NL%+1 Natural Resist%CONTINUE%
ItemDisplay[NMAG !RW SK153=2]: %NAME%%NL%+2 Natural Resist%CONTINUE%
ItemDisplay[NMAG !RW SK153=3]: %NAME%%NL%+3 Natural Resist%CONTINUE%
ItemDisplay[NMAG !RW SK154=1]: %NAME%%NL%+1 War Cry%CONTINUE%
ItemDisplay[NMAG !RW SK154=2]: %NAME%%NL%+2 War Cry%CONTINUE%
ItemDisplay[NMAG !RW SK154=3]: %NAME%%NL%+3 War Cry%CONTINUE%
ItemDisplay[NMAG !RW SK155=1]: %NAME%%NL%+1 Battle Command%CONTINUE%
ItemDisplay[NMAG !RW SK155=2]: %NAME%%NL%+2 Battle Command%CONTINUE%
ItemDisplay[NMAG !RW SK155=3]: %NAME%%NL%+3 Battle Command%CONTINUE%
//Druid
ItemDisplay[NMAG !RW (SK221>0 OR SK222>0 OR SK223>0 OR SK224>0 OR SK225>0 OR SK226>0 OR SK227>0 OR SK228>0 OR SK229>0 OR SK230>0 OR SK231>0 OR SK232>0 OR SK233>0 OR SK234>0 OR SK235>0 OR SK236>0 OR SK237>0 OR SK238>0 OR SK239>0 OR SK240>0 OR SK241>0 OR SK242>0 OR SK243>0 OR SK244>0 OR SK245>0 OR SK246>0 OR SK247>0 OR SK248>0 OR SK249>0 OR SK250>0 OR SK370>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK221=1]: %NAME%%NL%+1 Raven%CONTINUE%
ItemDisplay[NMAG !RW SK221=2]: %NAME%%NL%+2 Raven%CONTINUE%
ItemDisplay[NMAG !RW SK221=3]: %NAME%%NL%+3 Raven%CONTINUE%
ItemDisplay[NMAG !RW SK222=1]: %NAME%%NL%+1 Poison Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK222=2]: %NAME%%NL%+2 Poison Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK222=3]: %NAME%%NL%+3 Poison Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK223=1]: %NAME%%NL%+1 Werewolf%CONTINUE%
ItemDisplay[NMAG !RW SK223=2]: %NAME%%NL%+2 Werewolf%CONTINUE%
ItemDisplay[NMAG !RW SK223=3]: %NAME%%NL%+3 Werewolf%CONTINUE%
ItemDisplay[NMAG !RW SK224=1]: %NAME%%NL%+1 Lycanthropy%CONTINUE%
ItemDisplay[NMAG !RW SK224=2]: %NAME%%NL%+2 Lycanthropy%CONTINUE%
ItemDisplay[NMAG !RW SK224=3]: %NAME%%NL%+3 Lycanthropy%CONTINUE%
ItemDisplay[NMAG !RW SK225=1]: %NAME%%NL%+1 Firestorm%CONTINUE%
ItemDisplay[NMAG !RW SK225=2]: %NAME%%NL%+2 Firestorm%CONTINUE%
ItemDisplay[NMAG !RW SK225=3]: %NAME%%NL%+3 Firestorm%CONTINUE%
ItemDisplay[NMAG !RW SK226=1]: %NAME%%NL%+1 Oak Sage%CONTINUE%
ItemDisplay[NMAG !RW SK226=2]: %NAME%%NL%+2 Oak Sage%CONTINUE%
ItemDisplay[NMAG !RW SK226=3]: %NAME%%NL%+3 Oak Sage%CONTINUE%
ItemDisplay[NMAG !RW SK227=1]: %NAME%%NL%+1 Spirit Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK227=2]: %NAME%%NL%+2 Spirit Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK227=3]: %NAME%%NL%+3 Spirit Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK228=1]: %NAME%%NL%+1 Werebear%CONTINUE%
ItemDisplay[NMAG !RW SK228=2]: %NAME%%NL%+2 Werebear%CONTINUE%
ItemDisplay[NMAG !RW SK228=3]: %NAME%%NL%+3 Werebear%CONTINUE%
ItemDisplay[NMAG !RW SK229=1]: %NAME%%NL%+1 Molten Boulder%CONTINUE%
ItemDisplay[NMAG !RW SK229=2]: %NAME%%NL%+2 Molten Boulder%CONTINUE%
ItemDisplay[NMAG !RW SK229=3]: %NAME%%NL%+3 Molten Boulder%CONTINUE%
ItemDisplay[NMAG !RW SK230=1]: %NAME%%NL%+1 Arctic Blast%CONTINUE%
ItemDisplay[NMAG !RW SK230=2]: %NAME%%NL%+2 Arctic Blast%CONTINUE%
ItemDisplay[NMAG !RW SK230=3]: %NAME%%NL%+3 Arctic Blast%CONTINUE%
ItemDisplay[NMAG !RW SK231=1]: %NAME%%NL%+1 Carrion Vine%CONTINUE%
ItemDisplay[NMAG !RW SK231=2]: %NAME%%NL%+2 Carrion Vine%CONTINUE%
ItemDisplay[NMAG !RW SK231=3]: %NAME%%NL%+3 Carrion Vine%CONTINUE%
ItemDisplay[NMAG !RW SK232=1]: %NAME%%NL%+1 Feral Rage%CONTINUE%
ItemDisplay[NMAG !RW SK232=2]: %NAME%%NL%+2 Feral Rage%CONTINUE%
ItemDisplay[NMAG !RW SK232=3]: %NAME%%NL%+3 Feral Rage%CONTINUE%
ItemDisplay[NMAG !RW SK233=1]: %NAME%%NL%+1 Maul%CONTINUE%
ItemDisplay[NMAG !RW SK233=2]: %NAME%%NL%+2 Maul%CONTINUE%
ItemDisplay[NMAG !RW SK233=3]: %NAME%%NL%+3 Maul%CONTINUE%
ItemDisplay[NMAG !RW SK234=1]: %NAME%%NL%+1 Fissure%CONTINUE%
ItemDisplay[NMAG !RW SK234=2]: %NAME%%NL%+2 Fissure%CONTINUE%
ItemDisplay[NMAG !RW SK234=3]: %NAME%%NL%+3 Fissure%CONTINUE%
ItemDisplay[NMAG !RW SK235=1]: %NAME%%NL%+1 Cyclone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK235=2]: %NAME%%NL%+2 Cyclone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK235=3]: %NAME%%NL%+3 Cyclone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK236=1]: %NAME%%NL%+1 Wolverine Heart%CONTINUE%
ItemDisplay[NMAG !RW SK236=2]: %NAME%%NL%+2 Wolverine Heart%CONTINUE%
ItemDisplay[NMAG !RW SK236=3]: %NAME%%NL%+3 Wolverine Heart%CONTINUE%
ItemDisplay[NMAG !RW SK237=1]: %NAME%%NL%+1 Dire Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK237=2]: %NAME%%NL%+2 Dire Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK237=3]: %NAME%%NL%+3 Dire Wolf%CONTINUE%
ItemDisplay[NMAG !RW SK238=1]: %NAME%%NL%+1 Rabies%CONTINUE%
ItemDisplay[NMAG !RW SK238=2]: %NAME%%NL%+2 Rabies%CONTINUE%
ItemDisplay[NMAG !RW SK238=3]: %NAME%%NL%+3 Rabies%CONTINUE%
ItemDisplay[NMAG !RW SK239=1]: %NAME%%NL%+1 Fire Claws%CONTINUE%
ItemDisplay[NMAG !RW SK239=2]: %NAME%%NL%+2 Fire Claws%CONTINUE%
ItemDisplay[NMAG !RW SK239=3]: %NAME%%NL%+3 Fire Claws%CONTINUE%
ItemDisplay[NMAG !RW SK240=1]: %NAME%%NL%+1 Twister%CONTINUE%
ItemDisplay[NMAG !RW SK240=2]: %NAME%%NL%+2 Twister%CONTINUE%
ItemDisplay[NMAG !RW SK240=3]: %NAME%%NL%+3 Twister%CONTINUE%
ItemDisplay[NMAG !RW SK241=1]: %NAME%%NL%+1 Solar Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK241=2]: %NAME%%NL%+2 Solar Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK241=3]: %NAME%%NL%+3 Solar Creeper%CONTINUE%
ItemDisplay[NMAG !RW SK242=1]: %NAME%%NL%+1 Hunger%CONTINUE%
ItemDisplay[NMAG !RW SK242=2]: %NAME%%NL%+2 Hunger%CONTINUE%
ItemDisplay[NMAG !RW SK242=3]: %NAME%%NL%+3 Hunger%CONTINUE%
ItemDisplay[NMAG !RW SK243=1]: %NAME%%NL%+1 Shock Wave%CONTINUE%
ItemDisplay[NMAG !RW SK243=2]: %NAME%%NL%+2 Shock Wave%CONTINUE%
ItemDisplay[NMAG !RW SK243=3]: %NAME%%NL%+3 Shock Wave%CONTINUE%
ItemDisplay[NMAG !RW SK244=1]: %NAME%%NL%+1 Volcano%CONTINUE%
ItemDisplay[NMAG !RW SK244=2]: %NAME%%NL%+2 Volcano%CONTINUE%
ItemDisplay[NMAG !RW SK244=3]: %NAME%%NL%+3 Volcano%CONTINUE%
ItemDisplay[NMAG !RW SK245=1]: %NAME%%NL%+1 Tornado%CONTINUE%
ItemDisplay[NMAG !RW SK245=2]: %NAME%%NL%+2 Tornado%CONTINUE%
ItemDisplay[NMAG !RW SK245=3]: %NAME%%NL%+3 Tornado%CONTINUE%
ItemDisplay[NMAG !RW SK246=1]: %NAME%%NL%+1 Barbs Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK246=2]: %NAME%%NL%+2 Barbs Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK246=3]: %NAME%%NL%+3 Barbs Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK247=1]: %NAME%%NL%+1 Grizzly%CONTINUE%
ItemDisplay[NMAG !RW SK247=2]: %NAME%%NL%+2 Grizzly%CONTINUE%
ItemDisplay[NMAG !RW SK247=3]: %NAME%%NL%+3 Grizzly%CONTINUE%
ItemDisplay[NMAG !RW SK248=1]: %NAME%%NL%+1 Fury%CONTINUE%
ItemDisplay[NMAG !RW SK248=2]: %NAME%%NL%+2 Fury%CONTINUE%
ItemDisplay[NMAG !RW SK248=3]: %NAME%%NL%+3 Fury%CONTINUE%
ItemDisplay[NMAG !RW SK249=1]: %NAME%%NL%+1 Armageddon%CONTINUE%
ItemDisplay[NMAG !RW SK249=2]: %NAME%%NL%+2 Armageddon%CONTINUE%
ItemDisplay[NMAG !RW SK249=3]: %NAME%%NL%+3 Armageddon%CONTINUE%
ItemDisplay[NMAG !RW SK250=1]: %NAME%%NL%+1 Hurricane%CONTINUE%
ItemDisplay[NMAG !RW SK250=2]: %NAME%%NL%+2 Hurricane%CONTINUE%
ItemDisplay[NMAG !RW SK250=3]: %NAME%%NL%+3 Hurricane%CONTINUE%
ItemDisplay[NMAG !RW SK370=1]: %NAME%%NL%+1 Gust%CONTINUE%
ItemDisplay[NMAG !RW SK370=2]: %NAME%%NL%+2 Gust%CONTINUE%
ItemDisplay[NMAG !RW SK370=3]: %NAME%%NL%+3 Gust%CONTINUE%
//Necromancer
ItemDisplay[NMAG !RW (SK66>0 OR SK67>0 OR SK68>0 OR SK69>0 OR SK70>0 OR SK71>0 OR SK72>0 OR SK73>0 OR SK74>0 OR SK75>0 OR SK76>0 OR SK77>0 OR SK78>0 OR SK79>0 OR SK80>0 OR SK81>0 OR SK82>0 OR SK83>0 OR SK84>0 OR SK85>0 OR SK86>0 OR SK87>0 OR SK88>0 OR SK89>0 OR SK90>0 OR SK91>0 OR SK92>0 OR SK93>0 OR SK94>0 OR SK95>0 OR SK367>0 OR SK381>0 OR SK374>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK66=1]: %NAME%%NL%+1 Amplify Damage%CONTINUE%
ItemDisplay[NMAG !RW SK66=2]: %NAME%%NL%+2 Amplify Damage%CONTINUE%
ItemDisplay[NMAG !RW SK66=3]: %NAME%%NL%+3 Amplify Damage%CONTINUE%
ItemDisplay[NMAG !RW SK67=1]: %NAME%%NL%+1 Teeth%CONTINUE%
ItemDisplay[NMAG !RW SK67=2]: %NAME%%NL%+2 Teeth%CONTINUE%
ItemDisplay[NMAG !RW SK67=3]: %NAME%%NL%+3 Teeth%CONTINUE%
ItemDisplay[NMAG !RW SK68=1]: %NAME%%NL%+1 Bone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK68=2]: %NAME%%NL%+2 Bone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK68=3]: %NAME%%NL%+3 Bone Armor%CONTINUE%
ItemDisplay[NMAG !RW SK69=1]: %NAME%%NL%+1 Skele Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK69=2]: %NAME%%NL%+2 Skele Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK69=3]: %NAME%%NL%+3 Skele Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK70=1]: %NAME%%NL%+1 Skele Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK70=2]: %NAME%%NL%+2 Skele Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK70=3]: %NAME%%NL%+3 Skele Warrior%CONTINUE%
ItemDisplay[NMAG !RW SK71=1]: %NAME%%NL%+1 Dim Vision%CONTINUE%
ItemDisplay[NMAG !RW SK71=2]: %NAME%%NL%+2 Dim Vision%CONTINUE%
ItemDisplay[NMAG !RW SK71=3]: %NAME%%NL%+3 Dim Vision%CONTINUE%
ItemDisplay[NMAG !RW SK72=1]: %NAME%%NL%+1 Weaken%CONTINUE%
ItemDisplay[NMAG !RW SK72=2]: %NAME%%NL%+2 Weaken%CONTINUE%
ItemDisplay[NMAG !RW SK72=3]: %NAME%%NL%+3 Weaken%CONTINUE%
ItemDisplay[NMAG !RW SK73=1]: %NAME%%NL%+1 Poison Dagger%CONTINUE%
ItemDisplay[NMAG !RW SK73=2]: %NAME%%NL%+2 Poison Dagger%CONTINUE%
ItemDisplay[NMAG !RW SK73=3]: %NAME%%NL%+3 Poison Dagger%CONTINUE%
ItemDisplay[NMAG !RW SK74=1]: %NAME%%NL%+1 Corpse Explo%CONTINUE%
ItemDisplay[NMAG !RW SK74=2]: %NAME%%NL%+2 Corpse Explo%CONTINUE%
ItemDisplay[NMAG !RW SK74=3]: %NAME%%NL%+3 Corpse Explo%CONTINUE%
ItemDisplay[NMAG !RW SK75=1]: %NAME%%NL%+1 Clay Golem%CONTINUE%
ItemDisplay[NMAG !RW SK75=2]: %NAME%%NL%+2 Clay Golem%CONTINUE%
ItemDisplay[NMAG !RW SK75=3]: %NAME%%NL%+3 Clay Golem%CONTINUE%
ItemDisplay[NMAG !RW SK76=1]: %NAME%%NL%+1 Iron Maiden%CONTINUE%
ItemDisplay[NMAG !RW SK76=2]: %NAME%%NL%+2 Iron Maiden%CONTINUE%
ItemDisplay[NMAG !RW SK76=3]: %NAME%%NL%+3 Iron Maiden%CONTINUE%
ItemDisplay[NMAG !RW SK77=1]: %NAME%%NL%+1 Terror%CONTINUE%
ItemDisplay[NMAG !RW SK77=2]: %NAME%%NL%+2 Terror%CONTINUE%
ItemDisplay[NMAG !RW SK77=3]: %NAME%%NL%+3 Terror%CONTINUE%
ItemDisplay[NMAG !RW SK78=1]: %NAME%%NL%+1 Bone Wall%CONTINUE%
ItemDisplay[NMAG !RW SK78=2]: %NAME%%NL%+2 Bone Wall%CONTINUE%
ItemDisplay[NMAG !RW SK78=3]: %NAME%%NL%+3 Bone Wall%CONTINUE%
ItemDisplay[NMAG !RW SK79=1]: %NAME%%NL%+1 Golem Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK79=2]: %NAME%%NL%+2 Golem Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK79=3]: %NAME%%NL%+3 Golem Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK80=1]: %NAME%%NL%+1 Skeletal Mage%CONTINUE%
ItemDisplay[NMAG !RW SK80=2]: %NAME%%NL%+2 Skeletal Mage%CONTINUE%
ItemDisplay[NMAG !RW SK80=3]: %NAME%%NL%+3 Skeletal Mage%CONTINUE%
ItemDisplay[NMAG !RW SK81=1]: %NAME%%NL%+1 Confuse%CONTINUE%
ItemDisplay[NMAG !RW SK81=2]: %NAME%%NL%+2 Confuse%CONTINUE%
ItemDisplay[NMAG !RW SK81=3]: %NAME%%NL%+3 Confuse%CONTINUE%
ItemDisplay[NMAG !RW SK82=1]: %NAME%%NL%+1 Life Tap%CONTINUE%
ItemDisplay[NMAG !RW SK82=2]: %NAME%%NL%+2 Life Tap%CONTINUE%
ItemDisplay[NMAG !RW SK82=3]: %NAME%%NL%+3 Life Tap%CONTINUE%
ItemDisplay[NMAG !RW SK83=1]: %NAME%%NL%+1 Desecrate%CONTINUE%
ItemDisplay[NMAG !RW SK83=2]: %NAME%%NL%+2 Desecrate%CONTINUE%
ItemDisplay[NMAG !RW SK83=3]: %NAME%%NL%+3 Desecrate%CONTINUE%
ItemDisplay[NMAG !RW SK84=1]: %NAME%%NL%+1 Bone Spear%CONTINUE%
ItemDisplay[NMAG !RW SK84=2]: %NAME%%NL%+2 Bone Spear%CONTINUE%
ItemDisplay[NMAG !RW SK84=3]: %NAME%%NL%+3 Bone Spear%CONTINUE%
ItemDisplay[NMAG !RW SK85=1]: %NAME%%NL%+1 Blood Golem%CONTINUE%
ItemDisplay[NMAG !RW SK85=2]: %NAME%%NL%+2 Blood Golem%CONTINUE%
ItemDisplay[NMAG !RW SK85=3]: %NAME%%NL%+3 Blood Golem%CONTINUE%
ItemDisplay[NMAG !RW SK86=1]: %NAME%%NL%+1 Attract%CONTINUE%
ItemDisplay[NMAG !RW SK86=2]: %NAME%%NL%+2 Attract%CONTINUE%
ItemDisplay[NMAG !RW SK86=3]: %NAME%%NL%+3 Attract%CONTINUE%
ItemDisplay[NMAG !RW SK87=1]: %NAME%%NL%+1 Decrepify%CONTINUE%
ItemDisplay[NMAG !RW SK87=2]: %NAME%%NL%+2 Decrepify%CONTINUE%
ItemDisplay[NMAG !RW SK87=3]: %NAME%%NL%+3 Decrepify%CONTINUE%
ItemDisplay[NMAG !RW SK88=1]: %NAME%%NL%+1 Bone Prison%CONTINUE%
ItemDisplay[NMAG !RW SK88=2]: %NAME%%NL%+2 Bone Prison%CONTINUE%
ItemDisplay[NMAG !RW SK88=3]: %NAME%%NL%+3 Bone Prison%CONTINUE%
ItemDisplay[NMAG !RW SK90=1]: %NAME%%NL%+1 Iron Golem%CONTINUE%
ItemDisplay[NMAG !RW SK90=2]: %NAME%%NL%+2 Iron Golem%CONTINUE%
ItemDisplay[NMAG !RW SK90=3]: %NAME%%NL%+3 Iron Golem%CONTINUE%
ItemDisplay[NMAG !RW SK91=1]: %NAME%%NL%+1 Lower Resist%CONTINUE%
ItemDisplay[NMAG !RW SK91=2]: %NAME%%NL%+2 Lower Resist%CONTINUE%
ItemDisplay[NMAG !RW SK91=3]: %NAME%%NL%+3 Lower Resist%CONTINUE%
ItemDisplay[NMAG !RW SK92=1]: %NAME%%NL%+1 Poison Nova%CONTINUE%
ItemDisplay[NMAG !RW SK92=2]: %NAME%%NL%+2 Poison Nova%CONTINUE%
ItemDisplay[NMAG !RW SK92=3]: %NAME%%NL%+3 Poison Nova%CONTINUE%
ItemDisplay[NMAG !RW SK93=1]: %NAME%%NL%+1 Bone Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK93=2]: %NAME%%NL%+2 Bone Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK93=3]: %NAME%%NL%+3 Bone Spirit%CONTINUE%
ItemDisplay[NMAG !RW SK94=1]: %NAME%%NL%+1 Fire Golem%CONTINUE%
ItemDisplay[NMAG !RW SK94=2]: %NAME%%NL%+2 Fire Golem%CONTINUE%
ItemDisplay[NMAG !RW SK94=3]: %NAME%%NL%+3 Fire Golem%CONTINUE%
ItemDisplay[NMAG !RW SK95=1]: %NAME%%NL%+1 Revive%CONTINUE%
ItemDisplay[NMAG !RW SK95=2]: %NAME%%NL%+2 Revive%CONTINUE%
ItemDisplay[NMAG !RW SK95=3]: %NAME%%NL%+3 Revive%CONTINUE%
ItemDisplay[NMAG !RW SK367=1]: %NAME%%NL%+1 Blood Warp%CONTINUE%
ItemDisplay[NMAG !RW SK367=2]: %NAME%%NL%+2 Blood Warp%CONTINUE%
ItemDisplay[NMAG !RW SK367=3]: %NAME%%NL%+3 Blood Warp%CONTINUE%
ItemDisplay[NMAG !RW SK381=1]: %NAME%%NL%+1 Dark Pact%CONTINUE%
ItemDisplay[NMAG !RW SK381=2]: %NAME%%NL%+2 Dark Pact%CONTINUE%
ItemDisplay[NMAG !RW SK381=3]: %NAME%%NL%+3 Dark Pact%CONTINUE%
ItemDisplay[NMAG !RW SK374=1]: %NAME%%NL%+1 Curse Master%CONTINUE%
ItemDisplay[NMAG !RW SK374=2]: %NAME%%NL%+2 Curse Master%CONTINUE%
ItemDisplay[NMAG !RW SK374=3]: %NAME%%NL%+3 Curse Master%CONTINUE%
//Paladin
ItemDisplay[NMAG !RW (SK96>0 OR SK97>0 OR SK98>0 OR SK99>0 OR SK100>0 OR SK101>0 OR SK102>0 OR SK103>0 OR SK104>0 OR SK105>0 OR SK106>0 OR SK107>0 OR SK108>0 OR SK109>0 OR SK110>0 OR SK111>0 OR SK112>0 OR SK113>0 OR SK114>0 OR SK115>0 OR SK116>0 OR SK117>0 OR SK118>0 OR SK119>0 OR SK120>0 OR SK121>0 OR SK122>0 OR SK123>0 OR SK124>0 OR SK125>0 OR SK364>0 OR SK371>0 OR SK378>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK96=1]: %NAME%%NL%+1 Sacrifice%CONTINUE%
ItemDisplay[NMAG !RW SK96=2]: %NAME%%NL%+2 Sacrifice%CONTINUE%
ItemDisplay[NMAG !RW SK96=3]: %NAME%%NL%+3 Sacrifice%CONTINUE%
ItemDisplay[NMAG !RW SK97=1]: %NAME%%NL%+1 Smite%CONTINUE%
ItemDisplay[NMAG !RW SK97=2]: %NAME%%NL%+2 Smite%CONTINUE%
ItemDisplay[NMAG !RW SK97=3]: %NAME%%NL%+3 Smite%CONTINUE%
ItemDisplay[NMAG !RW SK98=1]: %NAME%%NL%+1 Might%CONTINUE%
ItemDisplay[NMAG !RW SK98=2]: %NAME%%NL%+2 Might%CONTINUE%
ItemDisplay[NMAG !RW SK98=3]: %NAME%%NL%+3 Might%CONTINUE%
ItemDisplay[NMAG !RW SK99=1]: %NAME%%NL%+1 Prayer%CONTINUE%
ItemDisplay[NMAG !RW SK99=2]: %NAME%%NL%+2 Prayer%CONTINUE%
ItemDisplay[NMAG !RW SK99=3]: %NAME%%NL%+3 Prayer%CONTINUE%
ItemDisplay[NMAG !RW SK100=1]: %NAME%%NL%+1 Res Fire%CONTINUE%
ItemDisplay[NMAG !RW SK100=2]: %NAME%%NL%+2 Res Fire%CONTINUE%
ItemDisplay[NMAG !RW SK100=3]: %NAME%%NL%+3 Res Fire%CONTINUE%
ItemDisplay[NMAG !RW SK101=1]: %NAME%%NL%+1 Holy Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK101=2]: %NAME%%NL%+2 Holy Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK101=3]: %NAME%%NL%+3 Holy Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK102=1]: %NAME%%NL%+1 Holy Fire%CONTINUE%
ItemDisplay[NMAG !RW SK102=2]: %NAME%%NL%+2 Holy Fire%CONTINUE%
ItemDisplay[NMAG !RW SK102=3]: %NAME%%NL%+3 Holy Fire%CONTINUE%
ItemDisplay[NMAG !RW SK103=1]: %NAME%%NL%+1 Thorns%CONTINUE%
ItemDisplay[NMAG !RW SK103=2]: %NAME%%NL%+2 Thorns%CONTINUE%
ItemDisplay[NMAG !RW SK103=3]: %NAME%%NL%+3 Thorns%CONTINUE%
ItemDisplay[NMAG !RW SK104=1]: %NAME%%NL%+1 Defiance%CONTINUE%
ItemDisplay[NMAG !RW SK104=2]: %NAME%%NL%+2 Defiance%CONTINUE%
ItemDisplay[NMAG !RW SK104=3]: %NAME%%NL%+3 Defiance%CONTINUE%
ItemDisplay[NMAG !RW SK105=1]: %NAME%%NL%+1 Res Cold%CONTINUE%
ItemDisplay[NMAG !RW SK105=2]: %NAME%%NL%+2 Res Cold%CONTINUE%
ItemDisplay[NMAG !RW SK105=3]: %NAME%%NL%+3 Res Cold%CONTINUE%
ItemDisplay[NMAG !RW SK106=1]: %NAME%%NL%+1 Zeal%CONTINUE%
ItemDisplay[NMAG !RW SK106=2]: %NAME%%NL%+2 Zeal%CONTINUE%
ItemDisplay[NMAG !RW SK106=3]: %NAME%%NL%+3 Zeal%CONTINUE%
ItemDisplay[NMAG !RW SK107=1]: %NAME%%NL%+1 Charge%CONTINUE%
ItemDisplay[NMAG !RW SK107=2]: %NAME%%NL%+2 Charge%CONTINUE%
ItemDisplay[NMAG !RW SK107=3]: %NAME%%NL%+3 Charge%CONTINUE%
ItemDisplay[NMAG !RW SK108=1]: %NAME%%NL%+1 Bless Aim%CONTINUE%
ItemDisplay[NMAG !RW SK108=2]: %NAME%%NL%+2 Bless Aim%CONTINUE%
ItemDisplay[NMAG !RW SK108=3]: %NAME%%NL%+3 Bless Aim%CONTINUE%
ItemDisplay[NMAG !RW SK109=1]: %NAME%%NL%+1 Cleansing%CONTINUE%
ItemDisplay[NMAG !RW SK109=2]: %NAME%%NL%+2 Cleansing%CONTINUE%
ItemDisplay[NMAG !RW SK109=3]: %NAME%%NL%+3 Cleansing%CONTINUE%
ItemDisplay[NMAG !RW SK110=1]: %NAME%%NL%+1 Res Light%CONTINUE%
ItemDisplay[NMAG !RW SK110=2]: %NAME%%NL%+2 Res Light%CONTINUE%
ItemDisplay[NMAG !RW SK110=3]: %NAME%%NL%+3 Res Light%CONTINUE%
ItemDisplay[NMAG !RW SK111=1]: %NAME%%NL%+1 Vengeance%CONTINUE%
ItemDisplay[NMAG !RW SK111=2]: %NAME%%NL%+2 Vengeance%CONTINUE%
ItemDisplay[NMAG !RW SK111=3]: %NAME%%NL%+3 Vengeance%CONTINUE%
ItemDisplay[NMAG !RW SK112=1]: %NAME%%NL%+1 Bless Hammer%CONTINUE%
ItemDisplay[NMAG !RW SK112=2]: %NAME%%NL%+2 Bless Hammer%CONTINUE%
ItemDisplay[NMAG !RW SK112=3]: %NAME%%NL%+3 Bless Hammer%CONTINUE%
ItemDisplay[NMAG !RW SK113=1]: %NAME%%NL%+1 Concentration%CONTINUE%
ItemDisplay[NMAG !RW SK113=2]: %NAME%%NL%+2 Concentration%CONTINUE%
ItemDisplay[NMAG !RW SK113=3]: %NAME%%NL%+3 Concentration%CONTINUE%
ItemDisplay[NMAG !RW SK114=1]: %NAME%%NL%+1 Holy Freeze%CONTINUE%
ItemDisplay[NMAG !RW SK114=2]: %NAME%%NL%+2 Holy Freeze%CONTINUE%
ItemDisplay[NMAG !RW SK114=3]: %NAME%%NL%+3 Holy Freeze%CONTINUE%
ItemDisplay[NMAG !RW SK115=1]: %NAME%%NL%+1 Vigor%CONTINUE%
ItemDisplay[NMAG !RW SK115=2]: %NAME%%NL%+2 Vigor%CONTINUE%
ItemDisplay[NMAG !RW SK115=3]: %NAME%%NL%+3 Vigor%CONTINUE%
ItemDisplay[NMAG !RW SK116=1]: %NAME%%NL%+1 Conversion%CONTINUE%
ItemDisplay[NMAG !RW SK116=2]: %NAME%%NL%+2 Conversion%CONTINUE%
ItemDisplay[NMAG !RW SK116=3]: %NAME%%NL%+3 Conversion%CONTINUE%
ItemDisplay[NMAG !RW SK117=1]: %NAME%%NL%+1 Holy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK117=2]: %NAME%%NL%+2 Holy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK117=3]: %NAME%%NL%+3 Holy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK118=1]: %NAME%%NL%+1 Holy Shock%CONTINUE%
ItemDisplay[NMAG !RW SK118=2]: %NAME%%NL%+2 Holy Shock%CONTINUE%
ItemDisplay[NMAG !RW SK118=3]: %NAME%%NL%+3 Holy Shock%CONTINUE%
ItemDisplay[NMAG !RW SK119=1]: %NAME%%NL%+1 Sanctuary%CONTINUE%
ItemDisplay[NMAG !RW SK119=2]: %NAME%%NL%+2 Sanctuary%CONTINUE%
ItemDisplay[NMAG !RW SK119=3]: %NAME%%NL%+3 Sanctuary%CONTINUE%
ItemDisplay[NMAG !RW SK120=1]: %NAME%%NL%+1 Meditation%CONTINUE%
ItemDisplay[NMAG !RW SK120=2]: %NAME%%NL%+2 Meditation%CONTINUE%
ItemDisplay[NMAG !RW SK120=3]: %NAME%%NL%+3 Meditation%CONTINUE%
ItemDisplay[NMAG !RW SK121=1]: %NAME%%NL%+1 Fist.Heaven%CONTINUE%
ItemDisplay[NMAG !RW SK121=2]: %NAME%%NL%+2 Fist.Heaven%CONTINUE%
ItemDisplay[NMAG !RW SK121=3]: %NAME%%NL%+3 Fist.Heaven%CONTINUE%
ItemDisplay[NMAG !RW SK122=1]: %NAME%%NL%+1 Fanaticism%CONTINUE%
ItemDisplay[NMAG !RW SK122=2]: %NAME%%NL%+2 Fanaticism%CONTINUE%
ItemDisplay[NMAG !RW SK122=3]: %NAME%%NL%+3 Fanaticism%CONTINUE%
ItemDisplay[NMAG !RW SK123=1]: %NAME%%NL%+1 Conviction%CONTINUE%
ItemDisplay[NMAG !RW SK123=2]: %NAME%%NL%+2 Conviction%CONTINUE%
ItemDisplay[NMAG !RW SK123=3]: %NAME%%NL%+3 Conviction%CONTINUE%
ItemDisplay[NMAG !RW SK124=1]: %NAME%%NL%+1 Redemption%CONTINUE%
ItemDisplay[NMAG !RW SK124=2]: %NAME%%NL%+2 Redemption%CONTINUE%
ItemDisplay[NMAG !RW SK124=3]: %NAME%%NL%+3 Redemption%CONTINUE%
ItemDisplay[NMAG !RW SK125=1]: %NAME%%NL%+1 Salvation%CONTINUE%
ItemDisplay[NMAG !RW SK125=2]: %NAME%%NL%+2 Salvation%CONTINUE%
ItemDisplay[NMAG !RW SK125=3]: %NAME%%NL%+3 Salvation%CONTINUE%
ItemDisplay[NMAG !RW SK364=1]: %NAME%%NL%+1 Holy Nova%CONTINUE%
ItemDisplay[NMAG !RW SK364=2]: %NAME%%NL%+2 Holy Nova%CONTINUE%
ItemDisplay[NMAG !RW SK364=3]: %NAME%%NL%+3 Holy Nova%CONTINUE%
ItemDisplay[NMAG !RW SK371=1]: %NAME%%NL%+1 Holy Light%CONTINUE%
ItemDisplay[NMAG !RW SK371=2]: %NAME%%NL%+2 Holy Light%CONTINUE%
ItemDisplay[NMAG !RW SK371=3]: %NAME%%NL%+3 Holy Light%CONTINUE%
ItemDisplay[NMAG !RW SK378=1]: %NAME%%NL%+1 Joust%CONTINUE%
ItemDisplay[NMAG !RW SK378=2]: %NAME%%NL%+2 Joust%CONTINUE%
ItemDisplay[NMAG !RW SK378=3]: %NAME%%NL%+3 Joust%CONTINUE%
//Sorceress
ItemDisplay[NMAG !RW (SK36>0 OR SK37>0 OR SK38>0 OR SK39>0 OR SK40>0 OR SK41>0 OR SK42>0 OR SK43>0 OR SK44>0 OR SK45>0 OR SK46>0 OR SK47>0 OR SK48>0 OR SK49>0 OR SK50>0 OR SK51>0 OR SK52>0 OR SK53>0 OR SK54>0 OR SK55>0 OR SK56>0 OR SK57>0 OR SK58>0 OR SK59>0 OR SK60>0 OR SK61>0 OR SK62>0 OR SK63>0 OR SK64>0 OR SK65>0 OR SK369>0 OR SK383>0 OR SK376>0)]: %NAME%%DARK_GREEN%%CONTINUE%
ItemDisplay[NMAG !RW SK36=1]: %NAME%%NL%+1 Fire Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK36=2]: %NAME%%NL%+2 Fire Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK36=3]: %NAME%%NL%+3 Fire Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK37=1]: %NAME%%NL%+1 Warmth%CONTINUE%
ItemDisplay[NMAG !RW SK37=2]: %NAME%%NL%+2 Warmth%CONTINUE%
ItemDisplay[NMAG !RW SK37=3]: %NAME%%NL%+3 Warmth%CONTINUE%
ItemDisplay[NMAG !RW SK38=1]: %NAME%%NL%+1 Ch. Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK38=2]: %NAME%%NL%+2 Ch. Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK38=3]: %NAME%%NL%+3 Ch. Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK39=1]: %NAME%%NL%+1 Ice Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK39=2]: %NAME%%NL%+2 Ice Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK39=3]: %NAME%%NL%+3 Ice Bolt%CONTINUE%
ItemDisplay[NMAG !RW SK40=1]: %NAME%%NL%+1 Cold Enchant%CONTINUE%
ItemDisplay[NMAG !RW SK40=2]: %NAME%%NL%+2 Cold Enchant%CONTINUE%
ItemDisplay[NMAG !RW SK40=3]: %NAME%%NL%+3 Cold Enchant%CONTINUE%
ItemDisplay[NMAG !RW SK41=1]: %NAME%%NL%+1 Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK41=2]: %NAME%%NL%+2 Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK41=3]: %NAME%%NL%+3 Inferno%CONTINUE%
ItemDisplay[NMAG !RW SK42=1]: %NAME%%NL%+1 Static Field%CONTINUE%
ItemDisplay[NMAG !RW SK42=2]: %NAME%%NL%+2 Static Field%CONTINUE%
ItemDisplay[NMAG !RW SK42=3]: %NAME%%NL%+3 Static Field%CONTINUE%
ItemDisplay[NMAG !RW SK43=1]: %NAME%%NL%+1 Telekinesis%CONTINUE%
ItemDisplay[NMAG !RW SK43=2]: %NAME%%NL%+2 Telekinesis%CONTINUE%
ItemDisplay[NMAG !RW SK43=3]: %NAME%%NL%+3 Telekinesis%CONTINUE%
ItemDisplay[NMAG !RW SK44=1]: %NAME%%NL%+1 Frost Nova%CONTINUE%
ItemDisplay[NMAG !RW SK44=2]: %NAME%%NL%+2 Frost Nova%CONTINUE%
ItemDisplay[NMAG !RW SK44=3]: %NAME%%NL%+3 Frost Nova%CONTINUE%
ItemDisplay[NMAG !RW SK45=1]: %NAME%%NL%+1 Ice Blast%CONTINUE%
ItemDisplay[NMAG !RW SK45=2]: %NAME%%NL%+2 Ice Blast%CONTINUE%
ItemDisplay[NMAG !RW SK45=3]: %NAME%%NL%+3 Ice Blast%CONTINUE%
ItemDisplay[NMAG !RW SK46=1]: %NAME%%NL%+1 Blaze%CONTINUE%
ItemDisplay[NMAG !RW SK46=2]: %NAME%%NL%+2 Blaze%CONTINUE%
ItemDisplay[NMAG !RW SK46=3]: %NAME%%NL%+3 Blaze%CONTINUE%
ItemDisplay[NMAG !RW SK47=1]: %NAME%%NL%+1 Fire Ball%CONTINUE%
ItemDisplay[NMAG !RW SK47=2]: %NAME%%NL%+2 Fire Ball%CONTINUE%
ItemDisplay[NMAG !RW SK47=3]: %NAME%%NL%+3 Fire Ball%CONTINUE%
ItemDisplay[NMAG !RW SK48=1]: %NAME%%NL%+1 Nova%CONTINUE%
ItemDisplay[NMAG !RW SK48=2]: %NAME%%NL%+2 Nova%CONTINUE%
ItemDisplay[NMAG !RW SK48=3]: %NAME%%NL%+3 Nova%CONTINUE%
ItemDisplay[NMAG !RW SK49=1]: %NAME%%NL%+1 Lightning%CONTINUE%
ItemDisplay[NMAG !RW SK49=2]: %NAME%%NL%+2 Lightning%CONTINUE%
ItemDisplay[NMAG !RW SK49=3]: %NAME%%NL%+3 Lightning%CONTINUE%
ItemDisplay[NMAG !RW SK50=1]: %NAME%%NL%+1 Shiver Armor%CONTINUE%
ItemDisplay[NMAG !RW SK50=2]: %NAME%%NL%+2 Shiver Armor%CONTINUE%
ItemDisplay[NMAG !RW SK50=3]: %NAME%%NL%+3 Shiver Armor%CONTINUE%
ItemDisplay[NMAG !RW SK51=1]: %NAME%%NL%+1 Fire Wall%CONTINUE%
ItemDisplay[NMAG !RW SK51=2]: %NAME%%NL%+2 Fire Wall%CONTINUE%
ItemDisplay[NMAG !RW SK51=3]: %NAME%%NL%+3 Fire Wall%CONTINUE%
ItemDisplay[NMAG !RW SK52=1]: %NAME%%NL%+1 Enchant Fire%CONTINUE%
ItemDisplay[NMAG !RW SK52=2]: %NAME%%NL%+2 Enchant Fire%CONTINUE%
ItemDisplay[NMAG !RW SK52=3]: %NAME%%NL%+3 Enchant Fire%CONTINUE%
ItemDisplay[NMAG !RW SK53=1]: %NAME%%NL%+1 Chain Light%CONTINUE%
ItemDisplay[NMAG !RW SK53=2]: %NAME%%NL%+2 Chain Light%CONTINUE%
ItemDisplay[NMAG !RW SK53=3]: %NAME%%NL%+3 Chain Light%CONTINUE%
ItemDisplay[NMAG !RW SK54=1]: %NAME%%NL%+1 Teleport%CONTINUE%
ItemDisplay[NMAG !RW SK54=2]: %NAME%%NL%+2 Teleport%CONTINUE%
ItemDisplay[NMAG !RW SK54=3]: %NAME%%NL%+3 Teleport%CONTINUE%
ItemDisplay[NMAG !RW SK55=1]: %NAME%%NL%+1 Glacial Spike%CONTINUE%
ItemDisplay[NMAG !RW SK55=2]: %NAME%%NL%+2 Glacial Spike%CONTINUE%
ItemDisplay[NMAG !RW SK55=3]: %NAME%%NL%+3 Glacial Spike%CONTINUE%
ItemDisplay[NMAG !RW SK56=1]: %NAME%%NL%+1 Meteor%CONTINUE%
ItemDisplay[NMAG !RW SK56=2]: %NAME%%NL%+2 Meteor%CONTINUE%
ItemDisplay[NMAG !RW SK56=3]: %NAME%%NL%+3 Meteor%CONTINUE%
ItemDisplay[NMAG !RW SK57=1]: %NAME%%NL%+1 Thunder Storm%CONTINUE%
ItemDisplay[NMAG !RW SK57=2]: %NAME%%NL%+2 Thunder Storm%CONTINUE%
ItemDisplay[NMAG !RW SK57=3]: %NAME%%NL%+3 Thunder Storm%CONTINUE%
ItemDisplay[NMAG !RW SK58=1]: %NAME%%NL%+1 Energy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK58=2]: %NAME%%NL%+2 Energy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK58=3]: %NAME%%NL%+3 Energy Shield%CONTINUE%
ItemDisplay[NMAG !RW SK59=1]: %NAME%%NL%+1 Blizzard%CONTINUE%
ItemDisplay[NMAG !RW SK59=2]: %NAME%%NL%+2 Blizzard%CONTINUE%
ItemDisplay[NMAG !RW SK59=3]: %NAME%%NL%+3 Blizzard%CONTINUE%
ItemDisplay[NMAG !RW SK60=1]: %NAME%%NL%+1 Chill Armor%CONTINUE%
ItemDisplay[NMAG !RW SK60=2]: %NAME%%NL%+2 Chill Armor%CONTINUE%
ItemDisplay[NMAG !RW SK60=3]: %NAME%%NL%+3 Chill Armor%CONTINUE%
ItemDisplay[NMAG !RW SK61=1]: %NAME%%NL%+1 Fire Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK61=2]: %NAME%%NL%+2 Fire Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK61=3]: %NAME%%NL%+3 Fire Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK62=1]: %NAME%%NL%+1 Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK62=2]: %NAME%%NL%+2 Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK62=3]: %NAME%%NL%+3 Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK63=1]: %NAME%%NL%+1 Light Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK63=2]: %NAME%%NL%+2 Light Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK63=3]: %NAME%%NL%+3 Light Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK64=1]: %NAME%%NL%+1 Frozen Orb%CONTINUE%
ItemDisplay[NMAG !RW SK64=2]: %NAME%%NL%+2 Frozen Orb%CONTINUE%
ItemDisplay[NMAG !RW SK64=3]: %NAME%%NL%+3 Frozen Orb%CONTINUE%
ItemDisplay[NMAG !RW SK65=1]: %NAME%%NL%+1 Cold Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK65=2]: %NAME%%NL%+2 Cold Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK65=3]: %NAME%%NL%+3 Cold Mastery%CONTINUE%
ItemDisplay[NMAG !RW SK369=1]: %NAME%%NL%+1 Ice Barrage%CONTINUE%
ItemDisplay[NMAG !RW SK369=2]: %NAME%%NL%+2 Ice Barrage%CONTINUE%
ItemDisplay[NMAG !RW SK369=3]: %NAME%%NL%+3 Ice Barrage%CONTINUE%
ItemDisplay[NMAG !RW SK383=1]: %NAME%%NL%+1 Lesser Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK383=2]: %NAME%%NL%+2 Lesser Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK383=3]: %NAME%%NL%+3 Lesser Hydra%CONTINUE%
ItemDisplay[NMAG !RW SK376=1]: %NAME%%NL%+1 Combustion%CONTINUE%
ItemDisplay[NMAG !RW SK376=2]: %NAME%%NL%+2 Combustion%CONTINUE%
ItemDisplay[NMAG !RW SK376=3]: %NAME%%NL%+3 Combustion%CONTINUE%

//Show me exactly RES value on PALADIN shields
ItemDisplay[CL3 NMAG RES=5]: %GRAY%[5%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=6]: %GRAY%[6%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=7]: %GRAY%[7%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=8]: %GRAY%[8%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=9]: %GRAY%[9%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=10]: %GRAY%[10%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=11]: %GRAY%[11%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=12]: %GRAY%[12%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=13]: %GRAY%[13%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=14]: %GRAY%[14%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=15]: %GRAY%[15%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=16]: %GRAY%[16%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=17]: %GRAY%[17%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=18]: %GRAY%[18%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=19]: %GRAY%[19%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=20]: %GRAY%[%DARK_GREEN%20%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=21]: %GRAY%[%DARK_GREEN%21%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=22]: %GRAY%[%DARK_GREEN%22%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=23]: %GRAY%[%DARK_GREEN%23%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=24]: %GRAY%[%DARK_GREEN%24%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=25]: %GRAY%[%GREEN%25%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=26]: %GRAY%[%GREEN%26%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=27]: %GRAY%[%GREEN%27%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=28]: %GRAY%[%GREEN%28%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=29]: %GRAY%[%GREEN%29%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=30]: %GRAY%[%GREEN%30%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=31]: %GRAY%[%GREEN%31%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=32]: %GRAY%[%GREEN%32%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=33]: %GRAY%[%GREEN%33%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=34]: %GRAY%[%GREEN%34%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=35]: %GRAY%[%GREEN%35%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=36]: %GRAY%[%GREEN%36%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=37]: %GRAY%[%GREEN%37%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=38]: %GRAY%[%GREEN%38%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=39]: %GRAY%[%GREEN%39%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=40]: %GRAY%[%GREEN%40%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=41]: %GRAY%[%GREEN%41%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=42]: %GRAY%[%GREEN%42%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=43]: %GRAY%[%GREEN%43%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=44]: %GRAY%[%GREEN%44%WHITE%r%GRAY%] %NAME%%CONTINUE%
ItemDisplay[CL3 NMAG RES=45]: %GRAY%[%GREEN%45%WHITE%r%GRAY%] %NAME%%CONTINUE%

//Highlight RW Bases with high DEF
ItemDisplay[xtp !SOCK=1 !ETH !INF NMAG DEF>249]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[(uui OR uea OR ula) (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>449]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[utu (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>459]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[urs (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>479]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[utp (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>499]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[uar (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>574]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[EQ2 ELT !SOCK=1 ETH !INF NMAG DEF>699]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[uit (SOCK=0 OR SOCK=4) !ETH !INF NMAG DEF>139]: %DOT-D6%%NAME%%CONTINUE%
ItemDisplay[uit (SOCK=0 OR SOCK=4) ETH !INF NMAG DEF>209]: %DOT-D6%%NAME%%CONTINUE%

//High DEF Bases (w/o ED)
ItemDisplay[xtp !SOCK=1 !ETH !INF NMAG DEF>249 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[(uui OR uea OR ula) (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>449 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[utu (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>459 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[urs (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>479 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[utp (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>499 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[uar (SOCK=0 OR SOCK>2) !ETH !INF NMAG DEF>574 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[EQ2 ELT !SOCK=1 ETH !INF NMAG DEF>699 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[uit (SOCK=0 OR SOCK=4) !ETH !INF NMAG DEF>139 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[uit (SOCK=0 OR SOCK=4) ETH !INF NMAG DEF>209 ED<5]: %NAME% %DARK_GREEN%*%CONTINUE%

//Superior Bases with ED
//Armors
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=5]: %GRAY%[%BLUE%5%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=5]: %GRAY%[%BLUE%5%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=6]: %GRAY%[%BLUE%6%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=6]: %GRAY%[%BLUE%6%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=7]: %GRAY%[%BLUE%7%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=7]: %GRAY%[%BLUE%7%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=8]: %GRAY%[%BLUE%8%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=8]: %GRAY%[%BLUE%8%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=9]: %GRAY%[%BLUE%9%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=9]: %GRAY%[%BLUE%9%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=10]: %GRAY%[%BLUE%10%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=10]: %GRAY%[%BLUE%10%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=11]: %GRAY%[%BLUE%11%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=11]: %GRAY%[%BLUE%11%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=12]: %GRAY%[%BLUE%12%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=12]: %GRAY%[%BLUE%12%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=13]: %GRAY%[%BLUE%13%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=13]: %GRAY%[%BLUE%13%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=14]: %GRAY%[%BLUE%14%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=14]: %GRAY%[%BLUE%14%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((xtp !SOCK=1) OR ((uui OR uea OR ula OR utu OR urs OR utp OR uar) (SOCK=0 OR SOCK>2)) OR (uit (SOCK=0 OR SOCK=4)) OR (((ush OR xsh) OR (CL3 (EXC OR ELT) RES>19)) (SOCK=0 OR SOCK>1)) OR ((ci3 OR uh9) (SOCK=0 OR SOCK=3))) !ETH !INF SUP NMAG ED=15]: %GRAY%[%BLUE%15%%GRAY%] %NAME% %BLUE%*%CONTINUE%
ItemDisplay[((EQ2 ELT !SOCK=1) OR ((uit OR (CL3 ELT (RES>19 OR AR>100))) (SOCK=0 OR SOCK=4))) ETH !INF SUP NMAG ED=15]: %GRAY%[%BLUE%15%%GRAY%] %NAME% %BLUE%*%CONTINUE%
//Weapons
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=5]: %GRAY%[%RED%5%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=5]: %GRAY%[%RED%5%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=6]: %GRAY%[%RED%6%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=6]: %GRAY%[%RED%6%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=7]: %GRAY%[%RED%7%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=7]: %GRAY%[%RED%7%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=8]: %GRAY%[%RED%8%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=8]: %GRAY%[%RED%8%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=9]: %GRAY%[%RED%9%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=9]: %GRAY%[%RED%9%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=10]: %GRAY%[%RED%10%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=10]: %GRAY%[%RED%10%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=11]: %GRAY%[%RED%11%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=11]: %GRAY%[%RED%11%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=12]: %GRAY%[%RED%12%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=12]: %GRAY%[%RED%12%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=13]: %GRAY%[%RED%13%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=13]: %GRAY%[%RED%13%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=14]: %GRAY%[%RED%14%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=14]: %GRAY%[%RED%14%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((6cb OR 7wa OR 7cr) SOCK=0) OR (((amc OR amb) TABSK0>2) (SOCK=3 OR SOCK=4)) OR (((amd OR ame) TABSK2>2) OR (8rx OR 6rx) SOCK=4) OR (7wa SOCK>3) OR (7cr SOCK>2)) !ETH !INF SUP NMAG ED=15]: %GRAY%[%RED%15%%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[((7kr (SOCK=0 OR SOCK=3)) OR ((7vo OR 7tr OR 7bt OR 7ba OR 7fb OR 7wa OR 7gd OR 7p7 OR 7h7 OR 72h OR 7gs OR 7gm) SOCK=0) OR ((7bt OR 7ba OR 7ga OR 7gi OR 7m7 OR 7gm OR 7fb OR 7gd OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=5) OR ((7gm OR 7gd OR 7p7 OR 7h7) SOCK=6) OR ((7fb OR 7gd OR 7gs OR 7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) SOCK=4) OR ((72h OR 7fb OR 7gd OR 7gs) SOCK=3) OR (7wa SOCK>3)) ETH !INF SUP NMAG ED=15]: %GRAY%[%RED%15%%GRAY%] %NAME% %RED%*%CONTINUE%

//RW Bases with socketing recipes
//Hand of Justice/CTA Scepters
ItemDisplay[(wsp OR 9ws OR 7ws) (SK100>2 OR SK125>2 OR SK108>2) NMAG !INF !SUP SOCK=0]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(wsp OR 9ws OR 7ws) SK117>2 NMAG !INF !SUP SOCK=0]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Spirit Swords
ItemDisplay[crs NMAG !INF !SUP SOCK=0 (ILVL>25 AND ILVL<41) CLVL<80]: %NAME% %TAN%[%DARK_GREEN%Larzuk 4soc%TAN%]{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[crs NMAG !INF !SUP SOCK=0 ILVL>40 CLVL<80]: %NAME% %TAN%[%DARK_GREEN%Cube for 4soc%TAN%]{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[crs NMAG !INF !SUP SOCK=0 ILVL>40]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(bsd OR lsd) NMAG !INF !SUP SOCK=0 ILVL>25 CLVL<80]: %NAME% %TAN%[%DARK_GREEN%Larzuk 4soc%TAN%]{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Flails
ItemDisplay[fla NMAG !INF !SUP SOCK=0]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Daggers
ItemDisplay[7kr NMAG !INF !SUP SOCK=0]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//White
ItemDisplay[WP12 !(wnd OR ywn OR 9wn) (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Splendor
ItemDisplay[NEC (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Memory
ItemDisplay[(cst OR bst OR 8cs OR 8bs OR 6cs OR 6bs OR (wst OR 8ws OR 6ws)) SK58>2 !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Faith/Bows
ItemDisplay[(amc OR amb) TABSK0>2 !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(6cb OR 8rx OR 6rx) !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Infi/Insi/Pride and Obedience/Doom
ItemDisplay[(7vo OR 7tr) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(7wc OR 7pa OR 7s8 OR 7h7 OR 7br OR 7st) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Grief/Beast/Passion
ItemDisplay[7wa !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(7m7 OR 7gm OR 7ga OR 7gi OR 7bt OR 7ba) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Death/Oath
ItemDisplay[7fb ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(7wa OR 7gd) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Breath of the Dying/Last Wish
ItemDisplay[7cr !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(7wa OR 7gd OR 7p7) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Lawbringer
ItemDisplay[(72h OR 7gs) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Chaos
ItemDisplay[(7ar OR 7tw OR 7qr OR 9tw) (SK275>0 OR SK276>0 OR SK278>0) ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Plague
ItemDisplay[(clw OR btl OR skr OR 9ar OR 9lw OR 9tw OR 9qr OR 7ar OR 7wb OR 7lw OR 7tw OR 7qr) (SK262>2 OR SK266>2 OR SK267>2 OR SK271>2 OR SK272>2 OR SK273>2 OR SK276>2 OR SK277>2 OR SK278>2 OR SK265>2 OR (SK278>1 AND SK265>1) OR SK366>2 OR SK280>2) !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(SCEPTER !(scp OR 9sc OR 7sc)) (SK101>2 OR SK112>2 OR SK118>2 OR SK121>2) !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Amazon Spears
ItemDisplay[(amd OR ame) TABSK2>2 !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Armors
ItemDisplay[(xtp OR utp OR uui OR uea OR ula OR utu OR urs OR uar) !ETH !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %YELLOW%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[EQ2 ELT ETH !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %YELLOW%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Helmets
ItemDisplay[CL2 (SK149>2 OR SK154>2) !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CL1 (SK221>2 OR SK225>2 OR SK227>2 OR SK237>2 OR SK238>2 OR SK239>2 OR SK240>2 OR SK243>2 OR SK244>2 OR SK245>2 OR SK247>2 OR SK249>2 OR SK250>2) !ETH !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CL1 (((SK227>1 OR SK221>1) AND SK237>1 AND SK247>1) OR (SK240>1 AND SK245>1 AND SK250>1) OR ((SK240>2 OR SK250>2) AND SK245>2) OR (SK240>2 AND (SK245>2 OR SK250>2))) !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
//Shields
ItemDisplay[CL3 ELT AR>100 ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%GRAY%[%RED%ed%GRAY%] %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CL3 ELT RES>19 ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%GRAY%%NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CL3 (EXC OR ELT) RES>19 !ETH !INF !SUP SOCK=0 NMAG]: %DOT-D6%%GRAY%%NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CL3 RES>19 !ETH !INF !SUP SOCK=0 NMAG CLVL<80]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(ush OR xsh) !ETH !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[uit !INF !SUP SOCK=0 NMAG]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}

//RuneWord Bases SUP SOCK=0 only
//CTA Scepters
ItemDisplay[(wsp OR 9ws OR 7ws) SK117>2 SOCK=0 (INF OR SUP) NMAG]: %DOT-D6%%NAME%
//Daggers
ItemDisplay[7kr SOCK=0 SUP NMAG]: %NAME%
//White
ItemDisplay[WP12 !(wnd OR ywn OR 9wn) (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) SOCK=0 (INF OR SUP) NMAG]: %NAME%
//Splendor
ItemDisplay[NEC (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) SOCK=0 SUP !ETH NMAG]: %DOT-D6%%NAME%
//Memory
ItemDisplay[(cst OR bst OR 8cs OR 8bs OR 6cs OR 6bs) SK58>2 SOCK=0 (INF OR SUP) NMAG]: %DOT-D6%%NAME%
//Bows/Crossbows
ItemDisplay[6cb SOCK=0 SUP NMAG]: %NAME%
//Infi/Insi/Pride and Obedience/Doom
ItemDisplay[(7vo OR 7tr) ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Grief/Beast/Passion
ItemDisplay[(7bt OR 7ba) ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Death/Oath
ItemDisplay[7fb ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Breath of the Dying/Last Wish
ItemDisplay[(7wa OR 7cr) SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
ItemDisplay[(7wa OR 7gd OR 7p7 OR 7h7) ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Hammers
ItemDisplay[7gm ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Lawbringer
ItemDisplay[(72h OR 7gs) ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Chaos
ItemDisplay[(7ar OR 7tw OR 7qr OR 9tw) (SK275>0 OR SK276>0 OR SK278>0) ETH SOCK=0 SUP NMAG]: %DOT-D6%%NAME%
//Plague
ItemDisplay[(SCEPTER !(scp OR 9sc OR 7sc OR wsp OR 9ws OR 7ws)) (SK101>2 OR SK112>2 OR SK118>2 OR SK121>2) SOCK=0 (INF OR SUP) NMAG]: %NAME%
ItemDisplay[(clw OR btl OR skr OR 9ar OR 9lw OR 9tw OR 9qr OR 7ar OR 7wb OR 7lw OR 7tw OR 7qr) (SK262>2 OR SK266>2 OR SK267>2 OR SK271>2 OR SK272>2 OR SK273>2 OR SK276>2 OR SK277>2 OR SK278>2 OR SK265>2 OR (SK278>1 AND SK265>1) OR SK366>2 OR SK280>2) SOCK=0 (INF OR SUP) NMAG]: %DOT-D6%%NAME%
//Armors
ItemDisplay[(xtp OR utp OR uui OR uea OR ula OR utu OR urs OR uar) SOCK=0 SUP NMAG]: %NAME%
ItemDisplay[EQ2 ELT ETH SOCK=0 SUP NMAG]: %NAME%
//Helmets
ItemDisplay[(ci3 OR uh9) SOCK=0 !ETH SUP NMAG]: %DOT-D6%%NAME%
ItemDisplay[CL2 (SK149>2 OR SK154>2) SOCK=0 !ETH SUP NMAG]: %DOT-D6%%NAME%
ItemDisplay[CL1 (SK221>2 OR SK225>2 OR SK227>2 OR SK237>2 OR SK238>2 OR SK239>2 OR SK240>2 OR SK243>2 OR SK244>2 OR SK245>2 OR SK247>2 OR SK249>2 OR SK250>2) SOCK=0 !ETH SUP NMAG]: %NAME%
ItemDisplay[CL1 (((SK227>1 OR SK221>1) AND SK237>1 AND SK247>1) OR (SK240>1 AND SK245>1 AND SK250>1) OR ((SK240>2 OR SK250>2) AND SK245>2) OR (SK240>2 AND (SK245>2 OR SK250>2))) SOCK=0 !ETH SUP NMAG]: %DOT-D6%%NAME%
//Shields
ItemDisplay[CL3 ELT AR>100 SOCK=0 ETH SUP NMAG]: %DOT-D6%%GRAY%[%RED%ed%GRAY%] %NAME%
ItemDisplay[CL3 ELT RES>19 SOCK=0 ETH SUP NMAG]: %DOT-D6%%NAME%
ItemDisplay[CL3 (EXC OR ELT) RES>19 SOCK=0 !ETH SUP NMAG]: %DOT-D6%%NAME%
ItemDisplay[CL3 (RES>19 AND CLVL<80) SOCK=0 !ETH SUP NMAG]: %NAME%
ItemDisplay[(ush OR xsh) SOCK=0 !ETH SUP NMAG]: %NAME%
ItemDisplay[uit SOCK=0 SUP NMAG]: %NAME%

//RuneWord Bases with Notes about Possible RuneWords 
//Chests
ItemDisplay[xtp !INF !ETH NMAG !RW SOCK=2]: %NAME%{%GRAY%Prudence, Smoke, Stealth%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(xtp OR utp OR uui OR uea OR ula OR utu OR urs OR uar) !INF !ETH NMAG !RW SOCK=3]: %NAME%{%GRAY%Peace, Principle, Rain, Treachery, Wealth%NL%Enlightenment, Gloom, Lionheart, Myth,%NL%%TAN%RWs: %GRAY%Bone, Dragon, Duress, Enigma,}
ItemDisplay[(xtp OR utp OR uui OR uea OR ula OR utu OR urs OR uar) !INF !ETH NMAG !RW SOCK=4]: %NAME%{%GRAY%Chains of Honor, Fortitude, Stone%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Bramble,}
ItemDisplay[EQ2 ELT !INF ETH NMAG !RW SOCK=2]: %NAME%{%GRAY%Prudence, Smoke, Stealth%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[EQ2 ELT !INF ETH NMAG !RW SOCK=3]: %NAME%{%GRAY%Peace, Principle, Rain, Treachery, Wealth%NL%Enlightenment, Gloom, Lionheart, Myth,%NL%%TAN%RWs: %GRAY%Bone, Dragon, Duress, Enigma,}
ItemDisplay[EQ2 ELT !INF ETH NMAG !RW SOCK=4]: %NAME%{%GRAY%Chains of Honor, Fortitude, Stone%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Bramble,}
//Helmets
ItemDisplay[(ci3 OR uh9) !INF !ETH NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL2 (SK149>2 OR SK154>2) !INF !ETH NMAG !RW SOCK=2]: %NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL1 (SK221>2 OR SK225>2 OR SK227>2 OR SK237>2 OR SK238>2 OR SK239>2 OR SK240>2 OR SK243>2 OR SK244>2 OR SK245>2 OR SK247>2 OR SK249>2 OR SK250>2) !INF !ETH NMAG !RW SOCK=2]: %NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL1 (((SK227>1 OR SK221>1) AND SK237>1 AND SK247>1) OR (SK240>1 AND SK245>1 AND SK250>1) OR ((SK240>2 OR SK250>2) AND SK245>2) OR (SK240>2 AND (SK245>2 OR SK250>2))) !INF !ETH NMAG !RW SOCK=2]: %DOT-D6%%NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL2 (SK149>2 OR SK154>2) !INF !ETH NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL1 (SK221>2 OR SK225>2 OR SK227>2 OR SK237>2 OR SK238>2 OR SK239>2 OR SK240>2 OR SK243>2 OR SK244>2 OR SK245>2 OR SK247>2 OR SK249>2 OR SK250>2) !INF !ETH NMAG !RW SOCK=3]: %NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL1 (((SK227>1 OR SK221>1) AND SK237>1 AND SK247>1) OR (SK240>1 AND SK245>1 AND SK250>1) OR ((SK240>2 OR SK250>2) AND SK245>2) OR (SK240>2 AND (SK245>2 OR SK250>2))) !INF !ETH NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Shields
ItemDisplay[CL3 ELT !INF ETH NMAG !RW SOCK=4 AR>100]: %DOT-D6%%GRAY%[%RED%ed%GRAY%] %NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL3 ELT !INF ETH NMAG !RW SOCK=4 RES>19]: %DOT-D6%%NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL3 (EXC OR ELT) !INF !ETH NMAG !RW SOCK=2 RES>19]: %DOT-D6%%NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL3 (EXC OR ELT) !INF !ETH NMAG !RW SOCK=3 RES>19]: %DOT-D6%%NAME%{%GRAY%Pledge, Dragon, Dream, Sanctuary%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Ancient's}
ItemDisplay[CL3 (EXC OR ELT) !INF !ETH NMAG !RW SOCK=4 RES>19]: %DOT-D6%%NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL3 !INF !ETH NMAG !RW SOCK=2 RES>19 CLVL<80]: %NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CL3 !INF !ETH NMAG !RW SOCK=3 RES>19 CLVL<80]: %NAME%{%GRAY%Pledge, Dragon, Dream, Sanctuary%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Ancient's}
ItemDisplay[CL3 !INF !ETH NMAG !RW SOCK=4 RES>19 CLVL<80]: %NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(ush OR xsh) !INF !ETH NMAG !RW SOCK=2]: %NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(ush OR xsh) !INF !ETH NMAG !RW SOCK=3]: %NAME%{%GRAY%Pledge, Dragon, Dream, Sanctuary%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Ancient's}
ItemDisplay[uit !INF NMAG !RW SOCK=4]: %NAME%{%GRAY%Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Splendor Shields
ItemDisplay[NEC (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) !INF !ETH SOCK=2 NMAG !RW]: %DOT-D6%%NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Weapons
//Bows/Crossbows
ItemDisplay[(amc OR amb) NMAG !RW TABSK0>2 SOCK=4]: %DOT-D6%%NAME%{%GRAY%Harmony, Ice, Passion, Phoenix, Wrath%NL%Faith, Fortitude, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Brand,}
ItemDisplay[(amc OR amb) NMAG !RW TABSK0>2 SOCK=3]: %NAME%{%GRAY%Edge, Melody, Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[6cb NMAG !RW SOCK=3]: %NAME%{%GRAY%Edge, Melody, Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(6cb OR 8rx OR 6rx) NMAG !RW SOCK=4]: %NAME%{%GRAY%Harmony, Ice, Passion, Phoenix, Wrath%NL%Faith, Fortitude, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Brand,}
//Daggers
ItemDisplay[7kr !INF NMAG !RW SOCK=3]: %NAME%{%GRAY%Fury, Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Axes
ItemDisplay[7wa !INF NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Oath, Passion, Phoenix%NL%Fortitude, Hand of Justice, Kingslayer,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Famine,}
ItemDisplay[7wa !INF NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Eternity, Grief, Honor%NL%Call to Arms, Death, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[7wa !INF NMAG !RW SOCK=6]: %DOT-D6%%NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
ItemDisplay[(7bt OR 7ba OR 7ga OR 7gi) !INF ETH NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Eternity, Grief, Honor%NL%Call to Arms, Death, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
//Hammers
ItemDisplay[(7m7 OR 7gm) !INF ETH NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Doom, Eternity, Honor%NL%Beast, Call to Arms,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[7gm !INF ETH NMAG !RW SOCK=6]: %DOT-D6%%NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
//Scepters
ItemDisplay[(wsp OR 9ws OR 7ws) (SK100>2 OR SK125>2 OR SK108>2) !INF !ETH NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Passion, Phoenix, Rift%NL%Holy Thunder, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(wsp OR 9ws OR 7ws) SK117>2 NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[(wsp OR 9ws OR 7ws) !INF !ETH NMAG !RW SOCK=4]: %NAME%{%GRAY%Passion, Phoenix, Rift%NL%Holy Thunder, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(SCEPTER !(scp OR 9sc OR 7sc)) !INF !ETH NMAG !RW (SK101>2 OR SK112>2 OR SK118>2 OR SK121>2) SOCK=3]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Fury, King's Grace, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Swords
ItemDisplay[crs NMAG SOCK=0 (ILVL>25 AND ILVL<41) CLVL<80]: %NAME% %TAN%[%DARK_GREEN%Larzuk 4soc%TAN%]
ItemDisplay[(bsd OR lsd) NMAG SOCK=0 ILVL>25 CLVL<80]: %NAME% %TAN%[%DARK_GREEN%Larzuk 4soc%TAN%]
ItemDisplay[(crs OR bsd OR lsd) NMAG !RW SOCK=4]: %NAME%{%GRAY%Phoenix, Spirit, Voice of Reason%NL%Hand of Justice, Kingslayer, Oath, Passion,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[crs NMAG !RW SOCK=5]: %NAME%{%GRAY%Destruction, Grief, Honor%NL%Call to Arms, Eternity, Death,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[7cr NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Lawbringer, Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury, King's Grace,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[7cr NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Phoenix, Spirit, Voice of Reason%NL%Hand of Justice, Kingslayer, Oath, Passion,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[7cr NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Destruction, Grief, Honor%NL%Call to Arms, Eternity, Death,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[7cr NMAG !RW SOCK=6]: %DOT-D6%%NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
ItemDisplay[(72h OR 7fb OR 7gd OR 7gs) ETH NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Lawbringer, Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury, King's Grace,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(7fb OR 7gd OR 7gs) ETH NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Phoenix, Spirit, Voice of Reason%NL%Hand of Justice, Kingslayer, Oath, Passion,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(7fb OR 7gd) ETH NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Destruction, Grief, Honor%NL%Call to Arms, Eternity, Death,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[7gd ETH NMAG !RW SOCK=6]: %DOT-D6%%NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
//Maces
ItemDisplay[fla NMAG !RW !INF SOCK=3]: %NAME%{%GRAY%Fury, Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Black,}
ItemDisplay[fla NMAG !RW !INF SOCK=4]: %NAME%{%GRAY%Oath, Passion, Phoenix, Voice of Reason%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[fla NMAG !RW !INF SOCK=5]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Wands
ItemDisplay[WP12 (SK67>2 OR SK74>2 OR SK94>2 OR SK75>2 OR SK70>2 OR SK84>2 OR SK83>2 OR SK92>2 OR SK93>2 OR SK79>2 OR SK80>2 OR SK85>2 OR SK95>2) SOCK=2 NMAG !RW]: %NAME%{%GRAY%Strength, White%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Staves
ItemDisplay[(cst OR bst OR 8cs OR 8bs OR 6cs OR 6bs OR wst OR 8ws OR 6ws) SK58>2 NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Insight, Memory, Passion, Phoenix%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(wst OR 8ws OR 6ws) SK58>2 NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Polearms/Spears/Amazon Spears
ItemDisplay[(7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) ETH NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Passion, Phoenix, Pride, Rift%NL%Hand of Justice, Infinity, Insight,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(7wc OR 7pa OR 7s8 OR 7vo OR 7h7 OR 7tr OR 7br OR 7st OR 7p7) ETH NMAG !RW SOCK=5]: %DOT-D6%%NAME%{%GRAY%Eternity, Honor, Obedience%NL%Call to Arms, Destruction, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(7p7 OR 7h7) ETH NMAG !RW SOCK=6]: %DOT-D6%%NAME%{%GRAY%Breath of the Dying, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(amd OR ame) TABSK2>2 !ETH !INF NMAG !RW SOCK=4]: %DOT-D6%%NAME%{%GRAY%Passion, Phoenix, Pride, Rift%NL%Hand of Justice, Infinity, Insight,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
//Claws
ItemDisplay[(7ar OR 7tw OR 7qr OR 9tw) (SK275>0 OR SK276>0 OR SK278>0) !INF ETH NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Pattern, Plague, Venom, Wind%NL%Chaos, Fury, Malice,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(clw OR btl OR skr OR 9ar OR 9lw OR 9tw OR 9qr OR 7ar OR 7wb OR 7lw OR 7tw OR 7qr) (SK262>2 OR SK266>2 OR SK267>2 OR SK271>2 OR SK272>2 OR SK273>2 OR SK276>2 OR SK277>2 OR SK278>2 OR SK265>2 OR (SK278>1 AND SK265>1) OR SK366>2 OR SK280>2) !INF NMAG !RW SOCK=3]: %DOT-D6%%NAME%{%GRAY%Pattern, Plague, Venom, Wind%NL%Chaos, Fury, Malice,%NL%%TAN%Note%WHITE%: Possible RuneWords:}

//Notes for upgrading
ItemDisplay[ARMOR NORM RARE ID]: %NAME%{%YELLOW%This Item %WHITE%+ %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR EXC RARE ID]: %NAME%{%YELLOW%This Item %WHITE%+ %ORANGE%Ko %WHITE%+ %ORANGE%Pul %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON NORM RARE ID]: %NAME%{%YELLOW%This Item %WHITE%+ %ORANGE%Ort %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON EXC RARE ID]: %NAME%{%YELLOW%This Item %WHITE%+ %ORANGE%Fal %WHITE%+ %ORANGE%Um %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR NORM CRAFT ID]: %NAME%{%ORANGE%This Item %WHITE%+ %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR EXC CRAFT ID]: %NAME%{%ORANGE%This Item %WHITE%+ %ORANGE%Ko %WHITE%+ %ORANGE%Pul %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON NORM CRAFT ID]: %NAME%{%ORANGE%This Item %WHITE%+ %ORANGE%Ort %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON EXC CRAFT ID]: %NAME%{%ORANGE%This Item %WHITE%+ %ORANGE%Fal %WHITE%+ %ORANGE%Um %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR NORM UNI ID]: %NAME%{%GOLD%This Item %WHITE%+ %ORANGE%Tal %WHITE%+ %ORANGE%Shael %WHITE%+ Perf O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR EXC UNI ID]: %NAME%{%GOLD%This Item %WHITE%+ %ORANGE%Ko %WHITE%+ %ORANGE%Lem %WHITE%+ Perf O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON NORM UNI ID]: %NAME%{%GOLD%This Item %WHITE%+ %ORANGE%Ral %WHITE%+ %ORANGE%Sol %WHITE%+ Perf %GREEN%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON EXC UNI ID]: %NAME%{%GOLD%This Item %WHITE%+ %ORANGE%Lum %WHITE%+ %ORANGE%Pul %WHITE%+ Perf %GREEN%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR NORM SET ID]: %NAME%{%GREEN%This Item %WHITE%+ %ORANGE%Tal %WHITE%+ %ORANGE%Shael %WHITE%+ Perf O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[ARMOR EXC SET ID]: %NAME%{%GREEN%This Item %WHITE%+ %ORANGE%Ko %WHITE%+ %ORANGE%Lem %WHITE%+ Perf O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON NORM SET ID]: %NAME%{%GREEN%This Item %WHITE%+ %ORANGE%Ral %WHITE%+ %ORANGE%Sol %WHITE%+ Perf %GREEN%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}
ItemDisplay[WEAPON EXC SET ID]: %NAME%{%GREEN%This Item %WHITE%+ %ORANGE%Lum %WHITE%+ %ORANGE%Pul %WHITE%+ Perf %GREEN%O%NL%%TAN%Note%WHITE%: Upgrading Recipe:}

//Potentially expensive (Woth some GOLD) items
ItemDisplay[(7tk OR 7bk OR 7ta) (NMAG OR ((MAG OR RARE) !ID)) !ETH !INF]: %NAME% %GRAY%(%TAN%$%WHITE%%PRICE%%GRAY%)
ItemDisplay[(WAND OR SOR) (SK86>1 OR SK87>1 OR SK88>1 OR SK89>1 OR SK90>1 OR SK91>1 OR SK92>1 OR SK93>1 OR SK94>1 OR SK95>1 OR SK56>1 OR SK57>1 OR SK58>1 OR SK59>1 OR SK60>1 OR SK61>1 OR SK62>1 OR SK63>1 OR SK64>1 OR SK65>1) !ETH !INF NMAG CLVL>79]: %NAME%

//Show me quantitiy of all stackables
ItemDisplay[!(ARMOR OR WEAPON OR tbk OR ibk) QTY>0]: %NAME% %TAN%x %WHITE%%QTY%%CONTINUE%

//Standard of Heroes
ItemDisplay[std]: %PX-9D%%NAME%{%WHITE%+10% Experience%NL%+20% Magic&Gold Find%NL%+20% Monster Density%NL%%TAN%Note: %WHITE%Cube it with Map to gain:}

//Always show me those items
ItemDisplay[UNI OR SET OR RW OR CRAFT]: %NAME%

//Show me every identified item
ItemDisplay[(ARMOR OR WEAPON) (MAG OR RARE OR SET OR UNI OR CRAFT) ID]: %NAME%

//Project Diablo 2 items
ItemDisplay[wss]: %MAP-0A%%NAME% %ORANGE%*{%RED%Warning%WHITE%: It can Brick your Item/Map%NL%%TAN%Note%WHITE%: Use it to %RED%Corrupt %WHITE%Item/Map:}
ItemDisplay[scrb]: %BORDER-A9%%NAME% %ORANGE%*{%RED%Group Dungeon%NL%%TAN%Note%WHITE%: Cube it with %GRAY%[%ORANGE%T3%GRAY%] %WHITE%Map to Make:}
ItemDisplay[imra]: %NAME% %ORANGE%*{%WHITE%Map + %GOLD%Orb %WHITE%+ %BLUE%Jewel %WHITE%+ %ORANGE%Rune>9%NL%%TAN%Note%WHITE%: Imbue White Map to %YELLOW%Rare%WHITE%:}
ItemDisplay[rera]: %NAME% %ORANGE%*{%YELLOW%Map %WHITE%+ %GOLD%Orb %WHITE%+ Perf Gem + %ORANGE%Rune>9%NL%%TAN%Note%WHITE%: Reroll %YELLOW%Rare %WHITE%Map:}
ItemDisplay[upma]: %NAME% %ORANGE%*{%BLUE%Map %WHITE%+ %GOLD%Orb %WHITE%+ Perf %GRAY%O %WHITE%+ %ORANGE%Rune>9%NL%%TAN%Note%WHITE%: Imbue %BLUE%Magic %WHITE%Map to %YELLOW%Rare%WHITE%:}
ItemDisplay[imma]: %NAME% %ORANGE%*{%WHITE%Map + %GOLD%Orb %WHITE%+ %BLUE%Jewel %NL%%TAN%Note%WHITE%: Imbue White Map to %BLUE%Magic%WHITE%:}
ItemDisplay[scou]: %NAME% %ORANGE%*{%BLUE%M%WHITE%a%YELLOW%p %WHITE%+ %GOLD%Orb %WHITE%+ %ORANGE%Hel Rune%NL%%TAN%Note%WHITE%: Imbue %BLUE%Magic%WHITE%/%YELLOW%Rare %WHITE%Map to White:}
ItemDisplay[upmp]: %NAME% %ORANGE%*{%WHITE%3x%BLUE%M%WHITE%a%YELLOW%p %TAN%(%WHITE%Tier:%ORANGE%x%TAN%) %WHITE%+ %GOLD%Orb %WHITE%= Map %TAN%(%WHITE%Tier:%ORANGE%x%WHITE%+1%TAN%)%NL%Note%WHITE%: Upgrade Maps for higher Tier:}
ItemDisplay[lbox]: %BORDER-0A%%NAME% %ORANGE%*%NL%%GREEN%pick me up{%WHITE%Two-Handed Weapon = 4 max%NL%One-Handed Weapon = 2 max%NL%Helmet, Chest, Shield = 2 max%NL%%TAN%Note%WHITE%: Use it to %TAN%Socket %WHITE%an Item}

//Project Diablo 2 Maps
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49) NMAG]: %WHITE%%NAME%%CONTINUE%
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49) MAG]: %BLUE%%NAME%%CONTINUE%
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49) RARE]: %YELLOW%%NAME%%CONTINUE%
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19)]: %GRAY%[%DARK_GREEN%T1%GRAY%] %NAME% %DARK_GREEN%*%CONTINUE%
ItemDisplay[(t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29)]: %GRAY%[%TAN%T2%GRAY%] %NAME% %TAN%*%CONTINUE%
ItemDisplay[(t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39)]: %GRAY%[%ORANGE%T3%GRAY%] %NAME% %ORANGE%*%CONTINUE%
ItemDisplay[(t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49)]: %GRAY%[%RED%Dungeon%GRAY%] %NAME% %RED%*%CONTINUE%
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49) (!ID OR NMAG)]: %MAP-7F%%NAME%%CONTINUE%
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49) MAG]: %NAME%{%WHITE%To Modify Maps visit Anya%NL%%TAN%Note%WHITE%: to Reroll: Cube with 3xPerf %GRAY%O}
ItemDisplay[(t10 OR t11 OR t12 OR t13 OR t14 OR t15 OR t16 OR t17 OR t18 OR t19 OR t20 OR t21 OR t22 OR t23 OR t24 OR t25 OR t26 OR t27 OR t28 OR t29 OR t30 OR t31 OR t32 OR t33 OR t34 OR t35 OR t36 OR t37 OR t38 OR t39 OR t40 OR t41 OR t42 OR t43 OR t44 OR t45 OR t46 OR t47 OR t48 OR t49)]: %NAME%{%TAN%Note%WHITE%: To Modify Maps visit Anya}
ItemDisplay[dcma]: %MAP-0A%%GRAY%*%RED%* %NAME% %RED%*%GRAY%*{%RED%DO IT AT YOUR OWN RISK!%NL%%TAN%Note%WHITE%: %GRAY%You better not go in there...}
ItemDisplay[dcbl OR dcho OR dcso]: %MAP-0A%%NAME% %RED%*{%TAN%Note%WHITE%: %RED%Diablo Clone %GRAY%walks nearby...}

//Essences
ItemDisplay[tes]: %PX-9D%%NAME%{%TAN%Essence %WHITE%from: %BLUE%Andariel %WHITE%or %BLUE%Duriel}
ItemDisplay[ceh]: %PX-9D%%NAME%{%TAN%Essence %WHITE%from: %TAN%Mephisto}
ItemDisplay[bet]: %PX-9D%%NAME%{%TAN%Essence %WHITE%from: %RED%Diablo}
ItemDisplay[fed]: %PX-9D%%NAME%{%TAN%Essence %WHITE%from: %DARK_GREEN%Baal}

//Uber Keys
ItemDisplay[pk1]: %PX-9D%%NAME%{%TAN%Key %WHITE%from: %RED%Countess %WHITE%or %RED%Blood Raven}
ItemDisplay[pk2]: %PX-9D%%NAME%{%TAN%Key %WHITE%from: %BLUE%Summoner %WHITE%or %BLUE%Bloodwitch}
ItemDisplay[pk3]: %PX-9D%%NAME%{%TAN%Key %WHITE%from: %PURPLE%Nihlathak %WHITE%or %PURPLE%Izual}

//Organs
ItemDisplay[mbr]: %PX-9D%%NAME%{%WHITE%to open %GRAY%Uber %RED%Tristram%NL%%TAN%Note%WHITE%: Cube %ORANGE%ANY %WHITE%3 Organs}
ItemDisplay[bey]: %PX-9D%%NAME%{%WHITE%to open %GRAY%Uber %RED%Tristram%NL%%TAN%Note%WHITE%: Cube %ORANGE%ANY %WHITE%3 Organs}
ItemDisplay[dhn]: %PX-9D%%NAME%{%WHITE%to open %GRAY%Uber %RED%Tristram%NL%%TAN%Note%WHITE%: Cube %ORANGE%ANY %WHITE%3 Organs}

//Runes Notes
ItemDisplay[r01s]: %NAME%{%TAN%Note%WHITE%: 3xEl + %GRAY%key %WHITE%= Eld%NL%%NL%Shield: +15 Defense%NL%Armor/Helm: +15 Defense%NL%Weapon: +50 Attack Rating%NL%}
ItemDisplay[r02s]: %NAME%{%TAN%Note%WHITE%: 3xEld + %GRAY%key %WHITE%= Tir%NL%%NL%Shield: 7% Block Chance%NL%Armor/Helm: -15% Stamina Drain%NL%Weapon: +75% Dmg, +50 AR vs Undead%NL%}
ItemDisplay[r03s]: %NAME%{%TAN%Note%WHITE%: 3xTir + %GRAY%key %WHITE%= Nef%NL%%NL%Shield: +2 to Mana per Kill%NL%Armor/Helm: +2 to Mana per Kill%NL%Weapon: +2 to Mana per Kill%NL%}
ItemDisplay[r04s]: %NAME%{%TAN%Note%WHITE%: 3xNef + %GRAY%key %WHITE%= Eth%NL%%NL%Shield: +30 Defense Vs. Missile%NL%Armor/Helm: +30 Defense Vs. Missile%NL%Weapon: Knockback%NL%}
ItemDisplay[r05s]: %NAME%{%TAN%Note%WHITE%: 3xEth + %GRAY%key %WHITE%= Ith%NL%%NL%Shield: Regenerate Mana 15%%NL%Armor/Helm: Regenerate Mana 15%%NL%Weapon: -25% Target Defense%NL%}
ItemDisplay[r06s]: %NAME%{%TAN%Note%WHITE%: 3xIth + %GRAY%key %WHITE%= Tal%NL%%NL%Shield: 15% Damage to Mana%NL%Armor/Helm: 15% Damage to Mana%NL%Weapon: +9 to Max Damage%NL%}
ItemDisplay[r07s]: %NAME%{%TAN%Note%WHITE%: 3xTal + %GRAY%key %WHITE%= Ral%NL%%NL%Shield: Psn Res +35%%NL%Armor/Helm: Psn Res +30%%NL%Weapon: +75 Psn Dmg Over 5 Sec%NL%}
ItemDisplay[r08s]: %NAME%{%TAN%Note%WHITE%: 3xRal + %GRAY%key %WHITE%= Ort%NL%%NL%Shield: Fire Resist +35%%NL%Armor/Helm: Fire Resist +30%%NL%Weapon: +5-30 Fire Dmg%NL%}
ItemDisplay[r09s]: %NAME%{%TAN%Note%WHITE%: 3xOrt + %GRAY%key %WHITE%= Thul%NL%%NL%Shield: Light Resist +35%%NL%Armor/Helm: Light Resist +30%%NL%Weapon: +1-50 Light Dmg%NL%}
ItemDisplay[r10s]: %NAME%{%TAN%Note%WHITE%: 3xThul + %GRAY%key %WHITE%= Amn%NL%%NL%Shield: Cold Resist +35%%NL%Armor/Helm: Cold Resist +30%%NL%Weapon: +3-14 Cold Dmg%NL%}
ItemDisplay[r11s]: %NAME%{%TAN%Note%WHITE%: 3xAmn + %GRAY%key %WHITE%= Sol%NL%%NL%Shield: Attacker Takes Dmg 14%NL%Armor/Helm: Attacker Takes Dmg 14%NL%Weapon: 7% Life Leech%NL%}
ItemDisplay[r12s]: %NAME%{%TAN%Note%WHITE%: 3xSol + %GRAY%key %WHITE%= Shael%NL%%NL%Shield: Damage Reduced by 7%NL%Armor/Helm: Damage Reduced by 7%NL%Weapon: +9 to Min Damage%NL%}
ItemDisplay[r13s]: %NAME%{%TAN%Note%WHITE%: 3xShael + %GRAY%key %WHITE%= Dol%NL%%NL%Shield: 20% Fast Block%NL%Armor/Helm: 20% Fast Hit Recovery%NL%Weapon: 20% Inc Attack Speed%NL%}
ItemDisplay[r14s]: %NAME%{%TAN%Note%WHITE%: 3xDol + %GRAY%key %WHITE%= Hel%NL%%NL%Shield: Replenish Life +10%NL%Armor/Helm: Replenish Life +10%NL%Weapon: 25% Enhanced Damage%NL%}
ItemDisplay[r15s]: %NAME%{%TAN%Note%WHITE%: 3xHel + %GRAY%key %WHITE%= Io%NL%%NL%Shield: Requirements -15%%NL%Armor/Helm: Requirements -15%%NL%Weapon: Requirements -20%%NL%}
ItemDisplay[r16s]: %NAME%{%TAN%Note%WHITE%: 3xIo + %GRAY%key %WHITE%= Lum%NL%%NL%Shield: +10 to Vitality%NL%Armor/Helm: +10 to Vitality%NL%Weapon: +10 to Vitality%NL%}
ItemDisplay[r17s]: %NAME%{%TAN%Note%WHITE%: 3xLum + %GRAY%key %WHITE%= Ko%NL%%NL%Shield: +10 to Energy%NL%Armor/Helm: +10 to Energy%NL%Weapon: +10 to Energy%NL%}
ItemDisplay[r18s]: %NAME%{%TAN%Note%WHITE%: 3xKo + %GRAY%key %WHITE%= Fal%NL%%NL%Shield: +10 to Dexterity%NL%Armor/Helm: +10 to Dexterity%NL%Weapon: +10 to Dexterity%NL%}
ItemDisplay[r19s]: %NAME%{%TAN%Note%WHITE%: 3xFal + %GRAY%key %WHITE%= Lem%NL%%NL%Shield: +10 to Strength%NL%Armor/Helm: +10 to Strength%NL%Weapon: +10 to Strength%NL%}
ItemDisplay[r20s]: %NAME%{%TAN%Note%WHITE%: 3xLem + %GRAY%key %WHITE%= Pul%NL%%NL%Shield: 50% Extra Gold%NL%Armor/Helm: 50% Extra Gold%NL%Weapon: 75% Extra Gold%NL%}
ItemDisplay[r21s]: %NAME%{%TAN%Note%WHITE%: 2xPul + %GRAY%key %WHITE%= Um%NL%%NL%Shield: 30% Enhanced Def%NL%Armor/Helm: 30% Enhanced Def%NL%Weapon: +75% Dmg, +100 AR vs Demon%NL%}
ItemDisplay[r22s]: %NAME%{%TAN%Note%WHITE%: 2xUm + %GRAY%key %WHITE%= Mal%NL%%NL%Shield: All Res +22%NL%Armor/Helm: All Res +15%NL%Weapon: 25% Chance of Open Wounds%NL%}
ItemDisplay[r23s]: %NAME%{%TAN%Note%WHITE%: 2xMal + %GRAY%key %WHITE%= Ist%NL%%NL%Shield: Magic Dmg Red by 7%NL%Armor/Helm: Magic Dmg Red by 7%NL%Weapon: Prevent Monster Heal%NL%}
ItemDisplay[r24s]: %NAME%{%TAN%Note%WHITE%: 2xIst + %GRAY%key %WHITE%= Gul%NL%%NL%Shield: 25% Magic Find%NL%Armor/Helm: 25% Magic Find%NL%Weapon: 30% Magic Find%NL%}
ItemDisplay[r25s]: %NAME%{%TAN%Note%WHITE%: 2xGul + %GRAY%key %WHITE%= Vex%NL%%NL%Shield: +4% to Max Psn Res%NL%Armor/Helm: +4% to Max Psn Res%NL%Weapon: +20% to Attack Rating%NL%}
ItemDisplay[r26s]: %NAME%{%TAN%Note%WHITE%: 2xVex + %GRAY%key %WHITE%= Ohm%NL%%NL%Shield: +4% to Max Fire Res%NL%Armor/Helm: +4% to Max Fire Res%NL%Weapon: 7% Mana Leech%NL%}
ItemDisplay[r27s]: %NAME%{%TAN%Note%WHITE%: 2xOhm + %GRAY%key %WHITE%= Lo%NL%%NL%Shield: +4% to Max Cold Res%NL%Armor/Helm: +4% to Max Cold Res%NL%Weapon: 50% Enhanced Damage%NL%}
ItemDisplay[r28s]: %NAME%{%TAN%Note%WHITE%: 2xLo + %GRAY%key %WHITE%= Sur%NL%%NL%Shield: +4% to Max Light Res%NL%Armor/Helm: +4% to Max Light Res%NL%Weapon: 20% Deadly Strike%NL%}
ItemDisplay[r29s]: %NAME%{%TAN%Note%WHITE%: 2xSur + %GRAY%key %WHITE%= Ber%NL%%NL%Shield: +50 to Mana%NL%Armor/Helm: Inc Max Mana 5%%NL%Weapon: +4 Life After Each Kill%NL%}
ItemDisplay[r30s]: %NAME%{%TAN%Note%WHITE%: 2xBer + %GRAY%key %WHITE%= Jah%NL%%NL%Shield: Dmg Red by 4%%NL%Armor/Helm: Dmg Red by 4%%NL%Weapon: 20% Chance of Crushing Blow%NL%}
ItemDisplay[r31s]: %NAME%{%TAN%Note%WHITE%: 2xJah + %GRAY%key %WHITE%= Cham%NL%%NL%Shield: +50 to Life%NL%Armor/Helm: Inc Max Life 5%%NL%Weapon: Ignore Target's Defense%NL%}
ItemDisplay[r32s]: %NAME%{%TAN%Note%WHITE%: 2xCham + %GRAY%key %WHITE%= Zod%NL%%NL%Shield: Cannot be Frozen%NL%Armor/Helm: Cannot be Frozen%NL%Weapon: Freezes Target +3%NL%}
ItemDisplay[r33s]: %NAME%{%TAN%Note%WHITE%: Zod + Perf %GRAY%O %WHITE%= Repair any Item%NL%%NL%%WHITE%Shield: Indestructible%NL%Armor/Helm: Indestructible%NL%Weapon: Indestructible%NL%}
ItemDisplay[RUNE>0]: %NAME%{%TAN%Note%WHITE%: Cube %ORANGE%Runes %WHITE%to %GRAY%(un)%WHITE%stack them%NL%}

//Gems Notes
ItemDisplay[gzvs]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: +24 Def%NL%Armor/Helm: +8 to Strength%NL%Weapon: +100 to Attack Rating%NL%}
ItemDisplay[glys]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: 28% Light Res%NL%Armor/Helm: 20% Magic Find%NL%Weapon: 1-30 Light Damage%NL%}
ItemDisplay[glbs]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: 28% Cold Res%NL%Armor/Helm: +31 to Mana%NL%Weapon: 6-10 Cold Damage%NL%}
ItemDisplay[glgs]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: 28% Psn Res%NL%Armor/Helm: +8 Dexterity%NL%Weapon: +60 Psn Dmg over 6 Sec%NL%}
ItemDisplay[glrs]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: 28% Fire Res%NL%Armor/Helm: +31 to Life%NL%Weapon: 10-16 Fire Dmg%NL%}
ItemDisplay[glws]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: All Res +14%%NL%Armor/Helm: +80 to AR%NL%Weapon: +54% Dmg vs Undead%NL%}
ItemDisplay[skls]: %NAME%{%TAN%Note%WHITE%: 3xFlawless + %GRAY%key %WHITE%= Perf%NL%%NL%%WHITE%Shield: Atcker+16Dmg%NL%Armor/Helm: Rep Life 4, Reg Mana 12%%NL%Weapon: 3%Life 3%Mana %NL%}
ItemDisplay[gpvs]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: +30 Def%NL%Armor/Helm: +10 to Strength%NL%Weapon: +150 to Attack Rating%NL%}
ItemDisplay[gpys]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: 40% Light Res%NL%Armor/Helm: 24% Magic Find%NL%Weapon: 1-40 Light Damage%NL%}
ItemDisplay[gpbs]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: 40% Cold Res%NL%Armor/Helm: +38 to Mana%NL%Weapon: 10-14 Cold Damage%NL%}
ItemDisplay[gpgs]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: 40% Psn Res%NL%Armor/Helm: +10 Dexterity%NL%Weapon: +100 Psn Dmg over 7 Sec%NL%}
ItemDisplay[gprs]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: 40% Fire Res%NL%Armor/Helm: +38 to Life%NL%Weapon: 15-20 Fire Dmg%NL%}
ItemDisplay[gpws]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: All Res +19%%NL%Armor/Helm: +100 to AR%NL%Weapon: +68% Dmg vs Undead%NL%}
ItemDisplay[skzs]: %PX-70%%NAME%{%TAN%Note%WHITE%: Cube Gems to %GRAY%(un)%WHITE%stack%NL%%NL%%WHITE%Shield: Atcker+20Dmg%NL%Armor/Helm: Rep Life 5, Reg Mana 19%%NL%Weapon: 4%Life 3%Mana %NL%}

//HIDE EVERYTHING ELSE part 1
ItemDisplay[(ARMOR OR WEAPON) (MAG OR RARE) CLVL<41]: %NAME%
ItemDisplay[(ARMOR OR WEAPON) (EXC OR ELT) (MAG OR RARE) (CLVL>40 AND CLVL<80)]: %NAME%
ItemDisplay[((CHEST OR HELM OR SHIELD) OR (WEAPON AND !THROWING)) (EXC OR ELT) NMAG !ETH SUP SOCK=0 CLVL<80]: %NAME%
ItemDisplay[((CHEST OR HELM OR SHIELD) OR (WEAPON AND !THROWING)) (EXC OR ELT) NMAG !ETH !INF SOCK=0 CLVL<80]: %NAME%%CONTINUE%
ItemDisplay[((POLEARM OR SPEAR) AND !THROWING) NMAG ETH !INF SOCK=0 CLVL<80]: %NAME%%CONTINUE%

//Notes about Possible RuneWords
//Chest, Head, Shield
ItemDisplay[CHEST NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Prudence, Smoke, Stealth%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CHEST NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Peace, Principle, Rain, Treachery, Wealth%NL%Enlightenment, Gloom, Lionheart, Myth,%NL%%TAN%RWs: %GRAY%Bone, Dragon, Duress, Enigma,}
ItemDisplay[CHEST NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Chains of Honor, Fortitude, Stone%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Bramble,}
ItemDisplay[(HELM OR CIRC) NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(HELM OR CIRC) NORM !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Pledge, Dragon, Dream, Sanctuary%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Ancient's}
ItemDisplay[CL3 NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CHEST (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Prudence, Smoke, Stealth%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[CHEST (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Principle, Rain, Treachery, Wealth%NL%Gloom, Lionheart, Myth, Peace,%NL%Dragon, Duress, Enigma, Enlightenment,%NL%%TAN%RWs: %GRAY%Bone,}
ItemDisplay[CHEST (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Chains of Honor, Fortitude, Stone%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Bramble,}
ItemDisplay[(HELM OR CIRC) (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(HELM OR CIRC) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Pledge, Dragon, Dream, Sanctuary%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Ancient's}
ItemDisplay[CL3 (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Exile, Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SHIELD (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Phoenix, Spirit%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Weapons 2soc
ItemDisplay[(BOW OR XBOW) NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Zephyr%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WAND NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Strength, White%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[STAFF NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Leaf, Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(SWORD OR AXE OR mac OR mst OR fla) !leg NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Steel, Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR OR leg) NORM !INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(BOW OR XBOW) (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Zephyr%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WAND (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Strength, White%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[STAFF (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Leaf, Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(SWORD OR AXE OR 9ma OR 9mt OR 9fl OR 7ma OR 7mt OR 7fl) (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Steel, Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR) (EXC OR ELT) !INF SOCK=2 NMAG !RW CLVL<80]: %NAME%{%GRAY%Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Weapons 3soc
ItemDisplay[(BOW OR XBOW) NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Edge, Melody, Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SIN NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Pattern, Plague, Venom, Wind%NL%Chaos, Fury, Malice,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(AXE OR POLEARM) NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SWORD NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Lawbringer, Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury, King's Grace,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Fury, King's Grace, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(clb OR spc OR mac OR mst OR fla) NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Fury, Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Black,}
ItemDisplay[(whm OR mau OR gma) NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Black, Fury, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR OR leg) NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fury,}
ItemDisplay[WEAPON !leg NORM !INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(BOW OR XBOW) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Edge, Melody, Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SIN (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Pattern, Plague, Venom, Wind%NL%Chaos, Fury, Malice,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(AXE OR POLEARM) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SWORD (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Lawbringer, Malice, Plague, Venom, Wind%NL%Crescent Moon, Fury, King's Grace,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Fury, King's Grace, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(9cl OR 9sp OR 9ma OR 9mt OR 9fl OR 7cl OR 7sp OR 7ma OR 7mt OR 7fl) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Fury, Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Black,}
ItemDisplay[(9wh OR 9m9 OR 9gm OR 7wh OR 7m7 OR 7gm) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Black, Fury, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR) (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Fury, Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON (EXC OR ELT) !INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Weapons 4soc
ItemDisplay[(BOW OR XBOW) NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Harmony, Ice, Passion, Phoenix, Wrath%NL%Faith, Fortitude, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Brand,}
ItemDisplay[fla NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Oath, Passion, Phoenix, Voice of Reason%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[SWORD NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Phoenix, Spirit, Voice of Reason%NL%Hand of Justice, Kingslayer, Oath, Passion,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(POLEARM OR SPEAR OR JAV) NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Passion, Phoenix, Pride, Rift%NL%Hand of Justice, Infinity, Insight,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[SCEPTER NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Passion, Phoenix, Rift%NL%Holy Thunder, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[AXE NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Oath, Passion, Phoenix%NL%Fortitude, Hand of Justice, Kingslayer,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Famine,}
ItemDisplay[STAFF NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Insight, Memory, Passion, Phoenix%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(whm OR mau OR gma) NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Justice, Passion, Phoenix%NL%Famine, Fortitude, Hand of%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON NORM !INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Hand of Justice, Passion, Phoenix%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(BOW OR XBOW) (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Harmony, Ice, Passion, Phoenix, Wrath%NL%Faith, Fortitude, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Brand,}
ItemDisplay[(9fl OR 7fl) (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Oath, Passion, Phoenix, Voice of Reason%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[SWORD (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Phoenix, Spirit, Voice of Reason%NL%Hand of Justice, Kingslayer, Oath, Passion,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(POLEARM OR SPEAR OR JAV) (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Passion, Phoenix, Pride, Rift%NL%Hand of Justice, Infinity, Insight,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[SCEPTER (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Passion, Phoenix, Rift%NL%Holy Thunder, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[AXE (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Oath, Passion, Phoenix%NL%Fortitude, Hand of Justice, Kingslayer,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Famine,}
ItemDisplay[STAFF (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Insight, Memory, Passion, Phoenix%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[(9wh OR 9m9 OR 9gm OR 7wh OR 7m7 OR 7gm) (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Justice, Passion, Phoenix%NL%Famine, Fortitude, Hand of%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON (EXC OR ELT) !INF SOCK=4 NMAG !RW CLVL<80]: %NAME%{%GRAY%Hand of Justice, Passion, Phoenix%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
//Weapons 5soc
ItemDisplay[SCEPTER NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[(whm OR mau OR gma) NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Doom, Eternity, Honor%NL%Beast, Call to Arms,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[AXE NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Eternity, Grief, Honor%NL%Call to Arms, Death, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[SWORD NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Destruction, Grief, Honor%NL%Call to Arms, Eternity, Death,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(POLEARM OR SPEAR OR JAV) NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Eternity, Honor, Obedience%NL%Call to Arms, Destruction, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR) NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON NORM !INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Call to Arms%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[(9wh OR 9m9 OR 9gm OR 7wh OR 7m7 OR 7gm) (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Doom, Eternity, Honor%NL%Beast, Call to Arms,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[AXE (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Eternity, Grief, Honor%NL%Call to Arms, Death, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[SWORD (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Destruction, Grief, Honor%NL%Call to Arms, Eternity, Death,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(POLEARM OR SPEAR OR JAV) (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Eternity, Honor, Obedience%NL%Call to Arms, Destruction, Doom,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON !(BOW OR XBOW OR SOR) (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WEAPON (EXC OR ELT) !INF SOCK=5 NMAG !RW CLVL<80]: %NAME%{%GRAY%Call to Arms%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Weapons 6soc
ItemDisplay[(AXE OR SWORD OR (whm OR mau OR gma)) NORM !INF SOCK=6 NMAG !RW CLVL<31]: %NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
ItemDisplay[WEAPON NORM !INF SOCK=6 NMAG !RW CLVL<31]: %NAME%{%GRAY%Breath of the Dying, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(AXE OR SWORD OR (9wh OR 9m9 OR 9gm OR 7wh OR 7m7 OR 7gm)) (EXC OR ELT) !INF SOCK=6 NMAG !RW CLVL<80]: %NAME%{%GRAY%of the Dying, Last Wish, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Breath}
ItemDisplay[WEAPON (EXC OR ELT) !INF SOCK=6 NMAG !RW CLVL<80]: %NAME%{%GRAY%Breath of the Dying, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords:}
//Inferior Class Items
ItemDisplay[(SOR OR WAND OR SCEPTER OR STAFF OR DRU OR BAR OR NEC OR (SIN !(NORM OR 9ar OR 9wb OR 9xf))) INF SOCK=0 NMAG !RW CLVL<31]: %NAME%
ItemDisplay[(DRU OR BAR) INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Lore, Nadir%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(DRU OR BAR) INF SOCK=3 NMAG !RW CLVL<80]: %NAME%{%GRAY%Dream, Delirium, Radiance%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[WAND INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Strength, White%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SOR INF SOCK=2 NMAG !RW CLVL<31]: %NAME%
ItemDisplay[SOR INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Plague, Venom%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[STAFF INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Leaf, Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[STAFF INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fury,}
ItemDisplay[STAFF INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Insight, Memory, Passion, Phoenix%NL%Hand of Justice, Heart of the Oak,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[STAFF INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[STAFF INF SOCK=6 NMAG !RW CLVL<31]: %NAME%{%GRAY%Breath of the Dying, Silence%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Malice, Plague, Venom, Wind%NL%Fury, King's Grace, Lawbringer,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[SCEPTER INF SOCK=4 NMAG !RW CLVL<31]: %NAME%{%GRAY%Passion, Phoenix, Rift%NL%Holy Thunder, Hand of Justice,%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Fortitude,}
ItemDisplay[SCEPTER INF SOCK=5 NMAG !RW CLVL<31]: %NAME%{%GRAY%Call to Arms, Eternity, Honor%NL%%TAN%Note%WHITE%: Possible RuneWords: %GRAY%Beast,}
ItemDisplay[(SIN !(NORM OR 9ar OR 9wb OR 9xf)) INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Strength%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[(SIN !(NORM OR 9ar OR 9wb OR 9xf)) INF SOCK=3 NMAG !RW CLVL<31]: %NAME%{%GRAY%Pattern, Plague, Venom, Wind%NL%Chaos, Fury, Malice,%NL%%TAN%Note%WHITE%: Possible RuneWords:}
ItemDisplay[NEC INF SOCK=2 NMAG !RW CLVL<31]: %NAME%{%GRAY%Rhyme, Splendor%NL%%TAN%Note%WHITE%: Possible RuneWords:}

//Notes for socketing
ItemDisplay[CHEST NORM !INF !SUP SOCK=0 NMAG CLVL<31]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %YELLOW%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(WEAPON AND !THROWING) NORM !INF !SUP SOCK=0 NMAG CLVL<31]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(HELM OR CIRC) NORM !INF !SUP SOCK=0 NMAG CLVL<31]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[SHIELD NORM !INF !SUP SOCK=0 NMAG CLVL<31]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[CHEST (EXC OR ELT) !INF !SUP SOCK=0 NMAG CLVL<80]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %YELLOW%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(WEAPON AND !THROWING) (EXC OR ELT) !INF !SUP SOCK=0 NMAG CLVL<80]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %PURPLE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[(HELM OR CIRC) (EXC OR ELT) !INF !SUP SOCK=0 NMAG CLVL<80]: %NAME%{%WHITE%This Item + %ORANGE%Ral %WHITE%+ %ORANGE%Thul %WHITE%+ Perf %BLUE%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}
ItemDisplay[SHIELD (EXC OR ELT) !INF !SUP SOCK=0 NMAG CLVL<80]: %NAME%{%WHITE%This Item + %ORANGE%Tal %WHITE%+ %ORANGE%Amn %WHITE%+ Perf %RED%O%NL%%TAN%Note%WHITE%: Socketing Recipe:}

//HIDE EVERYTHING ELSE part 2
ItemDisplay[(am5 OR ama OR amf) NMAG !RW TABSK2>0 CLVL<31]: %NAME%
ItemDisplay[(am5 OR ama OR amf) NMAG !RW TABSK2>2 CLVL<80]: %NAME%
ItemDisplay[(ARMOR OR WEAPON) INF]: 
ItemDisplay[(ARMOR OR WEAPON) !leg CLVL>30]: 

//It???s just different sizes. BORDER > MAP > DOT > PX.

