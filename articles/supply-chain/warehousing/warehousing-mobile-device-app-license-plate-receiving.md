---
title: Rekisterikilven vastaanotto varastosovelluksen avulla
description: Tässä ohjeaiheessa selitetään, kuinka varastosovellus määritetään tukemaan rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: f921d08572038d2ac53948825a8ca2459103b7f7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245151"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a>Rekisterikilven vastaanotto varastosovelluksen avulla

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa selitetään, kuinka varastosovellus määritetään niin, että se tukee rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.

Tämän toiminnon avulla voit nopeasti kirjata saapuvaa varastoa koskevan vastaanoton, joka liittyy ennakkoilmoitukseen (ASN). Järjestelmä luo automaattisesti ASN-arvon, kun siirtotilauksen lähetys suoritetaan varastoinnin hallintaprosessien avulla. Ostotilausprosessin aikana ASN voidaan tallentaa manuaalisesti, tai se voidaan tuoda automaattisesti käyttämällä saapuvan ASN-tietoyksikkö prosessia.

ASN-tiedot linkitetään kuormiin ja lähetyksiin *pakkausrakenteiden* kautta, joissa kuormalavat (päärekisterikilvet) voivat sisältää palvelupyyntöjä (sisäkkäisiä rekisterikilpiä).

> [!NOTE]
> Kun käytetään sisäkkäisten rekisterikilpien pakkausrakenteita, järjestelmä tallentaa varastotapahtumien määrän pääkäyttöoikeusrekisterikilpeen. Jos haluat käynnistää fyysisen käytettävissä olevan varaston siirtämisen pääkäyttöoikeusrekisterikilvestä sisäkkäisiin rekisteritietoihin perustuen, mobiililaitteen on määritettävä pakkausrakenteen tietojen perusteella valikkovaihtoehto, joka perustuu *pakkauksen sisäkkäinen rekisterikilpi* -töiden luomisprosessiin.

## <a name="warehousing-mobile-device-app-processing"></a>Varastoinnin mobiililaitteiden sovelluksen käsittely

Kun työntekijä tarkistaa saapuvan rekisterikilven tunnuksen, järjestelmä alustaa rekisterikilven vastaanottoprosessin. Näiden tietojen perusteella rekisterikilven sisältö (ASN-palvelimesta peräisin olevat tiedot) rekisteröidään fyysisesti saapuvien laiturisijaintiin. Seuraavat virrat riippuvat liiketoimintaprosessin tarpeista.

## <a name="work-policies"></a>Työkäytännöt

Kuten (esimerkiksi) *Ilmoita valmiiksi* -mobiililaitteen valikkovaihtoehtoprosessi, rekisterikilven vastaanottoprosessi tukee useita työnkulkuja määritettyjen asetusten perusteella.

### <a name="work-policies-with-work-creation"></a>Työkäytännöt ja työn luominen

Kun rekisteröit saapuvat nimikkeet käyttämällä työkäytäntöä, joka luo työtä, järjestelmä luo ja tallentaa hyllytystyötiedot kullekin rekisteröinnille. Jos käytät *rekisterikilven vastaanotto- ja hyllytys* -työprosessia, rekisteröintiä ja hyllytystä käsitellään yhtenä työvaiheena yhden mobiililaitteen valikkovaihtoehdon avulla. Jos käytät *rekisterikilven vastaanotto* -prosessia, vastaanotto- ja hyllytysprosessit käsitellään kahtena eri varaston työvaiheena, joilla kullakin on oma mobiililaitevalikkovaihtoehto.

### <a name="work-policies-without-work-creation"></a>Työkäytännöt ilman työn luomista

Voit käyttää rekisterikilven vastaanottoprosessia luomatta työtä. Jos määrität työkäytäntöjä, joilla on *siirtovastaanotto* - ja/tai *ostotilausten* -työtilaustyyppiprosessi, ja käytät *rekisterikilven vastaanottaminen (ja hyllyttäminen)* -prosessia, seuraavat kaksi varastoinnin mobiilisovelluksen prosessia eivät luo työtä. Sen sijaan ne vain rekisteröivät saapuvan fyysisen varaston saapuvien vastaanoton rekisterikilpeen.

- *Rekisterikilven vastaanotto*
- *Rekisterikilven vastaanotto ja poispano*

> [!NOTE]
> - Työkäytännölle on määritettävä vähintään yksi sijainti **Varastopaikat**-osassa. Et voi määrittää samaa sijaintia useille työkäytännöille.
> - Varastointilaitteen valikkovaihtoehtojen **Tulosta tarra** -asetus ei tulosta rekisterikilven otsikkoa ilman työn luontia.

Jotta tämä toiminto olisi käytettävissä järjestelmässäsi, sinun on otettava käyttöön *rekisterikilven vastaanottolaajennukset*-ominaisuus [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Vastaanota varastosijaintiin, joka ei seuraa rekisterikilpiä

On mahdollista käyttää varastopaikkaa, joka on määritetty sijaintiprofiiliin, vaikka **rekisterikilven seurantaa** ei olisikaan käytössä. Näin ollen, kun vastaanotat varaston, voit rekisteröidä käytettävissä olevan varaston suoraan sijaintiin ilman töiden luontia.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Mobiililaitteen valikkovaihtoehtojen lisääminen kuhunkin vastaanottosijaintiin varastossa

*Rekisterikilven vastaanottoparannukset* -toiminnon avulla voit vastaanottaa tietoja missä tahansa varastossa lisäämällä sijaintikohtaiset rekisterikilven vastaanotto- (ja hyllytys)-valikkokohteet varastointimobiilisovellukseen. Aiemmin järjestelmä tuki vain kullekin varastolle määritettyä oletussijaintia. Kuitenkin, kun tämä toiminto on käytössä, mobiililaitteen valikkovaihtoehdot rekisterikilven vastaanottamiseen (ja hyllyttämiseen) tarjoavat nyt **Käytä oletustietoja** -vaihtoehdon, jonka avulla voit valita kullekin valikkokohteelle mukautetun sijainnin. (Tämä vaihtoehto on jo käytettävissä joidenkin muun tyyppisten valikkovaihtoehtojen yhteydessä.)

Jotta tämä toiminto olisi käytettävissä järjestelmässäsi, sinun on otettava käyttöön *rekisterikilven vastaanottolaajennukset*-ominaisuus [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Vastaanottavan yhteenvetosivun näyttäminen tai ohittaminen

Voit käyttää *ohjausobjektia, näytetäänkö vastaanottavan yhteenvetosivun mobiililaitteissa* -ominaisuutta, jotta saat lisätietoja fyysisen varastoinnin sovelluskulusta osana rekisterikilven vastaanottoprosessia.

Kun tämä toiminto on otettu käyttöön, mobiililaitteiden valikkokohteet, jotka koskevat rekisteritietoja tai rekisterikilven vastaanottoa ja hyllytystä, sisältävät **näytön vastaanottamisen yhteenvetosivu** -asetuksen. Tällä asetuksella on seuraavat vaihtoehdot:

- **Näytä yksityiskohtainen yhteenveto** – Rekisterikilven vastaanottamisen aikana työntekijät näkevät ylimääräisen sivun, jossa näkyvät kaikki ASN-tiedot.
- **Ohita yhteenveto** – Työntekijät eivät näe kaikkia ASN-tietoja. Varastotyöntekijät eivät voi määrittää käsittelykoodia tai lisätä poikkeuksia vastaanottoprosessin aikana.

Jotta tämä toiminto olisi käytettävissä järjestelmässäsi, sinun on otettava käyttöön *ohjausobjekti, joka näyttää vastaanottajan yhteenvetosivun ominaisuuksien hallinnan mobiililaitteissa* -toiminto [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Estä siirtotilauksen lähettämien rekisterikilpien käyttö muissa varastoissa kuin kohdevarastossa

Rekisterikilven vastaanottoprosessia ei voi käyttää, jos ASN sisältää rekisterikilven tunnuksen, joka on jo olemassa ja jolla on fyysisiä käytettävissä olevia tietoja varastosijainnissa, joka ei ole sama kuin varastosijainti, jossa rekisterikilpi rekisteröidään.

Siirtotilausten tapauksissa, joissa kuljetusvarasto ei jäljitä rekisterikilpiä (eikä näin ollen myöskään kirjaa fyysistä käytettävissä olevaa varastoa rekisterikilpeä kohden), voit käyttää *Estä siirtotilauksen mukana toimitettuja rekisterikilpiä käytettäväksi muissa varastoissa kuin kohdevarastossa* -toimintoa, joka estää kauttakuljetuksessa olevien rekisterikilpien fyysisten käytettävissä olevien päivitysten käytön.

Jotta tämä toiminto olisi käytettävissä järjestelmässä, sinun on otettava käyttöön *Estä siirtotilauksen lähetysrekisterikilvet, joita käytetään muissa varastoissa kuin ominaisuuksien hallinnan kohdevarastossa* -ominaisuus [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Voit hallita toimintoja, kun tämä toiminto on käytettävissä, noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Yleinen**-välilehden **Rekisterikilvet**-pikavälilehdessä, että **Kuljetusvaraston rekisterikilpikäytäntö** -kenttä on jokin seuraavista arvoista:

    - **Salli ei-seurattujen rekisterikilpien uudelleenkäyttö** – Järjestelmä toimii samalla tavalla kuin se toimii, kun *Estä siirtotilauksen toimittamien rekisterikilpien käyttö muissa varastoissa kuin kohdevarasto* -toiminto ei ole käytössä. Tämä arvo on oletusasetus, kun aktivoit ominaisuuden ensimmäisen kerran.
    - **Ei-seuratun rekisterikilven uudelleenkäytön estäminen** – Kohdevarastossa sallitaan vain käytettävissä olevat päivitykset, jotka liittyvät toimitettuun rekisterikilpeen, kunnes siirtotilaus on vastaanotettu.

## <a name="more-information"></a>Lisätietoja

Lisätietoja mobiililaitteiden valikkokohteista on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).

Lisätietoja *Ilmoita valmiiksi* -tuotantoskenaariosta on kohdassa [fyysisen varastoinnin työkäytäntöjen yleiskuvaus](warehouse-work-policies.md).

Lisätietoja saapuvien kuormien hallinnasta on kohdassa [Ostotilausten saapuvien kuormien varastokäsittely](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]