---
title: Määritä minimi-/maksimitäydennysprosessi
description: Seuraavassa menettelyssä kuvataan, miten voit määrittää uuden täydennysprosessin, joka käyttää minimi-/maksimitäydennysstrategiaa.
author: perlynne
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f032f95377fdc6f8ec7fbbfa7aadab8fc448be5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577765"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Määritä minimi-/maksimitäydennysprosessi

[!include [banner](../../includes/banner.md)]

Seuraavassa menettelyssä kuvataan, miten voit määrittää uuden täydennysprosessin, joka käyttää minimi-/maksimitäydennysstrategiaa. Sijainnin täydennystyö luodaan, kun varaston vähimmäistaso laskee minimitason alle. Menettelyssä näytetään myös, miten kiinteitä keräilysijainteja voi käyttää sallimaan täydennys vaikka varastosaldo laskisikin minimitason alle, ja miten täydennysprosessin voi määrittää ajettavaksi säännöllisesti eräajona. Yleensä varastopäällikkö tekee nämä tehtävät. Voit suorittaa tämän menettelyn USMF-malliyrityksessä käyttämällä alla olevia esimerkkiarvoja, tai voit suorittaa sen omilla tiedoillasi. Jos käytät omia tietoja, varmista, että sinulla on varasto, jolla varastonhallintaprosessit ovat käytössä.


## <a name="create-a-fixed-picking-location"></a>Luo kiinteä keräilysijainti
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Kiinteät sijainnit**. Tämä on valinnainen tehtävä minimi-/maksimitäydennysprosessissa, mutta jos käytät kiinteää keräilyvarastopaikkaa, varasto voidaan täydentää vaikka se laskee alle vähimmäistason, koska järjestelmä määrittää, mitkä on täydennettävä, vaikka täydennettävää ei olisikaan.
2. Valitse **Uusi**.
3. Syötä tai valitse arvo **Nimiketunnus**-kentässä. Jos käytössä on USMF, voit valita nimikkeen A0001.  
4. Syötä tai valitse arvo **Toimipaikka**-kenttään. Jos käytössä on USMF, valitse toimipaikka 2.  
5. Anna tai valitse **Varasto**-kentässä arvo. Jos käytössä on USMF, voit valita varaston 24.  
6. Syötä tai valitse arvo **Sijainti**-kenttään. Jos käytössä on USMF, valitse CP-003.  
7. Sulje sivu.

## <a name="create-a-replenishment-location-directive"></a>Luo täydennyssijainnin direktiivi
1. Valitse **Varastonhallinta > Asetukset > Sijaintidirektiivit**. Sijaintidirektiivejä käytetään määrittämään, mistä nimikkeet tulee keräillä täydennysprosessissa.
2. Valitse **Työtilauksen tyyppi** -kentässä Täydennys.
3. Napsauta **Toimintoruudussa** **Uusi**.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Työtyyppi**-kentässä Keräilyt.
6. Syötä tai valitse arvo **Toimipaikka**-kenttään. Jos käytössä on USMF, valitse toimipaikka 2.  
7. Anna tai valitse **Varasto**-kentässä arvo. Jos käytössä on USMF, voit valita varaston 24.  
8. Valitse **Tallenna**.
9. Valitse **Rivit**-osiosta **Uusi**.
10. Merkitse valittu rivi luettelossa.
11. Lisää **Määrään**-kenttään numero. Voit esimerkiksi asettaa sen arvoon 9999.  
12. Valitse **Salli jakaminen** -valintaruutu. Jos valitset tämän vaihtoehdon, töiden luontiprosessi sallii työrivien määrien jakamisen useille sijainneille.  
13. Valitse **Tallenna**.
14. Valitse **Sijaintidirektiivin toiminnot** -osiosta **Uusi**.
15. Merkitse valittu rivi luettelossa.
16. Kirjoita arvo **Nimi**-kenttään.
17. Valitse **Tallenna**.
18. Valitse **toimintoruudussa** **Muokkaa kyselyä**. Voit muokata tätä kyselyä lisätäksesi rajoituksia varaston valintasijainnille täydennysprosessissa. On esimerkiksi mahdollista, että varastoa tulisi käyttää ainoastaan irtotavara-alueelta.
19. Valitse **OK**.
20. Sulje sivu.

## <a name="create-a-replenishment-work-template"></a>Luo täydennystyömalli
1. Siirry kohtaan **Varastonhallinta > Asetukset > Työ > Työmallit**. Työmallin avulla järjestelmää ohjataan minimi-/maksimitäydennysprosessin luomisessa. Työmallissa on oltava rivi vähintään keräilylle ja asettamiselle. Työmallin ilmoitetaan olevan virheellinen, kunnes kaikki tarpeellinen tieto on täytetty. 
2. Valitse **Työtilauksen tyyppi** -kentässä Täydennys.
3. Napsauta **Toimintoruudussa** **Uusi**.
4. Kirjoita **Työmalli**-kenttään arvo.
5. Valitse **Tallenna**.
6. Valitse **Työmallin tiedot** -osiosta **Uusi**.
7. Valitse **Työtyyppi**-kentässä Keräilyt.
8. Syötä tai valitse arvo **Työluokan tunnus** -kenttään. Tämän tulisi olla täydentämiseen liittyvä työn luokka. Jos USMF on käytössä, valitse Täydennys.  
9. Valitse **Työmallin tiedot** -osiosta **Uusi**.
10. Merkitse valittu rivi luettelossa.
11. Valitse **Työtyyppi**-kentässä Määritä.
12. Syötä tai valitse arvo **Työluokan tunnus** -kenttään.
13. Valitse **Tallenna**.
14. Sulje sivu.

## <a name="create-a-new-replenishment-template"></a>Luo uusi täydennysmalli
1. Valitse **Varastonhallinta > Asetukset > Täydennys > Täydennysmallit**. Täydennysmallilla määritetään täydennettävät nimikkeet ja määrät sekä täydennettävä sijainti.
2. Napsauta **Toimintoruudussa** **Uusi**.
3. Kirjoita **Täydennysmalli**-kenttään arvo. Anna mallille nimi, joka osoittaa, että se on minimi-/maksimitäydennysprosessia varten.  
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Salli aallon kysynnän käyttää varaamattomia määriä** -valintaruutu. Jos valitset tämän vaihtoehdon, se ottaa käyttöön aaltokysynnän täydennyksen kuluttamaan määriä, jotka liittyvät minimi-/maksimitäydennysprosessiin. Tästä voi esimerkiksi olla hyötyä, jos minimi-/maksimitäydennystyötä ei ole käsitelty heti, jotta tarpeettomien kysyntää vastaavien täydennystöiden luonti voidaan välttää.
6. Valitse **Täydennysmallin tiedot** -osiosta **Uusi**.
7. Syötä **Järjestysnumero**-kenttään numero.
8. Kirjoita **Kuvaus**-kenttään arvo.
9. Merkitse valittu rivi luettelossa.
10. Syötä tai valitse arvo **Täydennysyksikkö**-kenttään. Valitse esimerkiksi arvo pcs. Tämä asetus on pakollinen. Voit määrittää eri mittayksikön täydennystyölle verrattuna mallissa määritettyihin minimi- ja maksimivaraston tasoihin.
11. Syötä tai valitse arvo **Työmalli**-kenttään. Valitse aiemmin luomasi työmalli.  
12. Syötä numero **Vähimmäismäärä**-kenttään. Valitse vähimmäismäärä, joka käynnistää täydennyksen. Määritä arvoksi esimerkiksi 50. Voit jättää tämän kentän arvoksi nollan, jos täydennät kiinteää sijaintia ja **Täydennä tyhjät kiinteät sijainnit** -asetuksen arvo on Kyllä. Suosittelemme myös, että käytät **Täydennä vain kiinteät sijainnit** -asetusta suorituskyvyn parantamiseksi.
13. Syötä numero **Enimmäismäärä**-kenttään. Määritä arvoksi esimerkiksi 100.  
14. Syötä tai valitse arvo **Yksikkö**-kenttään. Määritä vähimmäis- ja enimmäismäärien yksikkö. Määritä arvoksi esimerkiksi pcs.  
15. Valitse **Täydennä tyhjät kiinteät sijainnit** -valintaruutu. Valitse tämä valintaruutu, kun haluat täydentää kiinteät sijainnit, kun ne ovat tyhjät. Muussa tapauksessa vain sijainnit, jossa määrä on käytettävissä, täydennetään.
16. Valitse **Täydennä vain kiinteät sijainnit** -valintaruutu.
17. Napsauta **Valitse tuotteet**. Tässä voit määrittää, mitkä tuotteet tulee täydentää. Jos Kiinteät keräilysijainnit -asetus on valittuna, sijainnit on myös määritettävä tähän kyselyyn. Saatavilla on sekä variantti- että tuotekohtaisia kyselyitä.
18. Valitse **Nimikkeet**-rivi.
19. Kirjoita arvo **Ehdot**-kenttään. Valitse kiinteisiin sijainteihin täydennettävät nimikkeet. Kirjoita esimerkiksi A* valitaksesi kaikki nimiketunnukset, jotka alkavat A:lla.
20. Valitse **Lisää**. Lisää sijainnin entiteetti (jos se on jo olemassa) rajataksesi täydennystyön kiinteisiin keräilysijainteihin varaston tietyllä alueella.
21. Merkitse valittu rivi luettelossa.
22. Aseta **Taulukko**-kentän arvoksi Sijainnit.
23. Valitse **Kenttä**-kenttään Sijainnin profiilitunnus.
24. Anna tai valitse arvo **Ehdot**-kentässä.
25. Valitse **OK**.
26. Sulje sivu.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Aseta täydennysprosessi ajettavaksi eräajona
1. Valitse **Varastonhallinta > Täydennys > Täydennykset**. Täydennykset-sivulla voit asettaa täydennykset ajettavaksi eräajona tai vaatia, että ne käynnistetään manuaalisesti.
2. Valitse **Suodatin**.
3. Merkitse valittu rivi luettelossa.
4. Anna tai valitse arvo **Ehdot**-kentässä.
5. Valitse **OK**.
6. Laajenna **Suorita taustalla** -osa.
7. Aseta **Eräkäsittely**-asetuksen arvoksi Kyllä.
8. Valitse **Toistuminen**.
9. Valitse **Päättymispäivä puuttuu** -vaihtoehto.
10. Määritä **Toistumisen kuvio**. Valitse esimerkiksi Päivää.  
11. Valitse **OK**.
12. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]