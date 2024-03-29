---
title: Varaston konfigurointi – yleiskatsaus
description: Tässä artikkelissa kerrotaan, miten varasto määritetään. Artikkeli sisältää tietoja varastoasettelun ja -prosessien ottamisesta käyttöön.
author: perlynne
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11554"
- intro-internal
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7643a333c269a7e1976563ff0f10b89c1fb91674
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065183"
---
# <a name="warehouse-configuration-overview"></a>Varaston konfigurointi – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten varasto määritetään. Artikkeli sisältää tietoja varastoasettelun ja -prosessien ottamisesta käyttöön.

> [!NOTE]
> Tämä artikkeli koskee **Varastonhallinta**-moduulin ominaisuuksia. Se ei koske **Inventoinnin- ja varastonhallinta** -moduulin varasto-ominaisuuksia.

## <a name="warehouse-layout"></a>Varastoasettelu
Supply Chain Managementin varastonhallintaprosessit (WMS) mahdollistavat varastoasettelun määrittämisen joustavasti muuttuvien tarpeiden mukaan siten, että varastoa voidaan käyttää mahdollisimman tehokkaasti.

-   Voit määrittää suuren ja pienen prioriteetin varastoalueita tavaroiden optimaalisen sijoitusta varten.
-   Voit jakaa varaston vyöhykkeisiin erilaisten varastotarpeiden mukaan, joita ovat esimerkiksi lämpötilavaatimukset tai nimikkeiden erilaiset läpimenoajat.
-   Voit määrittää eri tasoisia varastosijainteja (kuten toimipaikka, varasto, käytävä, teline, lokeroni ja lokeropaikka).
-   Voit ryhmittää sijainnit fyysisen kapasiteetin rajoitusasetuksilla.
-   Voit määrittää kyselymäärityssäännöillä, miten nimikkeet varastoidaan ja kerätään.

WMS:n käyttö Supply Chain Managementissa edellyttää, että varasto luodaan ja WMS otetaan siinä käyttöön. Valitse **Varastot**-sivulla **Käytä varastonhallintaprosesseja**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Vyöhykeryhmät, vyöhykkeet, sijaintityypit ja sijainnit

Osana varastoasettelun käyttöönottoprosessia on määritettävä varaston vyöhykeryhmät ja vyöhykkeet, sijaintiprofiilit, sijaintityypit ja sijainnit.

-   **Vyöhykeryhmät** – vyöhykkeiden looginen tai fyysinen ryhmittely varastossa.
-   **Vyöhykkeet** – sijaintien looginen tai fyysinen ryhmittely varastossa.
-   **Sijaintiprofiilit** – sellaisten sijaintien looginen tai fyysinen ryhmittely, joilla on samat varastosijainnit käsittelykäytännöt (siellä voidaan varastoida esimerkiksi eri nimiketunnusten yhdistelmä, joka käyttää samoja fyysisen kapasiteetin rajoituksia).
-   **Sijaintityypit** – Varastosijaintien looginen tai fyysinen ryhmittely. Voit esimerkiksi luoda sijaintityypin kaikille väliaikaisille sijainneille. **Varastonhallinnan parametrit** -sivun pakolliset asetukset määrittävät väliaikaisten sijaintityyppien ja lopullisen lähetyssijaintityypin määritysprosessin.
-   **Sijainnit** – Sijaintitietojen alin taso. Sijaintien avulla voidaan seurata, mihin käytettävissä oleva varasto on varastoitu ja mistä se kerätään varastossa.

Varastoasettelun määrittämistä varten luotuja yksiköitä käytetään kyselyissä, jotka määritetään työmalleissa siirtämään varaston työtilauksia. Niinpä sinun on otettava esimerkiksi vyöhykkeitä ja sijaintityyppejä määritettäessä huomioon, miten varaston eri alueita käytetään eri prosesseissa. Ota huomioon myös tietyn alueen fyysiset ominaisuudet. Joillakin alueilla voi esimerkiksi käyttää vain tietyn tyyppistä trukkia. Tai jos yrityksen tiloissa on sekä valmiita tuotteita että tuotantoa, Supply Chain Management -järjestelmään kannattaa ehkä luoda yksi varasto mutta erottaa sitten nämä toiminnot luomalla kaksi vyöhykeryhmää. Anna yksiköille kuvaileva nimi, jotta ne on helppo tunnistaa, kun käytät niitä mallikyselyissä.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Sijainnin varastointirajoitukset, sijaintiprofiilit ja kiinteät keräilysijainnit

Varaston fyysinen asettelu on otettava huomioon, koska se vaikuttaa tallennuskapasiteettiin (sijainnin varastointirajoitukset ja sijaintiprofiilit) ja koska se liittyy yritykseen optimoida varastoprosessit. 

Sijainnin varastointirajoitukset varmistavat, että ei luoda työtä, jossa varasto pyydetään sijoittamaan sijaintiin, jonka fyysinen kapasiteetti ei ole riittävä. Jos esimerkiksi joihinkin varaston sijainteihin voi sijoittaa vain yhden kuormalavan, sijainnin varastointirajoitukset voidaan ottaa käyttöön. **Määrä**-arvoksi voidaan valita **1** ja **Yksikkö**-arvoksi voidaan valita tietyssä sijaintiprofiiliryhmittelyssä **PL**. 

Jos sijainnin kapasiteettirajoitusten hallinta edellyttää lisälaskutoimituksia, voidaan käyttää sijaintiprofiiliasetuksia. Tässä tapauksessa kapasiteettiin laskennassa otetaan huomioon paino ja tilavuus. 

Jotta lähtevät prosessit olisivat optimaalisia, on harkittava käytetäänkö kiinteitä keräilysijainteja ja/tai pakkaussijainteja. Vähimmäis- tai enimmäistäydennystä käytetään usein irtotavara-alueelta keräilysijaintiin tapahtuvassa täydennysprosesseissa, ja samassa varastossa voidaan ottaa käyttöön useita kiinteitä keräilysijainteja tuotevarianteille. Harkitse, miten joustavuus paranee ottamalla käyttöön erillisiä kysynnän täydennyksen ylityssijainteja, joita käytetään vain aallon tai kuormituksen täydennyskäsittelyssä.

### <a name="location-setup-wizard"></a>Ohjattu sijaintien asennustoiminto

Voit luoda varastoon nopeasti sijainteja ohjatulla **Sijaintien asennus**-toiminnolla. Voit ylläpitää sijaintien nimimuotoilua osana tätä prosessia.

## <a name="warehouse-processes"></a>Varastoprosessit
On tärkeää, että varaston määrityksen osana otetaan käyttöön liiketoiminnan vaatimusten mukaiset varastoprosessit. Tärkeimmät määritettävät komponentit ovat aaltomallit, työmallit, työpoolit ja sijaintidirektiivit.

### <a name="wave-templates"></a>Aaltomallit

Aaltomallien avulla voidaan ottaa käyttöön lähtevien varastoon vapautusprosessi. Heti kun tilausrivit vapautetaan (joko suoraan lähdeasiakirjasta, erätyöprosessien kautta tai aiemmin luotujen kuormitusten kautta), käyttöön otetaan aaltomallitoiminto. 

Voit luoda kolmentyyppisiä aaltomalleja: 
-   **Lähetys**
-   **Tuotantotilaus**
-   **Kanban** 

Parametreilla määritetään, miten pitkälle järjestelmä käsittelee lähtevät työt. Aaltomalli valitaan aaltomallijakson ja mallissa määritettyjen ehtojen perusteella. Jos malli on jaksossa ylimpänä, kyseisen mallin ehdot tarkistetaan ensimmäisenä. Jos ehdot täyttyvät, aaltomalli käsitellään. Muussa tapauksessa tarkistetaan seuraavan mallin ehdot jne. Tarkimmat ehdot sisältävä malli onkin syytä sijoittaa ylimmäksi aaltomallin jaksoluettelossa, jolloin se käsitellään ensimmäisenä. Voit esimerkiksi haluta käsitellä tietyn rahdinkuljettajan työt tänään ja siirtää väliaikaisesti muiden rahdinkuljettajien töiden käsittelyä. Siinä tapauksessa kyseisen rahdinkuljettajan työn valitsevan aaltomallin on oltava luettelossa korkeammalla kuin muiden mallien. Muussa tapauksessa muiden rahdinkuljettajien työt voidaan käsitellä ennen kuin kyseisen rahdinkuljettajan työt valmistuvat. 

Aallon käsittelymenetelmät on määritettävä kussakin aaltomallissa. Käytettävissä olevat menetelmät vaihtelevat aaltomallin tyypin mukaan.

### <a name="work-templates"></a>Työmallit

Työmallin määritykset ovat tärkeitä varastonhallinnan työprosessien määrityksessä. Ne määrittävät suoritettavat työt ja miten työ suoritetaan. Malleissa voi olla myös sijaintidirektiiviin linkitetty direktiivikoodi, joka määrittää, missä työ suoritetaan. Työmallit sisältävät kyselyn, joka määrittää työn ehdot. Kussakin mallissa on oltava vähintään yksi keräystyövaihe ja yksi määritystoiminto, joiden perusteella suoritetaan perustyövaihe, jossa käytettävissä oleva varasto siirretään sijainnista toiseen. 

Jos useiden työntekijöiden on voitava käsitellä joidenkin varastotoimintojen töitä, kannattaa harkita *väliaikaisen* varaston käyttöä ja työn suorittamisen erottelua eri työluokkiin.

### <a name="work-pools"></a>Työpoolit

Työt voidaan ryhmitellä työpoolien avulla. Voit esimerkiksi luoda työpoolin luokitellaksesi työn, joka tapahtuu tietyssä varastosijainnissa. Voit määrittää laskentaa lukuun ottamatta kaikkien työtyyppien kohdalla työpoolin työmalliin. Voit määrittää inventoinnissa työpoolin seuraavilla sivuilla:

-   Inventointisuunnitelmat
-   Inventointirajat
-   Inventointityö sijainnin mukaan
-   Inventointityö nimikkeen mukaan

Kun työn mallien avulla luodaan työ, työpooli liitetään automaattisesti työhön. 

Työpoolin tunnuksilla voidaan myös rajoittaa tietylle varastotyöntekijälle ohjattavia työtyyppejä, jos toiminto on määritetty soveltuvassa mobiililaitteen valikkovaihtoehdossa.

### <a name="location-directives"></a>Sijaintidirektiivit

Nimen mukaisesti sijaintidirektiiveillä ohjataan työtapahtumia sopiviin varastosijainteihin. Niillä siis toisin sanoen määritetään, missä keräys ja määritys tapahtuu. 

Voit helpottaa ja nopeuttaa kuhunkin sijaintidirektiiviriviin liitettyjen toimintojen määrittämistä käyttämällä jotakin valmista strategiaa. Voit esimerkiksi hakea **Tyhjä sijainti ilman saapuvia töitä** -strategialla vapaita sijainteja varastosta. **FEFO - erän varaus** -strategialla voi puolestaan käyttää lähtevien myyntikeräykseen.

## <a name="additional-resources"></a>Lisäresurssit

[Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa](tasks/configure-locations-wms-enabled-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]