---
title: Kirjausmääritykset
description: Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä. Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e9d1e593f58e8fc9e12ddac7664b6e67ecda6a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "359770"
---
# <a name="posting-definitions"></a>Kirjausmääritykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä. Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.

Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot. Voit tarkastella tuettuja asiakirjoja ja kirjaustyyppejä **Tapahtuman kirjausmääritykset** -sivulla. 

Voit aloittaa kirjausmääritysten käyttämisen valitsemalla **Kirjanpitoparametrit**-sivun **Käytä kirjausmäärityksiä** -vaihtoehto. Alkuperäisten merkintöjen ja muiden kuin tuettujen kirjaustyyppien ja asiakirjojen kirjausprofiilit on määritettävä myös kirjausmääritysten käyttämisen yhteydessä. 

Kirjausmääritysten avulla otetaan käyttöön ostotilausten varauskirjanpito ja ostoehdotuksien alustavan varauksen kirjanpito.

## <a name="defining-posting-definitions"></a>Kirjausmääritysten määrittäminen
Määritä **Kirjausmääritykset**-sivulla vastaavuusehto ja merkinnät, jotka luodaan vastaavuuden löytymisen yhteydessä. Alkuperäisten merkintöjen vastaavuusehdot arvioidaan kirjanpidollisina jakoina. 

**Kirjausmääritykset**-sivulla voi myös liittää prioriteettinumerot merkintäriveihin rivien arviointijärjestyksen hallintaa varten. Alimman prioriteettinumeron omaavat rivit arvioidaan ensin. Ensin arvioidaan siis rivit, joiden prioriteetti on 1, sen jälkeen rivit, joiden prioriteetti on 2 jne. Kun vastaavuus löytyy, muut vastaavuusehdot ohitetaan. Lisäksi vain alkuperäistä tapahtumaa vastaavassa ryhmässä olevat ehdot luovat merkintöjä. 

Voit tarkistaa kirjausmääritykset ohjatun **kirjausmäärityksen testauksen** avulla. Kun kirjausmäärityksen alkuperäinen mallimerkintä on määritetty, luodut merkinnät tulevat näkyviin. 

Voit käyttää kirjausmäärityksen versioita yhdessä voimaantulopäivien kanssa. Voit esimerkiksi luoda kirjausmäärityksestä tulevan version, joka kirjataan uuden tilikauden eri kirjanpitotilille. 

Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla.

## <a name="linking-posting-definitions"></a>Kirjausmääritysten linkittäminen
Voit linkittää kirjausmäärityksen toiseen kirjausmääritysten luomisen yhteydessä. Linkitetyn määrityksen ehdot otetaan huomioon nykyisen kirjausmäärityksen ehtojen lisäksi. Tämä toiminto säästää aikaa, koska nykyisen kirjausmäärityksen **Kirjausmerkinnät**-sivun **Merkinnät**-pikavälilehden ehtoja ei tarvitse syöttää uudelleen, jos kyseiset rivit on jo syötetty toisessa määrityksessä. 

Lisää kaavioihin tai tauluihin linkit, joita saatat käyttää. Voit välttää ristiriidat nykyisen kirjausmäärityksen kanssa varmistamalla, että kaikkien linkittämiesi kirjausmääritysten rivit ovat yksilöiviä. 

Seuraavat rajoitukset ovat voimassa, kun luot kirjausmääritysten linkkejä:

-   Annettu kirjausmääritys voi olla linkki toiseen kirjausmääritykseen tai toinen kirjausmääritys on voitu linkittää siihen. Molempia ei voi tehdä. Kirjausmäärityksestä voi kuitenkin olla linkki useisiin kirjausmäärityksiin.
-   Voit määrittää linkkejä vain saman moduulin kirjausmäärityksiin.
-   Voit liittää kirjausmäärityksen mihin tahansa tapahtumatyyppiin, mutta tapahtumatyypin on kuuluttava samaan moduuliin kuin kirjausmääritys. **Tapahtuman kirjausmääritykset** -sivulla näet tapahtumatyypin moduulin.


Lisätietoja on kohdassa [Määritysesimerkkien kirjaaminen](example-posting-definitions.md). 


