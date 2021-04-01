---
title: Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa
description: Tässä opastuksessa selvitetään, miten voit määrittää sijaintiasetuset varastoon, jossa uusi varastonhallintajärjestelmä on otettu käyttöön. (Kyse on varastosta, jossa käytetään varastonhallinnan lisäprosesseja.)
author: perlynne
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8df9f17d9d8c0c84c7c6a829308d44d70bae612f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239107"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa

[!include [banner](../../includes/banner.md)]

Tässä opastuksessa selvitetään, miten voit määrittää sijaintiasetuset varastoon, jossa uusi varastonhallintajärjestelmä on otettu käyttöön. (Kyse on varastosta, jossa käytetään varastonhallinnan lisäprosesseja.) Yleensä tämän prosessin tekee varastopäällikkö. Voit suorittaa opastuksen USMF-demoyrityksen tiedoilla tai käyttää omia tietoja. Edellytyksenä on, että vähintään yksi toimipaikka on määritetty.


## <a name="create-a-new-warehouse"></a>Luo uusi varasto
1. Valitse **Siirtymisruutu > Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Varastoerittely > Varastot**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Varasto**-kenttään.
4. Kirjoita arvo **Nimi**-kenttään.
5. Kirjoita arvo **Toimipaikka**-kenttään.
6. Laajenna **Varasto**-osa.
7. Valitse **Käyttäjän varastonhallintaprosessien virheloki** -asetukseksi Kyllä. Voit suorittaa tällä asetuksella varastoinnin lisäprosesseja varastotyön ja mobiililaitteiden avulla.
8. Sulje sivu.

## <a name="define-a-location-format"></a>Määritä sijainnin muoto
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Sijainnin muodot**. Sijainnin muodot ovat nimeämisjärjestelmä, jolla luodaan yksilölliset ja yhtenäiset nimet varastossa käytettäville eri sijaintien lokeropaikoille. Erottimien käyttö sijaintimuodon osana voi helpottaa sijainnin osien, kuten käytävänumeron, tunnistamista. Tässä esimerkissä luotavassa nimessä on neljä osaa. Ne voivat olla esimerkiksi käytävä, teline, hylly ja lokero.
2. Valitse **Uusi**.
3. Kirjoita **Sijainnin muoto** -kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Kirjoita **Segmentin kuvaus** -kenttään arvo. Tämä kuvaa, mihin sijainnin nimen ensimmäinen osa viittaa. Se voi olla esimerkiksi Käytävä.
6. Lisää **Pituus**-kenttään numero. Tämä määrittää, kuinka monta merkkiä sijainnin nimen tässä osassa on oltava. Huomaa, että kaikki osat, myös erottimet, sisältävän nimen enimmäispituus on 10 merkkiä.    
7. Kirjoita **Erotin**-kenttään arvo. Tämä määrittää, mitä merkkiä tai symbolia käytetään nimen ensimmäisen ja toisen osan välissä.  
8. Valitse **Tiedot**-osassa **Uusi**.
9. Kirjoita **Segmentin kuvaus** -kenttään arvo.
10. Lisää **Pituus**-kenttään numero.
11. Kirjoita **Erotin**-kenttään arvo.
12. Valitse **Tiedot**-osassa **Uusi**.
13. Kirjoita **Segmentin kuvaus** -kenttään arvo.
14. Lisää **Pituus**-kenttään numero.
15. Kirjoita **Erotin**-kenttään arvo.
16. Valitse **Tiedot**-osassa **Uusi**.
17. Kirjoita **Segmentin kuvaus** -kenttään arvo.
18. Lisää **Pituus**-kenttään numero.
19. Valitse **Tallenna**.
20. Sulje sivu.

## <a name="define-location-types"></a>Määritä sijaintityypit
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Sijaintityypit**. Sijainnin tyyppejä voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja. Ainakin väliaikaiset ja lopulliset lähetyssijainnit on luotava, jotta lähtevä varastonhallintaprosessi voidaan määrittää. 
2. Valitse **Uusi**.
3. Kirjoita arvo **Sijainnin tyyppi** -kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Sulje sivu.

## <a name="define-location-profile"></a>Määritä sijaintiprofiili
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit**. Sijaintiprofiilien määritys on erittäin tärkeä. Ryhmiteltyjä sijaintien kapasiteettia voidaan hallita täällä. Lisäksi vodaan hallita käytäntöjä, jotka liittyvät varastoitavan varaston valitsemiseen ja varastointitapaan. Sijaintiprofiileja voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja. Ainakin käyttäjän sijaintiprofiili on luotava, jotta varastonhallintaprosessit voidaan ottaa käyttöön.
2. Valitse **Uusi**.
3. Kirjoita **Sijainnin profiilitunnus** -kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Avaa haku napsauttamalla **Sijainnin muoto** -kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku napsauttamalla **Sijainnin tyyppi** -kentässä avattavan valikon painiketta.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Valitse **Salli yhdistetyt varastotilat** -valintaruutu tai poista sen valinta. Ota tämä asetus käyttöön, jos haluat sallia yhdistetyt varastotila-arvot sijainneissa, jotka ryhmitetään tällä sijaintiprofiililla. 
12. Valitse **Erän käsittelypäivien ohitussäännöt** -valintaruutu tai poista sen valinta. Ota tämä asetus käyttöön, jos haluat ohittaa säännön päivistä, jonka varastoerän vanhentumispäivämäärät voivat erota. Tällä tavoin voidaan yhdistää varastoeriä, joissa tätä sääntöä ei noudateta.  
13. Valitse **Salli inventointi** -valintaruutu tai poista sen valinta. Ottamalla tämän asetuksen käyttöön sallit inventoinnin käsittelyn kaikissa sijainneissa, jotka tullaan ryhmittelemään tällä sijaintiprofiililla. 
14. Laajenna tai tiivistä **Dimensiot**-osa. Dimensiot-välilehden avulla voit määrittää parametrit ja menetelmät, joilla voidaan laskea kuorman kapasiteetti tarkasti kussakin sijainnissa.  
15. Sulje sivu.

## <a name="enable-warehouse-management-parameters"></a>Ota varastonhallinnan parametrit käyttöön
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varastonhallinnan parametrit**. Varastontyön käsittely edellyttää, että käyttäjän profiilityypin, väliaikaissijainnin tyypin ja lopullisen toimitussijainnin tyypin parametrit määritetään. Heti kun lähtevä prosessi päättyy määrittämässäsi lopullisen toimitussijainnin tyypissä, liittyvien lähtevien tapahtumien tilaksi päivittyy Keräilty.
2. Laajenna tai tiivistä **Sijaintiprofiilit**-osa.
3. Avaa haku napsauttamalla **Käyttäjän sijainti** -kentässä avattavan valikon painiketta.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Laajenna tai tiivistä **Sijaintityypit**-osa.
6. Avaa haku napsauttamalla **Vaiheistussijainnin tyyppi** -kentässä avattavan valikon painiketta.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku napsauttamalla **Lopullisen lähetyssijainnin tyyppi** -kentässä avattavan valikon painiketta.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Sulje sivu.

## <a name="define-warehouse-zone-groups"></a>Määritä varastovyöhykeryhmät
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Varastovyöhykeryhmät**. Varastovyöhykkeitä voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja. Vyöhykeryhmä on luotava ennen vyöhykkeen määrittämistä.   
2. Valitse **Uusi**.
3. Kirjoita **Vyöhykeryhmän tunnus** -kenttään arvo.
4. Kirjoita **Vyöhykeryhmän nimi** -kenttään arvo.
5. Sulje sivu.

## <a name="define-warehouse-zones"></a>Määritä varastovyöhykkeet
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Vyöhykkeet**.
2. Valitse **Uusi**.
3. Kirjoita **Vyöhyketunnus**-kenttään arvo.
4. Kirjoita **Vyöhykkeen nimi** -kenttään arvo.
5. Avaa haku napsauttamalla **Vyöhykeryhmän tunnus** -kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Sulje sivu.

## <a name="create-locations-using-the-location-setup-wizard"></a>Luo sijainnit ohjatulla sijaintien asennustoiminnolla
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Ohjattu sijaintien asennustoiminto**.
2. Avaa haku valitsemalla **Varasto**-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Avaa haku napsauttamalla **Vyöhyketunnus**-kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku napsauttamalla **Sijainnin profiilitunnus** -kentässä avattavan valikon painiketta.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Merkitse valittu rivi luettelossa.
12. Lisää **Ensimmäinen numero** -kenttään numero. Ensimmäinen numero- ja Viimeinen numero -kentät määrittävät, kuinka monta sijaintia luodaan. Jos esimerkiksi sijainnin muodon kaikkien neljän rivin Ensimmäinen numero -arvoksi on määritetty 1 ja Viimeinen numero -arvoksi 3, luodaan 81 sijaintia (3x3x3x3).   
13. Lisää **Viimeinen numero** -kenttään numero.
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Lisää **Ensimmäinen numero** -kenttään numero.
16. Lisää **Viimeinen numero** -kenttään numero.
17. Etsi haluamasi tietue luettelosta ja valitse se.
18. Lisää **Ensimmäinen numero** -kenttään numero.
19. Lisää **Viimeinen numero** -kenttään numero.
20. Etsi haluamasi tietue luettelosta ja valitse se.
21. Lisää **Ensimmäinen numero** -kenttään numero.
22. Lisää **Viimeinen numero** -kenttään numero.
23. Valitse Luo.

## <a name="create-locations-manually"></a>Luo sijainnit manuaalisesti
1. Valitse **Varastonhallinta > Asetukset > Varasto > Sijainnit**. Sijaintien luonti varastoon manuaalisesti on helppoa. Sijainnin nimi ja profiilitunnus ovat pakollisia arvoja. 
2. Valitse **Uusi**.
3. Kirjoita arvo **Varasto**-kenttään.
4. Kirjoita arvo **Sijainti**-kenttään. Huomaa, että olet luomassa uutta sijaintia, joten sinun on kirjoitettava uusi yksilöllinen nimi. Et siis voi valita aiemmin luotua nimeä.
5. Kirjoita **Sijainnin profiilitunnus** -kenttään arvo.
6. Sulje sivu.

## <a name="define-pack-size-categories"></a>Määritä pakkauskokoluokat
1. Valitse **Varastonhallinta > Asetukset > Varasto > Pakkauskokoluokat**. Pakkauskokoluokkia voidaan käyttää ryhmittämään nimikkeitä, joiden fyysinen pakkauskoko on lähellä toisiaan. Tässä esimerkissä pakkauskokoluokan avulla hallitaan keräilysijaintien kapasiteettia tietyllä varastovyöhykkeellä. Huomaa, että vapautetulle tuoteyksikölle on määritettävä pakkauskokoluokan tunnus, jotta sitä voi käyttää osana varastointirajoitusten käsittelyä.  
2. Valitse **Uusi**.
3. Kirjoita **Pakkauskokoluokan tunnus** -kenttään arvo.
4. Kirjoita **Pakkauskokoluokan nimi** -kenttään arvo.
5. Sulje sivu.

## <a name="define-location-stocking-limits"></a>Määritä toimipaikan varastointirajoitukset
1. Valitse **Varastonhallinta > Asetukset > Varasto > Sijainnin varastointirajoitukset**. Sijainnin varastointirajoitukset auttavat varmistamaan, että ei luoda työtä, jossa varasto pyydetään sijoittamaan sijaintiin, jonka fyysinen kapasiteetti ei ole riittävä.  
2. Valitse **Uusi**.
3. Kirjoita arvo **Varasto**-kenttään.
4. Kirjoita **Sijainnin profiilitunnus** -kenttään arvo.
5. Kirjoita **Pakkauskokoluokan tunnus** -kenttään arvo.
6. Anna **Määrä**-kentässä numero.
7. Valitse **Tallenna**.
8. Sulje sivu.

## <a name="define-fixed-picking-locations"></a>Määritä kiinteät keräilysijainnit
1. Valitse **Varastonhallinta > Asetukset > Varasto > Kiinteät sijainnit**. Voit määrittää sijaintien käytön tuotteen tai tuotevariantin mukaan. Samalle tuotteelle voi luoda samaan varastoon useita kiinteitä sijainteja.     
2. Valitse **Uusi**.
3. Kirjoita arvo **Nimiketunnus**-kenttään.
4. Kirjoita arvo **Varasto**-kenttään.
5. Avaa haku valitsemalla **Sijainnit**-kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]