---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (6. toukokuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a4571abdb0e104af0a0657c75bf5a6b5764345a
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023858"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (6. toukokuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="select-optional-documents-upon-offer-creation"></a>Valinnaisten tiedostojen valitseminen tarjouksen luonnin yhteydessä

Kun valitset tarjouspakettimallin, Attract pyytää sinua nyt valitsemaan sovellettavat, valinnaiset asiakirjat kyseisen paketin mallista. Voit lisätä muita valinnaisia asiakirjoja tarjousta valmisteltaessa.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2282. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="platform-update-26-for-finance-and-operations"></a>Finance and Operationsin käyttöympäristöpäivitys 26

Lisätietoja Finance and Operationsin käyttöympäristöpäivitys 26:stä on artikkelissa [Dynamics 365 Finance and Operations -käyttöympäristöpäivitys 26:n esikatselutoiminnot (toukokuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Tämän viikon versiossa seuraavat entiteetit tukevat nyt mukautettuja kenttiä: etuus Calc Frequency, etuus-Calc Rate, etutyyppi, työkalenteri, lomatyökalenteri, maksusykli ja työntekijän tunnustyypit.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Massarekisteröinnin jättäminen, määrittämistason muuttaminen aiemmaksi päivämääräksi ei päivitä alkuperäistä jaksotusprosenttia (318526)

Kun joukkorekisteröit työntekijöitä ja muutat tasoperustetta, alkuperäinen jaksotus vastaa valittua tasoperustetta.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Työnkulku, jossa on päällekkäisiä paikanhaltijoita (313636)

Tämän version muutokset poistavat paikkamerkkien kaksoiskappaleet, kun työnkulkuilmoitukset lähetetään.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensiokenttiä ei päivitetä käytettäessä "Avaa Excelissä" (176261) -toimintoa

Tämän version avulla voit nyt päivittää taloushallinnon dimension käyttämällä **Avaa Excelissä** -toimintoa **Työntekijä**-sivulla. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Common Data Servicessä järjestelmään luotua työntekijän osoitetta ei synkronoida Talentiin (317555)

Tämän muutoksen avulla Common Data Servicessä luodut osoitteet päivitetään Talent: Core HR:ssä.


## <a name="in-preview"></a>Esiversiossa

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uusi sivu sijaintihierarkian tietojen tarkistamista varten

Henkilöstöhallinto (HR) ja järjestelmänvalvojat voivat nyt vahvistaa johtamishierarkian mahdollisesti vahingossa tuotuja kehäviittauksia varten. Voit käyttää tätä uutta sivua kohdasta **Organisaation hallinta > Linkit > Tehtävät > Tehtävähierarkian oikeellisuustarkistus**.

### <a name="specify-reason-codes-on-leave-types"></a>Määritä lomatyyppien syykoodit

Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä. Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi. Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa varmistamaan työntekijöille tarkat aikakatkaisuehdotukset. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä saldon syyt.

## <a name="coming-soon"></a>Tulossa pian

### <a name="indicate-instance-type-when-provisioning-talent"></a>Määritä esiintymätyyppi, kun Talentia valmistellaan

Uuden Talent-esiintymän valmistelun yhteydessä voit määrittää, onko esiintymän tyyppi **Tuotanto** vai **Eristys**, mahdollistaen uusien ominaisuuksien varhaisen testaamisen. Kaikki aiemmin luodut Talent-esiintymät päivitetään tuotantoesiintymän tyyppiin. Jos haluat, että jokin olemassa olevista instansseista päivitetään eristysesiintymätyypiksi, ota yhteyttä tukeen ja tee muutospyyntö.
