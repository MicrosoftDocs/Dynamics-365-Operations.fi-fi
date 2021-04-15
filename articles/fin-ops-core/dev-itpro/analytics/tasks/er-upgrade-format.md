---
title: ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muotomäärityksen ylläpitoa.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f8562bcab50a303b58174d177c6058f9417294
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744936"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER Muodon päivittäminen ottamalla käyttöön sitä koskeva uusi perusversio

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi ylläpitää muotokonfiguraatiota sähköiselle raportoinnille (ER). Seuraavassa menettelyssä kerrotaan, miten luodaan muodosta mukautettu versio konfiguroinnin lähteen (CP) tarjoaman muodon perusteella. Siinä käsitellään myös muodon uuden perusversion käyttöönotto.

Näitä vaiheita varten on suoritettava ensin seuraavien menettelyiden vaiheet: "Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi" ja "Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen". Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.

## <a name="select-format-configuration-for-customization"></a>Mukautettavan muotokonfiguraation valinta
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.

    Tässä esimerkissä malliyritys Litware, Inc. (https://www.litware.com) toimii konfiguraation lähteenä, joka tukee tietyn maan muotokonfiguraatioita sähköisille maksuille.    Malliyritys Proseware, Inc. (http://www.proseware.com) toimii kuluttajana Litware, Inc.:n toimittamalle muotokonfiguraatiolle. Proseware, Inc. käyttää muotoja tietyillä maan alueilla.  
2. Valitse Raportointikonfiguraatiot.
3. Valitse Näytä suodattimet.
4. Käytä seuraavia suodattimia: Anna suodattimen arvoksi Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen) käyttämällä Alkaa-suodatinoperaattoria.
  
    Valitun BACS-muotomäärityksen (Iso-Britannia, kuvitteellinen ja mukautettu) omistaja on toimittaja Litware, Inc.  

5. Valitse Näytä suodattimet.
6. Etsi haluamasi tietue luettelosta ja valitse se.

    Proseware Inc. käyttää mukauttamiseen tämän muodon versiota, jonka tila on Valmis.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Luo uusi konfiguraatio sähköisen asiakirjan mukautetulle muodolle
Proseware Inc. on vastaanottanut Litware, Inc:ltä palvelutilauksen mukaisesti version 1.1 BACS-muotokonfiguraatiosta (Iso-Britannia, kuvitteellinen), joka sisältää alustavan muodon sähköisten maksuasiakirjojen luomiseen Proseware Inc. haluaa käyttää konfiguraatiota vakiomuodossaan maassaan, mutta joitain mukautuksia tarvitaan tukemaan aluekohtaisia erityisvaatimuksia. Proseware Inc. haluaa säilyttää mahdollisuuden päivittää mukautetun muodon heti, kun uusi versio (joka sisältää muutoksia uusien maakohtaisten vaatimusten tukeen) on saatavilla Litware, Inc:ltä. Yritys haluaa myös suorittaa päivityksen mahdollisimman edullisesti.  

Tätä varten Proseware, Inc:n on luotava määritys käyttämällä Litware, Inc:n BACS-muotokonfiguraatiota (Iso-Britannia, kuvitteellinen) pohjana.  

1. Sulje sivu.
2. Valitse Proseware, Inc. ja tee siitä aktiivinen lähde.
3. Valitse Aseta aktiiviseksi.
4. Valitse Raportointikonfiguraatiot.
5. Laajenna puussa solmu Payments (simplified model).
6. Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).

    Valitse Litware, Inc:n BACS-muotokonfiguraatio (Iso-Britannia, kuvitteellinen). Proseware, Inc. käyttää versiota 1.1 mukautetun version pohjana.  

7. Avaa valintaikkuna napsauttamalla Luo konfigurointi.

    Näin voit luoda uuden määrityksen mukautetulle maksumuodolle.  

8. Anna Uusi-kentän arvoksi "Derive from Name: BACS (UK fictitious), Litware, Inc."

    Valitse Johda-vaihtoehto vahvistaaksesi BACS (Iso-Britannia, kuvitteellinen) -konfiguraation käytön pohjana mukautetulle versiolle.  

9. Syötä Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen ja mukautettu).
10. Kirjoita Kuvaus-kenttään BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen ja mukautettu).

    Aktiivinen konfiguraation lähde (Proseware, Inc.) syötetään tähän automaattisesti. Tämä lähde voi ylläpitää tätä konfiguraatiota. Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.  

11. Valitse Luo konfiguraatio.

## <a name="customize-your-format-for-the-electronic-document"></a>Sähköisen asiakirjan muodon mukauttaminen
1. Valitse Suunnittelutoiminto.
2. Valitse Laajenna tai tiivistä.
3. Valitse Laajenna tai tiivistä.
4. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.
5. Avaa valintaikkuna valitsemalla Lisää.
6. Valitse puussa solmu XML\Element.
7. Syötä Nimi-kenttään IBAN.
8. Valitse OK.
9. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\IBAN.
10. Avaa valintaikkuna valitsemalla Lisää.
11. Valitse puussa solmu Text\String.
12. Valitse OK.
13. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.
14. Anna Enimmäispituus-kentän arvoksi 60.
15. Valitse Yhdistämismääritys-välilehti.
16. Laajenna puussa solmu model.
17. Laajenna puussa solmu model\Payments.
18. Laajenna puussa solmu model\Payments\Creditor.
19. Laajenna puussa solmu model\Payments\Creditor\Account.
20. Valitse puussa malli\Maksut\Laskuttaja\Tili\IBAN.
21. Valitse puussa Xml\Sanoma\Maksut\Nimike =  model.Payments\Vendor\Bank\IBAN\String.
22. Valitse Sido.
23. Valitse Tallenna.

## <a name="validate-the-customized-format"></a>Mukautetun muodon vahvistaminen
1. Valitse Vahvista.

    Vahvista mukautetun muodon asettelu ja tietojen yhdistämisen muutokset, että kaikki sidokset ovat kunnossa.  

2. Sulje sivu.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Mukautetun muotomäärityksen nykyisen version tilan muuttaminen
Muuta suunnitellun muotomäärityksen tila Luonnos-tilasta Valmis-tilaan. Tällöin se on käytettävissä maksuasiakirjojen luomiseen.  

1. Voit muuttaa tilaa valitsemalla Muuta.

    Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.  

2. Valitse Valmis.
3. Kirjoita arvo Kuvaus-kenttään.
4. Valitse OK.
5. Etsi haluamasi tietue luettelosta ja valitse se.

    Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.1.1. Tämä tarkoittaa, että kyseessä on mukautetun BACS-muodon (Iso-Britannia, kuvitteellinen ja mukautettu) versio 1, joka perustuu BACS-muodon versioon 1, joka perustuu Maksut-tietomallin versioon 1 (yksinkertaistettu malli).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Mukautetun muodon maksutiedostojen luonnin testaaminen
Suorita Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen -menettelyn vaiheet rinnakkaisessa Finance and Operations -istunnossa. Valitse BACS-muoto (Iso-Britannia, kuvitteellinen ja mukautettu) sähköisen maksutavan parametreissa. Varmista, että luotu maksutiedosto sisältää on viimeisimmän XML-solmun, joka vastaa IBAN-koodia aluekohtaisten vaatimusten mukaisesti.  

## <a name="update-the-existing-country-specific-configuration"></a>Olemassaolevien maakohtaisten konfiguraatioiden päivittäminen
Litware, Inc. haluaa päivittää BACS-konfiguraation (Iso-Britannia, kuvitteellinen) ja ottaa käyttöön uudet maavaatimukset sähköisen asiakirjan muodon hallinnassa. Tämä sisältyy tulevaan konfiguraation versiopäivitykseen, joka tarjotaan palvelun tilaajille, joihin Proseware, Inc. kuuluu.  

Todellisissa palveluntoteutusprosesseissa Proseware Inc. voi tuoda jokaisen uuden version BACS-muodosta (Iso-Britannia, kuvitteellinen) Litware, Inc:n LCS-konfiguraatiosäilöstä. Näissä toimintaohjeissa tätä simuloidaan päivittämällä BACS-muoto (Iso-Britannia, kuvitteellinen) palveluntarjoajan puolesta.  

1. Sulje sivu.
2. Valitse lähteeksi Litware, Inc.
3. Valitse Aseta aktiiviseksi.
4. Valitse Raportointikonfiguraatiot.
5. Laajenna puussa solmu Payments (simplified model).
6. Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).

    Litware, Inc:n omistaman luonnosversion lähde-BACS (Iso-Britannia, kuvitteellinen) valitaan tuomaan uusien maakohtaisten vaatimusten tuki.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Sähköisen asiakirjan perusmuodon lokalisoiminen
Oletetaan, että Litware Inc:n on tuettava seuraavia uusia maakohtaisia vaatimuksia:  

- Arvo laskuttajan SWIFT-koodille jokaisessa maksutapahtumassa.
- 100 merkin raja toimittajan nimelle luontitiedostossa.  
- Uudet maakohtaiset vaatimukset  
- Valitse halutun konfiguraation luonnosversio tuodaksesi vaaditut muutokset.  


1. Valitse Suunnittelutoiminto.
2. Valitse Laajenna tai tiivistä.
3. Valitse Laajenna tai tiivistä.
4. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.
5. Avaa valintaikkuna valitsemalla Lisää.
6. Valitse puussa solmu XML\Element.
7. Syötä Nimi-kenttään SWIFT.
8. Valitse OK.
9. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\SWIFT.
10. Avaa valintaikkuna valitsemalla Lisää.
11. Valitse puussa solmu Text\String.
12. Valitse OK.
13. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.
14. Anna Enimmäispituus-kentän arvoksi 100.
15. Valitse Yhdistämismääritys-välilehti.
16. Laajenna puussa solmu model.
17. Laajenna puussa solmu model\Payments.
18. Laajenna puussa solmu model\Payments\Creditor.
19. Laajenna puussa solmu expand 'model\Payments\Creditor\Agent.
20. Valitse puussa malli\Maksut\Laskuttaja\Edustaja\SWIFT.
21. Valitse puussa Xml\Sanoma\Maksut\Nimike =  model.Payments\Vendor\Bank\SWIFT\String.
22. Valitse Sido.
23. Valitse Tallenna.

## <a name="validate-the-localized-format"></a>Lokalisoidun muodon tarkistaminen
1. Valitse Vahvista.
2. Sulje sivu.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Muotokonfiguraation nykyisen perusversion tilan muuttaminen
Muutta päivitetyn muotokonfiguraation perusversion tila luonnoksesta valmiiksi, jotta se on käytettävissä maksuasiakirjojen luomiseen ja siitä johdettujen muotokonfiguraatioiden päivityksiin.  

1. Voit muuttaa tilaa valitsemalla Muuta.

    Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.  

2. Valitse Valmis.
3. Kirjoita arvo Kuvaus-kenttään.
4. Valitse OK.
5. Etsi haluamasi tietue luettelosta ja valitse se.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Mukautetun muotokonfiguraation perusversion muuttaminen

Proseware, Inc. saa tiedon, että saatavilla on BACS-konfiguraation (Iso-Britannia, kuvitteellinen) versiopäivitys 1.2, jolla on mahdollista luoda sähköisiä maksuasiakirjoja vasta julkaistujen maakohtaisten vaatimusten mukaisesti. Proseware, Inc. haluaa käyttää uutta versiota maan standardien noudattamiseen.  

Tämän vuoksi Proseware, Inc:n on muutettava peruskonfiguraation versiota mukautetulle BACS-konfiguraatiolleen (Iso-Britannia, kuvitteellinen ja mukautettu). Käytä uutta versiota 1.2 edellisen BACS-muodon (Iso-Britannia, kuvitteellinen) 1.1-version sijaan.  

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Proseware, Inc -lähde ja merkitse aktiiviseksi.
3. Valitse Aseta aktiiviseksi.
4. Valitse Raportointikonfiguraatiot.
5. Laajenna puussa solmu Payments (simplified model).
6. Laajenna puussa solmu Payments (simplified model)\BACS (UK fictitious).
7. Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom).

    Valitse BACS-muodon (Iso-Britannia, kuvitteellinen ja mukautettu) konfiguraatio, jonka omistaa Proseware, Inc.  

    Käytä valitun konfiguraation luonnosversiota tuodaksesi vaaditut muutokset.  

8. Valitse Pohjusta.

    Valitse peruskonfiguraation uusi versio 1.2 käytettäväksi perusteena konfiguraation päivityksille.  

9. Valitse OK.

    Huomaa, että osaa muodon muutosten ristiriidoista, jotka havaitaan mukautetun version ja uuden perusversion yhdistämisen yhteydessä, ei voida yhdistää automaattisesti.  

## <a name="resolve-rebase-conflicts"></a>Pohjustusriitojen ratkaiseminen
1. Valitse Suunnittelutoiminto.
    
    Huomaa, että muutoksia toimittajan nimen pituusrajoitukseen ei voitu selvittää automaattisesti. Tämä esitetään sen vuoksi ristiriitojen luettelossa. Jokaiselle päivitystyypin ristiriidalle on seuraavat ratkaisuvaihtoehdot: - Käytä aiempaa perusarvoa (painike ruudukon yläpuolella) edellisen perusversion arvon mukaisesti (tässä tapauksessa 0).  - Käytä perusarvoa (painike ruudukon yläpuolella) uuden perusversion arvon mukaisesti (tässä tapauksessa 100).  - Säilytä oma (mukautettu) arvo (tässä tapauksessa 60).  Valitse Kohdista perusarvo -painiketta kohdistaaksesi maakohtaisesti sallitut 100 merkkiä toimittajan nimille.  

    Huomaa, että Proseware, Inc. ja Litware, Inc. käyttävät mukautettuja ja paikallisia versioita tästä muodosta käyttäen IBAN- ja SWIFT-koodeja liittyvissä komponenteissa, jotka yhdistetään automaattisesti hallitussa muodossa.  

2. Valitse Käytä aiempaa perusarvoa.

    Valitse Kohdista perusarvo -painiketta kohdistaaksesi maakohtaisesti sallitut 100 merkkiä toimittajan nimille.  

3. Valitse Tallenna.

    Muodon tallentaminen poistaa ratkaistut ristiriidat luettelosta.  

4. Sulje sivu.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Muotokonfiguraation uuden mukautetun version tilan muuttaminen
1. Voit muuttaa tilaa valitsemalla Muuta.

    Muuttaa päivitetyn mukautetun muotokonfiguraation tilan luonnoksesta valmiiksi. Muotomääritykset ovat nyt käytettävissä maksuasiakirjoja luotaessa. Huomaa, että valitun konfiguraation nykyisen version tila on Luonnos.  

2. Valitse Valmis.
3. Kirjoita arvo Kuvaus-kenttään.
4. Valitse OK.

    Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.2.2: BACS-perusmuodon (Iso-Britannia, kuvitteellinen ja mukautettu) versiona 2, joka perustuu BACS-perusmuodon (Iso-Britannia, kuvitteellinen) versioon 2, joka perustuu maksujen tietomallin versioon 1 (yksinkertaistettu malli).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Mukautetun muodon maksutiedostojen luonnin testaaminen
Suorita Käytä luotua muotoa sähköisten maksuasiakirjojen luomiseen -menettelyn vaiheet rinnakkaisessa Finance and Operations -istunnossa. Valitse luotu BACS-muoto (Iso-Britannia, kuvitteellinen ja mukautettu) sähköisen maksutavan parametreissa. Varmista, että luotu maksutiedosto sisältää on viimeisimmän Proseware, Inc:n XML-solmun, joka vastaa IBAN-tilikoodia aluekohtaisten vaatimusten mukaisesti. Tiedoston pitäisi myös sisältää viimeisin Litware, Inc:n XML-solmu, joka edustaa SWIFT-pankkikoodia maakohtaisten vaatimusten mukaisesti.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]