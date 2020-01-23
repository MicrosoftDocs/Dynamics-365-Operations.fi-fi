---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (5. marraskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896770"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (5. marraskuuta 2019)

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2598. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="copy-a-core-hr-instance"></a>Core HR -esiintymän kopioiminen

Tämän viikon julkaisussa Microsoft Dynamics 365 Talent: Core HR -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla. Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön. Lisätietoja:

- [Laaja ympäristön hallinta](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) Dynamics 365:n vuoden 2019 2. julkaisuaallon suunnitelmassa

- [Core HR -esiintymän kopiointi](hr-copy-instance.md) Talent-ohjeistuksessa

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Servicen integroinnin erätöitä ei luoda, kun Common Data Servicen integrointi otetaan käyttöön (388030)

Tämä muutos luo Common Data Servicen integroinnin erätyöt, kun se on otettu käyttöön.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity ei muuta ladattavan henkilön kuvan kokoa (369469)

Tämän viikon julkaisu muuttaa tapaa, jolla kuvien kokoa muutetaan suorituskyvyn parantamiseksi, kun tuonti tapahtuu tietojen hallinnan osana.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Toimen Käytettävissä toimeksiantoa varten -päivämäärä voi olla ennen aktivointipäivämäärää (340103)

Tämän muutoksen myötä tulee näkyviin varoitus, jos valitset **Käytettävissä toimeksiantoa varten** -päivämäärän, joka on ennen kuin toimen **aktivointipäivä**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Kompensaation muutospyyntöä ei voi luoda vaiheisiin perustuvien suunnitelmien työntekijän itsepalvelussa (376872)

Tämä julkaisu korjaa ongelmaa, joka liittyy kompensaatiomuutosten pyytämiseen vaiheisiin perustuvien suunnitelmien työntekijän itsepalvelussa. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Syykoodi ei synkronoidu Common Data Serviceen, jos kuvauksen pituus on yli 30 merkkiä, Core HR:n merkkiraja on 60 (352682)

tämän muutoksen ansiosta, yli 30 merkin syykoodit päivitetään Common Data Servicessa. Common Data Serviceen tehdyt muutokset heijastuvat myös takaisin Talentiin.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Osoitteen integrointi Talentista Finance and Operationsiin (351961)

Tämä julkaisu korjasi ongelman, jossa Talentissa päivitetyt osoitteet eivät päivittyneet Finance and Operationsissa. Osoitelohkojen muutokset päivittyvät nyt.

## <a name="coming-soon"></a>Tulossa pian

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).

### <a name="feature-management-workspace"></a>Ominaisuushallinnan työtila

Ominaisuudet lisätään ja päivitetään jokaisessa versiossa. Toiminnon hallintakokemus tarjoaa työtilan, jossa voit tarkastella kussakin julkaisussa toimitettujen toimintojen luetteloa. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

Lisätietoja tulevista toimintojen hallinnan muutoksista löytyy [Toimintojen hallinnan yleiskuvauksesta](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
