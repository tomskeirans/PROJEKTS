# Projekts (programma, kura atvieglo ikdienas uzdevumu sporta komentētājam/statistikas apkopotājam)

## Vispārīgs apraksts par ikdienas uzdevumu, kuru nepieciešams automatizēt

Katru nedēļu notiek spēles Latvijas 1.līgas čempionātā florbolā un tās tiek translētas tiešraidē, tāpēc uz tām tiek nozīmēti konkrēti komentētāji, kuri spēles laikā plašāk komentē spēles laukumā redzamos notikumus, kā arī veic dažādu statistikas rādītāju izpēti. Šāda statistikas atskaite un apskats spēles laikā raisa papildus interesi skatītājos, bet iegūt šo statistiku nav pats vieglākais uzdevums, jo kopā čempionātā ir *19* komandas, kuras regulāri aizvada spēles, tāpēc arī loģiski mainās visa statistika. Veikt statistikas aprēķinus manuāli būtu ļoti laikietilpīgs un sarežģīts uzdevums, kā arī, tā būtu no jauna jāaprēķina ik pēc kartas aizvadītās spēles.

Visa komandu statistika ir pieejama internetā, Latvijas Florbola savienības mājaslapā, bet šajā statistikā tiek atspoguļotas tikai pāris lietas un tas ir par maz pilnam statistikas apskatam. Nav pieejami, piemēram, tādi svarīgi statistikas rādītāji kā *vairākuma realizācijas procents*, *komandas vairākumu skaits* u.c. Šādi rādītāji būtiski apraksta komandas spēli nevienādos sastāvos un ir nepieciešami pilnīgai statistikas apskatei.

Papildus šim visam, statistika mājaslapā tiek attēlota pretī komandas nosaukuma saīsinājumam, kurš tiek veidots no 3 lielajiem burtiem. Ne vienmēr pēc šiem burtiem var saprast, kura komanda ir aprakstīta, tāpēc ir Excel fails, kurā ir atšifrēti šie komandu nosaukumu saīsinājumi un blakus ir rakstīts pilnais komandas nosaukums.

## Projekta apraksts

Balstoties uz iepriekšējo aprakstu ir nepieciešams izveidot programmu, kura:
1. Ļauj lietotājam ievadīt komandas nosaukuma saīsinājumu, kurš ir atrodams mājaslapā. Piemēram, lietotājs ievada komandas saīsinājumu ROC. 
2. Programma salīdzina šo saīsinājumu ar Excel failu 