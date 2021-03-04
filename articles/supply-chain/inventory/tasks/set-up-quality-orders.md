---
title: Määritä laatutilaukset
description: Seuraavissa vaiheissa kerrotaan, miten laadunhallintaprosessi otetaan käyttöön, kun saapuva varasto on tarkistettava heti saapumisen yhteydessä tehtävän rekisteröinnin jälkeen.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4577b8b189403b3d71eb634e159d51d2fa53ce12
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427328"
---
# <a name="set-up-quality-orders"></a>Määritä laatutilaukset

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten laadunhallintaprosessi otetaan käyttöön, kun saapuva varasto on tarkistettava heti saapumisen yhteydessä tehtävän rekisteröinnin jälkeen. Laatupäällikkö tekee yleensä tämän menettelyn. Prosessi sisältää laaturyhmän luomisen, kerättävien nimikkeiden määrittämisen ja testiryhmän, jonne kerätään laaturyhmän nimikkeille suoritettavat testit. Voit suorittaa tämän ohjauksen esittely-yrityksessä USMF.


## <a name="enable-quality-management"></a>Laadunhallinnan ottaminen käyttöön
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit**.
2. Valitse **Laadunhallinta**-välilehti.
3. Määritä **Käytä laadunhallintaa** -vaihtoehdon arvoksi Kyllä.
4. Valitse **Raportin asetukset**. Laadunhallinnan raportin määritys on jo määritetty USMF-yritykselle. Jos tätä ei ole tehty, lisäät uusia rivejä tässä erityyppisille raporttityypeille ja valitset kullakin raportilla käytettävän asiakirjan tyypin.  
5. Sulje sivu.
6. Sulje sivu.

## <a name="create-a-test"></a>Testin luominen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testit**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Testi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Tyyppi**-kentässä Asetus. Tässä esimerkissä valitaan Asetus-kohta, jolloin testitulokset on mahdollista liittää ennalta määrättyjen arvojen perusteella.  
6. Valitse **Tallenna**.
7. Sulje sivu.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Testimuuttujien luominen ja testitulosten tallennustavan määrittämisen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testimuuttujat**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Muuttuja**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Tallenna**.
6. Valitse **Tulokset**.
7. Valitse **Uusi**.
8. Kirjoita arvo **Tulos**-kenttään.
9. Kirjoita **Kuvaus**-kenttään arvo.
10. Valitse **Tuloksen tila** -kentässä Hyväksytty.
11. Valitse **Tallenna**.
12. Valitse **Uusi**.
13. Kirjoita arvo **Tulos**-kenttään.
14. Kirjoita **Kuvaus**-kenttään arvo.
15. Valitse **Tallenna**.
16. Sulje sivu.
17. Sulje sivu.

## <a name="set-up-item-sampling"></a>Nimikeotannan määrittäminen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Nimikeotanta**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimikeotanta**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Kirjoita numero **Arvo**-kenttään. Tämä arvo liittyy määrän määritykseen, joka valitaan viereisessä kentässä.  
6. Laajenna tai tiivistä **Prosessi**-osa.
7. Valitse **Täysi esto** -valintaruutu tai poista sen valinta. Jos valitset tämän asetuksen, koko erä tai tilausrivin määrä estetään, jos testi epäonnistuu. Jos tätä ei valita, vain laatutilauksen nimikkeet estetään.  
8. Valitse **Tallenna**.
9. Sulje sivu.

> [!NOTE]
> *Varastoprosessien laadunhallinta* -toiminto tarjoaa lisää nimikkeen otantatoimintoja. Se lisää käsitteen *Nimikkeen otanta-alueesta* ja mahdollisuuden määrittää täyden rekisterikilven määrä määritykseksi. Jos olet ottanut tämän toiminnon käyttöön, lisätietoja on kohdassa [Varastoprosessien laadunhallinta](../quality-management-for-warehouses-processes.md).

## <a name="create-a-quality-group"></a>Laaturyhmän luominen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Laaturyhmät**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Laaturyhmä**-kenttään. Käytä kuvaavaa nimeä, jonka avulla tunnistat, minkä tyyppisiä nimikkeitä ryhmä sisältää (otannan ehdot).  
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Tallenna**.
6. Valitse **Lisää nimikkeitä**.
7. Valitse **Nimiketunnus**-rivi. Tässä esimerkissä suodatus suoritetaan nimiketunnuksen perusteella.  
8. Kirjoita arvo **Ehdot**-kenttään. Kirjoita esimerkiksi T*, kun haluat suodattaa T-kirjaimella alkavien nimiketunnusten perusteella.  
9. Valitse **OK**.
10. Valitse **OK**.
11. Valitse **Nimikkeen laaturyhmät**.
12. Sulje sivu.
13. Sulje sivu.

## <a name="create-a-test-group"></a>Testiryhmän luominen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testiryhmät**.
2. Valitse **Uusi**.
3. Kirjoita **Testiryhmä**-kenttään arvo. Anna **testiryhmälle** nimi, jonka avulla muistat suoritettavien testien tyypin ja sen, mihin laaturyhmään liitos tehdään. Jos sitä käytetään esimerkiksi sellaisen laaturyhmän kanssa, joka valitsee T-kirjaimella alkavat nimikkeet, voit antaa nimeksi T-nimikkeen testit.  
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Nimikeotanta**-kentässä aiemmin luomasi nimikeotantarivi.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Valitse **Lisää**.
8. Syötä **Järjestysnumero**-kenttään numero.
9. Valitse **Testi**-kentässä aiemmin luomasi testi.
10. Etsi haluamasi tietue luettelosta ja valitse se.
11. Valitse **Testi**-välilehti.
12. Valitse **Muuttuja**-kentässä aiemmin luomasi muuttuja
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Avaa haku valitsemalla **Oletustulos**-kentässä avattavan valikon painike.
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
16. Valitse **Tallenna**.
17. Sulje sivu.

## <a name="define-when-quality-orders-will-be-created"></a>Laatutilausten luomisajankohdan määrittäminen
1. Valitse **Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Laatuliitokset**.
2. Valitse **Uusi**.
3. Valitse **Viitetyyppi**-kentässä vaihtoehto.
4. Valitse **Nimikekoodi**-kentässä Ryhmä. Tässä esimerkissä arvoksi valitaan Ryhmä ja käytetään aiemmin luotua laaturyhmää. Arvoksi voi määrittää myös Taulu, jos haluat määrittää nimikkeen manuaalisesti, tai Kaikki, jos haluat lisätä kaikki nimikkeet laatutilaukseen.  
5. Valitse **Nimike**-kentässä aiemmin luomasi laaturyhmä. Nimike-kentän käytettävissä olevat vaihtoehdot riippuvat Nimikekoodi-kentän määrityksestä.  
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Laajenna tai tiivistä Prosessi-osa.
8. Valitse **Tapahtumatyyppi**-kentässä vaihtoehto. Tämä on testin käynnistävä tapahtuma. Tässä käytettävissä olevat vaihtoehdot riippuvat Viitetyyppi-kentässä valitusta prosessista.  
9. Valitse **Suoritus**-kentässä vaihtoehto.
10. Laajenna tai tiivistä **Laatutilausprosessi**-osa.
11. Avaa haku valitsemalla **Tapahtuman esto** -kentässä avattavan valikon painike. Tässä kentässä on niiden prosessien luettelo, joita voidaan estää, jos laatutilaus on yhä avoin. Vaihtoehdot riippuvat Tapahtumatyyppi-kentässä valitusta arvosta.  
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä. Tämä riippuu aiemmin valituista arvoista. Määritä, onko seuraavat prosessit estettävä, kun lähdeasiakirjariviin on linkitettynä avoimia laatutilauksia.  
13. Laajenna tai tiivistä **Määritykset**-osa.
14. Valitse **Testiryhmä**-kentässä aiemmin luomasi testiryhmä.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Valitse **Tallenna**.
17. Sulje sivu.

> [!NOTE]
> *Varastoprosessien laadunhallinta* -toiminto tarjoaa lisävaihtoehtoja laatuliitosten perustamiseen. Se lisää uuden ehdon (**Käytettävissä oleva varastotyyppi**) ja uuden asetuksen (**Laadun käsittelykäytäntö**). Jos olet ottanut tämän toiminnon käyttöön, lisätietoja on kohdassa [Varastoprosessien laadunhallinta](../quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]