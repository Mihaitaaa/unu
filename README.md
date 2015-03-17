p3.awk 

if ( substr($1, 6, 3) % 7 == 0)
print $1, $2
fi

4. Rezolvata Alin

5.

p5.awk

if ( substr($1, 7, 2)  == 88 )
print $1, $2
fi

p6.awk

  if ( substr ($1, 12, 2) == 23 && substr ($1, 12, 3) == 230 || substr ($1, 12, 3) == 231 ||
substr ($1, 12, 3) == 232 || substr ($1, 12, 3) == 233 || substr ($1, 12, 3) == 234 || substr ($1, 12, 3) == 235 || substr ($1, 12, 3) == 236 ||
substr ($1, 12, 3) == 237 ||  substr ($1, 12, 3) == 238 || substr ($1, 12, 3) == 239 )
        print $1, $2
        fi

7. id = ir, afis nume complet, inloc vocale mici cu mari
awk -f unu.awk alin.txt | cut -d':' -f 5 | sed "y/aeiou/AEIOU"

unu.awk

{if(substr($1,3,2) == "ir")
print $1

fi}
