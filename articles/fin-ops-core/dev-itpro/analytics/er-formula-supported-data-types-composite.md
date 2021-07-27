---
title: Sähköisen raportoinnin kaavan tukemat yhdistelmätietotyypit
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) kaavojen tukemista yhdistelmätietotyypeistä.
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2593f3128ec103248e109f3c80f48b9d7a035f54
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355343"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Sähköisen raportoinnin kaavan tukemat yhdistelmätietotyypit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja [sähköisen raportoinnin (ER)](general-electronic-reporting.md) lausekkeiden tukemista yhdistelmätietotyypeistä. Yhdistelmätietotyypit ovat [luokka](#class), [säilö](#container), [tietue](#record), [tietueluettelo](#record-list) ja [objekti](#object).

## <a name="class"></a><a name="class"></a>Luokka

*Luokka*-tietotyyppi viittaa julkiseen sovellusluokkaan. ER:ssä sitä edustaa [*tietue*](#record), joka sisältää erillisen kentän jokaista viitatun luokan julkista menetelmää varten. Kun metodin kutsu määritetään parametrin avulla, myös metodin kutsumiseen määritetyssä ER-lausekkeessa on määritettävä asianmukaista tyyppiä olevat pakolliset argumentit.

ER-[määrityksen](general-electronic-reporting.md#data-model-and-model-mapping-components) ja -[muodon](general-electronic-reporting.md#FormatComponentOutbound) komponentteihin voidaan lisätä **Luokka**-tietolähde, joka näytetään tietolähteenä ja palauttaa *luokka*-tyypin arvon. Tämä tietolähde paljastaa luokan julkiset menetelmät, joita voi kutsua ajon aikana.

> [!NOTE]
> Vain arvon palauttavia menetelmiä voidaan kutsua ER-lausekkeista.
>
> ER-lausekkeista voidaan kutsua vain menetelmiä, joilla on väliltä nolla - kahdeksan argumenttia.

*Luokan* oletusarvo on **tyhjäarvo**.

Seuraavassa kuvassa kerrotaan, miten **Luokka**-tyypin **Järjestelmätiedot(xInfo)**-tietolähde lisätään. Näin **xInfo**-sovellusluokan esiintymä luodaan ja kutsutaan sen **productName()**-menetelmää valitun sovelluksen nimen saamiseksi. Nykyisen sovelluksen nimi haetaan ajonaikaisesta ER-tietomallin **Ohjelmiston nimi(SoftwareName)** -kenttään määritetyn `xInfo.productName`-sidonnan suorituksesta. Tämä sidonta kutsuu **xInfo**-sovellusluokan `productName()`-menetelmää, jota käytetään nykyisessä mallimäärityksessä **Järjestelmätiedot(xInfo)**- tietolähteenä.

[![Luokka-tietolähteen määrittäminen ER-mallin yhdistämismäärityksen suunnittelijassa.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Seuraavassa kuvassa havainnollistetaan, miten ER-muoto on määritetty laittamaan sovelluksen nimen luotuihin tiedostoihin. Käytetyn tietomallin **Ohjelmiston nimi(SoftwareName)** -kenttä sidottiin ER-muodon XML-elementtiin **softwareUsed** upotettuun **Merkkijono**-komponenttiin. Siten nykyisen sovelluksen nimi sijoitetaan ajon aikana XML-elementtiin **softwareUsed** XML-muodossa olevaan luotuun dokumenttiin.

[![Sähköisen lähtevän asiakirjan rakenteen konfiguroiminen ER-muodon suunnitteluohjelmassa.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Säilö

*Säilö*-tietotyyppi sisältää binaarimuotoista sisältöä. *Säilö*-arvon avulla voidaan siirtää tietyt tiedot tallennuksesta luotuun tiedostoon. ER-kehyksessä tätä tietotyyppiä käytetään usein mediasisällön, kuten yrityksen logon, laittamiseen luotuihin tiedostoihin.

> [!NOTE]
> Vaikka jokaista medianimikettä voidaan esittää *säilö*-arvona, kaikki *säilö*-arvot eivät ole mediakohteita. Jos määrität ER-muodon niin, että se käyttää *säilöä* kuvan laittamiseen luotuihin tiedostoihin, mutta viitattu *säilö* ei palauta mediasisältöä, seuraavaa esimerkkiä muistuttava poikkeus heitetään:voi olla seuraava esimerkki: "Koodin virhekäsittely: binaarimuotoisen objektin menetelmässä constructFromContainer-kutsussa on virheellisiä parametreja".

*Säilön* oletusarvo on **tyhjäarvo**.

Seuraavassa kuvassa havainnollistetaan, miten *Säilö*-tyypin **Bittikartta(Image)** -kenttä on sidottu **Myyntilasku**-mallin määrityksen **Säilö**-tyypin tietomallin **Logo**-kenttään. Tämä sidonta mahdollistaa yrityksen logon käytön missä tahansa **SalesInvoice**-juurimääritykseen suunnitellussa ER-muodossa, joka käyttää tätä mallimääritystä ajon aikana.

[![Säilö-tyypin kentän sitominen ER-mallin määrityksen suunnittelutoiminnossa.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Tallenna

*Tietue* on kokoelma nimettyjä kenttiä, joista jokaisen arvona on joko [primitiivinen](er-formula-supported-data-types-primitive.md) tietotyyppi tai yhdistelmätietotyyppi. Yleensä *tietue* edustaa yhtä tietuetta tietueluettelossa. Tässä tapauksessa jokainen nimike edustaa yksittäisiä kenttiä, menetelmiä ja suhteita.

*Tietueen* oletusarvo on **tyhjä**.

> [!NOTE]
> Kun saat tyhjän *tietueen* kentän arvon, palautetaan asianmukaisen tietotyypin oletusarvo.

*Tietue* voidaan noutaa seuraavien toimintojen avulla:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Lisätietoja *tietue*-arvojen muuntamisesta on [luetteloluokan ER-toimintojen luettelossa](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Tietueluettelo

*Tietueluettelo* on *tietue*-tyypin nimikkeiden luettelo. Yleensä *tietueluettelon* avulla voidaan esittää tietokantataulukosta haettujen tietueiden luettelo.

*Tietueluettelon* tietueita käytetään oletusarvoisesti peräkkäin. Voit käyttää tiettyä tietuetta [INDEX](er-functions-list-index.md)-toiminnolla ja määrittää *kokonaisluku*-indeksin.

*Tietueluettelon* oletusarvo on **tyhjä**. [ISEMPTY](/er-functions-list-isempty.md)-toiminnolla voit arvioida, onko *tietueluettelo* tyhjä.

> [!NOTE]
> Jos *tietueluettelo* on tyhjä ja *tietueelle* yritetään saada kentän arvo ajon aikana, poikkeus voidaan heittää ajon aikana. Tietoja tämän tyypin suoritusaikapoikkeusten ehkäisemisestä on ohjeaiheessa [Tyhjien luetteloiden huomioonottaminen](er-components-inspections.md#i9).

*Tietueluettelo* voidaan alustaa seuraavien toimintojen avulla:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Lisätietoja *tietueluettelo*-arvojen muuntamisesta on [luetteloluokan ER-toimintojen luettelossa](er-functions-category-list.md). Tietoja *tietueluettelon* nimikkeiden esittelystä, täyttämisestä sovellustiedoilla ja tietojen käyttämisestä sitten liiketoiminta-asiakirjojen tuottamiseen:  [Mukautetun raportin tulostamisen määrittäminen uudessa ER-ratkaisussa](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekti

*Objekti* viittaa *luokan* tilan sisältävään esiintymään. Yleensä *objekti* käynnistetään lähdekoodissa. Se siirretään sitten ER-mallimääritykseen ja sisältää suorituskontekstin tiedot.

*Objektin* oletusarvo on **tyhjäarvo**.

Seuraavassa kuvassa osoitetaan *Objekti*-tyypin **ReportDataContract**-tietolähde lisätään välittämään tietoja luodusta laskusta lähdekoodista **Projektilasku**-mallimääritykseen. Esimerkiksi laskuinstanssin teksti välitetään suorituskontekstin osana. Tämä teksti otetaan lähdekoodista ajon aikana ER-tietomallin **Huomautus**-kenttään konfiguroidun `ReportDataContract.parmInvoiceInstanceText`-sidonnan suorituksessa. Tämä sidonta kutsuu **PSAProjInvoiceContract**-sovellusluokan `parmInvoiceInstanceText()`-menetelmää, jota käytetään nykyisessä mallimäärityksessä **ReportDataContract**-tietolähteenä.

[![Objekti-tietolähteen määrittäminen ER-mallin yhdistämismäärityksen suunnittelijassa.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Tietoja suorituskontekstin tietojen siirtäminen lähdekoodista käynnissä olevalle ER-ratkaisulle on kohdassa [Kehitä sovelluksen artefaktit kutsumaan suunniteltua raporttia](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kaavakieli](er-formula-language.md)
- [Tuetut primitiiviset tietotyypit](er-formula-supported-data-types-primitive.md)
