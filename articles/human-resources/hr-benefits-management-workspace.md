---
title: Etujen hallinnan työtila
description: Tässä aiheessa kuvataan Dynamics 365 Human Resources -sovellukseen sisältyvä etujen hallinnan työtila.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6cc1432e108c74706dea124a62024272e65b6c1
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512471"
---
# <a name="benefits-management-workspace"></a>Etujen hallinnan työtila

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resources -sovellukseen sisältyvä **etujen hallinnan työtila**.

> [!NOTE]
> Jos haluat nähdä **etujen hallinnan työtilan**, sinun täytyy ottaa **(Esikatselu) Etujen hallinnan työtila** -ominaisuus käyttöön ominaisuuksien hallinnasta. Lisätietoja esiversiotoimintojen käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).<br><br>![Etujen hallinnan työtilan käyttöönotto.](./media/hr-benefits-management-workspace-enable.png)

**Etujen hallinnan työtilan** avulla voit katsastaa nopeasti etujen nimikkeet, jotka vaativat huomiotasi. Tällä sivulla näytetään seuraavat tiedot:

- Toimintoa odottavien nimikkeiden kokonaismäärät
- Työntekijät, joilla on vahvistamattomia valintoja
- Työntekijät, jotka rekisteröityvät etuihin äskettäin
- Työntekijät, joilla on tulevia elinkaaritapahtumia
- Uudet työntekijät, jotka eivät ole rekisteröityneet
- Työntekijät, joilla on aktiivisia elinkaaritapahtumia
- Työntekijät, joilla on avoimia rekisteröitymisiä, jotka eivät ole valinneet yhtään suunnitelmaa

![Etujen hallinnan työtila.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Toimintonimikkeiden tarkasteleminen

Voit tarkastella toimintonimikkeitä valitsemalla ruudun tai välilehden. Jos valitset välilehden, voit tarkastella ja valita työntekijöitä suoraan työtilan sivulta.

![Toimintonimikkeet.](./media/hr-benefits-management-workspace-action-items.png)

Jos valitset ruudun, siirryt kyseiselle sivulle. Esimerkiksi seuraavien ruutujen valitseminen näyttää **Työntekijän etuussuunnitelmat** -sivun, joka on suodatettu näyttämään toimenpiteitä vaativat työntekijät:

- **Vahvistamattomat valinnat**
- **Avoimet rekisteröinnit, joilla ei ole uloskuitattuja suunnitelmia**
- **Rekisteröity etuihin**
- **Uutta työntekijää ei ole rekisteröity**

![Työntekijän etusuunnitelmat.](./media/hr-benefits-management-workspace-plans.png)

**Aktiiviset elinkaaritapahtumat**- tai **Tulevat elinkaaritapahtumat** -valinta siirtää aktiivisten tai tulevien elinkaaritapahtumien luetteloon.

![Elinkaaritapahtumat.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Käsitellään

Jos haluat käsitellä rekisteröintikelpoisuutta, elinkaaritapahtumia tai hintamuutosten päivityksiä, valitse asiaankuuluva nimike siirtymispalkista.

![Käsittely.](./media/hr-benefits-management-workspace-processing.png)

Voit tarkastaa prosessin tulokset valitsemalla **Prosessin tulokset** -sivun.

![Prosessin tulokset.](./media/hr-benefits-management-workspace-process-results.png)

Lisätietoja etujen käsittelystä on kohdissa:

- [Rekisteröitymiskelpoisuuksien käsittely](hr-benefits-process-enrollment-eligibility.md)
- [Elämäntapahtumien muutosten käsittely](hr-benefits-process-life-event-changes.md)
- [Elämäntapahtumien oikeutusten käsittely](hr-benefits-process-life-event-eligibility.md)
- [Elämäntapahtumien käsittely](hr-benefits-process-life-events.md)
- [Hintamuutosten käsittely](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Ajanjakson muuttaminen

Jos haluat tarkastella etuja toiselta ajanjaksolta, valitse se avattavassa **Kausi**-luettelossa.

![Ajanjakson muuttaminen.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Avaa rekisteröinti -välilehti

Voit tarkastella toimintonimikkeitä valitsemalla joko ruudun tai välilehden. Jos valitset välilehden, voit tarkastella ja valita työntekijöitä suoraan työtilan sivulta.
**Avaa rekisteröinti** -välilehdellä on avoimen rekisteröintiprosessin tunnuslukuja, 

Avointa rekisteröintiä koskevat tiedot ovat näkyvissä 30 päivää ennen **rekisteröitymisen alkamispäivämäärää**. Se määritetään **Kaudet**-määrityksissä valitsemalla ensin **Etujen hallinta** > **Linkit** > **Kaudet** ja sitten **Rekisteröitymisen alkamispäivämäärä** -kenttä.  Tämä asetus voidaan muuttaa valitsemalla **Human Resourcesin jaetut parametrit** > **Etujen hallinta** > **Avaa rekisteröitymisvaihtoehdot** ja päivittämällä **Määrä**-kenttä.  

**Avaa rekisteröinti** -välilehdessä on seuraavat tiedot:
 - Työntekijät, jotka eivät ole aloittaneet avointa rekisteröintiprosessia
 - Työntekijät, joiden valintoja käsitellään
 - Työntekijät, joiden valintaprosessi on valmis
 - Vahvistamattomat valinnat

**Yhteenvetoruudut**

- **Ei aloitettu** – **Ei aloitettu** -ruudussa on niiden työntekijöiden määrä, jotka eivät ole aloittaneet rekisteröintiprosessia. **Ei aloitettu** -ruutu on suodatettu luettelo niistä työntekijöistä, jotka eivät ole valinneet, peruuttaneet tai kuitanneet ulos mitään suunnitelmaa avoimen rekisteröintisuunnitelmakautena. Pakolliset suunnitelmat ohitetaan, eivätkä ne sisälly luetteloon, koska ne valitaan oletusarvoisesti työntekijälle.  Tähän ruutuun voi porautua takaisin **Työntekijän etuussuunnitelma** -sivulla. Näkyviin tulee silloin luettelo, jotka eivät ole aloittaneet avointa rekisteröintiprosessia.

  > [!NOTE]
  > Jos avoimen rekisteröinnin edistymistä ei haluta seurata **suunnitelman tyypin** osalta, se voidaan jättää pois valitsemalla **Etujen hallinta** > **Linkit** > **Työntekijän itsepalveluparametrit** > **Etuussuunnitelmien ruudun asetukset** ja päivittämällä **Seuraa avoimen rekisteröitymisen edistymistä** -kenttä.  Joissakin luoduissa suunnitelmissa on esimerkiksi mahdollista, että **Suunnitelman tyyppi** = **Muu**. Nämä suunnitelmat saattavat olla valinnaisia suunnitelma, joiden rekisteröitymisen etenemistä ei haluta seurata. Jos tätä suunnitelman tyyppiä ei valita, näiden tyyppien suunnitelmat ohitetaan seurattaessa edistymistä tai valmistumista **Avaa rekisteröinti** -välilehdessä. Tämä asetus koskee sitä suunnitelman tyyppiä, joka on valittu kaikille kausille ja kaikkiin yrityksiin.

- **Käsittelyssä** – **Käsittelyssä**-ruudussa on niiden työntekijöiden määrä, joiden valintoja käsitellään. **Käsittelyssä**-ruutu on suodatettu luettelo työntekijöistä, joilla on ainakin yksi peruutettu tai valittu suunnitelma. Pakolliset suunnitelmat ohitetaan, eivätkä ne sisälly luetteloon, koska ne valitaan oletusarvoisesti työntekijälle. Tähän ruutuun voi porautua takaisin **Työntekijän etuussuunnitelman joukkopäivitys** -sivulla, jolloin valittujen ja peruutettujen suunnitelmien tarkastelu on mahdollista.

- **Rekisteröity etuihin** – **Rekisteröity etuihin** -ruudussa on niiden työntekijöiden määrä, jotka ovat rekisteröityneet etuihin kokonaisuudessaan. **Rekisteröity etuihin** -ruutu on suodatettu luettelo työntekijöistä, jotka ovat joko valinneet tai peruuttaneet kaikki suunnitelmat. Kysely jättää ulkopuolelle ne suunnitelmat, joiden avointa rekisteröintiä ei seurata **Työntekijän itsepalveluparametrit** -sivulla. Tähän ruutuun voi porautua takaisin **Työntekijän etusuunnitelmat** -sivulla, jolloin näkyvissä on työntekijäluettelo.

- **Vahvistamattomat valinnat** – **Vahvistamattomat valinnat** -ruudussa on niiden työntekijöiden määrä, joilla on valitut tai peruutetut suunnitelmat on vahvistettava. Tähän ruutuun voi porautua takaisin, jolloin näkyvissä on **Työntekijän etusuunnitelmien joukkopäivitys** -sivu.

**Tehtävä**

- **Ei aloitettu** – **Ei aloitettu** -väliruudussa on luettelo niistä työntekijöistä, jotka eivät ole aloittaneet rekisteröintiprosessia. **Ei aloitettu** -ruutu on suodatettu luettelo niistä työntekijöistä, jotka eivät ole valinneet, peruuttaneet tai kuitanneet ulos mitään suunnitelmaa avoimen rekisteröintisuunnitelmakautena. Pakolliset suunnitelmat ohitetaan, eivätkä ne sisälly luetteloon, koska ne valitaan oletusarvoisesti työntekijälle. **Työntekijän etusuunnitelman tiedot** -sivu voidaan näyttää työntekijään porautumalla.

- **Valintoja käsittelyssä** – **Valintoja käsittelyssä** -välilehdessä on luettelo työntekijöistä, joiden valintoja käsitellään. **Valintoja käsittelyssä**-ruutu on suodatettu luettelo työntekijöistä, joilla on ainakin yksi peruutettu tai valittu suunnitelma. Pakolliset suunnitelmat ohitetaan, eivätkä ne sisälly luetteloon, koska ne valitaan oletusarvoisesti työntekijälle. **Työntekijän etusuunnitelman tiedot** -sivu voidaan näyttää työntekijään porautumalla.

## <a name="view-more-options"></a>Lisävaihtoehtojen tarkasteleminen

Saat lisätietoja tai lisää toimintoja valitsemalla **Linkit**.

![Linkit.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Lisätietoja

[Etujen hallinnan yleiskatsaus](hr-benefits-management-overview.md)
