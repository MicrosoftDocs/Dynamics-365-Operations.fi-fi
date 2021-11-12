---
title: Mobiililaitteen käyttäjäasetukset
description: Tässä aiheessa kuvataan varastotyöntekijöiden mobiililaitteen käyttäjäasetusten hallinta.
author: MarkusFogelberg
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 51c530fd0043a4ec5a82660af72c001be25b7e62
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647482"
---
# <a name="mobile-device-user-settings"></a>Mobiililaitteen käyttäjäasetukset

[!include [banner](../../includes/banner.md)]

Uusi varastonhallinnan mobiilisovellus sisältää joukon sovelluskohtaisia asetuksia, jotka auttavat käyttäjäkokemuksen räätälöinnissä. Koska sovellusta voidaan käyttää näytöltään erikokoisten ja kokoonpanoltaan erilaisilla laitteilla (kuten tabletilla, puhelimella tai muulla mobiililaitteella), se voi olla hyödyllinen näiden asetusten keskitettyyn hallintaan Microsoft Dynamics 365 Supply Chain Managementilla.

*Mobiililaitteen käyttäjäasetukset* -toiminnolla voit määrittää yleisiä käyttäjäasetuksia, jotka tulevat käyttöön kaikilla laitteilla. Voit myös määrittää yksityiskohtaisempia käyttäjäasetuksia yksittäisille laitemerkeille, laitemalleille ja/tai työntekijöille. Kun työntekijä kirjautuu varastonhallinnan mobiilisovellukseen, sovellus noutaa yksityiskohtaisimman Supply Chain Managementiin tallennetun asetusprofiilin kulloisellekin merkki-, laite- ja/tai käyttäjätunnukselle ja ottaa sen käyttöön.

Tämän toiminnon avulla työntekijät voivat aloittaa uuden laitteen käytön nopeammin. Seuraavassa on muutamia esimerkkejä:

- Järjestelmänvalvojat voivat määrittää vakioasetuksia, jotka toimivat parhaiten tietyn valmistajan ja/tai tietynmallisissa laitteissa. Tämän ansiosta työntekijät voivat aloittaa uuden laitteen käytön ilman pakollista asetusten muuttamista.
- Jos yritykselläsi on joukko identtisiä laitteita, jotka jaetaan työntekijöille, laitteilla on aina käytössä työntekijöiden haluamat asetukset aina, kun he kirjautuvat sisään, vaikka he eivät olisi koskaan käyttäneet kulloisenakin päivänä valitsemaansa fyysistä laitetta.
- Supply Chain Managementissa järjestelmänvalvojat voivat tarkastella ja muokata kaikkia tallennettuja asetuksia ja myös yksittäisten työntekijöiden asetuksia. Tämä ominaisuus auttaa heitä vianmäärityksessä tai uusien toimintojen hienosäätämisessä.

> [!IMPORTANT]
> *Mobiililaitteen käyttäjäasetukset* -toiminto on käytössä vain uudessa varastonhallinnan mobiilisovelluksessa. Se ei toimi vanhan varastosovelluksen yhteydessä.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Mobiililaitteen käyttäjäasetustoiminnon käyttöönotto

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Uuden varastointisovelluksen käyttäjäasetukset, kuvakkeet ja vaiheiden otsikot*

## <a name="create-and-manage-user-settings"></a>Käyttäjäasetusten luonti ja hallinta

**Mobiililaitteen käyttäjäasetukset** -sivun avulla voit luoda, tarkastella ja hallita asetusprofiileja kaikilla yksityiskohtien tasolla. Kun työntekijä muokkaa ensimmäisen kerran uuden laitteen käyttäjäasetuksiaan, tälle sivulle lisätään automaattisesti uusi profiili, jos sellaista ei vielä ole. Tämä profiili päivittyy tämän jälkeen aina, kun työntekijä tekee muutoksen.

Voit myös määrittää asetusprofiilin, jota sovelletaan kaikkiin laitemerkkeihin, laitemalleihin ja/tai työntekijöihin. Tämän jälkeen voit lisätä yksityiskohtaisuutta ottamalla käyttöön yksityiskohtaisempia asetuksia yksittäisille merkeille, malleille ja/tai työntekijöille.

Noudattamalla näitä ohjeita voit luoda ja hallita mobiililaitteen käyttäjäasetuksia.

1. Siirry kohtaan **Varastonhallinta \> Määritys \> Mobiililaite \> Mobiililaitteen käyttäjäasetukset**.
1. Avaa olemassa olevan käyttäjäasetusprofiilin tietue valitsemalla se luetteloruudusta. Vaihtoehtoisesti voit luoda uuden profiilin valitsemalla toimintoruudusta **Uusi**.

    Kunkin luetteloruudun profiiliin on merkitty merkki, malli ja/tai käyttäjätunnus, johon profiilia sovelletaan. Yleisemmillä profiileilla joidenkin tai kaikkien näiden ominaisuuksien arvona on *Kaikki*.

1. Määritä uuden tai valitun asetusprofiilin tietueen otsikossa seuraavat kentät:

    - **Laitteen merkin nimi** – Valitse laitteen merkki, johon profiilia sovelletaan. Jos profiilia on tarkoitus soveltaa kaikkiin merkkeihin, tämä kenttä jätetään tyhjäksi. Arvojen luettelo sisältää kaikki merkit, jotka on määritetty järjestelmässä. Tietoja merkkiluettelon määrittämisestä on seuraavassa osassa.
    - **Laitteen mallitunnus** – Valitse laitteen malli, johon profiilia sovelletaan. Jos profiilia on tarkoitus soveltaa kaikkiin valitun merkin malleihin, tämä kenttä jätetään tyhjäksi. Arvojen luettelo sisältää kaikki mallit, jotka on määritetty merkille, joka on valittu **Laitteen merkin nimi** -kentässä. Tietoja kunkin merkin malliluettelon määrittämisestä on seuraavassa osassa.
    - **Käyttäjätunnus** – Valitse sen varastotyöntekijän käyttäjätunnus, johon profiilia sovelletaan. Jos profiilia on tarkoitus soveltaa kaikkiin työntekijöihin, tämä kenttä jätetään tyhjäksi.

1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Painikkeen sijainti** – Valitse, miten painikkeet sijoitetaan laitteella. Sovelluksen elementtejä siirretään siten, että ne sopivat paremmin työntekijän tarpeisiin tai kätisyyteen. Käytettävissä olevat vaihtoehdot ovat *Oikea alakulma (oletus)*, *Vasen alakulma*, *Oikea yläkulma* ja *Vasen yläkulma*.
    - **Näytön suunta** – Valitse näytön suunta, jota sovelluksessa käytetään oletusarvoisesti.
    - **Skannaus kameralla** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää laitteen kameraa syöttökenttien skannaamiseen, kun ensisijaiseksi syöttötavaksi on valittu *Skannaus*. Jos laitteessasi on sisäinen skanneri, määritä tämän asetuksen arvoksi *Ei*, jolloin käytetään kyseistä skanneria.
    - **Näytä tuotekuva** – Valitse, näytetäänkö vapautetun tuotteen tuotekuvat, jos niitä on käytettävissä. Lisätietoja tuotekuvien lisäämisestä: [Kuvan lisääminen tuotteelle](../pim/tasks/add-image-product.md).
    - **Näytön väriteema** – Valitse laitteen väriteema.
    - **Äänitaso** – Valitse laitteen äänitaso. Valitse arvo väliltä 0 (nolla) – 10. Arvo *0* tarkoittaa äänettömyyttä ja arvo *10* tarkoittaa suurinta äänenvoimakkuutta. Oletusarvona on *4*.
    - **Värinätaso** – Valitse laitteen värinätaso. Valitse arvo väliltä 0 (nolla) – 5. Arvo *0* tarkoittaa, että värinä on pois käytöstä, ja arvo *5* tarkoittaa suurinta värinätasoa. Oletusarvona on *1*.
    - **Tekstin skaalausprosentti** – Määritä tekstin koko vakiokoon prosenttiosuutena. Anna arvo välillä 70–400. Arvo *70* edustaa pienintä tekstikokoa ja arvo *400* suurinta tekstikokoa. Oletusarvona on *100*.
    - **Painikkeiden skaalausprosentti** – Määritä painikkeiden koko vakiokoon prosenttiosuutena. Anna arvo välillä 50–200. Arvo *50* edustaa pienintä painikekokoa ja arvo *200* suurinta painikekokoa. Oletusarvona on *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Mobiililaitemerkkien luominen ja hallinta

**Mobiililaitteiden merkit** -sivulla voit tarkastella, luoda ja hallita laitemerkkejä ja -malleja, joita voi käyttää asetusprofiilien kanssa. Mobiilisovellus noutaa ja lähettää automaattisesti paikallisen merkkinimen ja mallitunnuksen, kun työntekijä muokkaa asetuksiaan ensimmäistä kertaa tietyllä laitteella. Siten useimmat näistä tietueista ovat automaattisesti luotuja. Voit kuitenkin myös hallita kaikkia sivun tietueita. Voit esimerkiksi syöttää kullekin merkille ja mallille höydyllisempiä kuvauksia, jotta ne on helpompi erottaa samanlaisista tai epäselvistä mallitunnuksista.

Noudattamalla näitä ohjeita voit luoda ja hallita mobiililaitteiden merkkejä ja malleja.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitebrändit**.
1. Voit avata mobiililaitteen merkin tietueen valitsemalla sen luetteloruudusta. Vaihtoehtoisesti voit luoda uuden merkin valitsemalla toimintoruudusta **Uusi**.
1. Määritä uuden tai valitun laitemerkin tietueen otsikossa seuraavat kentät:

    - **Laitteen merkin nimi** – Laitteen merkin nimi, kuten *Microsoft Corporation*.
    - **Kuvaus** – Voit kirjoittaa kuvauksen, jonka avulla merkki erottuu helpommin muista merkeistä.

1. **Mobiililaitteen mallit** -pikavälilehdellä näkyvät kaikki valitun laitemerkin mallit. Voit lisätä ruudukkoon rivejä tai poistaa niitä työkalurivin painikkeiden avulla. Voit määrittää kullekin riville seuraavat kentät:

    - **Laitteen mallitunnus** – Laitteen mallitunnus, kuten *Surface Book 2*.
    - **Kuvaus** – Voit kirjoittaa kuvauksen, jonka avulla merkki erottuu helpommin muista mallitunnuksista.

## <a name="additional-resources"></a>Lisäresurssit

- [Varastonhallinnan mobiilisovelluksen asentaminen ja yhteyden muodostaminen](install-configure-warehouse-management-app.md)
- [Warehouse Management -mobiilisovelluksen vaihekuvakkeiden ja otsikoiden määrittäminen](step-icons-titles.md)