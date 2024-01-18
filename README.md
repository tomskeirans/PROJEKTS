# Projekts (programma, kura atvieglo ikdienas uzdevumu sporta komentētājam/statistikas apkopotājam)

## Vispārīgs apraksts par ikdienas uzdevumu, kuru nepieciešams automatizēt

Katru nedēļu notiek spēles Latvijas 1.līgas čempionātā florbolā un tās tiek translētas tiešraidē, tāpēc uz tām tiek nozīmēti konkrēti komentētāji, kuri spēles laikā plašāk komentē spēles laukumā redzamos notikumus, kā arī veic dažādu statistikas rādītāju izpēti. Šāda statistikas atskaite un apskats spēles laikā raisa papildus interesi skatītājos, bet iegūt šo statistiku nav pats vieglākais uzdevums, jo kopā čempionātā ir *19* komandas, kuras regulāri aizvada spēles, tāpēc arī loģiski mainās visa statistika. Veikt statistikas aprēķinus manuāli būtu ļoti laikietilpīgs un sarežģīts uzdevums, kā arī, tā būtu no jauna jāaprēķina ik pēc kartas aizvadītās spēles.

Visa komandu statistika ir pieejama internetā, Latvijas Florbola savienības mājaslapā, bet šajā statistikā tiek atspoguļotas tikai pāris lietas un tas ir par maz pilnam statistikas apskatam. Nav pieejami, piemēram, tādi svarīgi statistikas rādītāji kā *vairākuma realizācijas procents*, *komandas vairākumu skaits* u.c. Šādi rādītāji būtiski apraksta komandas spēli nevienādos sastāvos un ir nepieciešami pilnīgai statistikas apskatei.

Papildus šim visam, statistika mājaslapā tiek attēlota pretī komandas nosaukuma saīsinājumam, kurš tiek veidots no 3 lielajiem burtiem. Ne vienmēr pēc šiem burtiem var saprast, kura komanda ir aprakstīta, tāpēc ir Excel fails, kurā ir atšifrēti šie komandu nosaukumu saīsinājumi un blakus ir rakstīts pilnais komandas nosaukums.

## Projekta apraksts

Balstoties uz iepriekšējo aprakstu ir nepieciešams izveidot programmu, kura:
1. Ļauj lietotājam ievadīt komandas nosaukuma saīsinājumu, kurš ir atrodams mājaslapā. Piemēram, lietotājs ievada komandas saīsinājumu ROC. 
2. Programma salīdzina šo saīsinājumu ar Excel failu, kurā tie ir atšifrēti un attiecīgi iegūst pilno komandas nosaukumu, kuru vēlāk ir jāizvada, lai lietotājs varētu to redzēt. Fails, kurā ir pieejami pilnie nosaukumi: 

- 'komandas.xlsx'

3. Pēc ievadītā saīsinājuma programmai ir automātiski jāatver mājaslapa (https://www.floorball.lv/lv/2023/chempionats/v1/statistika_komandas#kopsavilkums) un no tās jāiegūst šāda informācija:
    1. *Attiecīgās komandas soda minūtes, kuras ir pret šo komandu jeb cik vairākuma minūtes kopā komandai ir bijušas*. (24.kolonna)
    2. *Attiecīgās komandas iemestie vārti vairākumā*. (12.kolonna)
4. Pēc šīs iegūtās informācijas programmai ir jāveic vairāki aprēķini, lai iegūtu:
    1. *Attiecīgās komandas vairākumu skaitu*, ko aprēķina kopējās vairākuma minūtes dalot ar 2, jo katrs vairākums ilgst 2 min. (Iegūtais rezultāts jānoapaļo līdz veseliem skaitļiem)
    2. *Attiecīgās komandas vairākuma realizācijas procentu*, kuru aprēķina dalot kopējo iemesto vārtu skaitu vairākumā ar jau aprēķināto vairākumu skaitu. (Iegūtais rezultāts jānoapaļo līdz veseliem procentiem)
5. Visi iegūtie rezultāti (komandas pilnais nosaukums, soda minūtes pret komandu, vārti vairākumā, vairākumu skaits un vairākuma realizācijas procents) ir jāizvada, lai komentētājs/lietotājs varētu viegli tos nolasīt.

## Projektā izmantotās Python bibliotēkas

Savā projektā izmantoju **Selenium** automatizācijas bibliotēku, kura ļauj veikt vairākas darbības tīmekļa pārlūkprogrammā. Savā projektā to izmantoju, lai atvērtu tīmekļa lapu, veiktu meklēšanu tajā un iegūtu informāciju no tabulas šajā lapā. Vēl izmantoju bibliotēku **openpyxl**, lai darbotos ar Excel failu. Izmantoju to, lai nolasītu datus no faila, kurā tika glabāta informācija par komandām.

## Izmantošanas metodes

Programmas izmantošanas metodes ir ļoti plašas. Programma ir ātri pielāgojama arī citu statistikas rādītāju apskatei un aprēķinam. Tā ļauj lietotājam/komentētājam pāris sekunžu laikā uzzināt katras komandas statistikas rādītājus un lietotājam nav nepieciešams pašam meklēt ne komandas pilno nosaukumu, ne aprēķināt un izgūt dažādus interesējošus statistikas rādītājus. Programmu noteikti var lietot arī ziņu redaktori, kuri veido pēc spēles rakstus.

## Links uz video

https://www.youtube.com/watch?v=4WLog6easDk
