---
title: Kattavuusasetukset
description: Tässä ohjeaiheessa on tietoja kattavuusasetuksista, joita pääajoitus käyttää nimiketarpeiden laskennassa.
author: ChristianRytt
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d0fec443ee4c531d2bc7edc6623d309e863348b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569790"
---
# <a name="coverage-settings"></a>Kattavuusasetukset

[!include [banner](../includes/banner.md)]

Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.

Voit määrittää kattavuusasetukset useilla eri tavoilla:

- Määritä kattavuusryhmän kattavuusasetukset.

    Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset. Luodaksesi kattavuusryhmän, valitse **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**. Voit linkittää kattavuusryhmän tuotteeseen. Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää. Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehden **Kattavuusryhmä**-kenttää. Oletusarvoisesti, jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä yleistä kattavuusryhmää.

- Määritä tuotteen kattavuusasetukset.

    Voit luoda tietyn tuotteen kattavuusasetukset. Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Valitse tuote ja napsauta toimintoruudussa **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu. Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla. **Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.

- Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla.

    Ohjattu toiminto opastaa vaiheittain ensisijaisen nimikkeen kattavuusparametrien määrittämisessä. Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla toimintoruudusta **Ohjattu toiminto**.

- Määritä dimensioryhmän kattavuusasetukset.

    Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-pikavälilehden **Hallinta**-osassa **Varastodimensioryhmä**-linkkiä. Valitse **Varastodimensioryhmät** -sivulta **Kattavuussuunnitelma dimension mukaan** -valintaruutu, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset. **Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.


## <a name="coverage-codes"></a>Kattavuuskoodit

Pääsuunnittelu voidaan määrittää käyttämään erilaisia täydennysmenetelmiä. Täydennysmenetelmät tai eräkoon muuttamismenetelmät ovat tekniikoita, joiden avulla järjestelmä voi määrittää ostettujen tai tuotettujen nimikkeiden eräkoon. 

Kullekin täydennysmenetelmälle määritetään jokin seuraavista kattavuuskoodeista:

- **Manuaalinen** – Eräkoon muuttamismenetelmä, jossa järjestelmä ei ehdota nimikkeelle osto-, siirto- tai tuotantotilauksia. Nimikkeen suunnittelija vastaa nimikkeen täydentämiseen tarvittavien tilausten luomisesta.
- **Tarpeen mukaan** – Eräkoon muuttamismenetelmä, jossa järjestelmä nimikkeelle tarpeen mukaan suunnitellun osto-, siirto- tai tuotantotilauksen. Tätä menetelmää käytetään yleensä kalliille nimikkeille, joilla on ajoittaista kysyntää.  
- **Kausikohtainen** – Eräkoon muuttamismenetelmä, joka yhdistää kausikohtaisen kysynnän nimikkeen yhteen tilaukseen. Tilaus suunnitellaan kauden ensimmäiselle päivälle, ja sen määrä täyttää määritetyn kauden nettotarpeet. Kausi alkaa nimikkeen ensimmäisestä kysynnästä ja kattaa määritetyn ajanjakson. Seuraava kausi alkaa nimikkeen seuraavista tarpeista.
- **Min./Maks.** – Eräkoon muuttamismenetelmä, joka sisältää varaston täydennyksen tietylle tasolle, kun ennustettu käytettävissä oleva määrä alittaa raja-arvon. Täydennysmäärä on enimmäistason ja ennustetun käytettävissä olevan tason välinen erotus.


## <a name="additional-resources"></a>Lisäresurssit

[Pääsuunnitelmien yleiskatsaus](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]