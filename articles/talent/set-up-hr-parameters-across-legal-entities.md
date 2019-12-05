---
title: Yritysten välisten henkilöstöhallinnon (HR) parametrien määrittäminen
description: Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille. Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 9c205973097c82a4b131a3784392fa8d8cb5ecba
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812807"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>Yritysten välisten henkilöstöhallinnon (HR) parametrien määrittäminen

[!include [banner](includes/banner.md)]

Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille. Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.

Jotkin tietuetyypit, kuten Toimi-tietueet, jaetaan yritysten kesken. Näille tietueille on määritettävä jaetut parametrit. Voit esimerkiksi käyttää **Henkilöstöhallinnon jaetut parametrit** -sivua yritysten kesken jaettujen henkilöstöparametrien määrittämiseen. 

**Henkilöstöhallinnon jaetut parametrit** -sivulla parametrit ryhmitellään alueisiin niiden toimintojen perusteella. 

### <a name="previously-released-functionality"></a>Aiemmin julkaistu toiminto
**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita. On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille. Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla. Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstön hallinta** &gt; **Linkit-välilehti** &gt; **Asennus** &gt; **Tunnustyypit**. Voit syöttää yksinkertaisen koodin ja kuvauksen. 

### <a name="if-youre-using-dynamics-365-talent"></a>Jos käytät Dynamics 365 Talentia
**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita. On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille. Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla. Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstöhallinto** &gt; **Asetukset** &gt; **Tunnustyypit**. Voit syöttää yksinkertaisen koodin ja kuvauksen. 

**Numerojärjestykset**-välilehdellä voit valita numerosarjat, joita käytetään seuraaville tietueille: Henkilöstönumero, Toimi, Käyttäjäpyynnön tunnus, -9-asiakirja, Hakija, Keskustelu, Etutunnus ja Henkilöstötoiminto (jos tämä tietuetyyppi on otettu käyttöön). Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua. Käytä sivun hakutoimintoa löytääksesi tämän sivun. 

Ilmaise **Toimet**-välilehdellä, ovatko uudet toimet oletusarvoisesti käytettävissä toimeksiantoa varten:

-   **Aina** – Voit määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Kun toimet on luotu, **Käytettävissä toimeksiantoa varten** -päivämäärä ja -aika **Yleinen** -välilehden **Toimi**-sivulla asetetaan automaattisesti sen luontipäivämääräksi ja -ajaksi.
-   **Ei koskaan** – Et voi määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Jos valitset tämän vaihtoehdon, sinun on avattava **Toimi**-sivu kullekin uudelle toimelle sen tullessa saataville ja syötä tämän jälkeen **Yleinen**-välilehdellä **Käytettävissä toimeksiantoa varten** päivämäärä ottaaksesi käyttöön työntekijän määrityksen.


<a name="additional-resources"></a>Lisäresurssit
--------

[Yrityskohtaisten henkilöstöhallinnon (HR) parametrien määrittäminen](set-up-company-specific-hr-parameters.md)



