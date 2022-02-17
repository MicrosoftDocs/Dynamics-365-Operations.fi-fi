---
title: Henkilöstötoiminnot – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, jos organisaatiosi käyttää henkilöstötoimintoja.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c952bdc95b49c92fea34aef63b57c7e193b2f09a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065148"
---
# <a name="personnel-actions-faq"></a>Henkilöstötoiminnot – usein kysytyt kysymykset


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa on vastauksia kysymyksiin, joita sinulla saattaa olla, jos organisaatiosi käyttää henkilöstötoimintoja. Henkilökunnan toiminnot ovat lisävaiheita, jotka on suoritettava, kun suoritat tiettyjä henkilökuntaan liittyviä tehtäviä. 

Esimerkkejä tehtävistä, jotka voivat edellyttää henkilökunnan toimintoja:
 - Uusien toimien luonti. 
 - Aiemmin luotujen toimiarvojen muokkaaminen. 
 - Uusien työntekijöiden palkkaaminen. 
 - Työntekijöiden siirtäminen. 
 - Työntekijän kompensaation muuttaminen 
 - Toimimääritysten muuttaminen. 
 - Työntekijöiden irtisanominen.

> [!NOTE]
> Henkilöstötoiminnot ovat käytettävissä vain, jos **Henkilöstöhallinnon jaetut parametrit** -sivun **Henkilöstötoiminnot**-välilehden **Ota käyttöön työntekijätoiminnot** ja **Ota käyttöön toimen toiminnot** -kenttien arvoksi on määritetty **Kyllä**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Miten selvittää, edellyttääkö organisaationi henkilökunnan toimintoja?
Henkilökunnan tehtävää tarvitaan organisaatiossasi, jos sinua pyydetään valitsemaan henkilöstötoimenpide, kun luodaan uusia toimia, muutetaan aiemmin luotuja toimia, palkataan uusia työntekijöitä, siirretään työntekijöitä, muutetaan työntekijän kompensaatiota, muutetaan työtehtävät, päätetään työntekijöiden työsuhteita tai työntekijöille annetaan lomaa. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Mikä ero on toimen toiminnolla ja työntekijätoiminnolla?
Henkilöstötoimintoja on kahta eri tyyppiä.

- **Toimi**- toiminto – Toimitoiminto suoritetaan nykyisissä tai uusissa toimissa. Esimerkiksi toimen toiminto voi olla pakollinen, jos vaihdat olemassa olevan toimen arvon tai jos luot uuden kausiluontoisen toimen. 

- **Työntekijä**-toiminto – Työntekijätoiminnon suoritetaan aiemmin luoduille työntekijöille tai uusille työntekijöille. Työntekijätoimintoa saatetaan vaatia esimerkiksi uuden työntekijän palkkauksessa tai nykyisen työntekijän ylennyksessä. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Mitä henkilöstötoimintojen tilat tarkoittavat?
Henkilöstötoimenpiteillä voi olla seuraavia tiloja:

- **Luonnos** – Jos työnkulkua käytetään, toimintoa ei ole lähetetty. Jos työnkulkua ei käytetä, toimintoa ei ole vielä suoritettu.
- **Tarkistuksessa** – Henkilöstötoiminto on lähetetty työnkulkuun, mutta työnkulku ei ole valmis.
- **Hyväksytty ja odottaa**– Työnkulku on valmis, mutta muutoksia toteutetaan vielä. **Peruutettu** – Työnkulku tai henkilöstötoimenpide peruutettiin. **Hylätty** – Hyväksyjä hylkäsi toimintopyynnön.
- **Käsittelytoiminto** – Toimintopyyntö on hyväksytty ja muutoksia toteutetaan parhaillaan.
- **Työnkulku valmis** – Työnkulku on valmis ja muutokset on käsitelty. **Epäonnistui** – Työnkulku epäonnistui, koska tiedot ovat vanhentuneet. Näytä uusimmat tiedot valitsemalla **Aktivoi uudelleen** ja jatka.
- **Valmis** – Toimen luonti tai muokkaus onnistui, työntekijän palkkaus, siirto tai irtisanominen onnistui tai työntekijän kompensaatio muuttui. **Virhe** – Tapahtui jostain muusta kuin vanhentuneista tiedoista aiheutunut ongelma. Selvitä virheen syy avaamalla **henkilöstötoimenpiteiden sanomaloki**.
- **Hylätty** – Hyväksyjä hylkäsi toimintopyynnön.

## <a name="can-i-delete-a-personnel-action"></a>Voinko poistaa henkilökohtaisen toimenpiteen?
Kyllä, voit poistaa henkilöstötoimenpiteet, joiden tilana on **Luonnos**, **Virhe**, **Ei hyväksytty** tai **Peruutettu**. Voit poistaa **Valmis**-tilassa olevia henkilöstötoimintoja vain, jos olet määrittänyt **Salli valmiiden työntekijätoimintojen poistaminen** -asetukseksi **Kyllä** **Henkilöstöhallinnon jaetut parametrit** -sivulla.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Mikä on nopein tapa tarkistaa henkilöstötoimintopyynnön tila?
Avaa mikä tahansa **Henkilöstötoiminto**-luettelosivu ja valitse henkilöstötoiminto.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Mitä minun pitäisi tehdä, jos henkilöstötoimintopyyntö epäonnistuu?
Jos henkilökunnan toimenpidepyyntö epäonnistuu, noudata seuraavia vaiheita ratkaistaksesi tämän ongelman ja lähetä pyyntö uudelleen:

> 1. Avaa ongelma käsittelevä sanoma napsauttamalla **toimintoruudussa** **Virheteksti**-painiketta.
> 
> 2. Lataa uusimmat tiedot valitsemalla **toimintoruudussa** **Aktivoi uudelleen** ja määritä henkilöstötoimenpiteen tilaksi jälleen **Luonnos**.
> 
> 3. Korjaa virhe ja valitse sitten **Valmis** tai **Lähetä**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Mitä tapahtuu työnkulkua käyttävälle henkilöstötoiminnolle, kun lopullinen hyväksyntä on valmis?
Jos virheitä ei ole, henkilökunnan toimenpide on vain lukukelpoinen. (Voit tarkastella historiatietoja **Kaikki työntekijätoiminnot** -luettelosivulla muttet voi muuttaa henkilöstötoimintoa). Kun henkilöstötoiminnon tila on **Valmis**, toimi- tai työntekijätietue on jo päivitetty. Voit tarkastella tehtyjä muutoksia avaamalla **Toimet**- tai **Työntekijät**-luettelosivun.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Miksi tulee seuraava virhe, kun syötän nollasta poikkeavan arvon palkkiokenttään? "Arvo ei ole sallitulla alueella. Sen on oltava 0,00–0,00."
Saat tämän ilmoituksen, koska **Työ**-lomakkeen **Taso** kenttä on tyhjä valittuun toimeen liitetyn työn kohdalla.

Korjaa tämä virhetilanne seuraavien ohjeiden avulla:

> 1. Valitse **Työntekijän toimen määritykset** -sivulla **Toimi**-kenttä.  
> 2. Avaa **Työ**-sivu napsauttamalla **Työ**-kentän arvoa.
> 3. Valitse toimintoruudussa **Muokkaa**.
> 4. Valitse **Kompensaatio**-välilehti.
> 5. Valitse **Taso**-kentässä taso.
> 6. Sulje **Työ**-sivu.
> 7. Sulje **Toimi**-sivu.
> 8. Palaa **Työntekijä**-sivun **Kompensaatio**-välilehteen ja valitse **Kiinteä kompensaatio**.  Valitse **Uusi** ja syötä työtekijän toimi **Toimi**-kenttään.  Anna arvo **Suunnitelma**-kentässä ja anna sitten työntekijän kompensaatio **Palkkio**-kenttä.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Miksi en voi muuttaa voimaantulopäivää työntekijätoimintosivun ylätunnisteessa?
Et voi muuttaa voimaantulopäivää, koska kenttään on täytetty toimintotyypin loogisin päivämäärä.

Esimerkiksi:

- **Irtisano työntekijä** -toiminnon otsikon voimassaolopäivä on **Työsuhteen loppumispäivämäärä** -kentässä annettu päivämäärä.
- **Palkkaa työntekijä** -toiminnon otsikon voimassaolopäivä on **Työsuhteen alkamispäivämäärä** -kentässä annettu päivämäärä.
- **Siirrä työntekijä** -toiminnon otsikon voimassaolopäivä on **Määrityksen alkamispäivä** -kentässä työntekijälle annettu päivämäärä.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
