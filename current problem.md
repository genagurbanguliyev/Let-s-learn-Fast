###### Current behavior:
news rss-dan parse edyan service ishlan wagty (mysal uchin: her 3minutdan) api-lere jogap berip bilenok. Loading...(client ahyr songy time-out err bermeli bolya yada timer ishlpap gutaryancha garashmaly bolya)

###### Desired behavior:
taze patoga chykarmaly news parse edyan timer service-y


###### Mana belli zatlar, bilyan zatlam:
1 sany worker bilen run edilende sheyle problem chykya. run edilende workerlerin sanyny kopeldip etseng onna api response gaytarmak meselesi chozulyar, yone worker nache sany bolsa rss-den gelyan kabir habarlar(mysal uchin: bir saytyn rss/ru hemde rss/tm api-lerinde ikisindede shobir news gelen yagdayynda) database-a nache worker bsa shoncha sapar goshulyar.

###### Dirap duran problema:


###### Barlap gormeli usullar:
 - rss parse timer service-y background-task yaly bir zat edip ishletmeli(error-syz ishledi yone pikir etyan netije bermedi.)
 - celery beat ulanyp ishletmeli (error)


###### Naili simulasiya edip bolar:
