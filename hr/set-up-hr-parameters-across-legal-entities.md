---
title: "Määritä henkilöstöhallinnon parametreja eri yrityksissä"
description: "Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille. Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: f83bc127f7bf3cdceb39a79c1e69f4f7e96f6462
ms.openlocfilehash: 1a23ec184538510527573de8dd334603dc973ae6
ms.contentlocale: fi-fi
ms.lasthandoff: 06/19/2017


---

# Määritä henkilöstöhallinnon parametreja eri yrityksissä
<a id="set-up-hr-parameters-across-legal-entities" class="xliff"></a>

[!include[banner](includes/banner.md)]


Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille. Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.

Jotkin tietuetyypit, kuten Toimi-tietueet, jaetaan yritysten kesken. Näille tietueille on määritettävä jaetut parametrit. Voit esimerkiksi käyttää **Henkilöstöhallinnon jaetut parametrit** -sivua yritysten kesken jaettujen henkilöstöparametrien määrittämiseen. 

**Henkilöstöhallinnon jaetut parametrit** -sivulla parametrit ryhmitellään alueisiin niiden toimintojen perusteella. 

### Aiemmin julkaistu toiminto
<a id="previously-released-functionality" class="xliff"></a>
**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita. On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille. Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla. Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstön hallinta** &gt; **Linkit-välilehti** &gt; **Asennus** &gt; **Tunnustyypit**. Voit syöttää yksinkertaisen koodin ja kuvauksen. 

### Jos käytät Dynamics 365 for Talentia
<a id="if-youre-using-dynamics-365-for-talent" class="xliff"></a>
**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita. On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille. Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla. Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstöhallinto** &gt; **Asetukset** &gt; **Tunnustyypit**. Voit syöttää yksinkertaisen koodin ja kuvauksen. 

**Numerojärjestykset**-välilehdellä voit valita numerosarjat, joita käytetään seuraaville tietueille: Henkilöstönumero, Toimi, Käyttäjäpyynnön tunnus, -9-asiakirja, Hakija, Keskustelu, Etutunnus ja Henkilöstötoiminto (jos tämä tietuetyyppi on otettu käyttöön). Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua. Käytä sivun hakutoimintoa löytääksesi tämän sivun. 

Ilmaise **Toimet**-välilehdellä, ovatko uudet toimet oletusarvoisesti käytettävissä toimeksiantoa varten:

-   **Aina** – Voit määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Kun toimet on luotu, **Käytettävissä toimeksiantoa varten** -päivämäärä ja -aika **Yleinen** -välilehden **Toimi**-sivulla asetetaan automaattisesti sen luontipäivämääräksi ja -ajaksi.
-   **Ei koskaan** – Et voi määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä. Jos valitset tämän vaihtoehdon, sinun on avattava **Toimi**-sivu kullekin uudelle toimelle sen tullessa saataville ja syötä tämän jälkeen **Yleinen**-välilehdellä **Käytettävissä toimeksiantoa varten** päivämäärä ottaaksesi käyttöön työntekijän määrityksen.


Lisätietoja
<a id="see-also" class="xliff"></a>
--------

[Määritä yrityskohtaisia henkilöstöhallinnon parametreja](set-up-company-specific-hr-parameters.md)




