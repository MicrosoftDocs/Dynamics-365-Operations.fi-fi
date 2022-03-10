---
title: Konfiguroi jaetut parametrit
description: Tässä aiheessa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039d8e2100824921d568c013fe3e113e1b091979
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729096"
---
# <a name="configure-shared-parameters"></a>Konfiguroi jaetut parametrit

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten **Toimi**-tietueille. Tässä aiheessa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.

Jotkin tietuetyypit, kuten **Toimi**-tietueet, jaetaan yritysten kesken. Näille tietueille on määritettävä jaetut parametrit. Esimerkiksi **Henkilöstöhallinnon jaetut parametrit** -sivua käytetään yritysten kesken jaettujen henkilöstöparametrien määrittämiseen. 

**Henkilöstöhallinnon jaetut parametrit** -sivulla parametrit ryhmitellään alueisiin niiden toimintojen perusteella. 

### <a name="settings"></a>Asetukset
**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita. On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille. Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla. Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstön hallinta** &gt; **Linkit** &gt; **Määritys** &gt; **Tunnustyypit**. Voit syöttää yksinkertaisen koodin ja kuvauksen. 

**Numerojärjestykset**-välilehdessä voidaan valita numerosarjat, joita käytetään seuraavissa tietueissa: **Henkilöstönumero**, **Toimi**, **Käyttäjäpyynnön tunnus**, **I-9-asiakirja**, **Hakija**, **Keskustelu**, **Etutunnus** ja **Henkilöstötoiminto** (jos tämä tietuetyyppi on otettu käyttöön). Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua. Käytä sivun hakutoimintoa löytääksesi tämän sivun. 

Ilmaise **Toimet**-välilehdellä, ovatko uudet toimet oletusarvoisesti käytettävissä toimeksiantoa varten:

- **Aina** – Voit määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Kun toimet on luotu, **Käytettävissä toimeksiantoa varten** -päivämäärä ja -aika **Yleinen** -välilehden **Toimi**-sivulla asetetaan automaattisesti sen luontipäivämääräksi ja -ajaksi.
- **Ei koskaan** – Et voi määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Jos valitset tämän vaihtoehdon, sinun on avattava kunkin uuden toimen **Toimi**-sivu, kun se tulee saataville. Syötä sitten **Yleiset**-välilehdessä **Käytettävissä toimeksiantoa varten** -päivämäärä mahdollistaaksesi työntekijän kohdistamisen.

Voit rajoittaa joidenkin tietojen tai linkkien käyttöoikeuksia **Lisäkäyttöoikeudet**-välilehdestä:

- **Rajoita työntekijätietojen käyttöoikeuksia** – Valitse tämä ominaisuus, jos käyttäjien on voitava tarkastella työntekijätietoja vain yrityksistä, joiden käyttöoikeudet heillä on, ja työnantajilta, jotka työskentelevät kyseisissä yrityksissä.

    Kun tämä ominaisuus valittu, soveltuvat käyttöoikeudet määritetään käyttäjille, joiden näkymää on rajoitettava, seuraavien ohjeiden mukaisesti:

    1. Valitse käyttäjä **Käyttäjät**-sivulta.
    1. Valitse käyttäjälle rooli. **Määritä organisaatiot** -vaihtoehto tulee näkyviin.
    1. Valitse **Määritä organisaatiot**.
    1. Valitse uudelta sivulta **Myönnä pääsy tiettyihin organisaatioihin yksittäin** ja valitse sitten organisaatiot, joihin käyttäjällä tulisi olla pääsy.
    1. Toista vaiheet 2–4 käyttäjän kaikille muille rooleille, mukaan lukien järjestelmäkäyttäjän roolin.

    > [!NOTE]
    > Yritysten, joihin käyttäjällä on pääsy, on oltava samoja käyttäjän kaikissa rooleissa.

- **Ota yritystenvälinen kompensaationäkymä käyttöön** – Työntekijöiden kompensaatio kohdistetaan yrityskohtaisesti. Joskus työntekijä voi olla töissä useissa yrityksissä samanaikaisesti. Kun tämä ominaisuus valitaan, kunkin yrityksen kompensaatio näytetään **Työntekijän itsepalvelu**- ja **Esimiehen itsepalvelu** -työtiloissa ilman, että yrityksiä olisi vaihdettava. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
