---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. tammikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461050"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. tammikuuta 2020)

Tässä artikkelissa käsitellään Dynamics 365 Talentin uusia tai muuttuneita toimintoja.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2697. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Työntekijöitä, joilla ei ole työtietoja, ei voi poistaa - (386157)

Tämä muutos lisää poistovaihtoehdon **Työntekijät, joilla ei ole työtä**-muotoa. Työntekijät näkyvät tässä lomakkeessa, kun työntekijälle ei ole tulevia, aktiivisia tai historiallisia työtehtäviä. Tässä versiossa Delete-toiminto on käytössä vain järjestelmänvalvojille. Ensi viikon versiossa suojaus päivitetään kuitenkin siten, että kaikki käyttäjät, joilla on HR-assistenttirooli, voivat poistaa työntekijöitä ilman työtehtävää. Voit tehdä nämä muutokset myös manuaalisesti noudattamalla seuraavia ohjeita.

1. Mene kohtaan **Suojauskonfiguraatio**.
2. Suodata **Oikeudet**-välilehdessä **Oikeudet**-luettelo ja **Ylläpidä työntekijöitä**.
3. Valitse **viitteet**-sarakkeesta **Näytä valikon vaihtoehdot**.
4. Valitse **Näytä valikon vaihtoehdot**-sarakkeesta **HcmWOrkersWithoutEmployment**.
5. Määritä **Poisto**-oikeuden myöntäminen.
6. Valitse **Julkaisemattomat objektit** -välilehti.
7. Valitse **Julkaise kaikki**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]