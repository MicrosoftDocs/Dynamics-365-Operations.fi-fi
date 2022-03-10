---
title: Siirrä tapahtumat Intrastatiin
description: Tämä menettely opastaa Intrastat-parametrien asetuksen ja tapahtumien siirron Intrastatiin.
author: Anasyash
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bcc40af54b235bddc9a8da5d6e07640788a22714017630d8cd493156dd8991a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725959"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Siirrä tapahtumat Intrastatiin

[!include [banner](../../includes/banner.md)]

Tämä menettely opastaa Intrastat-parametrien asetuksen ja tapahtumien siirron Intrastatiin. Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.


## <a name="create-new-and-update-existing-commodity-code"></a>Luo uusia kauppatavarakoodeja ja päivitä olemassa olevia koodeja
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat**.
2. Etsi tai valitse luettelosta tietue **Intrastat-kauppatavarakoodit**.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse puussa tietue. Valitse esimerkiksi **Intrastat\Speaker**.  
5. Valitse **Muokkaa**.
6. Laajenna **Ulkomaankauppa**-pikavälilehti.
7. Syötä tai valitse **Lisäyksiköt**-kentän arvo. Valitse esimerkiksi **pcs**.  
8. Valitse **Paino ei käytössä** -kentän arvoksi **Kyllä**.
9. Valitse puussa **Intrastat**.
10. Valitse **Uusi luokkasolmu**.
11. Kirjoita **Nimi**-kenttään kauppatavaran nimi. Kirjoita esimerkiksi **Muu kauppatavara**.  
12. Kirjoita **Koodi**-kenttään kauppatavarakoodi. Kirjoita esimerkiksi **995 00 00**.  
13. Kirjoita Kutsumanimi-kenttään arvo. Kirjoita esimerkiksi **Muu**.  
14. Valitse **Tallenna**.
15. Sulje sivu.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Määritä kauppatavarakoodi tuotehierarkialle ja vapautetulle tuotteelle
1. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimi**-kenttää arvolla **myynti**.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
3. Laajenna puussa **luokkasolmu**. Laajenna esimerkiksi **Myyntihierarkia\Kodin äänentoisto**.  
4. Valitse puussa **kauppatavarakoodille määritettävä luokka**. Valitse esimerkiksi **Myyntihierarkia\Kodin äänentoisto\Kaiuttimet.  
5. Laajenna **Kauppatavarakoodit**-pikavälilehti.
6. Valitse **Lisää**.
7. Valitse **Valitse hierarkia** -kentästä **Intrastat**.
8. Etsi kauppatavarakoodi luettelosta ja valitse se. Valitse esimerkiksi **920 20 34 Kaiutin**.  
9. Valitse koodi napsauttamalla oikeaa nuolta.
10. Valitse **OK**.
11. Valitse siirtymisruudussa **Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
12. Valitse luettelosta vapautettu tuote, joka liitetään kauppatavarakoodiin. Valitse esimerkiksi **D0001**.  
13. Valitse **Muokkaa**.
14. Laajenna **Ulkomaankauppa**-pikavälilehti.
15. Kirjoita **Kauppatavara**-kenttään kauppatavarakoodi. Valitse esimerkiksi arvo **920 20 34 Kaiutin**.    
16. Syötä **Kuluprosentti**-kenttään numero. Syötä arvoksi esimerkiksi **3**.  
17. Kirjoita tai valitse **Maa/alue**-kenttään alkuperämaa/-alue. Voit valita esimerkiksi arvon **AUT**.  
18. Laajenna **Varastonhallinta**-pikavälilehti.
19. Syötä **Nettopaino**-kenttään paino kilogrammoina. Syötä arvoksi esimerkiksi **2,5**.  
20. Valitse **Tallenna**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Määritä Intrastat-tapahtumakoodit ja ulkomaankaupan parametrit
1. Siirry siirtymisruudussa kohtaan **Moduulit > Vero > Asetukset > Ulkomaankauppa > Tapahtumakoodit**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Tapahtumakoodi**-kenttään. Kirjoita esimerkiksi **21** palautuksessa käytettäväksi tapahtumakoodiksi.  
4. Kirjoita tapahtumakoodin nimi **Nimi**-kenttään. Syötä kenttään esimerkiksi **Palautus**.  
5. Valitse **Tilastosumma**-kentästä haluamasi vaihtoehto. Valitse esimerkiksi **Tyhjä**, joka ilmaisee, että tapahtumien, joiden koodi on **21**, ilmoitettu tilastollinen arvo on aina nolla.  
6. Siirry siirtymisruudussa kohtaan **Moduulit > Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit**.
7. Syötä tai valitse arvo **Tapahtumakoodi**-kentässä. Voit valita esimerkiksi arvon **11**.  
8. Anna tai valitse **Hyvityslasku**-kentässä arvo. Tämä arvo tunnistaa myös fyysisen palautuksen. Fyysisen palautuksen hyvityslasku siirretään Intrastat-kirjauskansioon päinvastaisen suuntaiseksi. Esimerkiksi saapumisen palautus siirretään lähetyksenä.   Muussa tapauksessa hyvityslasku käsitellään korjauksena ja siirretään samansuuntaisena ja vastakkaisella merkillä. Esimerkiksi saapumisen korjaus siirretään saapumisena, jolla on negatiivinen summa ja aktiiviseksi merkinnäksi asetetaan **Korjaus**.  
9. Laajenna **Siirrä**-pikavälilehti.
10. Valitse **Kyllä** **Nimikkeet, joilla on kauppatavarakoodi** -kentässä. Valitse tämä vaihtoehto siirtääksesi ainoastaan tapahtumat, joille on määritetty kauppatavarakoodi. Tapahtumia, joilla ei ole kauppatavarakoodia ei siirretä Intrastatiin.  
11. Valitse **Siirrä, kun nämä kriteerit täyttyvät** -kenttään vaihtoehto. Valitse esimerkiksi **Yksi valituista**.  
12. Laajenna **Kauppatavarakoodihierarkia**-osa.
13. Valitse **Maan tai alueen ominaisuudet** -välilehti.
14. Valitse **Uusi**.
15. Syötä tai valitse arvo **Maa/alue**-kentässä. Valitse esimerkiksi arvo **FRA**.  
16. Kirjoita **Intrastat-koodi**-kenttään maan ISO-koodi.  Kirjoita esimerkiksi **FR**.  
17. Valitse **Maa-/aluetyyppi**-kentässä **EU**.
18. Valitse Numerojärjestykset-välilehti.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Määritä toimitustavat ja kulujen sisällyttämissäännöt Intrastatissa
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myynti ja markkinointi > Asetukset > Jakelu > Toimitustavat**.
2. Etsi haluamasi tietue luettelosta ja valitse se. Valitse esimerkiksi **20 Air**.  
3. Laajenna **Ulkomaankauppa**-pikavälilehti.
4. Valitse **Muokkaa**.
5. Syötä tai valitse arvo **Kuljetus**-kentässä. Voit valita esimerkiksi arvon **02**.  
6. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Kulujen määritys > Kulujen koodi**.
7. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Kulujen koodi -kenttää arvolla **rahti**.
8. Laajenna **Ulkomaankauppa**-pikavälilehti.
9. Valitse **Muokkaa**.
10. Valitse **Intrastat-laskun arvo** -kentässä **Kyllä**. Summa siirretään **Laskun kulut** -kenttään ja lasketaan yhteen Laskun summa -kenttään siirretyn summan kanssa. Valitse **Kyllä** **Tilastollinen Intrastat-arvo** -kentässä jos muutosten määrä on siirrettävä **Tilastolliset maksut** -kenttään ja laskettava yhteen **Tilastollinen summa** -kentän kanssa.  

## <a name="sell-products-for-eu-customers"></a>Tuotteiden myynti EU-asiakkaille
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Valitse **Asiakastili**-kentässä EU-asiakas. Valitse esimerkiksi **DE-012 Litware Retail**.  
4. Laajenna **Toimitus**-pikavälilehti.
5. Syötä tai valitse arvo **Toimitustapa**-kentässä. Valitse esimerkiksi **20 Air**.  
6. Valitse **OK**.
7. Valitse myyntitilausrivien ensimmäinen rivi.
8. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Voit valita esimerkiksi arvon **D001**.  
9. Laajenna **Rivin erittely** -pikavälilehti.
10. Valitse **Ulkomaankauppa**-välilehti. Kuljetus täytetään automaattisesti valitusta toimitustavasta.  
11. Syötä tai valitse arvo **Portti**-kentässä.
12. Valitse **Myyntitiedot**. Asetusten mukaan, tämä summa sisältyy **Intrastat-laskutusarvoon**.  
13. Valitse **Kulujen ylläpito**.
14. Syötä tai valitse arvo **Kulujen koodi** -kenttään. Valitse esimerkiksi **RAHTI**.  
15. Merkitse **Säilytä**-valintaruutu.
16. Kirjoita **Kulujen arvo** -kenttään luku. Syötä arvoksi esimerkiksi **10**.  
17. Valitse **Tallenna**.
18. Sulje sivu.
19. Valitse toimintoruudussa **Lasku**.
20. Valitse **Lasku**.
21. Laajenna **Parametrit**-osa.
22. Valitse **Määrä**-kentässä **Kaikki**.
23. Laajenna **Asetukset**-pikavälilehti.
24. Syötä **Laskun päivämäärä** -kenttään päivämäärä. Syötä arvoksi esimerkiksi **2015-01-31**.  
25. Valitse **OK**.
26. Valitse **OK**.
27. Sulje sivu.
28. Valitse **Uusi**.
29. Valitse **Asiakastili**-kentässä EU-asiakas. Valitse esimerkiksi **DE-013 Trey Wholesales**.
30. Valitse **OK**.
31. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Voit valita esimerkiksi arvon **D0001**.  
32. Valitse **Tallenna**.
33. Valitse **Lasku**.
34. Syötä **Laskun päivämäärä** -kenttään päivämäärä. Syötä esimerkiksi päivämäärä **2015-01-31**.  
35. Valitse **OK**.
36. Valitse **OK**.

## <a name="transfer-transactions-to-the-intrastat"></a>Tapahtumien siirtäminen Intrastatiin
1. Siirry siirtymisruudussa kohtaan **Moduulit > Vero > Ilmoitukset > Ulkomaankauppa > Intrastat**.
2. Valitse **Siirrä**.
3. Valitse **Myyntilasku**-kentässä **Kyllä**.
4. Valitse **Suodatin**.
5. Merkitse **Päivämäärä**-rivi luettelossa.
6. Kirjoita arvo **Ehdot**-kenttään. Kirjoita esimerkiksi suodatin kaudelle tammikuu 2015 (tarkka arvo riippuu päivämäärämuodosta): 1/1/2015..31/1/2015  
7. Valitse **OK**.
8. Valitse **OK**.
9. Etsi siirretty tietue luettelosta ja valitse se.
10. Valitse **Yleiset**-välilehti.
    
Tarkista siirretyt tiedot, mukaan lukien kohde- tai lähetysmaa tai -alue, alkuperämaa, paino, määrä, määrä lisäyksiköinä, kauppatavara, tapahtumakoodi, laskutusmäärät ja tilastolliset määrät. Voit muokata tietoja tarpeen mukaan.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]