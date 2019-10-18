---
title: EUR-00011 EU-myyntiluetteloraportoinnin määrittäminen
description: Tässä tehtävässä käsitellään yleisesti EU-myyntiluettelon raportoinnin edellytyksiä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b44d439bf1e991380fb7273a70e1f69f807c8b25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175125"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a>EUR-00011 EU-myyntiluetteloraportoinnin määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä käsitellään yleisesti EU-myyntiluettelon raportoinnin edellytyksiä. Lisätietoja EU:n myyntiluettelon raportoinnista ja edellytyksistä on ohjeissa.

Tämä tehtävä koskee kaikkia Euroopan maita/alueita. Opastuksessa on käytetty DEMF-demotietoyritystä ja Saksaa kotimaa-/alue-esimerkkinä. Opastuksessa käytetään myös Portugalia EU-esimerkkimaana/-alueena.

Nämä tehtävät on tarkoitettu järjestelmänvalvojille.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Tuo EU-myyntiluettelon raportoinnin sähköisen raportoinnin konfiguraatiot
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Aseta aktiiviseksi.
3. Valitse Säilöt.
4. Valitse Avaa.
5. Valitse toimintoruudussa Asetukset.
6. Valitse Lisäsuodatin/-lajittelu.
7. ValitseLisää.
8. Valitse Kenttä-kentässä Konfiguroinnin nimi.
9. Kirjoita Ehdot-kenttään EU-myyntiluettelo (DE).
10. Valitse OK.
11. Valitse Tuo.
12. Valitse Kyllä.
13. Valitse toimintoruudussa Asetukset.
14. Valitse Lisäsuodatin/-lajittelu.
15. Valitse Palauta.
16. ValitseLisää.
17. Valitse Kenttä-kentässä Konfiguroinnin nimi.
18. Kirjoita Ehdot-kenttään EU-myyntiluettelo riviraportti.
19. Valitse OK.
20. Valitse Tuo.
21. Valitse Kyllä.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Määritä EU-myyntiluetteloraportoinnin alv-koodit
1. Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäverokoodit.
2. Suodata pikasuodattimella Arvonlisäverokoodi-kenttä arvolla ALV19.
3. Laajenna Raportin asetukset -osa.
    * Tarkista, että Poissuljettu-valintana on Ei.  
    * Tehtäväopastuksen lukitus on ehkä avattava, jotta asetusta voi muuttaa.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Määritä EU-myyntiluetteloraportoinnin alv-ryhmät
1. Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.
2. Suodata pikasuodattimella Arvonlisäveroryhmä-kenttä arvolla MR-KOT.
3. Valitse Muokkaa.
4. Laajenna osa Asetukset.
5. Valitse luettelon ensimmäinen rivi.
6. Valitse Vapautus-valintaruutu.
7. Valitse luettelon toinen rivi.
8. Valitse Vapautus-valintaruutu.
9. Valitse luettelon kolmas rivi.
10. Valitse Vapautus-valintaruutu.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Määritä EU-myyntiluetteloraportoinnin nimikkeiden alv-ryhmät
1. Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.
2. Suodata pikasuodattimella Nimikkeen arvonlisäveroryhmä -kenttä arvolla TÄYSI.
    * Tarkista, että Raportointityyppi-valintana on Nimike.  
    * Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.  
3. Suodata pikasuodattimella Nimikkeen arvonlisäveroryhmä -kenttä arvolla PUN.
    * Tarkista, että Raportointityyppi-valintana on Palvelu.  
    * Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Määritä EU-myyntiluetteloraportoinnin maa- tai alueparametrit
1. Valitse Vero > Asetukset > Arvonlisävero > Maan/alueen parametrit.
2. Valitse Uusi.
3. Kirjoita Maa/alue-kenttään PRT.
4. Kirjoita Arvonlisävero -kenttään PT.

## <a name="create-tax-exempt-numbers"></a>Luo ALV-tunnukset
1. Valitse Vero > Asetukset > Arvonlisävero > ALV-tunnukset.
2. Valitse Uusi.
3. Kirjoita Maa/alue-kenttään PRT.
4. Kirjoita ALV-tunnus-kenttään PT12345.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>Määritä EU-myyntiluettelon raportointiparametrit
1. Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.
2. Valitse EU-myyntiluettelo-välilehti.
3. Valitse Ostojen siirto -kentässä Kyllä.
4. Laajenna Pyöristyssäännöt-osa.
5. Määritä pyöristyssäännöksi 0,1
6. Valitse Käytä vähimmäisarvoa -kentässä Kyllä.
7. Anna Desimaalien määrä -kentässä 2.
8. Laajenna Sähköinen raportointi -osa.
9. Valitse Tiedostomuodon yhdistäminen -kentässä EU-myyntiluettelo (DE).
10. Valitse Raporttimuodon yhdistäminen -kenttään EU-myyntiluettelon riviraportti.
11. Valitse Maan tai alueen ominaisuudet -välilehti.
    * Tarkista, että Maa-/aluetyyppi-kentän Maa/alue DEU -asetuksena on Kotimaa.  
    * Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.  
12. Valitse Uusi.
13. Kirjoita Maa/alue-kenttään PRT.
14. Kirjoita Intrastat-koodi-kenttään PT.
15. Valitse Maa-/aluetyyppi-kentässä EU.
16. Valitse Numerojärjestykset-välilehti.
    * Tarkista, että Numerojärjestyskoodi on määritetty viitteelle EU-myyntiluettelo.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Luo asiakas EU-myyntiluetteloraportoinnin esittelyä varten
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Valitse Uusi.
3. Kirjoita Asiakastili-kenttään PRT-001.
4. Kirjoita Nimi-kenttään Portugalilainen asiakas.
5. Valitse Asiakasryhmä-kentässä 10.
6. Valitse Arvonlisäveroryhmä-kentässä MR-KOT.
7. Valitse ALV-tunnus-kentässä PT12345.
8. Kirjoita Maa/alue-kenttään PRT.
9. Valitse Tallenna.

