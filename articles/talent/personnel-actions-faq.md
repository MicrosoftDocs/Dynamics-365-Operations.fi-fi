---
title: "Henkilöstötoimenpiteet [usein kysytyt kysymykset]"
description: "Tässä ohjeaiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, jos organisaatiosi käyttää henkilöstötoimintoja. Henkilökunnan toiminnot ovat lisävaiheita, jotka on suoritettava, kun suoritat tiettyjä henkilökuntaan liittyviä tehtäviä."
author: ShielaSogge
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 93004f45189d16e991a3962ef16b4a102caf07bd
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="personnel-actions-faq"></a>Henkilöstötoimenpiteet [usein kysytyt kysymykset]

[!include[banner](includes/banner.md)]

Tässä ohjeaiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, jos organisaatiosi käyttää henkilöstötoimintoja. Henkilökunnan toiminnot ovat lisävaiheita, jotka on suoritettava, kun suoritat tiettyjä henkilökuntaan liittyviä tehtäviä. Esimerkkejä henkilöstötoimintoja mahdollisesti vaativista tehtävistä ovat uusien toimien luonti, olemassa olevien toimien arvojen muuttaminen, uusien työntekijöiden palkkaus, työntekijöiden siirto, työntekijän kompensaation muuttaminen, toimen määritysten muuttaminen tai työntekijöiden työsuhteiden päättäminen.

**Huomautus:** Henkilöstötoiminnot ovat käytettävissä vain, jos **Henkilöstöhallinnon jaetut parametrit** -sivun **Henkilöstötoiminnot**-välilehden **Ota käyttöön työntekijätoiminnot** ja **Ota käyttöön toimen toiminnot** -kenttien arvoksi on asetettu **Kyllä**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Miten selvittää, edellyttääkö organisaationi henkilökunnan toimintoja?
Henkilökunnan tehtävää tarvitaan organisaatiossasi, jos sinua pyydetään valitsemaan henkilöstötoimenpide, kun luodaan uusia toimia, muutetaan aiemmin luotuja toimia, palkataan uusia työntekijöitä, siirretään työntekijöitä, muutetaan työntekijän kompensaatiota, muutetaan työtehtävät, päätetään työntekijöiden työsuhteita tai työntekijöille annetaan lomaa. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Mikä ero on toimen toiminnolla ja työntekijätoiminnolla?
Henkilöstötoimintoja on kahta eri tyyppiä.

- Toimen toiminto – Toimen toiminto suoritetaan nykyisissä tai uusissa toimissa. Esimerkiksi toimen toiminto voi olla pakollinen, jos vaihdat olemassa olevan toimen arvon tai jos luot uuden kausiluontoisen toimen. Lisätietoja toimen toimintojen käyttämisestä on ohjeaiheessa Avaintehtävät: aiemmin luodut työtekijätoimet tai Avaintehtävät: uudet työntekijätoimet.

- Työntekijätoiminto – Työntekijätoiminnon suoritetaan aiemmin luoduille työntekijöille tai uusille työntekijöille. Työntekijätoimintoa saatetaan vaatia esimerkiksi uuden työntekijän palkkauksessa tai nykyisen työntekijän ylennyksessä. Lisätietoja työntekijätoimintojen käyttämisestä on ohjeaiheessa Henkilöstötoimenpiteiden määrittäminen työntekijöille.

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Mitä henkilöstötoimintojen tilat tarkoittavat?
Henkilöstötoimenpiteillä voi olla seuraavia tiloja:

- **Luonnos** – Jos työnkulkua käytetään, toimintoa ei ole lähetetty. Jos työnkulkua ei käytetä, ei toimenpidettä ole vielä suoritettu.
- **Tarkistuksessa** – Henkilöstötoiminto on lähetetty työnkulkuun, mutta työnkulku ei ole valmis.
- **Hyväksytty ja odottaa**– Työnkulku on valmis, mutta muutoksia toteutetaan vielä. Peruutettu – Työnkulku tai henkilöstötoimenpide peruutettiin. Hylätty – Hyväksyjä hylkäsi toimintopyynnön.
- **Käsittelytoiminto** – Toimintopyyntö on hyväksytty ja muutoksia toteutetaan parhaillaan.
- **Työnkulku valmis** – Työnkulku on valmis ja muutokset on käsitelty. Ei hyväksytty – Työnkulku epäonnistui, koska tiedot ovat vanhentuneet. Näytä uusimmat tiedot valitsemalla Aktivoi uudelleen ja jatka
- **Valmis** – Toimen luonti tai muokkaus onnistui, työntekijän palkkaus, siirto tai irtisanominen onnistui tai työntekijän kompensaatio muuttui. Virhe – Ilmeni jostain muusta kuin vanhentuneista tiedoista aiheutunut ongelma. Selvitä virheen syy avaamalla henkilöstötoimenpiteiden sanomaloki.
- **Hylätty** – Hyväksyjä hylkäsi toimintopyynnön.

## <a name="can-i-delete-a-personnel-action"></a>Voinko poistaa henkilökohtaisen toimenpiteen?
Kyllä, voit poistaa henkilöstötoimenpiteet, joiden tilana on **Luonnos**, **Virhe**, **Ei hyväksytty** tai **Peruutettu**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Mikä on nopein tapa tarkistaa henkilöstötoimintopyynnön tila?
Avaa mikä tahansa henkilöstötoimintojen luettelosivuista ja valitse henkilöstötoiminto.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Mitä minun pitäisi tehdä, jos henkilöstötoimintopyyntö epäonnistuu?
Jos henkilökunnan toimenpidepyyntö epäonnistuu, noudata seuraavia vaiheita ratkaistaksesi tämän ongelman ja lähetä pyyntö uudelleen:

> 1. Avaa ongelma käsittelevä sanoma napsauttamalla **toimintoruudussa** **Virheteksti**-painiketta.

> 2. Lataa uusimmat tiedot valitsemalla **toimintoruudussa** **Aktivoi uudelleen** ja määritä henkilöstötoimenpiteen tilaksi jälleen **Luonnos**.

> 3. Korjaa virhe ja valitse sitten **Valmis** tai **Lähetä**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Mitä tapahtuu työnkulkua käyttävälle henkilöstötoiminnolle, kun lopullinen hyväksyntä on valmis?
Jos virheitä ei ole, henkilökunnan toimenpide on vain lukukelpoinen. (Voit tarkastella historiatietoja **Kaikki työntekijätoiminnot** -luettelosivulla, mutta et voi muuttaa henkilöstötoimenpidettä.) Kun henkilöstötoimenpiteen tila on **Valmis**, toimi tai työntekijä on jo päivitetty. Voit tarkastella tehtyjä muutoksia avaamalla **Toimet**- tai **Työntekijät**-luettelosivun.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Miksi tulee seuraava virhe, kun syötän nollasta poikkeavan arvon palkkiokenttään? Arvo ei ole sallitulla alueella. Sen on oltava 0,00–0,00.
Saat tämän ilmoituksen, koska työlomakkeen tasokenttä on tyhjä valittuun toimeen liitetyn työn kohdalla.

Korjaa tämä virhetilanne seuraavien ohjeiden avulla:

> 1. Valitse työntekijän toimen määrityslomakkeessa Toimi-kenttä.  
> 2. Avaa Työ-sivu napsauttamalla Työ-kentän arvoa.
> 3. Valitse toimintoruudussa Muokkaa.
> 4. Valitse Kompensaatio-välilehti.
> 5. Valitse Taso-kentässä taso.
> 6. Sulje Työ-sivu.
> 7. Sulje Toimi-sivu.
> 8. Palaa Työntekijä-sivun Kompensaatio-välilehteen ja valitse Kiinteä kompensaatio.  Valitse uusi ja anna työtekijän toimi Toimi-kenttään.  Anna ensin arvo Suunnitelma-kentässä ja sitten työntekijän kompensaatio Palkkio-kenttä.

## <a name="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form"></a>Miksi en voi muuttaa voimaantulopäivää työntekijätietolomakkeen otsikossa?
Et voi muuttaa voimaantulopäivää, koska kenttään on täytetty toimenpidetyypin kaikkein loogisin päivämäärä.

Esimerkiksi:

- **Irtisano työntekijä** -toiminnon otsikon voimassaolopäivä on **Työsuhteen loppumispäivämäärä** -kentässä annettu päivämäärä.
- **Palkkaa työntekijä** -toiminnon otsikon voimassaolopäivä on **Työsuhteen alkamispäivämäärä** -kentässä annettu päivämäärä.
- **Siirrä työntekijä** -toiminnon otsikon voimassaolopäivä on **Määrityksen alkamispäivä** -kentässä työntekijälle annettu päivämäärä.


