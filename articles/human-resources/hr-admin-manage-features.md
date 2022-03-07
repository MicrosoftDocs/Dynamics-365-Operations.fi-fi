---
title: Ominaisuuksien hallinta Human Resourcesissa
description: Tässä ohjeaiheessa käsitellään ominaisuuksien hallintatoimintoa ja sen käyttöä.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61e40f7177a1c8cf3d60a9a991ecbb0ed4d93aa1
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414630"
---
# <a name="manage-features-in-human-resources"></a>Ominaisuuksien hallinta Human Resourcesissa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Julkaisemme jatkuvasti uusia ominaisuuksia Microsoft Dynamics 365 Human Resourcesissa ja haluamme tarjota ne asiakkaillemme mahdollisimman pian. Tarjoamme esikatseluominaisuuksia, jotka ovat lähes valmiita yleiseen käyttöön ja ne ovat läpäisseet laajan testauksen. Haluamme saada vielä viimeisen asiakaspalautekierroksen, ennen kuin hyväksymme ominaisuudet yleisesti saataville.

Katso lisätietoja uusista ominaisuuksista Human Resourcesissa kohdista [Uutta Human Resourcesissa](hr-admin-whats-new.md) ja [Dynamics 365:n ja Power Platformin julkaisusuunnitelma](/dynamics365/release-plans/?panel=products1#pivot=products).

**Toimintojen hallinta** -työtilassa on luettelo kussakin julkaisussa toimitetuista toiminnoista. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota. Lisätietoja Toimintojen hallinnasta on kohdassa [Toimintojen hallinnan yleiskuvaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne **Toimintojen hallinta** -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.

Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. **Toimintojen hallinta** -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

## <a name="enable-or-disable-preview-features"></a>Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä

Jos haluat käyttää esikatselutoimintoja, sinun on ensin otettava ne käyttöön omassa ympäristössäsi. Esiversio-ominaisuuksien käyttöönotto on ympäristökohtainen.

> [!IMPORTANT]
> Esiversiotoiminnot ovat käytettävissä vain **eritys** ympäristöissä. Kun otat esikatseluominaisuuden käyttöön, sallit esikastseluominaisuudet organisaation kaikille käyttäjille kyseisessä ympäristössä. Kun poistat esikatseluominaisuuden käytöstä, esikatseluominaisuudet eivät ole käyttäjien käytettävissä. Esiversio-ominaisuuksilla on Human Resourcesissa rajoitettu tuki. Niissä voi olla tavallista vähemmän tietosuoja- ja suojausominaisuuksia, eivätkä ne sisälly Human Resourcesin palvelutasosopimukseen (SLA). Älä käytä esiversio-ominaisuuksia henkilötietojen (eli henkilökohtaisesti tunnistettavien tietojen) käsittelyyn tai muiden sellaisten tietojen käsittelyyn, jotka edellyttävät lain- tai säädöstenmukaista suojelua.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Ominaisuuksien hallinta** -ruutu.

3. Ota esikatseluomionaisuus käyttöön valitsemalla se luettelosta ja valitsemalla sitten **Ota käyttöön**. Poista esikatseluomionaisuus käytöstä valitsemalla se luettelosta ja valitsemalla sitten **Poista käytöstä**.

## <a name="enable-or-disable-benefits-management"></a>Etujenhallinnan käyttöönotto tai käytöstä poistaminen

Jos haluat ottaa etujenhallinnan käyttöön, käytä samoja toimintaohjeita kuin kohdassa [Esikatseluominaisuuksien käyttöönottaminen tai käytöstä poistaminen](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Etujenhallintaa ei voi poistaa käytöstä **Tuotanto**-ympäristössä sen jälkeen, kun se on käytössä. Voit kuitenkin poistaa etujenhallinnan käytöstä **Eristys**-ympäristössä.

Lisätietoja etujen hallinnan määrityksestä ja käytöstä on kohdassa [Etujen hallinnan yhteenveto](hr-benefits-management-overview.md).

Etujen hallinta **Edut** -työtilan toimintoja. Kun otat etujen hallinnan esikatseluominaisuuden käyttöön, et voi enää käyttää seuraavia **Edut**-työtilan lomakkeita:

- **Edut**
- **Edun elementit**
- **Osuuden laskentahinnat**
- **Edun rekisteröinnin tulokset**
- **Edun päättämisen ja laajennuksen tulokset**
- **Etukelpoisuuden käytäntösääntötyypit**
- **Etuuskelpoisuuden käytännöt**
- **Kelpoisuustapahtumat**

Voit tarkastella näiden sivujen tietoja vain luku -tilassa. Jos haluat muokata tietoja, sinun on ensin poistettava käytöstä etujenhallinta (sovellettavissa vain **Eristys**-ympäristöissä).

## <a name="enable-or-disable-leave-and-absence"></a>Loman ja poissaolon ottaminen käyttöön tai poistaminen käytöstä

Jos haluat ottaa loman ja poissaolon käyttöön, käytä samoja toimintaohjeita kuin kohdassa [Esikatseluominaisuuksien käyttöönottaminen tai käytöstä poistaminen](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Et voi poistaa **Useita lomatyyppejä** -toimintoa käytöstä, kun olet ottanut loma ja poissaolo -toiminnon käyttöön. Tämä koskee sekä **Eristys-** että **Tuotanto**-ympäristöjä.

Lisätietoja Lomien ja poissaolojen esikatseluominaisuuksista on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Lähetä meille palautetta

Haluamme kuulla kokemuksistasi esikatseluominaisuuksien parissa. Kannustamme sinua antamaan säännöllisesti palautetta, kun käytät näitä sivustoja tai muita ominaisuuksia:

- [Yhteisö](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Tämä sivusto on erinomainen resurssi, jossa käyttäjät voivat keskustella tapauksista, esittää kysymyksiä ja saada ohjeita yhteisöltä.
- Ilmoita meille, mitä ominaisuuksia haluaisit tuotteeseen ja kerro, mitä muutoksia nykyisiin ominaisuuksiin pitäisi mielestäsi tehdä. Ehdota tuoteideoita kohdassa [Human Resources -ideat](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Älä sisällytä mitään henkilötietoja (eli henkilökohtaisesti tunnistettavia tietoja) palautteeseesi tai tuotearvioihisi. Kerättyjä tietoja voidaan analysoida tarkemmin, eikä niitä käytetä pyyntöihin vastaamiseen tietosuojalakien mukaisesti. Henkilökohtaisiin tietoihin, jotka kerätään erillään näistä ohjelmista, sovelletaan [Microsoftin tietosuojalausuntoa](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Lisätietoja

- [Uutta henkilöstöhallinnossa](hr-admin-whats-new.md)
- [Dynamics 365:n ja Power Platformin julkaisusuunnitelma](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
