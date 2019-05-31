# CS526
Escape FPS Game Implementation
How to use:
1. Use ThirdPerson_BP in Unreal Engine 4
2. Replace Mannequin->Animations->ThirdPerson_AnimBP with the according file
3. Replace Mannequin\Character\Mesh files with 3 according files
4. Use:
AK as weapon
Projectile_Base as bullet
Simple_AI as dummy
Man_With_AK_47 as player


Reference:
https://www.youtube.com/watch?v=DywBqQtTHMo&list=PLL0cLF8gjBprG6487lxqSq-aEo6ZXLDLg&index=1
==================================================
Add AK47 to the character
#8 Video

attach AK47 to the character skeleton

spawn AK47->Man_With_AK47 blueprint->weapon attach block
=================================================

Shoot AK47
#9 Video

Let AK47 spawn projectile:
Open AK47 blueprint -> Fire projectile block (in event graph)

Press mouse to fire:
Open Man_With_AK47 blueprint->Fire block (in event graph)

Change speed& gravity& mesh of bullet:
Open Projectile_Base blueprint->change mesh or ProjectileMovement

Change shooting bullet out angle:
Open AK47 skeleton->MUZZLE->change angle while Play


==================================================

Make AK47 rotate up and down

#12 Video:UserControlRotation

''''''
1.Character Animation->Anim Graph

2. add 3X Transform Bone

'''''

details in Videos

Change rotate speed:

Open Character Animation->Event Graph->AIMING UP AND DOWN FOR SWAT (OR THIRDPERSON BP WITH GUN ONLY) block
->Output of Select Float (Green)
change ÷ float (set 1.2 as default) 
bigger->move slower
smaller->move faster
change rotation speed while Play

===================================================
AI take damage

#Video 24

Open Simple AI blueprint->Event Graph->take damage block &kill actor block
